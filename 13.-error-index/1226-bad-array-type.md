# 1226 : Bad array type

The parser detected an error in the array type before the specified symbol.

&#x20;

The following example illustrates this error:

```
function f(varArray[]) // error 1226: bad type of array identifier before varArray
{
variable index;
for (index = 0; index < varArray.GetSize(); index++)
varArray[index] = 0;
} 
```

