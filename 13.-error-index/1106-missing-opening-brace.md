# 1106 : Missing opening brace

The parser expected an opening brace to appear before the specified symbol.

&#x20;

The following example illustrates this error:

```
struct s long a;};  // error 1106: missing '{' before symbol 'long'
```

