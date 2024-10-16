# Terminate

## Description

This function is used to terminate a device.

### Syntax

```
Terminate (variable i_intDeviceID, 
           variable & o_strSiLAMessage)
```

### Arguments

| argument                 | value       | description                                                       |
| ------------------------ | ----------- | ----------------------------------------------------------------- |
| i\_intDeviceID \[in]     | int \[1..4] | Unique identifier for the device as returned by function Connect. |
| o\_strSiLAMessage \[out] | string      | The SiLA message returned by the device.                          |
