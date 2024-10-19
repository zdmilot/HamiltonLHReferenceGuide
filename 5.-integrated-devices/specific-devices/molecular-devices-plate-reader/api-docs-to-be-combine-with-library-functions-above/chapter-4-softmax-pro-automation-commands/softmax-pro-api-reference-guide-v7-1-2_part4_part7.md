# softmax pro api reference guide v7 1 2\_Part4\_Part7

Dispose

Void Dispose()\
The Dispose command closes the final automation application dialog. The termination dialog that contains the Terminate button displays in the SoftMax Pro Software after the script execution completes.

Parameters\
None

Example\
This example describes how to close the automation dialog and exit the automation application. This example includes the code to complete command execution and dispose of the interface dialog.

public void Main()\
{\
AutomationObject.Initialize();\
AutomationObject.CommandCompleted+= CommandCompleted;\
AutomationObject.ErrorReport+= Error;\
AutomationObject.OpenDrawer();\
}\
private void CommandCompleted( object sender,\
SoftMaxPro.AutomationClient.SMPAutomationClient.CommandStatusEventArg e)\
{\
Results.AppendResult("Command complete Command ID = " + e.QueueID.ToString() ); if( e.QueueEmpty)\
{\
Results.AppendResult("Queue empty - disconnecting events");\
AutomationObject.CommandCompleted -= CommandCompleted;\
AutomationObject.Dispose();\
}\
}\
private void Error( object sender,\
SoftMaxPro.AutomationClient.SMPAutomationClient.ErrorEventArgs e)\
{\
Results.AppendResult("Error: Command ID = " + e.QueueID.ToString() + " - " + e.Error); }
