# 1209 : Bad subscript expression

The parser detected an error in the subscript expression of an array before the specified symbol.

&#x20;

The following example illustrates this error:

```
method Main()
{
variable v;
long a[1];
a[?] = 1;  // error 1209: error in subscript expression before symbol '?'
}
```

&#x20;
