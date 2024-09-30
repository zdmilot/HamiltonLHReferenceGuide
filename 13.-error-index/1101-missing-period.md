# 1101 : Missing period

&#x20;The parser detected that there is missing a period before the specified symbol. Ensure that the method contains a period before the symbol and compile again.

&#x20;

The following example illustrates this error:

```
device d("SystemDeckLayout.lay", "ML_STAR", hslTrue);
d Plate1.GetCount(); // error 1101: missing '.' before identifier 'Plate1'
```
