# 0xa0220001: No memory

The system could not allocate or access enough memory or disk space for the specified operation.

&#x20;

The following example illustrates this error:&#x20;

```
method m()
{
variable v;
long a[1000000000]; /* error 0xa0220001: No memory */
return;
}
```
