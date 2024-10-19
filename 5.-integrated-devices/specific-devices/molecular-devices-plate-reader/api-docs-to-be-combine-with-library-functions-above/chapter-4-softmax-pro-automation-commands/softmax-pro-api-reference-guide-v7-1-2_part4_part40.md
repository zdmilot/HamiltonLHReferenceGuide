# SetTitle

Int32 SetTitle()\
The SetTitle command sets the title of a section in an experiment. The command confirms that the name is unique within the current experiment and if not, makes no change.

| <img src="../../../../../.gitbook/assets/0 (27).png" alt="" data-size="original"> | Note: This command can alter the names of the sections within an experiment, but it cannot alter the experiment name.                                      |
| --------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------- |
| <img src="../../../../../.gitbook/assets/1 (22).png" alt="" data-size="original"> | Note: For the SoftMax Pro Software - GxP edition, the document must be unlocked, the document status must be In Work, and all statements must be unsigned. |

Parameters\
None

Example\
This example describes how to set a Plate section title to Plate 100.

int mStatusID;\
public void Main()\
{\
AutomationObject.Initialize("localhost");\
AutomationObject.ErrorReport += Error;\
AutomationObject.CommandCompleted+= CommandCompleted;\
AutomationObject.InstrumentStatusChanged += InstrumentStatus;\
AutomationObject.SetReader("Offline", "SPECTRAmax M5e");\
AutomationObject.SetSimulationMode(true);\
AutomationObject.SelectSection("Plate1");\
mStatusID = AutomationObject.SetTitle("Plate-100");\
Results.AppendResult("Set Title Result : "+mStatusID.ToString());\
}\
private void CommandCompleted( object sender,\
SoftMaxPro.AutomationClient.SMPAutomationClient.CommandStatusEventArg e)\
{\
if( mStatusID == e.QueueID )\
{\
Results.AppendResult(e.StringResult);\
}\
if( e.QueueEmpty)\
{\
Results.AppendResult("Queue empty - disconnecting events");\
AutomationObject.ErrorReport -= Error;\
AutomationObject.CommandCompleted -= CommandCompleted;\
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
