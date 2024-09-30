# 1220 : Bad program

The parser detected an error in the structure of the program before the specified symbol.

&#x20;

The following example illustrates this error:

```
file f;
f.Open("worklist.txt", "r"); // error 1220: error in program structure at identifier 'f'
method main()
{
variable v;
v = 1;
}
```

&#x20;
