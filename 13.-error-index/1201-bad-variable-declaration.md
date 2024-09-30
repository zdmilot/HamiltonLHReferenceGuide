# 1201 : Bad variable declaration

The parser detected an error in a declaration of an array or structure tag variable before the specified symbol.

&#x20;

The following example illustrates this error:

```
long [10];    // error 1201: error in variable declaration before symbol '['
struct s
{
long 1a; // error 1201: error in variable declaration before number 1
};
```

&#x20;
