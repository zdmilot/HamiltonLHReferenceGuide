# 1321 : L-value is an array identifier

The parser detected a data reference which is an array.

&#x20;

The following example illustrates this error:

```
method main()
{
variable v;
long i[5];
i = 5;  // error 1321: 'i' : l-value is an array identifier
} 
```

