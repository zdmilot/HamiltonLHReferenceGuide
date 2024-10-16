# SetFanSpeed Method

Changes fan speed. Range of 12-100 as a percentage for the speed of the fan.

## Syntax

```
function SetFanSpeed(
	variable speed
) variable
```

AddLanguageTabSet("ID0EACA");

## **Parameters**

| Name  | Type                                                                                                                                             | Description                                                                                                                                    |
| ----- | ------------------------------------------------------------------------------------------------------------------------------------------------ | ---------------------------------------------------------------------------------------------------------------------------------------------- |
| speed | [System. AddLanguageSpecificTextSet("LST975420A4\_0?cs=.\|vb=.\|cpp=::\|nu=.\|fs=."); Int32](https://docs.microsoft.com/dotnet/api/system.int32) | Speed of which the fans should be changed to. Range of 12-100 as a percentage for the speed of the fan. Less then 12 is too slow for the fans. |

## **Return Value**

[Int32](https://docs.microsoft.com/dotnet/api/system.int32)\
0 if successful, 1 otherwise
