# Connect

## Description

This function is used to connect to the Inheco ODTC device.

### Syntax

```
Connect (variable i_strLocalIP
         variable i_strDeviceIP, 
         variable i_strDevicePort, 
         variable i_blnSimulationMode, 
         variable& o_intDeviceID, 
         variable& o_strMessage)
```

### Arguments

<table><thead><tr><th width="165">argument</th><th width="90">value</th><th>description</th></tr></thead><tbody><tr><td>i_strLocalIP [in]</td><td>string</td><td><p>The IP address of the computer.</p><p>If this parameter is set to an empty string, the library will try to retrieve the computer's IP address automatically.</p><p>If automatic IP address configuration doesn't work (i.e. two or more network cards in system with close IP addresses), configure the IP address to a fixed one and supply this address.</p></td></tr><tr><td></td><td></td><td></td></tr><tr><td>i_strDeviceIP [in]</td><td>string</td><td><p>The IP address of the ODTC device.</p><p>IP address must be in format "xxx.xxx.xxx.xxx".</p><p>The IP address of the device can be retrieved using the Inheco device finder tool located in the library directory:</p><ul><li>Start the application 'DeviceFinder (xxxxx).exe' where xxxxx represents a five-digit revision number</li><li>wait at least 20 seconds to see the retrieved ip address</li><li>if address is not found automatically, click button 'Find Device via Name/IP' and supply the string ODTC_XXXXXX where XXXXXX represents the last 6 characters of the device's MAC address.</li><li>The string to provide may be found on the label SiLA Service Configuration located on the device controller.</li></ul></td></tr><tr><td>i_strDevicePort [in]</td><td>string</td><td><p>The port used by the ODTC device. Should be set to "".</p><p>This parameter should only be set to a specific port on official request as the device has to be configured to use this special port!</p></td></tr><tr><td>i_blnSimulationMode [in]</td><td>boolean</td><td><p>Simulation mode for the library. Set to one of the following constants:</p><table><thead><tr><th>constant</th><th>value</th><th>description</th></tr></thead><tbody><tr><td>ASWGLOBAL::BOOL::FALSE</td><td>0</td><td>Device is not simulated.</td></tr><tr><td>ASWGLOBAL::BOOL::TRUE</td><td>1</td><td>Device is simulated.</td></tr></tbody></table></td></tr><tr><td>o_intDeviceID [out]</td><td>integer</td><td>Unique identifier for this device. Use this number as input for all subsequent function calls.</td></tr><tr><td>o_strMessage [out]</td><td>string</td><td>Informational message.</td></tr></tbody></table>
