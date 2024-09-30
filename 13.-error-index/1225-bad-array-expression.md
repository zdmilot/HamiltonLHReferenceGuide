# 1225 : Bad array expression

The parser detected an error in the array expression before the specified symbol.

&#x20;

The following example illustrates this error:

```
variable v, va[];
va = v;  // error 1225: error in array expression before symbol ';' 
```

