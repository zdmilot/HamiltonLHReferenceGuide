# SpinAndWait Method

Starts centrifuge spin cycle and waits for it to complete before returning control.

## Syntax

```
function SpinAndWait(
	variable rotationalGs,
	variable accelPercent,
	variable decelPercent,
	variable timeSeconds
) variable
```

## **Parameters**

| Name         | Type                                                                 | Description                                                                                                                                                                                     |
| ------------ | -------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| rotationalGs | [System.Double](https://docs.microsoft.com/dotnet/api/system.double) | rotational acceleration expressed in terms of G's, where G = gravitational force (valid values are 250 - 5000); max allowed value is hardware dependent and specified in the (App.config) file. |
| accelPercent | [System.Double](https://docs.microsoft.com/dotnet/api/system.double) | Rate of acceleration as a percentage (valid values are 1 - 100)                                                                                                                                 |
| decelPercent | [System.Double](https://docs.microsoft.com/dotnet/api/system.double) | Rate of deceleration as a percentage (valid values are 1 - 100)                                                                                                                                 |
| timeSeconds  | [System.Double](https://docs.microsoft.com/dotnet/api/system.double) | Any positive value in seconds; indicates time at full speed (does not include acceleration and deceleration)                                                                                    |

## **Return Value**

[Int32](https://docs.microsoft.com/dotnet/api/system.int32)\
Zero on success
