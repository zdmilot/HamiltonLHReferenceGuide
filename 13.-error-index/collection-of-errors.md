# Collection of Errors



<table><thead><tr><th width="167">Error Code</th><th>Error Description</th><th>Explanation</th></tr></thead><tbody><tr><td>0xa122000c</td><td>Function identifier is protected</td><td>The parser or executor detected at the specified line a protected function identifier in the symbol table. This happens for example if a device is declared in a local scope.</td></tr><tr><td>0xa122002c</td><td>No context</td><td>The executor failed at the specified line to create a new symbol table (context).</td></tr><tr><td>0xa123000a</td><td>Bad tree</td><td>The executor detected an error in the structure of the syntax tree.</td></tr><tr><td>0xa123000b</td><td>Invalid entry</td><td>The executor detected an invalid symbol table entry.</td></tr><tr><td>0xa123000f</td><td>Function identifier not found</td><td>The executor failed at the specified line to lookup a function identifier in the symbol table.</td></tr><tr><td>0xa123001a</td><td>Bad array identifier type</td><td>The executor detected at the specified line an unrecognized storage type for an array identifier.</td></tr><tr><td>0xa123001b</td><td>Tag insert failed</td><td>The parser or executor failed at the specified line to insert an identifier into the tag table of a structure definition.</td></tr><tr><td>0xa123000e</td><td>Setting value failed</td><td>The executor failed at the specified line to set the value of a symbol table entry.</td></tr><tr><td>0xa123001c</td><td>Dynamic memory identifier not bound</td><td>The executor detected at the specified line an identifier of a dynamic memory object that was not bound to a valid value.</td></tr><tr><td>0xa123001d</td><td>Tag identifier not bound</td><td>The executor detected at the specified line an identifier of a structure tag object that was not bound to a valid value.</td></tr><tr><td>0xa123001e</td><td>Structure reference out of bound</td><td><p></p><p>The executor detected at the specified line an invalid reference to an element of a structure. </p><p></p><p>The following example illustrates this error:</p><pre class="language-clike"><code class="lang-clike">method main()
{
    variable i;
    struct
    {
    long a[2];
    } s;
    for (i = 0; i &#x3C;= 2; i++)
    s.a[i] = i; /* error 0xa123001e: structure reference out bound*/
}
</code></pre></td></tr><tr><td>0xa123001f</td><td>Bad tag identifier type</td><td>The executor detected at the specified line an invalid data type.</td></tr><tr><td>0xa123002a</td><td>Unable to enter nesting level</td><td>The executor failed at the specified line to enter the nesting level.</td></tr><tr><td>0xa123002b</td><td>Unable to exit nesting level</td><td>The executor failed at the specified line to exit the nesting level.</td></tr><tr><td>0xa123002d</td><td>Failed to read file</td><td><p></p><p>The executor failed at the specified line to read the file.</p><p></p><p>The following example illustrates this error:</p><pre class="language-clike"><code class="lang-clike">file f;
string s;
f.ReadString(s); /* error 0xa123002d: failed to read file */
</code></pre></td></tr><tr><td>0xa123002e</td><td>Failed to create timer</td><td>The parser or executor failed at the specified line to create the timer.</td></tr><tr><td>0xa123002f</td><td>Failed to set timer</td><td>The executor failed at the specified line to set the timer.</td></tr><tr><td>0xa123004e</td><td>Int64 not supported</td><td>64 bit integers are not supported on a Windows 2000 platform.</td></tr><tr><td>0xa123004d</td><td>Sequence property not found</td><td>The specified sequence property was not found.</td></tr><tr><td>0xa0220001</td><td>No memory</td><td><p></p><p>The system could not allocate or access enough memory or disk space for the specified operation.</p><p> </p><p>The following example illustrates this error: </p><pre class="language-clike"><code class="lang-clike">method m()
{
variable v;
long a[1000000000]; /* error 0xa0220001: No memory */
return;
}
</code></pre></td></tr><tr><td>0xa223000d</td><td>Underspecified</td><td><p></p><p>The executor detected at the specified line underspecified formal parameters of a function.</p><p> </p><p>The following example illustrates this error:</p><pre class="language-clike"><code class="lang-clike">variable i;
i = IVal(); /* error 0xa223000d: underspecified actual parameters */
</code></pre></td></tr><tr><td>0xa223003a</td><td>Unable to find file</td><td><p></p><p>The executor could not find the file specified.</p><p> </p><p>The following example illustrates this error:</p><pre><code>method main()
{
&#x3C;&#x3C; "c:\\nonexist.hsl";  /* error 0xa2230013: unable to find file */
}
</code></pre></td></tr><tr><td></td><td></td><td></td></tr></tbody></table>
