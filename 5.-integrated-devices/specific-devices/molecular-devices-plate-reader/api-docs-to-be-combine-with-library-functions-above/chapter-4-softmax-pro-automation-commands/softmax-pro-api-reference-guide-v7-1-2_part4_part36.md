# softmax pro api reference guide v7 1 2\_Part4\_Part36

}\
private void CommandCompleted( object sender,\
SoftMaxPro.AutomationClient.SMPAutomationClient.CommandStatusEventArg e)\
{\
Results.AppendResult("Command complete Command ID = " + e.QueueID.ToString() ); if( mStatusID == e.QueueID )\
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
Results.AppendResult("Error: Command ID = " + e.QueueID.ToString() + " - " + e.Error); }

SetReader

Int32 SetReader(String port, String instrument)\
The SetReader command selects a microplate reader type and sets the instrument status. See Examples on page 101.

Parameters

| <img src="../../../../../.gitbook/assets/0 (26).png" alt="" data-size="original"> | Note: The parameters are case-sensitive. |
| --------------------------------------------------------------------------------- | ---------------------------------------- |

communication port

Type: String

The name of the communication port to look for the instrument (for example, COM1).

Offline sets the instrument state to Offline.\
instrument

Type: String

340PC384

DTX 800

DTX 880

Emax\
Emax Plus\
FilterMax F3\
FilterMax F5\
Flexstation III\
GEMINI EM\
GEMINI XPS\
PLUS190PC\
PLUS384\
SpectraMax i3\
SpectraMax i3x\
SpectraMax iD3\
SpectraMax iD5\
SPECTRAmax M2\
SPECTRAmax M2e\
SPECTRAmax M3\
SPECTRAmax M4\
SPECTRAmax M5\
SPECTRAmax M5e\
SpectraMax Paradigm\
VersaMaxPLUS\
Vmax
