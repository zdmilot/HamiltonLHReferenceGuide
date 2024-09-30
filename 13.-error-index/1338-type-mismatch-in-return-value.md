# 1338 : Type mismatch in return value

The parser detected a mismatch between the types of the return value of a function declaration and the corresponding function definition.

&#x20;

The following example illustrates this error:

```
function f();
function f() void  // error 1338: type mismatch in return value of function 'f'
{
} 
```

