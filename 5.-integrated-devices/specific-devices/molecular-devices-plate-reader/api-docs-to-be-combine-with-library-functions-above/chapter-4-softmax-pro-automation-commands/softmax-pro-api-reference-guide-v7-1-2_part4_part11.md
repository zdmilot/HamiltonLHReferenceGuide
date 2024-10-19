# GetAutosaveState

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
