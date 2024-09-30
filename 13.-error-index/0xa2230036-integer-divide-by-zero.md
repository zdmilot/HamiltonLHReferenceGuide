# 0xa2230036: Integer divide by zero

The executor detected at the specified line an integer divided by zero.

&#x20;

The following example illustrates this error:

```
method main()
{
variable v1, v2;
v1 = 0;
v2 = 1 / v1; /* error 0xa2230036: integer divide by zero */
}
```

&#x20;
