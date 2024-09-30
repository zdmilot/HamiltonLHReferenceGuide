# 1211 : Bad argument statement

The parser detected an error in the function argument statement before the specified symbol.

&#x20;

The following example illustrates this error:

```
string s1, s2;
s1 = "ABCD";
s2 = s1.Mid(2,); // error 1211: error in function argument statement before symbol ')'
```

&#x20;
