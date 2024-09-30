# 1002 : Syntax error before

The parser could not determine the meaning of an expression or statement within the source program.

The parser detected the syntax error at the specified line before the specified symbol.

&#x20;

The following example illustrates this error:

```
method Main()
{
variable v;
v = 1 0; // error 1002: syntax error before number 0
}
```

&#x20;
