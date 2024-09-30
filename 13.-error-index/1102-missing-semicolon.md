# 1102 : Missing semicolon

The parser expected a semicolon to appear before the specified symbol.

&#x20;

The following example illustrates this error:

```
string posId, labId;
posId = "A1"  /* error 1102: missing ';' before identifier 'labId' */
labId = "Plate2";
```

