# softmax pro api reference guide v7 1 2\_Part4\_Part13

GetDocuments

Int32 GetDocuments(folderName)\
The GetDocuments command extracts document information.

Parameters\
path

Type: String, Default = root

Type: String, Default = data

Values:

data - Gets a list of all data documents within the folder. For example, command GetDocuments (rootFolder) -> data gets a list of all documents in subfolders starting with the root folder.

protocol - Gets a list of all protocol documents within the folder. For example, command\
GetDocuments(rootFolder) -> protocol gets a list of all documents in subfolders starting with root folder.

all - Gets both document types.

Example\
This example describes how to extract folder information for export.

public void Main()\
{\
//initalize AutomationObject and hook events InitializeAndHookEvents();

//start of script commands\
var indexOfCommand = AutomationObject.GetDocuments("C:\xy", "data")

//AutomationObject.GetDocuments("Test","data"); //AutomationObject.OpenFile("DocumentAndName.sdax");

//var commandID = AutomationObject.ExportAs(mExportFolder + "Plate.txt",\
SoftMaxPro.AutomationClient.SMPAutomationClient.ExportAsFormat.PLATE );\
//Results.AppendResult("Command ID = " + commandID.ToString() );\
}\
private void Error( object sender,\
SoftMaxPro.AutomationClient.SMPAutomationClient.ErrorEventArgs e)\
{\
Results.AppendResult("Error: Command ID = " + e.QueueID.ToString() + " - " + e.Error); }\
private void CommandCompleted( object sender,\
SoftMaxPro.AutomationClient.SMPAutomationClient.CommandStatusEventArg e)\
{

Results.AppendResult("Command complete Command ID = " + e.QueueID.ToString() + " - " + e.StringResult);

//Script end, Queue is empty\
if( e.QueueEmpty)\
{\
Results.AppendResult("Queue empty - Script done."); UnhookEventsAndDispose();\
}\
}\
private void InitializeAndHookEvents()\
{\
Results.AppendResult("Initialize AutomationObject"); AutomationObject.Initialize("localhost");

Results.AppendResult("Hooking events");\
AutomationObject.ErrorReport += Error;\
AutomationObject.CommandCompleted+= CommandCompleted;\
AutomationObject.InstrumentStatusChanged += InstrumentStatus; }\
private void UnhookEventsAndDispose()\
{\
Results.AppendResult("Disconnecting events");\
AutomationObject.ErrorReport -= Error;\
AutomationObject.CommandCompleted -= CommandCompleted;\
AutomationObject.InstrumentStatusChanged -= InstrumentStatus;

Results.AppendResult("AutomationObject disposed.");\
AutomationObject.Dispose();\
}\
private void InstrumentStatus( object sender,\
SoftMaxPro.AutomationClient.SMPAutomationClient.InstrumentStatusEventArgs e) {\
Results.AppendResult("Status changed to " + e.Status);\
}
