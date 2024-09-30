# 1316 : Not a member function

The parser detected a function reference which is not a member function of the calling object.

&#x20;

The following example illustrates this error:

```
string s;
s.IStr(1);  // error 1316: 'IStr' : not a member function 
```

