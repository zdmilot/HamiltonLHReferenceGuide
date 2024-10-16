# GetConfiguration

## Description

This function is used to retrieve the current values of all configuration parameters of the device.

The configuration values returned by this command can be set using the following functions:

*
* SetDateTime
* SetNetWorkConfig
* SetLogLevel
  *

### Syntax

```
GetConfiguration (variable i_intDeviceID, 
                  variable i_strLockID, 
                  variable& o_strConfigurationXML,
                  variable& o_intSiLAReturnValue, 
                  variable& o_strSiLAMessage)
```

### Arguments

| argument                      | value       | description                                                                                                                                                           |
| ----------------------------- | ----------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| i\_intDeviceID \[in]          | int \[1..4] | Unique identifier for the device as returned by function Connect.                                                                                                     |
| i\_strLockID \[in]            | string      | <p>LockID for the device. This identifier has to be used in case the device is locked.</p><p>Use functions LockDevice and UnlockDevice to lock/unlock the device.</p> |
| o\_strConfigurationXML \[out] | string      | An XML formatted string with the current values of all configuration parameters.                                                                                      |
| o\_intSiLAReturnValue \[out]  | int         | The SiLA return code of the device.                                                                                                                                   |
| o\_strSiLAMessage \[out]      | string      | The SiLA message returned by the device.                                                                                                                              |
