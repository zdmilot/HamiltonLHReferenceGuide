# softmax pro api reference guide v7 1 2\_Part4\_Part19

GetTemperature

Int32 GetTemperature()\
The GetTemperature command returns the instrument incubator temperature.

Parameters\
None

Returns\
The function returns the command ID used to retrieve the data that the CommandCompleted Event returns.

Data Returned Through the CommandCompleted Event Return Type: Double\
Instrument incubator temperature

GetVersion

Int32 GetVersion()\
The GetVersion command returns the version number of the SoftMax Pro Software automation Interface.

Parameters\
None

Returns\
This function returns the command ID used to retrieve the data that the CommandCompleted Event returns.

Data Returned Through the CommandCompleted Event Return Type: String\
Returns the version number of the SoftMax Pro Software.

The return string is the following property:\
SMPAutomationClient.Version.VERSION6300

Example\
This example describes how to get the version number of the SoftMax Pro Software.

int mStatusID;\
public void Main()\
{\
AutomationObject.Initialize("localhost");\
AutomationObject.CommandCompleted+= CommandCompleted;\
AutomationObject.ErrorReport += Error;\
mStatusID = AutomationObject.GetVersion();\
}\
private void Error( object sender,\
SoftMaxPro.AutomationClient.SMPAutomationClient.ErrorEventArgs e)\
{\
Results.AppendResult("Error: Command ID = " + e.QueueID.ToString() + " - " + e.Error); }
