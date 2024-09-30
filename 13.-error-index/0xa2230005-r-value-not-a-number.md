# 0xa2230005: R-value not a number

The executor detected that the right hand side of the expression at the specified line is not a number.

&#x20;

The following example illustrates this error:

```
variable v, s("a");
v = 1 + s; /* error 0xa2230005: right hand side of expression is not a number */
```
