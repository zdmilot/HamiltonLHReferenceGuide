# SetShake

Int32 SetShake(Boolean shakestate)\
The SetShake command shakes the plate. When this command is set to true, starts shaking the plate tray until the Shake(false) command is sent. By default, the shake stops after 30 seconds in most instruments.

| <img src="../../../../../.gitbook/assets/0 (9) (1).png" alt="" data-size="original"> | Note: The SetShake command does not support the FilterMax F3, FilterMax F5, SpectraMax i3, SpectraMax i3x, and SpectraMax Paradigm. |
| ------------------------------------------------------------------------------------ | ----------------------------------------------------------------------------------------------------------------------------------- |

Parameters\
shakestate

Type: Boolean

true turns Shake on.

false turns Shake off.

Example\
This example describes how to turn the shake function on and then off.

public void Main()\
{\
AutomationObject.Initialize("localhost");\
AutomationObject.CommandCompleted += CommandCompleted;\
AutomationObject.ErrorReport += Error;\
AutomationObject.Initialize();\
AutomationObject.SetReader("Offline", "SPECTRAmax M2");\
AutomationObject.SetSimulationMode(true);\
AutomationObject.SelectSection("Plate1");\
AutomationObject.CloseDrawer();\
AutomationObject.SetShake(true);\
AutomationObject.StartRead();\
AutomationObject.SetShake(false);\
AutomationObject.OpenDrawer();\
}\
private void CommandCompleted( object sender,\
SoftMaxPro.AutomationClient.SMPAutomationClient.CommandStatusEventArg e) {\
if( e.QueueEmpty)\
{\
Results.AppendResult("Queue empty - disconnecting events"); AutomationObject.ErrorReport -= Error;\
AutomationObject.CommandCompleted -= CommandCompleted;\
AutomationObject.Dispose();\
}
