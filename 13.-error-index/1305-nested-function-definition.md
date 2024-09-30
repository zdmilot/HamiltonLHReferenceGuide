# 1305 : Nested function definition

Function definitions cannot be nested.

&#x20;

The following example illustrates this error:

```
function f0()
{
Trace("+f0");
function f1() // error 1305: can't have nested function definitions
{
return;
}
return;
Trace("-f0");
} 
```

