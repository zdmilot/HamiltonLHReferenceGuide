# 1334 : Skipped block intitialization

The initialization of a block is skipped by an onerror goto statement.

&#x20;

The following example illustrates this error:

```
method Main()
{
onerror goto a;
IStr("a");
 
if (0)
{
a:
{
Trace("a");
} // error 1334: initialization of block is skipped by onerror goto 'a'
}
} 
```

