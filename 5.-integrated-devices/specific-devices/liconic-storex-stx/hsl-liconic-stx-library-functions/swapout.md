# SwapOut

## Syntax:

&#x20;

| SwapOut ( | variable iUnitID | ) |
| --------- | ---------------- | - |

&#x20;

***

## Description:

&#x20;

This function rotates the swap station of the Liconic STX device identified by _iUnitID_ to 0°.&#x20;

&#x20;

***

## Arguments:

&#x20;

| argument      | range           | description                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| ------------- | --------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| iUnitID \[in] | integer \[1..4] | <p>UnitID of the device, set to one of the following constants:</p><p> </p><table data-header-hidden><thead><tr><th></th><th></th></tr></thead><tbody><tr><td>constant</td><td>description</td></tr><tr><td>HSLLiconicSTX::UNIT_1</td><td>initialize unit 1</td></tr><tr><td>HSLLiconicSTX::UNIT_2</td><td>initialize unit 2</td></tr><tr><td>HSLLiconicSTX::UNIT_3</td><td>initialize unit 3</td></tr><tr><td>HSLLiconicSTX::UNIT_4</td><td>initialize unit 4</td></tr></tbody></table> |

&#x20;
