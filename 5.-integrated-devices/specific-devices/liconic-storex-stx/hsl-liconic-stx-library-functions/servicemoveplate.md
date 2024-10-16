# ServiceMovePlate

## Syntax:

&#x20;

| ServiceMovePlate ( | variable iUnitID,       |   |
| ------------------ | ----------------------- | - |
|                    | variable iSrcPos,       |   |
|                    | variable iSrcSlot,      |   |
|                    | variable iSrcLevel,     |   |
|                    | variable iTransSrcSlot, |   |
|                    | variable iSrcPlateType, |   |
|                    | variable iTrgUnitID,    |   |
|                    | variable iTrgPos,       |   |
|                    | variable iTrgSlot,      |   |
|                    | variable iTrgLevel,     |   |
|                    | variable iTransTrgSlot, |   |
|                    | variable iTrgPlateType  | ) |

&#x20;

***

## Description:

&#x20;

This function issues a low level plate move for the Liconix STX device identified by _iUnitID_.

&#x20;

Hint:

This operation allows moving a plate within the bounds of one device or between the cascader system.

&#x20;

***

## Arguments:

&#x20;

| argument           | range           | description                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| ------------------ | --------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| iUnitID \[in]      | integer \[1..4] | <p>UnitID of the source device, set to one of the following constants:</p><p> </p><table data-header-hidden><thead><tr><th></th><th></th></tr></thead><tbody><tr><td>constant</td><td>description</td></tr><tr><td>HSLLiconicSTX::UNIT_1</td><td>unit 1</td></tr><tr><td>HSLLiconicSTX::UNIT_2</td><td>unit 2</td></tr><tr><td>HSLLiconicSTX::UNIT_3</td><td>unit 3</td></tr><tr><td>HSLLiconicSTX::UNIT_4</td><td>unit 4</td></tr></tbody></table> |
| iSrcPos \[in]      | integer         | <p>source position, set to one of the following values:</p><p> </p><table data-header-hidden><thead><tr><th></th><th></th></tr></thead><tbody><tr><td>position</td><td>description</td></tr><tr><td>1</td><td>transfer station</td></tr><tr><td>2</td><td>slot/level position</td></tr><tr><td>3</td><td>shovel</td></tr><tr><td>4</td><td>tunnel</td></tr></tbody></table>                                                                         |
| iSrcSlot \[in]     | integer         | source slot                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| iSrcLevel \[in]    | integer         | source level                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| iTransSrcSlot\[in] | integer         | number of a transport slot of the source device. It is obligatory for moving a plate between devices Base, Extend in Cascader. This parameter is even for Extended device and odd for Base device.                                                                                                                                                                                                                                                  |
| iSrcPlateType\[in] | integer         | <p>source plate type, set to one of the following values:</p><p> </p><table data-header-hidden><thead><tr><th></th><th></th></tr></thead><tbody><tr><td>type</td><td>description</td></tr><tr><td>0</td><td>MTP</td></tr><tr><td>1</td><td>DWP</td></tr><tr><td>3</td><td>P28</td></tr></tbody></table>                                                                                                                                             |
| iTrgUnitID \[in]   | integer         | <p>UnitID of the target device, set to one of the following constants:</p><p> </p><table data-header-hidden><thead><tr><th></th><th></th></tr></thead><tbody><tr><td>constant</td><td>description</td></tr><tr><td>HSLLiconicSTX::UNIT_1</td><td>unit 1</td></tr><tr><td>HSLLiconicSTX::UNIT_2</td><td>unit 2</td></tr><tr><td>HSLLiconicSTX::UNIT_3</td><td>unit 3</td></tr><tr><td>HSLLiconicSTX::UNIT_4</td><td>unit 4</td></tr></tbody></table> |
| iTrgPos \[in]      | integer         | <p>target position, set to one of the following values:</p><p> </p><table data-header-hidden><thead><tr><th></th><th></th></tr></thead><tbody><tr><td>position</td><td>description</td></tr><tr><td>1</td><td>transfer station</td></tr><tr><td>2</td><td>slot/level position</td></tr><tr><td>3</td><td>shovel</td></tr><tr><td>4</td><td>tunnel</td></tr></tbody></table>                                                                         |
| iTrgSlot \[in]     | integer         | target slot                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| iTrgLevel \[in]    | integer         | target level                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| iTransTrgSlot      | integer         | number of a transport slot of the target device. It is obligatory for moving a plate between devices Base, Extend in Cascader. This parameter is even for Extended device and odd for Base device.                                                                                                                                                                                                                                                  |
| iTrgPlateType\[in] | integer         | <p>target plate type, set to one of the following values:</p><p> </p><table data-header-hidden><thead><tr><th></th><th></th></tr></thead><tbody><tr><td>type</td><td>description</td></tr><tr><td>0</td><td>MTP</td></tr><tr><td>1</td><td>DWP</td></tr><tr><td>3</td><td>P28</td></tr></tbody></table>                                                                                                                                             |

&#x20;
