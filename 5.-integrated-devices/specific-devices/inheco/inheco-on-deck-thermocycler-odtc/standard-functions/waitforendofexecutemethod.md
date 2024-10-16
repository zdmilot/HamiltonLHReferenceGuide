# WaitForEndOfExecuteMethod

## Description

This function is used to asynchronously wait for a method.

To start a method, use function ExecuteMethod.

### Syntax

```
WaitForEndOfExecuteMethod (variable i_intDeviceID, 
                           variable i_intTimeOut,
                           variable i_intRequestID,
                           variable& o_intSiLAReturnValue, 
                           variable& o_strSiLAMessage)
```

### Arguments

| argument                     | value       | description                                                                                                          |
| ---------------------------- | ----------- | -------------------------------------------------------------------------------------------------------------------- |
| i\_intDeviceID \[in]         | int \[1..4] | Unique identifier for the device as returned by function Connect.                                                    |
| i\_intTimeOut \[in]          | int         | <p>Timeout for the function.</p><p>Use the output parameter <em>o_intDuration</em> of function ExecuteMethod.</p>    |
| i\_intRequestID \[in]        | int         | <p>RequestId for the function.</p><p>Use the output parameter <em>o_intRequestID</em> of function ExecuteMethod.</p> |
| o\_intSiLAReturnValue \[out] | int         | The SiLA return code of the device.                                                                                  |
| o\_strSiLAMessage \[out]     | string      | The SiLA message returned by the device.                                                                             |
