# 0xa2230015: Bad l-value

The executor detected at the specified line a bad left value for an operation.

&#x20;

The following example illustrates this error:

```
method main()
{
variable v1, v2, v3;
v1 = 1.5;
v2 = 1;
v3 = v1 & v2;  /* error 0xa2230015: bad l-value */
}
```

