# CO-RE 384 Head Wash liquid class error

The liquid class for CO-RE 384 Head Washer is either missing or not unique.

&#x20;

Check that the liquid class is defined once only for the needed tip type. The liquid device must be set as '384 CORE head wash station'.

&#x20;

_Parameters to be defined for a CO-RE 384 Head Washer liquid class:_

&#x20;

| **Field**                | **Selection / Input**                                                                              |
| ------------------------ | -------------------------------------------------------------------------------------------------- |
| Liquid Device            | Must be set to '**384 CORE head wash station'** or **'96 CORE head wash station'** on rocket tips. |
| Liquid                   | Not used.                                                                                          |
| Tip Type                 | Tip type which must be washed                                                                      |
| Dispense mode            | Must be set to '**Dispense surface empty tip**'                                                    |
|                          |                                                                                                    |
| Flow rate                | Used for empty tip into wash station, aspirate blowout air and dispense blowout volume.            |
| Mix flow rate            | Used for wash cycles.                                                                              |
| Air transport volume     | Should be set to 0.                                                                                |
| Blowout volume           | Used for blowout the tip after wash.                                                               |
| Swap speed               | Speed for leaving liquid after wash.                                                               |
| Settling time            | Waiting time after aspirate / dispense.                                                            |
| Over aspirate volume     | Should be set to 0.                                                                                |
| Clot retract height      | Not used.                                                                                          |
| Stop flow rate           | Used on dispense.                                                                                  |
| Stop back volume         | Not used.                                                                                          |
| Pressure LLD sensitivity | Not used.                                                                                          |
| Max height difference    | Not used.                                                                                          |

&#x20;
