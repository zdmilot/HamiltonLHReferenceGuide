# WriteSetClimate

## Syntax:

&#x20;

| WriteSetClimate ( | variable iUnitID,      |   |
| ----------------- | ---------------------- | - |
|                   | variable iTemperature, |   |
|                   | variable iHumidity,    |   |
|                   | variable iConcCO2,     |   |
|                   | variable iConcN2       | ) |

&#x20;

***

## Description:

This function sets new climate values for the Liconix STX device identified by _iUnitID_.

Hint: The values are not checked due to different restrictions for different models of the STX devices.

&#x20;

***

## Arguments:

| argument           | range           | description                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| ------------------ | --------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| iUnitID \[in]      | integer \[1..4] | <p>UnitID of the device, set to one of the following constants:</p><p> </p><table data-header-hidden><thead><tr><th></th><th></th></tr></thead><tbody><tr><td>constant</td><td>description</td></tr><tr><td>HSLLiconicSTX::UNIT_1</td><td>unit 1</td></tr><tr><td>HSLLiconicSTX::UNIT_2</td><td>unit 2</td></tr><tr><td>HSLLiconicSTX::UNIT_3</td><td>unit 3</td></tr><tr><td>HSLLiconicSTX::UNIT_4</td><td>unit 4</td></tr></tbody></table> |
| iTemperature \[in] | float           | desired temperature                                                                                                                                                                                                                                                                                                                                                                                                                          |
| iHumidity \[in]    | float           | desired humidity                                                                                                                                                                                                                                                                                                                                                                                                                             |
| iConcCO2 \[in]     | float           | desired CO2 concentration                                                                                                                                                                                                                                                                                                                                                                                                                    |
| iConcN2 \[in]      | float           | desired N2 concentration                                                                                                                                                                                                                                                                                                                                                                                                                     |

&#x20;
