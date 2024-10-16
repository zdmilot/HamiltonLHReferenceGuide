# GetLastData

## Description

This function is used to retrieve an xml string with all data collected during the runtime of a method.

### Syntax

```
GetLastData (variable i_intDeviceID, 
             variable i_strLockID, 
             variable& o_strResult,
             variable& o_intSiLAReturnValue, 
             variable& o_strSiLAMessage)
```

### Arguments

| argument                     | value       | description                                                                                                                                                           |
| ---------------------------- | ----------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| i\_intDeviceID \[in]         | int \[1..4] | Unique identifier for the device as returned by function Connect.                                                                                                     |
| i\_strLockID \[in]           | string      | <p>LockID for the device. This identifier has to be used in case the device is locked.</p><p>Use functions LockDevice and UnlockDevice to lock/unlock the device.</p> |
| o\_strResult \[out]          | string      | An xml string with all data collected during the last method run.                                                                                                     |
| o\_intSiLAReturnValue \[out] | int         | The SiLA return code of the device.                                                                                                                                   |
| o\_strSiLAMessage \[out]     | string      | The SiLA message returned by the device.                                                                                                                              |
