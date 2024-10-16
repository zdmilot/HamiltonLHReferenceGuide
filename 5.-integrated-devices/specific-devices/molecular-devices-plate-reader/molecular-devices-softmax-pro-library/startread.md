# StartRead

## Description

This function is used to read the current Plate or CuvetteSet section. If the current section is neither a Plate nor CuvetteSet section, the next Plate or CuvetteSet section is read.

The function just starts the method and returns - this behavior offers the possibility to do other things in parallel while the instrument is busy.

Warning It is mandatory to use function [WaitForReadFinished](chm://03ca6a293f9ae28bd0f386a42dcd2a1a/topics/WaitForReadFinished.html) before another function can be used!

### Syntax

```
StartRead()
```

### Arguments

This function has no arguments.

\
\
