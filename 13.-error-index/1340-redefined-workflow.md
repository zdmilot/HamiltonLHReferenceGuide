# 1340 : Redefined workflow

The workflow keyword marks the beginning and end of program execution. An HSL program can have at most one workflow.

&#x20;

The following example illustrates this error:

```
workflow A()
{
Trace("A");
}
workflow B()
{
Trace("B");
}    // error 1340: workflow has already been defined 
```

