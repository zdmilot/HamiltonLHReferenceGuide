# SetNetWorkConfig

## Description

This function is used to set the network configuration of the device.

If the default configuration with the supplied router is used, no network setting have to be made.

This function should only be used by experienced users as it could leave the device in an unusable state !

All changes to the network configuration will take effect after powercycling the device.

### Syntax

```
SetNetWorkConfig (variable i_intDeviceID, 
                  variable i_strLockID, 
                  variable i_strIPAddress,
                  variable i_strSubNet,
                  variable i_strGateWay,
                  variable i_strDNS1,
                  variable i_strDNS2,
                  variable& o_intSiLAReturnValue, 
                  variable& o_strSiLAMessage)
```

### Arguments

| argument                     | value       | description                                                                                                                                                                                                                                                                                                  |
| ---------------------------- | ----------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| i\_intDeviceID \[in]         | int \[1..4] | Unique identifier for the device as returned by function Connect.                                                                                                                                                                                                                                            |
| i\_strLockID \[in]           | string      | <p>LockID for the device. This identifier has to be used in case the device is locked.</p><p>Use functions LockDevice and UnlockDevice to lock/unlock the device.</p>                                                                                                                                        |
| i\_strIPAddress \[in]        | string      | <p>IP address of the device in format 'xxx.xxx.xxx.xxx' or 'DHCP' to use DHCP (recommended).</p><p>If an IP address is supplied, the parameter <em>i_strSubNet</em> has to be set also.</p>                                                                                                                  |
| i\_strSubNet \[in]           | string      | <p>Subnet mask of the device in format 'xxx.xxx.xxx.xxx'.</p><p>Is ignored if parameter <em>i_strIPAddress</em> is set to 'DHCP'.</p><p>This parameter has to be set in case parameter <em>i_strIPAddress</em> is set to a specific IP address.<br><br></p><p>A standard subnet mask is '255.255.255.0'.</p> |
| i\_strGateWay \[in]          | string      | <p>IP address of the gateway in format 'xxx.xxx.xxx.xxx'.</p><p>Is ignored if parameter <em>i_strIPAddress</em> is set to 'DHCP'.</p><p>This is an optional parameter.</p>                                                                                                                                   |
| i\_strDNS1 \[in]             | string      | <p>IP address of the name server 1 in format 'xxx.xxx.xxx.xxx'.</p><p>Is ignored if parameter <em>i_strIPAddress</em> is set to 'DHCP'.</p><p>This is an optional parameter.</p>                                                                                                                             |
| i\_strDNS2 \[in]             | string      | <p>IP address of the name server 2 in format 'xxx.xxx.xxx.xxx'.</p><p>Is ignored if parameter <em>i_strIPAddress</em> is set to 'DHCP'.</p><p>This is an optional parameter.</p>                                                                                                                             |
| o\_intSiLAReturnValue \[out] | int         | The SiLA return code of the device.                                                                                                                                                                                                                                                                          |
| o\_strSiLAMessage \[out]     | string      | The SiLA message returned by the device.                                                                                                                                                                                                                                                                     |
