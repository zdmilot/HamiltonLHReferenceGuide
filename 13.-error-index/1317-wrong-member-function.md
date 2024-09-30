# 1317 : Wrong member function

The parser detected a function reference which is not a member function of the calling object.

&#x20;

The following example illustrates this error:

```
string s;
s.Close();  // error 1317: 'Close' : wrong member function 
```

