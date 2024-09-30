# 0xa2230038: Returning address of local variable or temporary

The executor detected at the specified line a function returning the address of a local variable or a temporary. Local variables and temporaries are destroyed when a function returns; consequently the address returned will almost certainly be invalid.

When returning the address of a variable, the address of a formal or global variable should be returned, which will continue to exist after the function ends.

&#x20;

The following example illustrates this error:

```
function f()
{
event e;
return(e); /* error 0xa2230038: returning address of local variable or temporary */
}
```

&#x20;
