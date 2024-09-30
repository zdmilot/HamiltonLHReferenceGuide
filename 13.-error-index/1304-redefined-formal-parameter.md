# 1304 : Redefined formal parameter

The specified identifier has already been defined as a formal parameter.

&#x20;

The following example illustrates this error:

```
function foo(variable v, variable v) // error 1304: redefinition of formal parameter 'v'
{
} 
```

