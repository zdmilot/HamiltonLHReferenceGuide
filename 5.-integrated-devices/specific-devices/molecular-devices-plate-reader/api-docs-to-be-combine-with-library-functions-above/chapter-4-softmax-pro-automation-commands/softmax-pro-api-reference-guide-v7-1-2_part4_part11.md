# softmax pro api reference guide v7 1 2\_Part4\_Part11

GetAutosaveState

Int32 GetAutosaveState()\
The GetAutosaveState command returns the current autosave setting for the active document.

Parameters\
None

Returns\
This function returns the command ID used to retrieve the data that the CommandCompleted Event returns.

Data Returned Through the CommandCompleted Event Return type: String\
Returns the AutoSave state.

The return string is one of the following properties:

![](<../../../../../.gitbook/assets/0 (14).png>) SMPAutomationClient.AutoSaveState.OFF = AutoSave is turned off

![](<../../../../../.gitbook/assets/1 (17).png>) SMPAutomationClient.AutoSaveState.ON = AutoSave is turned on

GetCopyData

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
