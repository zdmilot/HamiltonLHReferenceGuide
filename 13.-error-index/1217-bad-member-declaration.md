# 1217 : Bad member declaration

The parser detected an error in the data member declaration of a structure before the specified symbol.

&#x20;

The following example illustrates this error:

```
struct
{
char c;
int x;  // error 1217: error in member declaration before identifier 'int'
} s;
```

&#x20;
