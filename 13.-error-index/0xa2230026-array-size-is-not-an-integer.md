# 0xa2230026: Array size is not an integer

The executor detected at the specified line an error in the size of an array.

&#x20;

The following example illustrates this error:

```
struct
{
long a[1.5]; /* error 0xa2230026: array size not an integer */
} s;
```

&#x20;
