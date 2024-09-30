# 0xa223003b : File not updatable

The executor detected at the specified line a request to update a non-updatable file.

&#x20;

The following example illustrates this error:

```
method Main()
{
file f;
variable s;
f.SetDelimiter(hslAsciiText);
f.AddField(1, s, hslString);
f.Open("c:\\temp\\ascii.txt", hslAppend);
s = "hello\n";
f.UpdateRecord(); /* error 0xa223003b: file not updatable */
/* ... */
}
```
