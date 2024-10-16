# SetParameters

## Description

This function is used to set the current values of a parameter of the device.

See the device's SiLA specification for the values to be set.

### Syntax

```
SetParameters (variable i_intDeviceID, 
               variable i_strLockID, 
               variable i_strParameterName,
               variable i_strParameterType,
               variable i_strParameterValue,
               variable& o_intSiLAReturnValue, 
               variable& o_strSiLAMessage)
```

### Arguments

| argument                     | value       | description                                                                                                                                                           |
| ---------------------------- | ----------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| i\_intDeviceID \[in]         | int \[1..4] | Unique identifier for the device as returned by function Connect.                                                                                                     |
| i\_strLockID \[in]           | string      | <p>LockID for the device. This identifier has to be used in case the device is locked.</p><p>Use functions LockDevice and UnlockDevice to lock/unlock the device.</p> |
| i\_strParameterName \[in]    | string      | Name of the parameter to set.                                                                                                                                         |
| i\_strParameterType \[in]    | string      | Type of the parameter to set.                                                                                                                                         |
| i\_strParameterValue \[in]   | string      | Value of the parameter to set.                                                                                                                                        |
| o\_intSiLAReturnValue \[out] | int         | The SiLA return code of the device.                                                                                                                                   |
| o\_strSiLAMessage \[out]     | string      | The SiLA message returned by the device.                                                                                                                              |
