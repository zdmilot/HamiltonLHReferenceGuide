# 1110 : Missing comma or closing parenthesis

The parser expected a comma or a closing parenthesis to appear before the specified symbol.

&#x20;

The following example illustrates this error:&#x20;

```
function foo(p1, p2  // error 1110: missing ',' or ')' before symbol '{'
{
variable v;
v = 1;
}
```

