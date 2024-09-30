# 1319 : L-value is not a structure identifier

The parser detected a data reference which is not a structure.

&#x20;

The following example illustrates this error:

```
method Main()
{
variable i;
struct s
{
long x;
};
i.x = 5; // error 1319: 'i' : l-value is not a structure identifier
} 
```

