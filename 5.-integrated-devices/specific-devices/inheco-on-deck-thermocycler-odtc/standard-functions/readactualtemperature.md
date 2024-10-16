# ReadActualTemperature

## Description

This function is used to retrieve the current values of the temperature sensors of the device.

### Syntax

```
ReadActualTemperature (variable i_intDeviceID, 
                       variable i_strLockID, 
                       variable& o_strTime,
                       variable& o_arrfltActualTemperatures[],
                       variable& o_arrstrActualTemperatureNames[],
                       variable& o_intSiLAReturnValue, 
                       variable& o_strSiLAMessage)
```

### Arguments

| argument                               | value                  | description                                                                                                                                                           |
| -------------------------------------- | ---------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| i\_intDeviceID \[in]                   | int \[1..4]            | Unique identifier for the device as returned by function Connect.                                                                                                     |
| i\_strLockID \[in]                     | string                 | <p>LockID for the device. This identifier has to be used in case the device is locked.</p><p>Use functions LockDevice and UnlockDevice to lock/unlock the device.</p> |
| o\_strTime \[out]                      | string                 | The time as received from the device.                                                                                                                                 |
| o\_arrfltActualTemperatures \[out]     | array of float values  | Array of 8 temperature values in °C.                                                                                                                                  |
| o\_arrstrActualTemperatureNames \[out] | array of string values | Array of 8 temperature names according to parameter _o\_arrfltActualTemperatures_.                                                                                    |
| o\_intSiLAReturnValue \[out]           | int                    | The SiLA return code of the device.                                                                                                                                   |
| o\_strSiLAMessage \[out]               | string                 | The SiLA message returned by the device.                                                                                                                              |
