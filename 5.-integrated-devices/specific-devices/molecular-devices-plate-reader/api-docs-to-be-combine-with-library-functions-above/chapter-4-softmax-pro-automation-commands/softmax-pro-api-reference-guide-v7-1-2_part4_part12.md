# GetCopyData

Int32 GetDataCopy()\
The GetCopyData command copies data to the client by way of an event. The format of the copied data depends on the display settings for the plate section (normally Raw Data), the read mode, the read type, and the number of wavelengths.

Parameters\
None

Returns\
This function returns the command ID used to retrieve the data that the CommandCompleted Event returns.

Data Returned Through the CommandCompleted Event Return type: String\
Returns the data for the Plate section.

Example\
This examples describes how to copy data to the client by way of an event.

int mCopyID;\
public void Main()\
{\
string now = System.DateTime.Now.ToString();\
Results.AppendResult(now);\
AutomationObject.Initialize("localhost");\
AutomationObject.ErrorReport += Error;\
AutomationObject.CommandCompleted += CommandCompleted;\
AutomationObject.InstrumentStatusChanged += InstrumentStatus; AutomationObject.SetReader("Offline", "SPECTRAmax M2");

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
{\
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
SoftMaxPro.AutomationClient.SMPAutomationClient.InstrumentStatusEventArgs e)\
{\
Results.AppendResult("Status changed to " + e.Status);\
{
