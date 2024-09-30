# 1337 : Type mismatch in formal parameter

The parser detected a mismatch between the types of an actual and the corresponding formal parameter of a function.

&#x20;

The following example illustrates this error:

```
function f(timer t) void
{
// ...
}
method M() void
{
variable v;
f(v); // error 1337: type mismatch in formal parameter 1 of function 'f'
} 
```

