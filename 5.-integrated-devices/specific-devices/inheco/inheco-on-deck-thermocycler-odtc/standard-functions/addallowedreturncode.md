# AddAllowedReturnCode

## Description

This function is used to add an error number to a list of error return values that are treated as successful return values.

### Syntax

```
AddAllowedReturnCode (variable i_intDeviceID, 
                      variable i_intReturnValueToIgnore)
```

### Arguments

| argument                        | value       | description                                                                                                                           |
| ------------------------------- | ----------- | ------------------------------------------------------------------------------------------------------------------------------------- |
| i\_intDeviceID \[in]            | int \[1..4] | Unique identifier for the device as returned by function Connect.                                                                     |
| i\_intReturnValueToIgnore \[in] | int         | <p>Error number to add to list.</p><p>See chapter SiLA ReturnCodes and Inheco SiLA documentation for the available error numbers.</p> |
