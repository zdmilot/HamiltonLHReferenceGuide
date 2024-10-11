# ExecuteMethod

## Description

This function is used to execute a method on the Inheco ODTC device.

The function just starts the method and returns - this behavior offers the possibility to do other things in parallel while the method is executed.

Use the output parameters _o\_intDuration_ and _o\_intRequestId_ as input parameter for function WaitForEndOfExecuteMethod.

This function executes a method that is available in device memory. Use function DownloadProtocol to download a protocol generated with the script editor to the device.

It is mandatory to use function WaitForEndOfExecuteMethod before starting the next method !

### Syntax

```
ExecuteMethod (variable i_intDeviceID, 
               variable i_strLockID,
               variable i_strMethodName, 
               variable i_intPriority,
               variable& o_intDuration,
               variable& o_intRequestID,
               variable& o_intSiLAReturnValue, 
               variable& o_strSiLAMessage)
```

### Arguments

| argument                     | value           | description                                                                                                                                                                                                                        |
| ---------------------------- | --------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| i\_intDeviceID \[in]         | int \[1..4]     | Unique identifier for the device as returned by function Connect.                                                                                                                                                                  |
| i\_strLockID \[in]           | string          | <p>LockID for the device. This identifier has to be used in case the device is locked.</p><p>Use functions LockDevice and UnlockDevice to lock/unlock the device.</p>                                                              |
| i\_strMethodName \[in]       | string          | <p>Method name to be excuted.</p><p>The method name must be defined in the protocol on the device.</p><p>Names are case-sensitive !</p>                                                                                            |
| i\_intPriority \[in]         | int \[0..10001] | <p>Priority for this method.</p><p>Set this parameter to 10000 to shorten the lid-preheating method to 40 seconds in case the lid has been heated up before.</p><p>In case of all standard methods, this parameter is ignored.</p> |
| o\_intDuration \[out]        | int             | <p>The expected duration of the method as calculated by the device.</p><p>Use this value as input parameter for function WaitForEndOfExecuteMethod.</p>                                                                            |
| o\_intRequestID \[out]       | int             | <p>The requestId of the method.</p><p>Use this value as input parameter for function WaitForEndOfExecuteMethod.</p>                                                                                                                |
| o\_intSiLAReturnValue \[out] | int             | The SiLA return code of the device.                                                                                                                                                                                                |
| o\_strSiLAMessage \[out]     | string          | The SiLA message returned by the device.                                                                                                                                                                                           |
