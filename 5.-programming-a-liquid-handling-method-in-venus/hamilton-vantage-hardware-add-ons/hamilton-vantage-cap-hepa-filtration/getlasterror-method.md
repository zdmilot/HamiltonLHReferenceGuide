# GetLastError Method

Gets the last error for the driver.

## Syntax

```
function GetLastError(
	variable& error
) variable
```

AddLanguageTabSet("ID0EACA");

## **Parameters**

| Name  | Type                                                                                                                                                                                                  | Description                                                                                                                              |
| ----- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------- |
| error | [System. AddLanguageSpecificTextSet("LSTA5FA676B\_0?cs=.\|vb=.\|cpp=::\|nu=.\|fs=."); String](https://docs.microsoft.com/dotnet/api/system.string)AddLanguageSpecificTextSet("LSTA5FA676B\_1?cpp=%"); | String representation of the last error on the device. If no error has occurred it will return a string staying "No error has occurred." |

## **Return Value**

[Int32](https://docs.microsoft.com/dotnet/api/system.int32)\
0 if successful, 1 otherwise
