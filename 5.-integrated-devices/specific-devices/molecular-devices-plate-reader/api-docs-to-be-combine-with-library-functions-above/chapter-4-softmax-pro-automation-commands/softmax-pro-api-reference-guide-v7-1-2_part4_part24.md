# softmax pro api reference guide v7 1 2\_Part4\_Part24

bool initialize(String server, int port)\
You can use the computer name or IP and port.

public void Main()\
{\
AutomationObject.Initialize("10.212.11.175", 9901)\
AutomationObject.CloseDocument();\
AutomationObject.NewDocument();\
}\
When the default port is not available for the SoftMax Pro Software you can add a registry key in HLM\SOFTWARE\Molecular Devices\Readers\SMP with key "Port" and a 32bit DWORD that contains the port address.

Logon

Int32 Logon(String userName, String password, String projectName)\
The Logon command logs a user onto the SoftMax Pro GxP Software. To prevent the display of the Logon dialog when the application starts, use /R in the program command line (for example, "SoftMaxProApp.exe /R"). See Computer System Requirements on page 8.

Parameters\
userName

Type: String

The user name for the account\
password

Type: String

The password for the account\
projectName

Type: String

The Project for the user to use

Logoff

Int32 Logoff()\
The Logoff command logs a user off from the SoftMax Pro GxP Software.

Parameters\
None.
