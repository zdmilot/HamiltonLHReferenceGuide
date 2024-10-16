# Connect Method

Connects to the device and gets the installed firmware version.![](blob:https://app.gitbook.com/2776e2d7-c8eb-4ae2-b475-705cc9eb20ec)

## Syntax

```
function Connect(
	variable deviceName,
	variable adapterDeviceId,
	variable simulateHardware,
	variable& firmwareVersion
) variable
```

## **Parameters**

| Name             | Type                                                                   | Description                                                          |
| ---------------- | ---------------------------------------------------------------------- | -------------------------------------------------------------------- |
| deviceName       | [System.String](https://docs.microsoft.com/dotnet/api/system.string)   | User assigned name for the device that will appear in error messages |
| adapterDeviceId  | [System.String](https://docs.microsoft.com/dotnet/api/system.string)   | The CAN adapter's windows device ID                                  |
| simulateHardware | [System.Boolean](https://docs.microsoft.com/dotnet/api/system.boolean) | Use 0 for actual hardware or 1 to simulate                           |
| firmwareVersion  | [System.String](https://docs.microsoft.com/dotnet/api/system.string)   | The firmware version                                                 |

## **Return Value**

[Int32](https://docs.microsoft.com/dotnet/api/system.int32)\
Zero on success

## Remarks

After the USB-CAN module driver is installed, the adapterDeviceId my be ascertained by navigating to Windows START → Programs → USB-CAN Module Utilities → Tools → USB-CAN module control. The value is identified as "DevNr".
