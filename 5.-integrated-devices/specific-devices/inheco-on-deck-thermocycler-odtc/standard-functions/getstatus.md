# GetStatus

## Description

This function is used to retrieve the status of the device.

### Syntax

```
GetStatus (variable i_intDeviceID, 
           variable& o_strDeviceId,
           variable& o_strState,
           variable& o_blnLocked,
           variable& o_strPMSId,
           variable& o_strCurrentTime,
           variable& o_intSiLAReturnValue, 
           variable& o_strSiLAMessage)
```

### Arguments

<table><thead><tr><th width="252">argument</th><th width="117">value</th><th>description</th></tr></thead><tbody><tr><td>i_intDeviceID [in]</td><td>int [1..4]</td><td>Unique identifier for the device as returned by function Connect.</td></tr><tr><td>o_strDeviceId [out]</td><td>string</td><td>Internal information of the device.</td></tr><tr><td>o_strState [out]</td><td>string</td><td><p>State as reported by the device.</p><p>One of the following values:<br><br></p><p>'startup', 'resetting', 'standby', 'idle', 'busy', 'paused', 'errorhandling', 'inerror', 'asynchpaused', 'pauserequested', 'processing', 'responsewaiting'</p></td></tr><tr><td>o_blnLocked [out]</td><td>boolean</td><td>Lock state of the device.</td></tr><tr><td>o_strPMSId [out]</td><td>string</td><td>Name of the PMS connected to teh device.</td></tr><tr><td>o_strCurrentTime [out]</td><td>string</td><td>Time as reported by the device.</td></tr><tr><td>o_intSiLAReturnValue [out]</td><td>int</td><td>The SiLA return code of the device.</td></tr><tr><td>o_strSiLAMessage [out]</td><td>string</td><td>The SiLA message returned by the device.</td></tr></tbody></table>
