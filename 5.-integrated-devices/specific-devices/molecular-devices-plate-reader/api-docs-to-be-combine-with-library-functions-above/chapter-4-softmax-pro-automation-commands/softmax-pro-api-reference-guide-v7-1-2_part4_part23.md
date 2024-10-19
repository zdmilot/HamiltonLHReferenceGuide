# Initialize

Boolean Initialize ()\
Boolean Initialize (String server)\
Boolean Initialize (String server, Int32 port)

Purpose\
The Initialize commands initialize the Automation Interface.

Parameters\
server

Type: String

the computer name or IP address of the server\
port

Type: Int32

the port address of the server

Returns\
Return Type: Boolean

![](<../../../../../.gitbook/assets/0 (19).png>) True = initialization was successful

![](<../../../../../.gitbook/assets/1 (19).png>) False = initialization failed

Examples\
There are three ways to use the Initialize command:

![](<../../../../../.gitbook/assets/2 (10).png>) bool initialize (), see page 73

![](<../../../../../.gitbook/assets/3 (12).png>) bool initialize(string server), see page 74

![](<../../../../../.gitbook/assets/4 (11).png>) bool initialize(String server, int port), see page 75

bool initialize ()\
With no parameters, the Initialize function uses the default host 'localhost' and default port of 9000.

bool mInitialize;\
public void Main()\
{\
mInitialize = AutomationObject.Initialize(); // Replace the target machine IP Address here\
AutomationObject.CommandCompleted += CommandCompleted;\
AutomationObject.ErrorReport += Error;\
AutomationObject.InstrumentStatusChanged += InstrumentStatus;\
Results.AppendResult("Inirialized : " + mInitialize.ToString());\
}\
private void CommandCompleted( object sender,\
SoftMaxPro.AutomationClient.SMPAutomationClient.CommandStatusEventArg e)\
{\
Results.AppendResult("Command complete Command ID = " + e.QueueID.ToString() ); if(mInitialize)\
{\
Results.AppendResult(e.StringResult);\
}\
Results.AppendResult("Queue empty - disconnecting events");\
AutomationObject.ErrorReport -= Error;\
AutomationObject.CommandCompleted -= CommandCompleted;\
AutomationObject.InstrumentStatusChanged -= InstrumentStatus;\
AutomationObject.Dispose();\
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

bool initialize(string server)\
The server parameter can be either the computer name or IP address and default port.

bool mInitialize;\
public void Main()\
{\
mInitialize = AutomationObject.Initialize("127.0.0.1"); // Replace the target machine IP Address here\
AutomationObject.CommandCompleted += CommandCompleted;\
AutomationObject.ErrorReport += Error;\
AutomationObject.InstrumentStatusChanged += InstrumentStatus;\
Results.AppendResult("Inirialized : " + mInitialize.ToString());\
}\
private void CommandCompleted( object sender,\
SoftMaxPro.AutomationClient.SMPAutomationClient.CommandStatusEventArg e)\
{\
Results.AppendResult("Command complete Command ID = " + e.QueueID.ToString() ); if(mInitialize)\
{\
Results.AppendResult(e.StringResult);\
}\
Results.AppendResult("Queue empty - disconnecting events");\
AutomationObject.ErrorReport -= Error;\
AutomationObject.CommandCompleted -= CommandCompleted;\
AutomationObject.InstrumentStatusChanged -= InstrumentStatus;\
AutomationObject.Dispose();\
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
