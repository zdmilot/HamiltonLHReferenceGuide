# PartialInventoryScan

## Syntax:

&#x20;

| PartialInventoryScan ( | variable iUnitID,      |   |
| ---------------------- | ---------------------- | - |
|                        | variable iInvFilename, |   |
|                        | variable iPartitionID, |   |
|                        | variable iPPD,         |   |
|                        | variable iBCR          | ) |

&#x20;

***

## Description:

This function starts a partial inventory scan in _iRatitionID_ on the Liconix STX device identified by _iUnitID_.

&#x20;

***

## Arguments:

&#x20;

| argument           | range           | description                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| ------------------ | --------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| iUnitID \[in]      | integer \[1..4] | <p>UnitID of the device, set to one of the following constants:</p><p> </p><table data-header-hidden><thead><tr><th></th><th></th></tr></thead><tbody><tr><td>constant</td><td>description</td></tr><tr><td>HSLLiconicSTX::UNIT_1</td><td>unit 1</td></tr><tr><td>HSLLiconicSTX::UNIT_2</td><td>unit 2</td></tr><tr><td>HSLLiconicSTX::UNIT_3</td><td>unit 3</td></tr><tr><td>HSLLiconicSTX::UNIT_4</td><td>unit 4</td></tr></tbody></table> |
| iInvFilename\[in]  | string          | <p>Filename for the inventory file. Use function <a href="chm://cd05d247795d14fdbd040c33a4f737ff/ReadInventoryFile.htm">ReadInventoryFile()</a> to read out the values of the file.</p><p> </p><p>Hint:</p><p>Always supply a full path with the filename.</p>                                                                                                                                                                               |
| iPartitionID \[in] | string          | partition ID as defined in the units Lni file.                                                                                                                                                                                                                                                                                                                                                                                               |
| iPPD \[in]         | boolean         | use plate present detector.                                                                                                                                                                                                                                                                                                                                                                                                                  |
| iBCR \[in]         | boolean         | use barcode reader.                                                                                                                                                                                                                                                                                                                                                                                                                          |

&#x20;
