# SetTraceLevel

## Description

This function is used to set the trace level for the library.

Initially, the module trace level is the same as the trace level that is set in the ASWStandard TraceLevel library. Set the trace level to a different level than the global level if you want to see more/less information from this library than of the rest. This is helpful for debug purposes.

### Syntax

```
SetTraceLevel(i_intTraceLevel)
```

### Arguments

\[in] i\_intTraceLevelTrace level for the library. Set to one of the following constants:\


* 1 (TRACE\_LEVEL\_RELEASE), Only show traces with release level.
* 2 (TRACE\_LEVEL\_DEBUG), Show all traces.
