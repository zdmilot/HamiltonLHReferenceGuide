# 0xa223003c : Recursive call

The executor detected at the specified line a (direct or indirect) recursive or concurrent function call.

&#x20;

The following example illustrates this error:

```
function f();
function f()   /* error 0xa223003c: recursive or concurrent function call */
{
f();
}
method main()
{
f();
}
```
