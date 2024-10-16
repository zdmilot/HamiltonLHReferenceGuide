# GetChillerTemperature Method

Gets the thermoelectric cooler temperature

## Syntax

```
function GetChillerTemperature(
	variable& chillerTemperature
) variable
```

## **Parameters**

| Name               | Type                                                                 | Description                         |
| ------------------ | -------------------------------------------------------------------- | ----------------------------------- |
| chillerTemperature | [System.Double](https://docs.microsoft.com/dotnet/api/system.double) | The chiller temperature in Celsius. |

## **Return Value**

[Int32](https://docs.microsoft.com/dotnet/api/system.int32)\
Zero on success![](blob:https://app.gitbook.com/1395453d-99f5-498d-9067-bb22d57f15e5)

## Remarks

The function will only work on HiG centrifuges equipped with a thermoelectric cooler.
