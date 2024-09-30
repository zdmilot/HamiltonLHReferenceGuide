# 1210 : Bad member selection

The parser detected an error in the selection a data member of a structure before the specified symbol.

&#x20;

The following example illustrates this error:

```
struct
{
long a[10];
} s;
s.[0] = 1;  // error 1210: error in member-selection before symbol '['
```

&#x20;
