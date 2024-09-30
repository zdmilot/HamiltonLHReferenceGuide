# 1325 : Handler undefined

The parser detected an **onerror goto** label, but the specified handler did not exist in the same function.

&#x20;

The following example illustrates this error:

```
method Main()
{
onerror goto MainError;
DoSomething();
return;
} // error 1325: handler 'MainError' was undefined 
```

