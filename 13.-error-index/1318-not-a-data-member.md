# 1318 : Not a data member

The parser detected a data reference which is not a data member of the calling object.

&#x20;

The following example illustrates this error:

```
device d("SystemDeckLayout.lay", "ML_STAR", hslTrue);
method main()
{
sequence s;
s = d.Plate; // error 1318: 'Plate' : not a data member
} 
```

