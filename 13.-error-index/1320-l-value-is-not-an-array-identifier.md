# 1320 : L-value is not an array identifier

The parser detected a data reference which is not an array.

&#x20;

The following example illustrates this error:

```
method main()
{
variable i;
i[3] = 5; // error 1320: 'i' : l-value is not an array identifier
} 
```

