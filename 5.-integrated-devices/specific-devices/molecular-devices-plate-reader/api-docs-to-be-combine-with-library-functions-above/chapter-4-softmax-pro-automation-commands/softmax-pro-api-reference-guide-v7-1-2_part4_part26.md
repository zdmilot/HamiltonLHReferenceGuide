# NewDocument

Int32 NewDocument()\
The NewDocument command creates a new document that uses the Default Protocol.spr protocol settings.

| <img src="../../../../../.gitbook/assets/0 (20) (1).png" alt="" data-size="original"> | Note: Not available for SoftMax Pro Software - GxP edition. |
| ------------------------------------------------------------------------------------- | ----------------------------------------------------------- |

Parameters\
None

Example\
This example describes how to create a new document that uses the default protocol settings.

int mStatusID;\
public void Main()\
{\
AutomationObject.Initialize("localhost");\
AutomationObject.CommandCompleted += CommandCompleted;\
AutomationObject.ErrorReport += Error;\
mStatusID = AutomationObject.NewDocument();\
}\
private void CommandCompleted( object sender,\
SoftMaxPro.AutomationClient.SMPAutomationClient.CommandStatusEventArg e)\
{\
Results.AppendResult("Command complete Command ID = " + e.QueueID.ToString() ); if( mStatusID == e.QueueID )\
{\
Results.AppendResult(e.StringResult);\
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
