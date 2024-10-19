# SetTraceLevel

## Description

This function is used to set the trace level for the library.

Initially, the module trace level is the same as the trace level that is set in the ASWStandard TraceLevel library. Set the trace level to a different level than the global level if you want to see more/less information from this library than of the rest. This is helpful for debug purposes.

It is possible to set the trace level for either the StoreX device or the barcode scanner by setting the appropriate ModuleID. Please take into account that the library trace level will be set to the new value with every function call!

### Syntax

SetTraceLevel (variable i\_intModuleIDStore, variable i\_intTraceLevel)

### Arguments

| argument                  | value           | description                                                                                                                                                                                                                                                                                                                                                                             |
| ------------------------- | --------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| i\_intModuleIDStore \[in] | integer \[0..3] | Unique identifier for the device as returned by function [Initialize](chm://c6eee35ebc6f05b6562520699a23e565/topics/Initialize.html).                                                                                                                                                                                                                                                   |
| i\_intTraceLevel \[in]    | integer \[1..2] | <p>Trace level for the device and the library. Set to one of the following predefined constants:<br><br></p><table><thead><tr><th>constant</th><th>value</th><th>description</th></tr></thead><tbody><tr><td>TRACE_LEVEL_RELEASE</td><td>1</td><td>Only show traces with release level.</td></tr><tr><td>TRACE_LEVEL_DEBUG</td><td>2</td><td>Show all traces.</td></tr></tbody></table> |
