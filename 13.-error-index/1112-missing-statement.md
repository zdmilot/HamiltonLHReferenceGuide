# 1112 : Missing statement

The parser expected a statement to appear before the specified symbol.

&#x20;

The following example illustrates this error:

```
method main()
{
variable v;
?   // error 1112: missing statement before symbol '?'
}
```

