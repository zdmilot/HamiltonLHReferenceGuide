# SimulationMode

Int32 SetSimulationMode(Boolean modestate)\
The SimulationMode command sets the SoftMax Pro Software into simulator mode.

Parameters\
modestate

Type: Boolean

true enables simulator mode.

false disables simulator mode.

Example\
This example describes how to select an instrument, enable simulator mode, and start a read.

int mStatusID;\
public void Main()\
{\
string now = System.DateTime.Now.ToString();\
Results.AppendResult(now);\
AutomationObject.Initialize("localhost");\
AutomationObject.ErrorReport += Error;\
AutomationObject.CommandCompleted+= CommandCompleted;\
AutomationObject.InstrumentStatusChanged += InstrumentStatus;\
AutomationObject.SetReader("Offline", "SPECTRAmax M5");\
mStatusID = AutomationObject.SetSimulationMode(true);\
Results.AppendResult("Simulation Mode Status = " +mStatusID.ToString());\
AutomationObject.SelectSection("Plate1");\
int read1 = AutomationObject.StartRead();\
Results.AppendResult("Read ID = " + read1.ToString());\
}\
private void Error( object sender,\
SoftMaxPro.AutomationClient.SMPAutomationClient.ErrorEventArgs e)\
{\
Results.AppendResult("Error: Command ID = " + e.QueueID.ToString() + " - " + e.Error); }\
private void CommandCompleted( object sender,\
SoftMaxPro.AutomationClient.SMPAutomationClient.CommandStatusEventArg e)

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
private void InstrumentStatus( object sender,\
SoftMaxPro.AutomationClient.SMPAutomationClient.InstrumentStatusEventArgs e) {\
Results.AppendResult("Status changed to " + e.Status);\
}
