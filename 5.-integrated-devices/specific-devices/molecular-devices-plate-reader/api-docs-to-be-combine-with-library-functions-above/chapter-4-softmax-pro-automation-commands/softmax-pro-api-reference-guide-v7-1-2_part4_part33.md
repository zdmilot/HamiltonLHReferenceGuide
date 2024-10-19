# SaveAs

Int32 SaveAs(String pathname)\
The SaveAs command saves the current document as a data document or a protocol. Define the document type by the file extension in the path statement. For the SoftMax Pro Software - Standard edition, use the \*.sda file extension for data documents and \*.spr file extension for protocols. For the SoftMax Pro Software -GxP edition, do not enter a file extension.

If a document with the same name already exists, the SoftMax Pro Software - Standard edition automatically overwrites the document with no warning.

| <img src="../../../../../.gitbook/assets/0 (25).png" alt="" data-size="original"> | Note: The SoftMax Pro Software - GxP edition does not allow you to save the document as a Protocol and prevents you from overwriting an existing document. |
| --------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------- |

Parameters\
pathname

Type: String

Fully qualified path and name of document to save, including the file extension.

Example\
This example describes how to save a document to an undefined “Temp” path. To define the path, you need to define the mPath string with an absolute or relative path that includes the name of the document and its file extension.

int mStatusID;\
string mPath="C:\\\temp\mydata.sda";\
public void Main() {\
AutomationObject.Initialize("localhost");\
AutomationObject.CommandCompleted += CommandCompleted;\
AutomationObject.ErrorReport += Error;\
mStatusID = AutomationObject.SaveAs(mPath);\
}\
private void CommandCompleted( object sender,\
SoftMaxPro.AutomationClient.SMPAutomationClient.CommandStatusEventArg e)\
{\
Results.AppendResult("Command complete Command ID = " + e.QueueID.ToString() ); if( mStatusID == e.QueueID )\
{\
Results.AppendResult(e.StringResult);

}\
if( e.QueueEmpty)\
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
