# 1324 : Not an l-value

The parser detected a left operand that is not an l-value.

&#x20;

The following example illustrates this error:

```
#define d1 1
#define d2 "a"
#define d3 'a'
 
method Main()
{
d1 = 2;    // error 1324: 'd1' : not an l-value
d2 = "b";  // error 1324: 'd2' : not an l-value
d3 = 'b';  // error 1324: 'd3' : not an l-value
} 
```

