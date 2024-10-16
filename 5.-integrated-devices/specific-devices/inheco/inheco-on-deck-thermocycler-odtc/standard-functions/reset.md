# Reset

## Description

This function is used to reset the Inheco ODTC device.

Use this function prior to any other functions!

### Syntax

```
Reset (variable i_intDeviceID, 
       variable i_blnSimulateOnDeviceBase, 
       variable i_intTimeToWait, 
       variable i_strLockID, 
       variable i_strDeviceId, 
       variable i_strPMSID, 
       variable & o_intSiLAReturnValue, 
       variable & o_strSiLAMessage)
```

### Arguments

<table><thead><tr><th width="187">argument</th><th width="98">value</th><th>description</th></tr></thead><tbody><tr><td>i_intDeviceID [in]</td><td>int [1..4]</td><td>Unique identifier for the device as returned by function Connect.</td></tr><tr><td>i_blnSimulateOnDeviceBase [in]</td><td>boolean</td><td><p>Simulation mode for the device. Set to one of the following constants:</p><table><thead><tr><th>constant</th><th>value</th><th>description</th></tr></thead><tbody><tr><td>ASWGLOBAL::BOOL::FALSE</td><td>0</td><td>Device is not simulated.</td></tr><tr><td>ASWGLOBAL::BOOL::TRUE</td><td>1</td><td>Device is simulated.</td></tr></tbody></table><p>This parameter enables the device simulation mode - all commands will be sent to the device and the device itself sends simulated answers.</p><p>This parameter is helpful to test the communication to the device without operating it.</p></td></tr><tr><td>i_intTimeToWait [in]</td><td>int</td><td><p>Timeout in seconds for this command.</p><p>Standard SiLA timeout value is 120 seconds.</p></td></tr><tr><td>i_strLockID [in]</td><td>string</td><td><p>LockID for the device. This identifier has to be used to lock and unlock the device.</p><p>Use functions LockDevice and UnlockDevice to lock/unlock the device.</p></td></tr><tr><td>i_strPMSID [in]</td><td>string</td><td>Identifier for the connected PMS.</td></tr><tr><td>i_strDeviceId [in]</td><td>string</td><td>Identifier for the device.</td></tr><tr><td>o_intSiLAReturnValue [out]</td><td>int</td><td>The SiLA return code of the device.</td></tr><tr><td>o_strSiLAMessage [out]</td><td>string</td><td>The SiLA message returned by the device.</td></tr></tbody></table>
