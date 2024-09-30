# 1303 : Redefined identifier

The specified identifier has already been declared. A variable must be specified once in a declaration before it can be used.

&#x20;

The following examples illustrate this error:

```
{
variable s;
sequence s;         // error 1303: identifier 's' has already been defined
}
 
function foo(variable v) // error 1303: identifier 'v' has already been defined
{
variable v;
} 
```

