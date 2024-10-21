# Recovery Button Enumeration and Recovery State Tracking

| Recovery Button ID | Recovery Button Text | Description                                                            |
| ------------------ | -------------------- | ---------------------------------------------------------------------- |
| 1                  | Abort                | Run is aborted.                                                        |
| 2                  | Cancel               | Run is canceled and a defined user error handler is started            |
| 3                  | Initialize           | Instrument is reinitialized                                            |
| 4                  | Repeat               | The command is repeated                                                |
| 5                  | Exclude              | The channel or position is excluded until a new tip pick up is called. |
| 6                  | Waste                | The tip is ejected to the default waste                                |
| 7                  | Air                  | Rest of missing volume is filled up with air                           |
| 8                  | Bottom               | Repeats the aspiration on container bottom                             |
| 9                  | Continue             | Continue without any change                                            |
| 10                 | Barcode              | Barcose is assigned manually                                           |
| 11                 | Next                 | Repeat the command on next sequence position                           |
| 12                 | Available            | Aspirate & dispense the available volume.                              |

\


\


| Executed Recovery         | Action State Tracked |
| ------------------------- | -------------------- |
| Abort                     | Fatal                |
| Exclude                   | Error                |
| Continue                  | Error                |
| Bottom                    | Error                |
| Air                       | Error                |
| Available                 | Error                |
| Waste (on Aspirate Error) | Error                |
| Cancel                    | Warning              |
| Barcode                   | Warning              |
| Initialize                | No Error             |
| Waste                     | No Error             |
| Repeat                    | No Error             |
| Next                      | No Error             |
| Refill                    | No Error             |
