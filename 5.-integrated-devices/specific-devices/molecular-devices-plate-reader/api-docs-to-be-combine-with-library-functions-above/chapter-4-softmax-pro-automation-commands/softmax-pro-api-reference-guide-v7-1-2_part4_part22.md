# ImportPlateTemplate

Int32 ImportPlateTemplate(string path)\
The ImportPlateTemplate command imports a template from a file into a Plate section.

| <img src="../../../../../.gitbook/assets/0 (18) (1).png" alt="" data-size="original"> | Note: For the SoftMax Pro Software - GxP edition, the document must be unlocked, the document status must be In Work, and all statements must be unsigned. |
| ------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------- |

Parameters\
path

Type: String

Fully qualified path name of the file that contains the template to import. The file must match the format you use for manual template imports.

Example\
This example describes how to import a plate template named platetemplate.txt.

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
mStatusID = AutomationObject.ImportPlateTemplate("C:\\\Program Files\\\Molecular Devices\\\SoftMax Pro\
7.0 Automation SDK\\\Scripts\\\PlateTemplate.txt");\
Results.AppendResult("Import Plate Template Status="+mStatusID.ToString()); }\
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
