# ImportPlateData



Int32 ImportPlateData(string importType, params string\[] importParameter) The ImportPlateData command imports data from a file into a Plate section in a document.

| <img src="../../../../../.gitbook/assets/0 (17) (1).png" alt="" data-size="original"> | Note: For the SoftMax Pro Software - GxP edition, the document must be unlocked, the document status must be In Work, and all statements must be unsigned. |
| ------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------- |

Parameters\
importType

Type: String

Must be one of the following:

• “Plate Format"

• "XML Format"\
importParameter

Type: Params String

Fully qualified path name of the file that contains the data to import. The file must match the format you use for manual data imports.

Example\
The example on the following page describes how to import plate data in Plate format from a file named data\_import.txt.

int mStatusID;\
public void Main()\
{\
AutomationObject.Initialize("localhost");\
AutomationObject.CommandCompleted += CommandCompleted;\
AutomationObject.ErrorReport += Error;\
AutomationObject.InstrumentStatusChanged += InstrumentStatus;\
AutomationObject.SetReader("Offline", "SPECTRAmax M5");\
AutomationObject.SetSimulationMode(true);\
AutomationObject.SelectSection("Plate1");\
mStatusID = AutomationObject.ImportPlateData("Plate Format”, "C:\\\Program\
Files\\\Molecular\
Devices\\\Import Templates\\\data\_import.txt");\
Results.AppendResult("Import Plate Data Status="+mStatusID.ToString());\
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
