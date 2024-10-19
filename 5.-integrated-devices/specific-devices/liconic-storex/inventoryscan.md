# InventoryScan

## Description

This function is used to retrieve information about the currently available plates inside the Liconic StoreX device.

Depending on the mode set by parameter _i\_intMode_ and the size of the device, this function may take some time.

### Syntax

InventoryScan (variable i\_intModuleIDStore, variable i\_intModuleIDScanner, variable i\_intStackerStart, variable i\_intStackerStop, variable i\_intMode, variable& o\_intNumberOfStackers, variable& o\_arrIntNumberOfLevels\[], variable& o\_arrIntStackerNumbers\[], variable& o\_arrStrBarcodes\[], variable& o\_arrIntAllocations\[])

### Arguments

| argument                       | value                      | description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| ------------------------------ | -------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| i\_intModuleIDStore \[in]      | integer \[0..3]            | Unique identifier for the Liconic StoreX device as returned by function [Initialize](chm://c6eee35ebc6f05b6562520699a23e565/topics/Initialize.html).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| i\_intModuleIDScanner \[in]    | integer \[0..160]          | Unique identifier for the barcode scanner device as returned by function [Initialize](chm://c6eee35ebc6f05b6562520699a23e565/topics/Initialize.html).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| i\_intStackerStart \[in]       | integer \[0..100]          | <p>Number of the stacker to start inventory scan.</p><p>Set to 0 for a full inventory scan.</p>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| i\_intStackerStop \[in]        | integer \[0..100]          | <p>Number of the stacker to stop inventory scan.</p><p>Set to 0 for a full inventory scan.</p>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| i\_intMode \[in]               | integer \[0..2]            | <p>Mode for the inventory scan. Set to one of the following predefined constants:<br><br></p><table><thead><tr><th>constant</th><th>value</th><th>description</th></tr></thead><tbody><tr><td>Liconic_Store_X::InventoryScanMode::BARCODE_ONLY</td><td>1</td><td>Use the integrated barcode scanner to detect plates (fastest).</td></tr><tr><td>Liconic_Store_X::InventoryScanMode::SENSOR_ONLY</td><td>2</td><td>Use the integrated shovel sensor to detect plates.</td></tr><tr><td>Liconic_Store_X::InventoryScanMode::COMBINED</td><td>3</td><td>Use the integrated shovel sensor and the barcode scanner to detect plates (slowest).</td></tr></tbody></table><p>If parameter <em>Liconic_Store_X::Option::ExtendedBarcodeReading</em> is enabled using function <a href="chm://c6eee35ebc6f05b6562520699a23e565/topics/OptionSet.html">OptionSet</a>, and <em>i_intMode</em> is not set to <em>Liconic_Store_X::InventoryScanMode::SENSOR_ONLY</em>, the barcode reading will take some time.</p> |
| o\_intNumberOfStackers \[out]  | integer                    | Number of stackers the inventory has been executed for.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| o\_arrIntNumberOfLevels \[out] | array of integer           | <p>Array containing the number of levels in each of the stackers.</p><p>Size of array is o_intNumberOfStackers.</p>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| o\_arrIntStackerNumbers \[out] | array of integer           | <p>Array containing the stacker number of each entry.</p><p>Size of array reflects number of positions scanned.</p>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| o\_arrStrBarcodes \[out]       | array of strings           | <p>Array containing all plate barcodes (checked by barcode scanner).</p><p>Size of array reflects number of positions scanned.A value of 'empty' is returned in case no barcode could have been read.</p>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| o\_arrIntAllocations \[out]    | array of integer \[−1,0,1] | <p>Array containing all plate allocations (checked by shovel sensor).</p><p>Size of array reflects number of positions scanned.A value of -1 is returned in case the shovel sensor has been disabled.</p>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |

\