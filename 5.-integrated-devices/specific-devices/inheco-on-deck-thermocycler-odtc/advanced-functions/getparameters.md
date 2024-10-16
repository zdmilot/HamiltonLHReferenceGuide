# GetParameters

## Description

This function is used to retrieve the current values of all parameters of the device.

The parameter values returned by this command can be set using the following functions:

*
* DownloadProtocol
* DisableTemperatureEvent
* SetCSVSeparator
  *

### Syntax

```
GetParameters (variable i_intDeviceID, 
               variable i_strLockID, 
               variable& o_strParametersXML,
               variable& o_intSiLAReturnValue, 
               variable& o_strSiLAMessage)
```

### Arguments

| argument                     | value       | description                                                                                                                                                           |
| ---------------------------- | ----------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| i\_intDeviceID \[in]         | int \[1..4] | Unique identifier for the device as returned by function Connect.                                                                                                     |
| i\_strLockID \[in]           | string      | <p>LockID for the device. This identifier has to be used in case the device is locked.</p><p>Use functions LockDevice and UnlockDevice to lock/unlock the device.</p> |
| o\_strParametersXML \[out]   | string      | An XML formatted string with the current values of all parameters.                                                                                                    |
| o\_intSiLAReturnValue \[out] | int         | The SiLA return code of the device.                                                                                                                                   |
| o\_strSiLAMessage \[out]     | string      | The SiLA message returned by the device.                                                                                                                              |
