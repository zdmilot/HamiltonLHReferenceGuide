# SiLA return codes

## Description

All functions use the following return codes:

| constant | description                                                              | Severity            | Solution                                                                                      |
| -------- | ------------------------------------------------------------------------ | ------------------- | --------------------------------------------------------------------------------------------- |
| 4        | Device is busy.                                                          | Uncorrectable Error | Wait retry                                                                                    |
| 5        | Error on LockID.                                                         | Uncorrectable Error | Check Lock and ID                                                                             |
| 6        | Error on RequestID.                                                      | Uncorrectable Error | Check RequestID or retry                                                                      |
| 9        | Command not allowed.                                                     | Uncorrectable Error | Command not allowed in tdis state wait until current process finished                         |
| 10       | Error in Data sent to Event Receiver.                                    | Uncorrectable Error | Retry                                                                                         |
| 11       | Invalid command parameter.                                               | Uncorrectable Error | Script error file corrupt?                                                                    |
| 12       | Finished with Warning.                                                   | Warning             | will be ignored by the device ignore returnvalue 12 Retry                                     |
| 1000     | Unhandled Exceptions / Hard Software Error(only MiniPC .Net Components). | Device Error        | ????                                                                                          |
| 1001     | Comm Error(e.g. Interrupted communication uC-MiniPC).                    | Device Error        | ????                                                                                          |
| 1002     | PMS Connector error.                                                     | Device Error        | ????                                                                                          |
| 1003     | Device Plugin error.                                                     | Device Error        | ????                                                                                          |
| 1004     | General warning.                                                         | Device Warning      | ????                                                                                          |
| 2000     | Hardware Error while operation.                                          | Device Error        | ???                                                                                           |
| 2001     | Connection failure P\&CU-ODTC.                                           | Device Error        | Terminate and reconnect                                                                       |
| 2002     | Door error.                                                              | Uncorrectable Error | Check door and retry                                                                          |
| 2003     | Method error (all runtime errors in an script being executed).           | Uncorrectable Error | Script error                                                                                  |
| 2004     | Unexpected bus communication return value.                               | Uncorrectable Error | Uncorrectable error                                                                           |
| 2005     | Temperature out of specification.                                        | Warning             | will be ignored by the device and replaced by error 12 ignore returnvalue 12 or 2005 or Retry |
| 2006     | General warning(e.g. environmental temperature to high).                 | Warning             | will be ignored by the device and replaced by error 12 ignore returnvalue 12 or 2006 or Retry |
| 2007     | AC power loss.                                                           | DeviceError         |                                                                                               |
