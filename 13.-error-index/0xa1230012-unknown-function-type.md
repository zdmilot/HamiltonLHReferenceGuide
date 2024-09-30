# 0xa1230012: Unknown function type

The executor detected at the specified line an unrecognized function type, i.e. the function referenced at the specified line has not been defined.

&#x20;

The following example illustrates this error:

```
function f();
method main()
{
f();    /* error 0xa1230012: unknown function type */
return;
}
```

&#x20;
