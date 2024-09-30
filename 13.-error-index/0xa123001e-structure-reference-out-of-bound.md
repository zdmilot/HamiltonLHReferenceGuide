# 0xa123001e: Structure reference out of bound

The executor detected at the specified line an invalid reference to an element of a structure.&#x20;



The following example illustrates this error:

```
method main()
{
    variable i;
    struct
    {
    long a[2];
    } s;
    for (i = 0; i <= 2; i++)
    s.a[i] = i; /* error 0xa123001e: structure reference out bound*/
}
```
