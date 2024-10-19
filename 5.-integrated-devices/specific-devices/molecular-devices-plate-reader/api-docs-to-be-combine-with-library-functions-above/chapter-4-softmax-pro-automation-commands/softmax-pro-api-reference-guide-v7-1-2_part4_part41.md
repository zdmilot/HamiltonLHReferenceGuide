# StartRead

Int32 StartRead()\
The StartRead command reads a Plate section or CuvetteSet section. If the current section is neither a Plate section nor CuvetteSet section, the command reads the next Plate section or CuvetteSet section.

The SoftMax Pro Software - Standard edition confirms that Auto Export is enabled and the SoftMax Pro Software - GxP edition confirms that Auto Save is enabled.

Parameters\
None

Example\
This example describes how to start a plate read.

int mCopyID;\
public void Main()\
{\
string now = System.DateTime.Now.ToString();\
Results.AppendResult(now);\
AutomationObject.Initialize("localhost");\
AutomationObject.ErrorReport += Error;\
AutomationObject.CommandCompleted+= CommandCompleted;\
AutomationObject.InstrumentStatusChanged += InstrumentStatus;\
AutomationObject.CloseDocument();\
AutomationObject.NewDocument();\
AutomationObject.SetReader("Offline", "SPECTRAmax M2");\
AutomationObject.SetSimulationMode(true);\
AutomationObject.SelectSection("Plate1");\
int read1 = AutomationObject.StartRead();\
Results.AppendResult("Read ID = " + read1.ToString());\
read1 = AutomationObject.StartRead();\
Results.AppendResult("Read ID = " + read1.ToString());\
read1 = AutomationObject.StartRead();\
Results.AppendResult("Read ID = " + read1.ToString());\
mCopyID = AutomationObject.GetDataCopy();\
}\
private void Error( object sender,\
SoftMaxPro.AutomationClient.SMPAutomationClient.ErrorEventArgs e)\
{\
Results.AppendResult("Error: Command ID = " + e.QueueID.ToString() + " - " + e.Error); }\
private void CommandCompleted( object sender,\
SoftMaxPro.AutomationClient.SMPAutomationClient.CommandStatusEventArg e)\
{

Results.AppendResult("Command complete Command ID = " + e.QueueID.ToString() ); if( mCopyID == e.QueueID )\
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
private void InstrumentStatus( object sender,\
SoftMaxPro.AutomationClient.SMPAutomationClient.InstrumentStatusEventArgs e) {\
Results.AppendResult("Status changed to " + e.Status);\
}
