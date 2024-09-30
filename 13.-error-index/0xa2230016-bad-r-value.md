# 0xa2230016: Bad r-value

The executor detected at the specified line a bad right value for an operation.

&#x20;

The following example illustrates this error:

```
method main()
{
variable v1, v2, v3;
v1 = 1;
v2 = 1.5;
v3 = v1 | v2;   /* error 0xa2230016: bad r-value */
}
```

