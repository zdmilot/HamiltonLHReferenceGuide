# Passing Formal Parameters

When a parameter Is passed to a function by value, a separate copy of that parameter is made, a copy that exists only inside the function. If, on the other hand, a parameter is passed by reference, and the function changes the value of that parameter, it is changed everywhere in the program.

&#x20;

| **Overview of passing formal parameters** |
| :---------------------------------------: |

| **Type** **(type)** | **By value** | **By reference** |
| ------------------- | ------------ | ---------------- |
| sequence            | yes          | yes              |
| variable            | yes          | yes              |
| string              | yes          | yes              |
| device              | NA           | always           |
| dialog              | NA           | always           |
| object              | NA           | always           |
| timer               | NA           | always           |
| event               | NA           | always           |
| file                | NA           | always           |
| type id\[]          | NA           | always           |

&#x20;

The following example illustrates the use of passing formal parameters by value:

```clike
function AddSequence(
variable index,      // index of source sequence
string seqBaseName,  // base name of source sequence
sequence targetSeq)  // target sequence (copy)
{
string seqName;      // name of source sequence
sequence sourceSeq;  // source sequence
variable currentPos; // current position
seqName = seqBaseName + IStr(index);
sourceSeq = ML_STAR.GetSequence(seqName);
for (currentPos = sourceSeq.SetCurrentPosition(1);
currentPos != 0;
currentPos = sourceSeq.Increment(1))
{
targetSeq.Add(sourceSeq.GetLabwareId(),sourceSeq.GetPositionId());
}
return(targetSeq);
}
 
method Main()
{
variable index;
variable numberOfPlates;
sequence plates;
numberOfPlates = InputBox("Enter number of plates:", "Get Input", "i");
for (index = 1; index <= numberOfPlates; index++)
plates = AddSequence(index, "Plate_", plates);
}
```



The efficiency of the same example can be improved by passing the formal parameter of the type sequence by reference:

```clike
function AddSequence(
variable index,      // index of source sequence
string seqBaseName,  // base name of source sequence
sequence& targetSeq) // target sequence (reference)
{
string seqName;      // name of source sequence
sequence sourceSeq;  // source sequence
variable currentPos; // current position
seqName = seqBaseName + IStr(index);
sourceSeq = ML_STAR.GetSequence(seqName);
for (currentPos = sourceSeq.SetCurrentPosition(1);
currentPos != 0;
currentPos = sourceSeq.Increment(1))
{
targetSeq.Add(sourceSeq.GetLabwareId(),sourceSeq.GetPositionId());
}
}
 
method Main()
{
variable index;
variable numberOfPlates;
sequence plates;
numberOfPlates = InputBox("Enter number of plates:", "Get Input", "i");
for (index = 1; index <= numberOfPlates; index++)
AddSequence(index, "Plate_", plates);
}
```

