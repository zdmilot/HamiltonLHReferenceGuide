# ImportPlate

## Syntax:

&#x20;

| ImportPlate ( | variable iUnitID, |   |
| ------------- | ----------------- | - |
|               | variable iSlot,   |   |
|               | variable iLevel   | ) |

&#x20;

***

## Description:

&#x20;

This function imports a plate to _iSlot / iLevel_ of the Liconix STX device identified by _iUnitID_.

&#x20;

Hint:

The values _iSlot_ and _iLevel_ are not checked due to different restrictions for different models of the STX devices.

&#x20;

***

## Arguments:

&#x20;

| argument      | range           | description                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| ------------- | --------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| iUnitID \[in] | integer \[1..4] | <p>UnitID of the device, set to one of the following constants:</p><p> </p><table data-header-hidden><thead><tr><th></th><th></th></tr></thead><tbody><tr><td>constant</td><td>description</td></tr><tr><td>HSLLiconicSTX::UNIT_1</td><td>unit 1</td></tr><tr><td>HSLLiconicSTX::UNIT_2</td><td>unit 2</td></tr><tr><td>HSLLiconicSTX::UNIT_3</td><td>unit 3</td></tr><tr><td>HSLLiconicSTX::UNIT_4</td><td>unit 4</td></tr></tbody></table> |
| iSlot \[in]   | integer         | slot where to store the plate                                                                                                                                                                                                                                                                                                                                                                                                                |
| iLevel \[in]  | integer         | level in _iSlot_ where to store the plate                                                                                                                                                                                                                                                                                                                                                                                                    |

&#x20;