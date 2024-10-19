# Initialize

## Description

This function is used to initialize a Liconic StoreX device.

### Syntax

Initialize (variable i\_intPortStore, variable i\_intPortScanner, variable i\_blnSimulationMode, variable& o\_intModuleIDStore, variable& o\_intModuleIDScanner)

### Arguments

| argument                     | value             | description                                                                                                                                                                                                                                                                                                                                                                 |
| ---------------------------- | ----------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| i\_intPortStore \[in]        | integer \[1..256] | Number of the serial port the device is connected to.                                                                                                                                                                                                                                                                                                                       |
| i\_intPortScanner \[in]      | integer \[0..256] | <p>Number of the serial port the barcode reader of the device is connected to.</p><p>Set this value to 0 in case the device has no barcode reader.</p>                                                                                                                                                                                                                      |
| i\_blnSimulationMode \[in]   | boolean           | <p>Simulation mode for the library. Set to one of the following predefined constants:<br><br></p><table><thead><tr><th>constant</th><th>value</th><th>description</th></tr></thead><tbody><tr><td>ASWGLOBAL::BOOL::FALSE</td><td>0</td><td>Device is not simulated.</td></tr><tr><td>ASWGLOBAL::BOOL::TRUE</td><td>1</td><td>Device is simulated.</td></tr></tbody></table> |
| o\_intModuleIDStore \[out]   | integer \[0..3]   | <p>Unique identifier for the StoreX device.</p><p>Use this number as input for all subsequent function calls.</p>                                                                                                                                                                                                                                                           |
| o\_intModuleIDScanner \[out] | integer \[0..160] | <p>Unique identifier for the scanner device.</p><p>Use this number as input for all subsequent function calls requiring the scanner ID.</p>                                                                                                                                                                                                                                 |

### Return Value
