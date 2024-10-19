# softmax pro api reference guide v7 1 2\_Part4\_Part8

ExportAs

Int32 ExportAs(String path, ExportAsFormat exportAsFormat)\
The ExportAs command exports data in the Columns, Plate, or .xml format. The ExportAs command overwrites any existing file without warning.

Parameters\
path

Type: String

Fully qualified path name\
exportAsFormat

Type: ExportAsFormat

TIME exports data in a single column of text for each well.

COLUMNS exports data in a single column of text for each well.

PLATE exports data in a text matrix corresponding to a microplate grid.

XML exports data in an XML file format.

Example\
This example describes how to output data in .xml, Plate, and Columns formats and uses TIME in the ExportAsFormat parameter to export data in the Columns format.

public void Main()\
{\
AutomationObject.Initialize("localhost");\
AutomationObject.ErrorReport += Error;\
AutomationObject.CommandCompleted += CommandCompleted;\
AutomationObject.SelectSection("Plate1");\
AutomationObject.SetReader("Offline", "SPECTRAmax M2");\
AutomationObject.SetSimulationMode(true);\
AutomationObject.StartRead();\
var commandID = AutomationObject.ExportAs("C:\\\test.xml",\
SoftMaxPro.AutomationClient.SMPAutomationClient.ExportAsFormat.XML ); Results.AppendResult("Command ID = " + commandID.ToString() ); commandID = AutomationObject.ExportAs("C:\\\Plate.txt",\
SoftMaxPro.AutomationClient.SMPAutomationClient.ExportAsFormat.PLATE ); Results.AppendResult("Command ID = " + commandID.ToString() );\
commandID = AutomationObject.ExportAs("C:\\\COLUMNS.txt",\
SoftMaxPro.AutomationClient.SMPAutomationClient.ExportAsFormat.TIME); Results.AppendResult("Command ID = " + commandID.ToString() ); }\
private void Error( object sender,\
SoftMaxPro.AutomationClient.SMPAutomationClient.ErrorEventArgs e)
