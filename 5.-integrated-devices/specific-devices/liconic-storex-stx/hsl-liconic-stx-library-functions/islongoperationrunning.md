# IsLongOperationRunning

## Syntax:

&#x20;

| IsLongOperationRunning ( | variable iUnitID, |   |
| ------------------------ | ----------------- | - |
|                          | variable& oStatus | ) |

&#x20;

***

## Description:

&#x20;

This function should be used to check the status of long time operations of the Liconix STX device identified by _iUnitID_.

&#x20;

Hint: The functions [Inventory()](chm://cd05d247795d14fdbd040c33a4f737ff/Inventory.htm) and [PartialInventoryScan()](chm://cd05d247795d14fdbd040c33a4f737ff/PartialInventoryScan.htm) return immediately after call but take some time where the device is inaccessible for other operations. Use this function to check the status of these functions before performing other commands.

&#x20;

***

## Arguments:

&#x20;

| argument       | range            | description                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| -------------- | ---------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| iUnitID \[in]  | integer \[1..4]  | <p>UnitID of the device, set to one of the following constants:</p><p> </p><table data-header-hidden><thead><tr><th></th><th></th></tr></thead><tbody><tr><td>constant</td><td>description</td></tr><tr><td>HSLLiconicSTX::UNIT_1</td><td>unit 1</td></tr><tr><td>HSLLiconicSTX::UNIT_2</td><td>unit 2</td></tr><tr><td>HSLLiconicSTX::UNIT_3</td><td>unit 3</td></tr><tr><td>HSLLiconicSTX::UNIT_4</td><td>unit 4</td></tr></tbody></table> |
| oStatus \[out] | integer \[-1..1] | <p>one of the following states:</p><p> </p><table data-header-hidden><thead><tr><th></th><th></th></tr></thead><tbody><tr><td>value</td><td>description</td></tr><tr><td>-1</td><td>operation finished unsuccessful</td></tr><tr><td>0</td><td>operation finished successful</td></tr><tr><td>1</td><td>operation running</td></tr></tbody></table>                                                                                          |

&#x20;
