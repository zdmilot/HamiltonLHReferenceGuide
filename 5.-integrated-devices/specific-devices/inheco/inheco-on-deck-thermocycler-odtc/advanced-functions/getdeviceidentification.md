# GetDeviceIdentification

## Description

This function is used to retrieve specific information of the device.

### Syntax

```
GetDeviceIdentification (variable i_intDeviceID, 
                         variable i_strLockID, 
                         variable& o_strDeviceFirmwareVersion,
                         variable& o_strDeviceManufacturer,
                         variable& o_strDeviceName,
                         variable& o_strDeviceSerialNumber,
                         variable& o_strSiLAInterfaceVersion,
                         variable& o_strSiLASubDeviceClass,
                         variable& o_strWsdl,
                         variable& o_intSiLAReturnValue, 
                         variable& o_strSiLAMessage)
```

### Arguments

| argument                           | value       | description                                                                                                                                                           |
| ---------------------------------- | ----------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| i\_intDeviceID \[in]               | int \[1..4] | Unique identifier for the device as returned by function Connect.                                                                                                     |
| i\_strLockID \[in]                 | string      | <p>LockID for the device. This identifier has to be used in case the device is locked.</p><p>Use functions LockDevice and UnlockDevice to lock/unlock the device.</p> |
| o\_strDeviceFirmwareVersion \[out] | string      | Internal information of the device.                                                                                                                                   |
| o\_strDeviceManufacturer \[out]    | string      | Internal information of the device.                                                                                                                                   |
| o\_strDeviceName \[out]            | string      | Internal information of the device.                                                                                                                                   |
| o\_strDeviceSerialNumber \[out]    | string      | Internal information of the device.                                                                                                                                   |
| o\_strSiLAInterfaceVersion \[out]  | string      | Internal information of the device.                                                                                                                                   |
| o\_strSiLASubDeviceClass \[out]    | string      | Internal information of the device.                                                                                                                                   |
| o\_strWsdl \[out]                  | string      | Internal information of the device.                                                                                                                                   |
| o\_intSiLAReturnValue \[out]       | int         | The SiLA return code of the device.                                                                                                                                   |
| o\_strSiLAMessage \[out]           | string      | The SiLA message returned by the device.                                                                                                                              |
