# ReadXferStationDetector2

## Syntax:

&#x20;

| ReadXferStationDetector2 ( | variable iUnitID,            |   |
| -------------------------- | ---------------------------- | - |
|                            | variable& oXferStationStatus | ) |

&#x20;

***

## Description:

&#x20;

This function returns the transfer station 2 status of the Liconix STX device identified by _iUnitID_.

&#x20;

***

## Arguments:

&#x20;

| argument                  | range           | description                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| ------------------------- | --------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| iUnitID \[in]             | integer \[1..4] | <p>UnitID of the device, set to one of the following constants:</p><p> </p><table data-header-hidden><thead><tr><th></th><th></th></tr></thead><tbody><tr><td>constant</td><td>description</td></tr><tr><td>HSLLiconicSTX::UNIT_1</td><td>unit 1</td></tr><tr><td>HSLLiconicSTX::UNIT_2</td><td>unit 2</td></tr><tr><td>HSLLiconicSTX::UNIT_3</td><td>unit 3</td></tr><tr><td>HSLLiconicSTX::UNIT_4</td><td>unit 4</td></tr></tbody></table> |
| oXferStationStatus \[out] | integer \[0..1] | <p>0: no plate present on transfer station</p><p>1: plate present on transfer station</p>                                                                                                                                                                                                                                                                                                                                                    |

&#x20;
