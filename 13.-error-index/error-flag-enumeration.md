# Error Flag Enumeration

### Error Flag Enumeration

| **ID** | **Description**                                                                                                                                                                                                                                                        |
| -----: | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
|      0 | Step ends with OK, no error occurred and no error handling was used. The block data contains the step-dependent information.                                                                                                                                           |
|      1 | Step ends with OK, Abort or Cancel. An error handling was necessary. The block data contains the step-dependent information. _Note:_ The step data for this block are invalid if one of the following recoveries were used: Cancel, Abort, Continue, Exclude or Waste. |
|      2 | Step ends with a fatal error. _Caution:_ The block data part is invalid. Result values 4-n may have undefined data.                                                                                                                                                    |

&#x20;
