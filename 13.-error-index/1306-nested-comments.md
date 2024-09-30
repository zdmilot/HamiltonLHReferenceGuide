# 1306 : Nested comments

The parser detected nested comments.

&#x20;

The following example illustrates this error:

```
/*
 A
 /* B */      // error 1306: can't have nested comments
 C
*/ 
```

