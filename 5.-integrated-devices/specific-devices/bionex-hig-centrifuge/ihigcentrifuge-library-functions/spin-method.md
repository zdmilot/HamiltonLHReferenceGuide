# Spin Method

Starts centrifuge spin cycle and immediately returns control to the method.

## Syntax

```
function Spin(
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

## Remarks

The [IsSpinning(Boolean)](chm://34b2263d11bef9c1c3f6e65f22fae21e/html/f6e1c4f3-34c1-22c4-9e23-532563e799e8.htm) function method MUST be called between a Spin() function call and other centrifuge functions that result in mechanical motion, because only a single command may be issued to the centrifuge at one time.\
\
