# ReadInventoryFile

## Syntax:

&#x20;

| ReadInventoryFile ( | variable iUnitID,         |   |
| ------------------- | ------------------------- | - |
|                     | variable iInvFilename,    |   |
|                     | variable& oBarcode\[],    |   |
|                     | variable& oCustomerID\[], |   |
|                     | variable& oPartition\[],  |   |
|                     | variable& oPPD\[],        |   |
|                     | variable& oSerialNo\[],   |   |
|                     | variable& oSystemID\[],   |   |
|                     | variable& oDeviceID\[],   |   |
|                     | variable& oCassetteNo\[], |   |
|                     | variable& oLevel\[],      |   |
|                     | oRow& oRow\[]             | ) |

&#x20;

***

Description:

&#x20;

This function reads an inventory file created by a Liconic STX device. Parameter _iUnitID_ is only used to refer to the error message array.&#x20;

&#x20;

Hint: This function may be used even before calling function [Initialize()](chm://cd05d247795d14fdbd040c33a4f737ff/Initialize.htm)

&#x20;

***

Arguments:

&#x20;

| argument           | range           | description                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| ------------------ | --------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| iUnitID \[in]      | integer \[1..4] | <p>UnitID of the device, set to one of the following constants:</p><p> </p><table data-header-hidden><thead><tr><th></th><th></th></tr></thead><tbody><tr><td>constant</td><td>description</td></tr><tr><td>HSLLiconicSTX::UNIT_1</td><td>unit 1</td></tr><tr><td>HSLLiconicSTX::UNIT_2</td><td>unit 2</td></tr><tr><td>HSLLiconicSTX::UNIT_3</td><td>unit 3</td></tr><tr><td>HSLLiconicSTX::UNIT_4</td><td>unit 4</td></tr></tbody></table> |
| iInvFilename \[in] | string          | <p>Filename of Inventory file. Set to the name used by function <a href="chm://cd05d247795d14fdbd040c33a4f737ff/Inventory.htm">Inventory()</a> and <a href="chm://cd05d247795d14fdbd040c33a4f737ff/PartialInventoryScan.htm">PartialInventoryScan()</a>.</p><p> </p><p>Hint:</p><p>Always supply a full path with the filename.</p>                                                                                                          |
| oBarcode \[out]    | array of string | value of a barcode (\<null> - no barcode or barcode reader is switched off)                                                                                                                                                                                                                                                                                                                                                                  |
| oCustomerID \[out] | array of string | IdCustomer value                                                                                                                                                                                                                                                                                                                                                                                                                             |
| oPartition \[out]  | array of string | name of the partition                                                                                                                                                                                                                                                                                                                                                                                                                        |
| oPPD \[out]        | array of string | value of the plate present detector (1 - plate is present, 0 - plate is not present or plate present detector is switched off)                                                                                                                                                                                                                                                                                                               |
| oSerialNo \[out]   | array of string | serial number of the plate                                                                                                                                                                                                                                                                                                                                                                                                                   |
| oSystemID \[out]   | array of string | identifier of the system which is assigned in the configuration file "System.lni" ( section - "System", Key - "SystemId")                                                                                                                                                                                                                                                                                                                    |
| oDeviceID \[out]   | array of string | identifier of the device                                                                                                                                                                                                                                                                                                                                                                                                                     |
| oCassetteNo \[out] | array of string | number of the cassette                                                                                                                                                                                                                                                                                                                                                                                                                       |
| oLevel \[out]      | array of string | value of the level within a cassette                                                                                                                                                                                                                                                                                                                                                                                                         |
| oRow \[out]        | array of string | number of a row (reserved for the future)                                                                                                                                                                                                                                                                                                                                                                                                    |

&#x20;
