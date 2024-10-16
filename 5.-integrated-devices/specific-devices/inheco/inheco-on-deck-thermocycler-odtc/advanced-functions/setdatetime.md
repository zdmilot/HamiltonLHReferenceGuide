# SetDateTime

## Description

This function is used to set the date and time of the device.

### Syntax

```
SetDateTime (variable i_intDeviceID, 
             variable i_strLockID, 
             variable i_strDateTime,
             variable& o_intSiLAReturnValue, 
             variable& o_strSiLAMessage)
```

### Arguments

| argument                     | value       | description                                                                                                                                                                                                                                                                           |
| ---------------------------- | ----------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| i\_intDeviceID \[in]         | int \[1..4] | Unique identifier for the device as returned by function Connect.                                                                                                                                                                                                                     |
| i\_strLockID \[in]           | string      | <p>LockID for the device. This identifier has to be used in case the device is locked.</p><p>Use functions LockDevice and UnlockDevice to lock/unlock the device.</p>                                                                                                                 |
| i\_strDateTime \[in]         | string      | <p>New date and time for the device in format 'YYYY-MM-DDTHH:MM:SSZ'.</p><p>Use the following function from library HSLTimLib.hsl:<br><br></p><ul><li>TimGetFormattedDate with the format string '%Y-%m-%dT'</li><li>TimGetFormattedTime with the format string '%H:%M:%SZ'</li></ul> |
| o\_intSiLAReturnValue \[out] | int         | The SiLA return code of the device.                                                                                                                                                                                                                                                   |
| o\_strSiLAMessage \[out]     | string      | The SiLA message returned by the device.                                                                                                                                                                                                                                              |
