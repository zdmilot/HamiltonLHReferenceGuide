# 1105 : Missing closing parenthesis

The parser expected a closing parenthesis to appear before the specified symbol.

&#x20;

The following example illustrates this error:

```
function foo()
{
return (1;  // error 1105: missing ')' before symbol ';'
}
```

