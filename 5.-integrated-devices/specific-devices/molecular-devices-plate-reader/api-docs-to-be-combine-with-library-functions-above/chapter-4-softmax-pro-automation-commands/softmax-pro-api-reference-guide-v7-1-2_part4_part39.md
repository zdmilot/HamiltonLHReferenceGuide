# SetTemperature

Int32 SetTemperature(Double temperature)\
The SetTemperature command sets the instrument incubator temperature. Set the temperature to zero to turn off the incubator.

Parameters\
Temperature

Type: Double

The number of degrees centigrade

Example\
This example describes how to set the incubator temperature to 20°C.

int ID;\
public void Main()\
{\
AutomationObject.Initialize("localhost");\
AutomationObject.InstrumentStatusChanged += InstrumentStatus; AutomationObject.CommandCompleted += CommandCompleted;\
AutomationObject.ErrorReport += Error;\
AutomationObject.SetReader("Offline", "SPECTRAmax M2"); AutomationObject.SetSimulationMode(true);\
ID = AutomationObject.SetTemperature(20.0);

Results.AppendResult("Set Temperature Status = " + ID.ToString());\
}\
private void CommandCompleted( object sender,\
SoftMaxPro.AutomationClient.SMPAutomationClient.CommandStatusEventArg e)\
{\
Results.AppendResult("Command complete Command ID = " + e.QueueID.ToString() ); if(ID == e.QueueID )\
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
SoftMaxPro.AutomationClient.SMPAutomationClient.ErrorEventArgs e)\
{\
Results.AppendResult("Error: Command ID = " + e.QueueID.ToString() + " - " + e.Error); }\
private void InstrumentStatus( object sender,\
SoftMaxPro.AutomationClient.SMPAutomationClient.InstrumentStatusEventArgs e)\
{\
Results.AppendResult("Status changed to " + e.Status);\
}
