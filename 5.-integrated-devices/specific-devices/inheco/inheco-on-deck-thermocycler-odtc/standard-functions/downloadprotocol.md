# DownloadProtocol

## Description

This function is used to transfer a protocol to the Inheco ODTC device.

Use function ExecuteMethod to start a method from the protocol.

### Syntax

```
DownloadProtocol (variable i_intDeviceID, 
                  variable i_strLockID,
                  variable i_strProtocolFile,
                  variable& o_intSiLAReturnValue, 
                  variable& o_strSiLAMessage)
```

### Arguments

| argument                     | value       | description                                                                                                                                                           |
| ---------------------------- | ----------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| i\_intDeviceID \[in]         | int \[1..4] | Unique identifier for the device as returned by function Connect.                                                                                                     |
| i\_strLockID \[in]           | string      | <p>LockID for the device. This identifier has to be used in case the device is locked.</p><p>Use functions LockDevice and UnlockDevice to lock/unlock the device.</p> |
| i\_strProtocolFile \[in]     | string      | <p>Full path to the protocol file.</p><p>Use the Inheco Script Editor to create and save new protocols.</p>                                                           |
| o\_intSiLAReturnValue \[out] | int         | The SiLA return code of the device.                                                                                                                                   |
| o\_strSiLAMessage \[out]     | string      | The SiLA message returned by the device.                                                                                                                              |
