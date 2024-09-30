# 0xa1230019: Array reference out of bound

The executor detected at the specified line an invalid index value to refer to an element of an array.&#x20;

&#x20;

The following example illustrates this error:

```
method main()
{
variable i;
long a[2];
for (i = 0; i <= 2; i++)
a[i] = i;     /* error 0xa1230019: array reference out of bound */
}
```

