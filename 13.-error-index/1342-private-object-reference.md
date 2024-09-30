# 1342 : Private object reference

&#x20;The specified private object cannot be referenced outside of its definition file.

&#x20;

The following example illustrates this error:

```
File A.hsl:
 
private variable v;
 
File B.hsl:
 
#include "A.hsl"
function f() void
{
v; // error 1342: private object 'v' cannot be referenced outside of its definition file
} 
```

