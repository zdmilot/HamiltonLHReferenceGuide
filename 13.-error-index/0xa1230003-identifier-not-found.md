# 0xa1230003: Identifier not found

The parser or executor could not find the specified identifier in the symbol table.

&#x20;

The following example illustrates this error as a run-time error of the executor:

```
/* there is no sequence with the name 'nonExistingSequence' defined in the deck named ML_STAR of the system deck layout SystemLayoutTest.lay */
 
function f(device d)
{
d.nonExistingSequence;  /* error 0xa1230003: failed to lookup identifier 'd.nonExistingSequence' in the symbol table */
}
 
method Main()
{
device d("SystemLayoutTest.lay", "ML_STAR", hslTrue);
f(d);
}
```

