# 1223 : Bad function reference

The parser detected a reference of the method. The method marks the beginning and end of program execution and therefore cannot be referenced.&#x20;

&#x20;

The following example illustrates this error:

```
method main()
{
Trace("main");
}
 
function foo()
{
main();  // error 1223: bad function reference
} 
```

