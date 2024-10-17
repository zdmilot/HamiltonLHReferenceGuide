# ReadAirFlow Method

Retrieves airflow information from sensor. This is a optional sensor or a sensor that was used on previous devices that may or may not be available now.

## Syntax

```
function ReadAirFlow(
	variable& airFlow
) variable
```

AddLanguageTabSet("ID0EACA");

## **Parameters**

| Name    | Type                                                                 | Description                                                                      |
| ------- | -------------------------------------------------------------------- | -------------------------------------------------------------------------------- |
| airFlow | [System.Single](https://docs.microsoft.com/dotnet/api/system.single) | Airflow value returned. If the sensor does not exist it returns a reading of 50. |

**Return Value**

[Int32](https://docs.microsoft.com/dotnet/api/system.int32)\
0 on success, 1 otherwise
