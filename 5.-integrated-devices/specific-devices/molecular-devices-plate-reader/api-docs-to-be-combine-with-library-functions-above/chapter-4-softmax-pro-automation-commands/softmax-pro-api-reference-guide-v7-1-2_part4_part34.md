# SelectNextPlateSection

Int32 SelectNextPlateSection()\
The SelectNextPlateSection command selects the next Plate section in an experiment.

Parameters\
None

Example\
This example describes how to select the next Plate section after the Plate1 Plate section.

int mStatusID;\
public void Main()\
{\
AutomationObject.Initialize("localhost");\
AutomationObject.ErrorReport += Error;\
AutomationObject.CommandCompleted+= CommandCompleted;\
AutomationObject.CloseDocument();\
AutomationObject.NewDocument();\
AutomationObject.NewPlate();\
AutomationObject.SelectSection("Plate1");\
mStatusID= AutomationObject.SelectNextPlateSection();\
}\
private void CommandCompleted( object sender,\
SoftMaxPro.AutomationClient.SMPAutomationClient.CommandStatusEventArg e)\
{\
Results.AppendResult("Command complete Command ID = " + e.QueueID.ToString() ); if( e.QueueEmpty)\
{\
Results.AppendResult("Queue empty - disconnecting events");

AutomationObject.ErrorReport -= Error;\
AutomationObject.CommandCompleted -= CommandCompleted;\
AutomationObject.Dispose();\
}\
}\
private void Error( object sender,\
SoftMaxPro.AutomationClient.SMPAutomationClient.ErrorEventArgs e)\
{\
Results.AppendResult("Error: Command ID = " + e.QueueID.ToString() + " - " + e.Error); }
