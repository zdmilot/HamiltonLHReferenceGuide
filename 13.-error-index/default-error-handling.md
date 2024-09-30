# Default Error Handling

### Dialog: Default Error Handling

&#x20;

**Flag error (Sample Tracker Database)**

If checked, an error recovery will be tracked on sample tracker database. The **Action State Tracked** depends on the executed recovery.\
If not activated, the action state is always set to 'No Error'.

&#x20;

### Error Recovery vs. Action State Tracked

| **Executed Recovery**     | **Action State Tracked** |
| ------------------------- | ------------------------ |
| Abort                     | Fatal                    |
| Exclude                   | Error                    |
| Continue                  | Error                    |
| Bottom                    | Error                    |
| Air                       | Error                    |
| Available                 | Error                    |
| Waste (on Aspirate Error) | Error                    |
| Cancel                    | Warning                  |
| Barcode                   | Warning                  |
| Initialize                | No Error                 |
| Waste                     | No Error                 |
| Repeat                    | No Error                 |
| Next                      | No Error                 |
| Refill                    | No Error                 |

&#x20;
