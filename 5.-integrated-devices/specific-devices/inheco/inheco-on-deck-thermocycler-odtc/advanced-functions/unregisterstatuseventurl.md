# UnregisterStatusEventURL

## Description

This function is used to remove an endpoint from the list of endpoints of the device to which events are sent.

### Syntax

```
UnregisterStatusEventURL (variable i_intDeviceID, 
                          variable i_strLockID, 
                          variable i_strURL,
                          variable& o_intSiLAReturnValue, 
                          variable& o_strSiLAMessage)
```

### Arguments

| argument                     | value       | description                                                                                                                                                           |
| ---------------------------- | ----------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| i\_intDeviceID \[in]         | int \[1..4] | Unique identifier for the device as returned by function Connect.                                                                                                     |
| i\_strLockID \[in]           | string      | <p>LockID for the device. This identifier has to be used in case the device is locked.</p><p>Use functions LockDevice and UnlockDevice to lock/unlock the device.</p> |
| i\_strURL \[in]              | string      | URL of the endpoint to remove.                                                                                                                                        |
| o\_intSiLAReturnValue \[out] | int         | The SiLA return code of the device.                                                                                                                                   |
| o\_strSiLAMessage \[out]     | string      | The SiLA message returned by the device.                                                                                                                              |
