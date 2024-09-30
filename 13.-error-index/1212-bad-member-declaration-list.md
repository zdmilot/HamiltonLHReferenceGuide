# 1212 : Bad member declaration list

The parser detected an error in the list of data member declarations of a structure before the specified symbol.

&#x20;

The following example illustrates this error:&#x20;

```
struct
{
LONG i;  // error 1212: error in member declaration list before identifier 'LONG'
} s;
```

&#x20;
