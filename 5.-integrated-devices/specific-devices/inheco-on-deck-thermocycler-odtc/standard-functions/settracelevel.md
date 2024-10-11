# SetTraceLevel

## Description

This function is used to set the trace level for the library.

Initially, the module trace level is the same as the trace level that is set in the ASWStandard TraceLevel library. Set the trace level to a different level than the global level if you want to see more/less information from this library than of the rest. This is helpful for debug purposes.

### Syntax

```
SetTraceLevel (variable i_intTraceLevel)
```

### Arguments

<table><thead><tr><th width="209">argument</th><th width="159">value</th><th>description</th></tr></thead><tbody><tr><td>i_intTraceLevel [in]</td><td>integer [0..2]</td><td><p>Trace level for the library. Set to one of the following constants:<br><br></p><table><thead><tr><th>constant</th><th>value</th><th>description</th></tr></thead><tbody><tr><td>TRACE_LEVEL_RELEASE</td><td>1</td><td>Only show traces with release level.</td></tr><tr><td>TRACE_LEVEL_DEBUG</td><td>2</td><td>Show all traces.</td></tr></tbody></table></td></tr></tbody></table>
