# 1310 : Redefined method

The method keyword marks the beginning and end of program execution. An HSL program must have exactly one method.

&#x20;

The following example illustrates this error:

```
method A()
{
Trace("A");
}
 
method B()
{
Trace("B");
}   // error 1310: method has already been defined 
```

