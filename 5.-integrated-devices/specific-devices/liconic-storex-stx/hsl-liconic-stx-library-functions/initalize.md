# Initalize

## Syntax:

| Initialize ( | variable iUnitID,        |   |
| ------------ | ------------------------ | - |
|              | variable iHostname,      |   |
|              | variable iPortNr,        |   |
|              | variable iTraceLevel,    |   |
|              | variable iSimulationMode | ) |

***

## Description:

This function initializes the Liconic STX device identified by iUnitID.&#x20;

Hint: This function has to be called before calling any other library function.

***

## Arguments:

| argument              | range               | description                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| --------------------- | ------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| iUnitID \[in]         | integer \[1..4]     | <p>UnitID of the device, set to one of the following constants:</p><p> </p><table data-header-hidden><thead><tr><th></th><th></th></tr></thead><tbody><tr><td>constant</td><td>description</td></tr><tr><td>HSLLiconicSTX::UNIT_1</td><td>initialize unit 1</td></tr><tr><td>HSLLiconicSTX::UNIT_2</td><td>initialize unit 2</td></tr><tr><td>HSLLiconicSTX::UNIT_3</td><td>initialize unit 3</td></tr><tr><td>HSLLiconicSTX::UNIT_4</td><td>initialize unit 4</td></tr></tbody></table> |
| iHostname \[in]       | string              | Host name of the computer the device is connected to, use “localhost”, if the device is connected to the computer where the method is executed.                                                                                                                                                                                                                                                                                                                                          |
| iPortNr \[in]         | integer \[1..65535] | <p>Port number to use to communicate with the device</p><p>Hint:</p><p>See file <em>DriverConfig.lni</em> (located in subdirectory <em>HSL Liconic STX</em> of Hamilton Bin directory), section [TCP], value port.</p>                                                                                                                                                                                                                                                                   |
| iTraceLevel \[in]     | integer \[0..2]     | <p>set to one of the following constants:</p><p> </p><table data-header-hidden><thead><tr><th></th><th></th></tr></thead><tbody><tr><td>constant</td><td>description</td></tr><tr><td>HSLLiconicSTX::TRACE_LEVEL_NONE</td><td>show no traces</td></tr><tr><td>HSLLiconicSTX::TRACE_LEVEL_NORMAL</td><td>show only necessary traces only</td></tr><tr><td>HSLLiconicSTX::TRACE_LEVEL_ TRACE_LEVEL_FULL</td><td>show all traces</td></tr></tbody></table>                                  |
| iSimulationMode \[in] | boolean             | <p>set to one of the following constants:</p><p> </p><table data-header-hidden><thead><tr><th></th><th></th></tr></thead><tbody><tr><td>constant</td><td>description</td></tr><tr><td>HSLLiconicSTX::TRUE</td><td>unit <em>iUnitID</em> is used in simulation mode</td></tr><tr><td>HSLLiconicSTX::FALSE</td><td>unit <em>iUnitID</em> is used in standard mode</td></tr></tbody></table>                                                                                                |

&#x20;
