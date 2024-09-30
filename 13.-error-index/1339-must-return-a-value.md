# 1339 : Must return a value

The specified function must return a value.

&#x20;

The following example illustrates this error:

```
function f(timer t) variable
{
t.SetTimer(2);
t.WaitTimer(hslFalse);
} // error 1339: function 'f' must return a value 
```

