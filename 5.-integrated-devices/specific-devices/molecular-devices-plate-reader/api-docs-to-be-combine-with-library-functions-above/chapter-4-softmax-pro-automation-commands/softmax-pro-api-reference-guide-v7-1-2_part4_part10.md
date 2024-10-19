# softmax pro api reference guide v7 1 2\_Part4\_Part10

GetAllFolders

Int32 GetAllFolders(string folder, string type)\
The GetAllFolders command returns folder information from the database or file system.

Parameters\
folder

Type: String, Default = root folder\
Type

Type: String, Default = data

Values:

data - Gets a list of all existing folders with data documents inside. For example, command GetAllFolders(rootFolder) -> data gets a list of all subfolders starting with rootfolder that contain data documents.

protocol - Gets a list of all existing folders with protocol documents inside. For example, command GetAllFolders(rootFolder) -> protocol gets a list of all subfolders starting with rootfolder that contain protocol documents.

all - Gets both document types.

Example\
This example describes how to extract folder information for export.

public void Main()\
{\
//initalize AutomationObject and hook events InitializeAndHookEvents();

//start of script commands\
AutomationObject.GetAllFolders();\
var indexOfCommand = GetAllFolder(rootFolder, "data") //AutomationObject.GetDocuments("Folder","data"); //AutomationObject.OpenFile("FolderAndName.sdax");

//var commandID = AutomationObject.ExportAs(mExportFolder + "Plate.txt",\
SoftMaxPro.AutomationClient.SMPAutomationClient.ExportAsFormat.PLATE );\
//Results.AppendResult("Command ID = " + commandID.ToString() );\
}\
private void Error( object sender,\
SoftMaxPro.AutomationClient.SMPAutomationClient.ErrorEventArgs e)\
{\
Results.AppendResult("Error: Command ID = " + e.QueueID.ToString() + " - " + e.Error); }

private void CommandCompleted( object sender,\
SoftMaxPro.AutomationClient.SMPAutomationClient.CommandStatusEventArg e)\
{\
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
