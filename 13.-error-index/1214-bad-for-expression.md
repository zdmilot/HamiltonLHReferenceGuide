# 1214 : Bad for expression

The parser detected an error in one of the for-expressions before the specified symbol.

&#x20;

The following example illustrates this error:&#x20;

```
for (i = 1; i < 10; +++i) // error 1214: error in for-expression before symbol '+'
a[i] = i;
```

&#x20;
