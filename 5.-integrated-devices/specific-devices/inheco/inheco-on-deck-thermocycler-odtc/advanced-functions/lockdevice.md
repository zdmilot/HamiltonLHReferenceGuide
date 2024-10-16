# LockDevice

## Description

This function is used to lock the ODTC device for use by other programs or users.

This function should be used after function Reset to ensure that the device will be locked exclusively.

As this function can lock up the whole device, it should only be used if necessary - do not use it if Venus is the only software controlling the device !

### Syntax

```
LockDevice (variable i_intDeviceID, 
            variable i_intTimeout,
            variable i_strPMSID,
            variable i_strLockID, 
            variable& o_intSiLAReturnValue, 
            variable& o_strSiLAMessage)
```

### Arguments

| argument                     | value       | description                                                                                                                                                                                                                                                                                                      |
| ---------------------------- | ----------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| i\_intDeviceID \[in]         | int \[1..4] | Unique identifier for the device as returned by function Connect.                                                                                                                                                                                                                                                |
| i\_intTimeout \[in]          | int \[0..]  | <p>Timeout for the function in seconds.</p><p>If the timeout duration is elapsed, the device will be set to standby mode.</p><p>Use a timeout value of 0 to lock the device without timeout.</p><p>In case a timeout of 0 seconds has been used, the device has to be unlocked using function UnlockDevice !</p> |
| i\_strPMSID \[in]            | string      | The name of the PMS that locked the device.                                                                                                                                                                                                                                                                      |
| i\_strLockID \[in]           | string      | <p>LockID for the device. This identifier has to be used in case the device is locked.</p><p>Use functions LockDevice and UnlockDevice to lock/unlock the device.</p>                                                                                                                                            |
| o\_intSiLAReturnValue \[out] | int         | The SiLA return code of the device.                                                                                                                                                                                                                                                                              |
| o\_strSiLAMessage \[out]     | string      | The SiLA message returned by the device.                                                                                                                                                                                                                                                                         |
