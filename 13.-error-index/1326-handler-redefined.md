# 1326 : Handler redefined

&#x20;The parser detected a handler that appeared before more than one statement in the same function.

&#x20;

The following example illustrates this error:

```
method Main()
{
onerror goto MainError;
DoSomething();
return;
 
MainError :
{
abort;
}
 
MainError :
{
abort;  // error 1326: 'MainError' : handler redefined
}
} 
```

