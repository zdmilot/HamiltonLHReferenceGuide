# NewPlate

Int32 NewPlate()\
The NewPlate command creates a new Plate section in an experiment.

| <img src="../../../../../.gitbook/assets/0 (23) (1).png" alt="" data-size="original"> | Note: For the SoftMax Pro Software - GxP edition, the user must have the Generate Compliance Data permission.                                              |
| ------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------- |
| <img src="../../../../../.gitbook/assets/1 (20).png" alt="" data-size="original">     | Note: For the SoftMax Pro Software - GxP edition, the document must be unlocked, the document status must be In Work, and all statements must be unsigned. |

Parameters\
None

Example\
This example describes how to create a Plate section in an experiment.

int mStatusID;\
public void Main()\
{\
AutomationObject.Initialize("localhost");\
AutomationObject.CommandCompleted += CommandCompleted;\
AutomationObject.ErrorReport += Error;\
AutomationObject.InstrumentStatusChanged += InstrumentStatus;\
AutomationObject.NewDocument();\
AutomationObject.NewPlate();\
AutomationObject.NewNotes();\
mStatusID = AutomationObject.NewPlate();\
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
AutomationObject.CommandCompleted -= CommandCompleted;

AutomationObject.InstrumentStatusChanged -= InstrumentStatus;\
AutomationObject.Dispose();\
}\
}\
private void Error( object sender,\
SoftMaxPro.AutomationClient.SMPAutomationClient.ErrorEventArgs e)\
{\
Results.AppendResult("Error: Command ID = " + e.QueueID.ToString() + " - " + e.Error); }\
private void InstrumentStatus( object sender,\
SoftMaxPro.AutomationClient.SMPAutomationClient.InstrumentStatusEventArgs e)\
{\
Results.AppendResult("Status changed to " + e.Status);\
}
