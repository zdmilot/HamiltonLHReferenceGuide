# Pause

## Description

This function is used to set the Inheco ODTC device to pause mode.

Using this function may have influence on the results !

### Syntax

```
Pause (variable i_intDeviceID, 
       variable i_strLockID, 
       variable & o_intSiLAReturnValue, 
       variable & o_strSiLAMessage)
```

### Arguments

| argument                     | value       | description                                                                                                                                                           |
| ---------------------------- | ----------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| i\_intDeviceID \[in]         | int \[1..4] | Unique identifier for the device as returned by function Connect.                                                                                                     |
| i\_strLockID \[in]           | string      | <p>LockID for the device. This identifier has to be used in case the device is locked.</p><p>Use functions LockDevice and UnlockDevice to lock/unlock the device.</p> |
| o\_intSiLAReturnValue \[out] | int         | The SiLA return code of the device.                                                                                                                                   |
| o\_strSiLAMessage \[out]     | string      | The SiLA message returned by the device.                                                                                                                              |
