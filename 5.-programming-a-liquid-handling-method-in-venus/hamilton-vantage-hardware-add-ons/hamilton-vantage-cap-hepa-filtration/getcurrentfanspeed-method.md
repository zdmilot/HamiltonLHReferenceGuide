# GetCurrentFanSpeed Method

Gets the current fan speed on the device.

## Syntax

```
function GetCurrentFanSpeed(
	variable& speed
) variable
```

AddLanguageTabSet("ID0EACA");

## **Parameters**

| Name  | Type                                                               | Description                                                                                                                                               |
| ----- | ------------------------------------------------------------------ | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| speed | [System.Int32](https://docs.microsoft.com/dotnet/api/system.int32) | Average speed across the fan speed sensors as a percentage. If the fans are turned off or there is a error this will report back a value of -1 for speed. |

## **Return Value**

[Int32](https://docs.microsoft.com/dotnet/api/system.int32)\
0 on success, 1 otherwise
