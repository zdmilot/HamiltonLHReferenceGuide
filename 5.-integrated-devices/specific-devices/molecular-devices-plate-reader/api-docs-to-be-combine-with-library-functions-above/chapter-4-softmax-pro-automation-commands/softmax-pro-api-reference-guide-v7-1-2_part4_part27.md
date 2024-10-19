# NewExperiment

Int32 NewExperiment()\
The NewExperiment command creates a new experiment in a document.

| <img src="../../../../../.gitbook/assets/0 (21).png" alt="" data-size="original"> | Note: For the SoftMax Pro Software - GxP edition, the document must be unlocked, the document status must be In Work, and all statements must be unsigned. |
| --------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------- |

Parameters\
None

Example\
This example describes how to create a new experiment in a document.

int mStatusID;\
public void Main()\
{\
AutomationObject.Initialize("localhost");\
AutomationObject.CommandCompleted += CommandCompleted;\
AutomationObject.ErrorReport += Error;\
AutomationObject.NewDocument();\
AutomationObject.NewNotes();\
AutomationObject.NewPlate();\
AutomationObject.NewNotes();\
mStatusID = AutomationObject.NewExperiment();\
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
SoftMaxPro.AutomationClient.SMPAutomationClient.ErrorEventArgs e)

{\
Results.AppendResult("Error: Command ID = " + e.QueueID.ToString() + " - " + e.Error); }
