# 1322 : L-value is structure identifier

The parser detected a data reference which is a structure.

&#x20;

The following example illustrates this error:

```
method main()
{
variable v;
struct
{
long i;
} s;
s = 0;  // error 1322: 's' : l-value is a structure identifier
} 
```

