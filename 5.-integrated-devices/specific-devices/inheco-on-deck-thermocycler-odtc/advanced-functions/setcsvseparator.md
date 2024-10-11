# SetCSVSeparator

## Description

This function is used to set the CSV character used for the reported data of function GetLastData.

### Syntax

```
SetCSVSeparator (variable i_intDeviceID, 
                 variable i_strLockID, 
                 variable i_strCSVSeparator,
                 variable& o_intSiLAReturnValue, 
                 variable& o_strSiLAMessage)
```

### Arguments

| argument                     | value       | description                                                                                                                                                                                |
| ---------------------------- | ----------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| i\_intDeviceID \[in]         | int \[1..4] | Unique identifier for the device as returned by function Connect.                                                                                                                          |
| i\_strLockID \[in]           | string      | <p>LockID for the device. This identifier has to be used in case the device is locked.</p><p>Use functions LockDevice and UnlockDevice to lock/unlock the device.</p>                      |
| i\_strCSVSeparator \[in]     | string      | <p>Separation character for data reported by function GetLastData.</p><p>Use a single char like ';' or ','.</p><p>Be aware that separators like '.' or ':' may lead to crippled data !</p> |
| o\_intSiLAReturnValue \[out] | int         | The SiLA return code of the device.                                                                                                                                                        |
| o\_strSiLAMessage \[out]     | string      | The SiLA message returned by the device.                                                                                                                                                   |
