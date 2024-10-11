# Returningavalue

## Returning a value

## Returning a Value

&#x20;

The return statement is used to stop the execution of a function and to return an optional scalar or aggregate value to the calling context of the function. The type of an optional scalar return value can be variable, string or sequence and the type of an optional aggregate return value can be one of the following : variable, string, sequence, dialog, object, timer, event or file.

The following example illustrates the use of the return statement:

&#x20;

function AddSequence(

variable index,      // index of source sequence

string seqBaseName,  // base name of source sequence

sequence targetSeq)  // target sequence (copy)

{

string seqName;      // name of source sequence

sequence sourceSeq;  // source sequence

variable currentPos; // current position

seqName = seqBaseName + IStr(index);

sourceSeq = ML\_STAR.GetSequence(seqName);

for (currentPos = sourceSeq.SetCurrentPosition(1);

currentPos != 0;

currentPos = sourceSeq.Increment(1))

{

targetSeq.Add(sourceSeq.GetLabwareId(), sourceSeq.GetPositionId());

}

return(targetSeq);

}

&#x20;

| **Overview of returning values from a function** |
| :----------------------------------------------: |

| **Type(type)** | **By value** | **By reference** |
| -------------- | ------------ | ---------------- |
| variable       | always       | NA               |
| sequence       | always       | NA               |
| string         | always       | NA               |
| device         | NA           | NA               |
| dialog         | NA           | NA               |
| object         | NA           | NA               |
| timer          | NA           | NA               |
| event          | NA           | NA               |
| file           | NA           | NA               |
| type id\[]     | always       | NA               |

&#x20;

***

_Created with the Personal Edition of HelpNDoc:_ [_Converting Word Docs to eBooks Made Easy with HelpNDoc_](https://www.helpndoc.com/step-by-step-guides/how-to-convert-a-word-docx-file-to-an-epub-or-kindle-ebook/)
