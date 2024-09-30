# 0xa223003d : Failed to wait for thread(s)

The executor failed at the specified line to wait for one or more threads to be signaled.

&#x20;

The following example illustrates this error:

```
function f()
{
}
 
method main()
{
variable handles[];
 
handles.AddAsLast( - Fork("f") );
Join(handles, hslInfinite);  /* error 0xa223003d: failed to wait for thread(s) */
}
```

