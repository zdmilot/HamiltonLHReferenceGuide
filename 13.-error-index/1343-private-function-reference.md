# 1343 : Private function reference

&#x20;The specified private function cannot be referenced outside of its definition file.

&#x20;

The following example illustrates this error:

```
File A.hsl:
 
private function f() void
{
 
}
 
File B.hsl:
 
#include "A.hsl"
function g() void
{
f(); // error 1343: private function 'f' cannot be referenced outside of its definition file
} 
```

