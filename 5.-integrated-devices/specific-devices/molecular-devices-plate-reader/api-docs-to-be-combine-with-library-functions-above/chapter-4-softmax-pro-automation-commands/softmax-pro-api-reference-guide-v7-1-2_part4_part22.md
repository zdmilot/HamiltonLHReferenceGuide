# softmax pro api reference guide v7 1 2\_Part4\_Part22

ImportPlateTemplate

Int32 ImportPlateTemplate(string path)\
The ImportPlateTemplate command imports a template from a file into a Plate section.

| <img src="../../../../../.gitbook/assets/0 (18).png" alt="" data-size="original"> | Note: For the SoftMax Pro Software - GxP edition, the document must be unlocked, the document status must be In Work, and all statements must be unsigned. |
| --------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------- |

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
