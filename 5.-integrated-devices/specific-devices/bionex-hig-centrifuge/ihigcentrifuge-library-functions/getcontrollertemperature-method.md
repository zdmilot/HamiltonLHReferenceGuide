# GetControllerTemperature Method

Gets the temperature of the DSP on the motion controller PCB.

## Syntax

```
function GetControllerTemperature(
	variable& controllerTemperature
) variable
```

## **Parameters**

| Name                  | Type                                                                 | Description                            |
| --------------------- | -------------------------------------------------------------------- | -------------------------------------- |
| controllerTemperature | [System.Double](https://docs.microsoft.com/dotnet/api/system.double) | The controller temperature in Celsius. |

## **Return Value**

[Int32](https://docs.microsoft.com/dotnet/api/system.int32)\
Zero on success
