# DoContinue

## Description

This function is used to continue a paused method on the Inheco ODTC device.

Use function Pause to pause a method on the device.

### Syntax

```
DoContinue (variable i_intDeviceID, 
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
