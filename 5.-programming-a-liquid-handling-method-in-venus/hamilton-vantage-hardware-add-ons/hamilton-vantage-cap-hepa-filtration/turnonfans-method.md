# TurnOnFans Method

Turns on the fans on the Vantage CAP. This function will determine the default speed at which the fans will spin based on the status of the door sensors for the hood.

## Syntax

```
function TurnOnFans() variable
```

AddLanguageTabSet("ID0EACA");

## **Return Value**

[Int32](https://docs.microsoft.com/dotnet/api/system.int32)\
0 on success, 1 otherwiseRemarksThis call will start the fan based on the DoorOpenFanSpeed (Default of 90%) and the FanSwitchSpeed (Default of 70%) firmware parameters that can be set by connecting to the device through DTK as a monitor and setting the values with the setter functions. If the door is open then when this command is called it will start the fans at the DoorOpenFanSpeed variable amount. If the door is closed it will start the fans at the FansSwitchSpeed value of speed.
