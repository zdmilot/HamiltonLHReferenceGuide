# SetLogLevel

## Description

This function is used to set the level of logs of the device.

The log level should only be changed when requested by Hamilton or Inheco personnel !

### Syntax

```
SetLogLevel (variable i_intDeviceID, 
             variable i_strLockID, 
             variable i_strLogLevel,
             variable& o_intSiLAReturnValue, 
             variable& o_strSiLAMessage)
```

### Arguments

| argument                     | value       | description                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| ---------------------------- | ----------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| i\_intDeviceID \[in]         | int \[1..4] | Unique identifier for the device as returned by function Connect.                                                                                                                                                                                                                                                                                                                                                                                                                |
| i\_strLockID \[in]           | string      | <p>LockID for the device. This identifier has to be used in case the device is locked.</p><p>Use functions LockDevice and UnlockDevice to lock/unlock the device.</p>                                                                                                                                                                                                                                                                                                            |
| i\_strLogLevel \[out]        | string      | <p>Log level of the device. Set to one of the following constants:</p><table><thead><tr><th>constant</th><th>value</th></tr></thead><tbody><tr><td>Inheco_ODTC::LogLevel::Debug</td><td>'DEBUG'</td></tr><tr><td>Inheco_ODTC::LogLevel::Info</td><td>'INFO'</td></tr><tr><td>Inheco_ODTC::LogLevel::Warning</td><td>'WARN'</td></tr><tr><td>Inheco_ODTC::LogLevel::Error</td><td>'ERROR'</td></tr><tr><td>Inheco_ODTC::LogLevel::Fatal</td><td>'FATAL'</td></tr></tbody></table> |
| o\_intSiLAReturnValue \[out] | int         | The SiLA return code of the device.                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| o\_strSiLAMessage \[out]     | string      | The SiLA message returned by the device.                                                                                                                                                                                                                                                                                                                                                                                                                                         |
