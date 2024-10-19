# GetNumberPlateSections

Int32 GetNumberPlateSections()\
The GetNumberPlateSections command returns the number of Plate sections in an experiment.

Parameters: None

Returns\
Returns the command ID used to retrieve the data that the CommandCompleted Event returns.

Data Returned Through the CommandCompleted Event Return Type: Int32\
Returns the number of Plate sections in the active experiment.

Example\
This example describes how to determine the number of Plate sections in an experiment.

int NumPlateSectionsID;\
public void Main()\
{\
AutomationObject.Initialize("localhost");\
AutomationObject.ErrorReport += Error;\
AutomationObject.CommandCompleted+= CommandCompleted;\
NumPlateSectionsID = AutomationObject.GetNumberPlateSections();\
Results.AppendResult("Status Command ID = " + NumPlateSectionsID .ToString()); }\
private void CommandCompleted( object sender,\
SoftMaxPro.AutomationClient.SMPAutomationClient.CommandStatusEventArg e)\
{\
Results.AppendResult("Command complete Command ID = " + e.QueueID.ToString() ); if( e.QueueID == NumPlateSectionsID )\
Results.AppendResult("Number of Plate Sections : " + e.IntResult.ToString() ); if( e.QueueEmpty)\
{\
Results.AppendResult("Queue empty - disconnecting events");\
AutomationObject.ErrorReport -= Error;\
AutomationObject.CommandCompleted -= CommandCompleted;\
AutomationObject.Dispose();\
}\
}\
private void Error( object sender,\
SoftMaxPro.AutomationClient.SMPAutomationClient.ErrorEventArgs e)\
{\
Results.AppendResult("Error: Command ID = " + e.QueueID.ToString() + " - " + e.Error); }
