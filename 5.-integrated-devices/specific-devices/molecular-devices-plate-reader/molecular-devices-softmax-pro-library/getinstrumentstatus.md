# GetInstrumentStatus

## Description

This function returns the state of the currently connected instrument.

### Syntax

```
GetInstrumentStatus(o_strInstrumentStatus)
```

### Arguments

\[out] o\_strInstrumentStatusThe status as a string. See variables in the namespace 'Molecular\_Devices\_SoftMax\_Pro::Status':\


* 'Idle'
* 'Busy'
* 'Error'
* 'Timeout'
* 'Offline'
* 'Stopping'
* 'Initializing'
* 'Unknown'
