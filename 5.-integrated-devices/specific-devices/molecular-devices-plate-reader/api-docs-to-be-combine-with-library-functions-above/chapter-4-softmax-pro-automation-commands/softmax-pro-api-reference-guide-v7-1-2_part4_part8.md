# ExportAs

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

{\
Results.AppendResult("Error: Command ID = " + e.QueueID.ToString() + " - " + e.Error); }\
private void CommandCompleted( object sender,\
SoftMaxPro.AutomationClient.SMPAutomationClient.CommandStatusEventArg e)\
{\
Results.AppendResult("Command complete Command ID = " + e.QueueID.ToString() ); if( e.QueueEmpty)\
{\
Results.AppendResult("Queue empty - disconnecting events");\
AutomationObject.ErrorReport -= Error;\
AutomationObject.CommandCompleted -= CommandCompleted;\
AutomationObject.Dispose();\
}\
}
