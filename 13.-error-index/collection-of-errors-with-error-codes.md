# Collection of Errors With Error Codes

| Error Code   | Error Description                                | Explanation                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|--------------|--------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0xa122000c   | Function identifier is protected                 | The parser or executor detected at the specified line a protected function identifier in the symbol table. This happens for example if a device is declared in a local scope.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| 0xa122002c   | No context                                       | The executor failed at the specified line to create a new symbol table (context).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| 0xa123000a   | Bad tree                                         | The executor detected an error in the structure of the syntax tree.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| 0xa123000b   | Invalid entry                                    | The executor detected an invalid symbol table entry.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| 0xa123000f   | Function identifier not found                    | The executor failed at the specified line to lookup a function identifier in the symbol table.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| 0xa123001a   | Bad array identifier type                        | The executor detected at the specified line an unrecognized storage type for an array identifier.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| 0xa123001b   | Tag insert failed                                | The parser or executor failed at the specified line to insert an identifier into the tag table of a structure definition.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| 0xa123000e   | Setting value failed                             | The executor failed at the specified line to set the value of a symbol table entry.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| 0xa123001c   | Dynamic memory identifier not bound              | The executor detected at the specified line an identifier of a dynamic memory object that was not bound to a valid value.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| 0xa123001d   | Tag identifier not bound                         | The executor detected at the specified line an identifier of a structure tag object that was not bound to a valid value.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| 0xa123001e   | Structure reference out of bound                 | The executor detected at the specified line an invalid reference to an element of a structure.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| 0xa123001f   | Bad tag identifier type                          | The executor detected at the specified line an invalid data type.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| 0xa123002a   | Unable to enter nesting level                    | The executor failed at the specified line to enter the nesting level.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| 0xa123002b   | Unable to exit nesting level                     | The executor failed at the specified line to exit the nesting level.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| 0xa123002d   | Failed to read file                              | The executor failed at the specified line to read the file.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| 0xa123002e   | Failed to create timer                           | The parser or executor failed at the specified line to create the timer.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| 0xa123002f   | Failed to set timer                              | The executor failed at the specified line to set the timer.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| 0xa123004e   | Int64 not supported                              | 64-bit integers are not supported on a Windows 2000 platform.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| 0xa123004d   | Sequence property not found                      | The specified sequence property was not found.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| 0xa0220001   | No memory                                        | The system could not allocate or access enough memory or disk space for the specified operation.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| 0xa223000d   | Underspecified                                   | The executor detected at the specified line underspecified formal parameters of a function.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| 0xa223003a   | Unable to find file                              | The executor could not find the file specified.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| 0xa1220007   | Unrecognized token                               | The executor detected an unrecognized token.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| 0xa1230002   | Inserting identifier failed                      | The parser or executor could not insert the specified identifier into the symbol table.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |                                                                                                                                                                   
| 0xa1230002 | Inserting identifier failed                      | The parser or executor could not insert the specified identifier into the symbol table.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| 0xa1230003 | Identifier not found                             | <p>The parser or executor could not find the specified identifier in the symbol table.<br><br> </p><p>The following example illustrates this error as a run-time error of the executor:</p><pre class="language-clike"><code class="lang-clike">/* there is no sequence with the name 'nonExistingSequence' defined in the deck named ML_STAR of the system deck layout SystemLayoutTest.lay */
 
function f(device d)
{
  d.nonExistingSequence;  /* error 0xa1230003: failed to lookup identifier 'd.nonExistingSequence' in the symbol table */
}
  
method Main()
{
  device d("SystemLayoutTest.lay", "ML_STAR", hslTrue);
  f(d);
}
</code></pre><p><br></p>            |
| 0xa1230006 | Not an identifier                                | The executor detected that the symbol table entry of the identifier at the specified line is not an identifier.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| 0xa1230008 | R-value not bound                                | The executor detected an r-value that was not bound to a valid value.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| 0xa1230010 | Bindings not found                               | The executor failed at the specified line to lookup the value bound to a formal parameter in the symbol table.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| 0xa1230011 | Temporary variable not found                     | The executor failed at the specified line to delete the identifier of a temporary variable in the symbol table.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| 0xa1230012 | Unknown function type                            | <p>The executor detected at the specified line an unrecognized function type, i.e. the function referenced at the specified line has not been defined.</p><p> </p><p>The following example illustrates this error:</p><pre class="language-clike"><code class="lang-clike">function f();
method main()
{
    f();    /* error 0xa1230012: unknown function type */
    return;
}
</code></pre>                                                                                                                                                                                                                                                                                |
| 0xa1230014 | Type mismatch                                    | <p><br>The executor detected at the specified line a mismatch between the types of an actual and the corresponding formal parameter of a function.<br></p><p>The following example illustrates this error:</p><pre class="language-clike"><code class="lang-clike">string s;
s = IStr("1"); /* error 0xa1230014: type mismatch */
</code></pre>                                                                                                                                                                                                                                                                                                                               |
| 0xa1230018 | Bad memory type                                  | The executor detected at the specified line a bad memory type for an array.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| 0xa1230019 | Array reference out of bound                     | <p>The executor detected at the specified line an invalid index value to refer to an element of an array.<br><br>The following example illustrates this error:</p><pre class="language-clike"><code class="lang-clike">method main()
{
variable i;
long a[2];
for (i = 0; i &#x3C;= 2; i++)
a[i] = i;     /* error 0xa1230019: array reference out of bound */
}

</code></pre>                                                                                                                                                                                                                                                                                               |
| 0xa1230020 | L-value is not a structure identifier            | The executor detected at the specified line a data reference which is not a structure.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| 0xa1230021 | L-value is not an array identifier               | The executor detected at the specified line a data reference which is not a array.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| 0xa1230022 | Failed to lookup tag identifier in tag table     | The executor detected at the specified line a tag identifier which is not a member of the structure.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| 0xa1230023 | Signal break                                     | The executor detected at the specified line an invalid break-statement.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| 0xa1230024 | Copy out of bound                                | The executor detected at the specified line a structure copy which is out of bound.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| 0xa1230025 | Signal return                                    | The executor detected at the specified line an invalid return-statement.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| 0xa1230027 | Failed to copy tag table                         | The executor failed at the specified line to copy the tag table.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| 0xa1230029 | Function has not been defined                    | The executor detected at the specified line a function that has not been defined.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| 0xa1230030 | Failed to wait timer                             | The executor failed at the specified line to wait for the timer to be signaled.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| 0xa1230031 | Failed to create event                           | The parser or executor failed at the specified line to create the event.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| 0xa1230032 | Failed to set event                              | The executor failed at the specified line to set the event.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| 0xa1230033 | Failed to wait event                             | The executor failed at the specified line to wait for the event to be signaled.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| 0xa1230034 | Bad argument                                     | <p>The executor detected at the specified line an error in the function argument.<br><br>The following example illustrates this error:</p><pre class="language-clike"><code class="lang-clike">s.SetCurrentPosition(1.5); /* error 0xa1230034: bad argument */
</code></pre>                                                                                                                                                                                                                                                                                                                                                                                                  |
| 0xa1230046 | Bad argument parameter                           | <p>The executor detected at the specified line an error in the specified function argument.<br><br>The following example illustrates this error:</p><pre class="language-clike"><code class="lang-clike">ActivateDelay(-5, hslSchedulingStart, methodHandle, "Plate 1", taskHandle, hslFlase);
/* error 0xa1230046: bad argument parameter 1 */
</code></pre>                                                                                                                                                                                                                                                                                                                 |
| 0xa2220017 | Unrecognized type                                | The executor detected at the specified line an unrecognized storage type.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| 0xa2220044 | Automation type not supported                    | The executor detected at the specified line a reference of an automation function having a parameter which automation type is not supported (see Automation types).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| 0xa2230005 | R-value not a number                             | <p>The executor detected that the right hand side of the expression at the specified line is not a number.<br></p><p>The following example illustrates this error:</p><pre class="language-clike"><code class="lang-clike">variable v, s("a");
v = 1 + s; /* error 0xa2230005: right hand side of expression is not a number */
</code></pre>                                                                                                                                                                                                                                                                                                                                 |
| 0xa2230009 | Bad number                                       | <p>The executor detected at the specified line an error in a number.<br></p><p>The folowing example illustrates this error:</p><pre class="language-clike"><code class="lang-clike">method main()
{
loop (2.0)  /* error 0xa2230009: bad number */
{
variable v;
v = 1;
}
}
</code></pre>                                                                                                                                                                                                                                                                                                                                                                                     |
| 0xa2230013 | Unable to find file                              | <p>The executor could not find the file specified.<br><br>The following example illustrates this error:</p><pre class="language-clike"><code class="lang-clike">method main()
{
&#x3C;&#x3C; "c:\\nonexist.hsl";  /* error 0xa2230013: unable to find file */
}
</code></pre>                                                                                                                                                                                                                                                                                                                                                                                                 |
| 0xa2230015 | Bad l-value                                      | <p>The executor detected at the specified line a bad left value for an operation.<br></p><p>The following example illustrates this error:</p><pre class="language-clike"><code class="lang-clike">method main()
{
variable v1, v2, v3;
v1 = 1.5;
v2 = 1;
v3 = v1 &#x26; v2;  /* error 0xa2230015: bad l-value */
}
</code></pre>                                                                                                                                                                                                                                                                                                                                              |
| 0xa2230016 | Bad r-value                                      | <p>The executor detected at the specified line a bad right value for an operation.<br><br>The following example illustrates this error:</p><pre class="language-clike"><code class="lang-clike">method main()
{
variable v1, v2, v3;
v1 = 1;
v2 = 1.5;
v3 = v1 | v2;   /* error 0xa2230016: bad r-value */
}
</code></pre>                                                                                                                                                                                                                                                                                                                                                    |
| 0xa2230026 | Array size is not an integer                     | <p>The executor detected at the specified line an error in the size of an array.<br></p><p>The following example illustrates this error:</p><pre class="language-clike"><code class="lang-clike">struct
{
long a[1.5]; /* error 0xa2230026: array size not an integer */
} s;
</code></pre>                                                                                                                                                                                                                                                                                                                                                                                   |
| 0xa2230035 | Syntax error                                     | The parser detected syntax error(s) in the method.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| 0xa2230036 | Integer divide by zero                           | <p>The executor detected at the specified line an integer divided by zero.<br><br>The following example illustrates this error:</p><pre class="language-clike"><code class="lang-clike">method main()
{
variable v1, v2;
v1 = 0;
v2 = 1 / v1; /* error 0xa2230036: integer divide by zero */
}

</code></pre>                                                                                                                                                                                                                                                                                                                                                                 |
| 0xa2230037 | Overspecified                                    | <p>The executor detected at the specified line overspecified formal parameters of a function.<br><br>The following example illustrates this error:</p><pre class="language-clike"><code class="lang-clike">Sin(1,1); /* error 0xa2230037: overspecified actual parameters */
</code></pre>                                                                                                                                                                                                                                                                                                                                                                                    |
| 0xa2230038 | Returning address of local variable or temporary | <p>The executor detected at the specified line a function returning the address of a local variable or a temporary. Local variables and temporaries are destroyed when a function returns; consequently the address returned will almost certainly be invalid.<br><br>When returning the address of a variable, the address of a formal or global variable should be returned, which will continue to exist after the function ends.<br><br>The following example illustrates this error:</p><pre class="language-clike"><code class="lang-clike">function f()
{
event e;
return(e); /* error 0xa2230038: returning address of local variable or temporary */
}
</code></pre> |
| 0xa223003b | File not updatable                               | <p>The executor detected at the specified line a request to update a non-updatable file.<br></p><p>The following example illustrates this error:</p><pre class="language-clike"><code class="lang-clike">method Main()
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
</code></pre>                                                                                                                                                                                                                       |
| 0xa223003c | Recursive call                                   | <p>The executor detected at the specified line a (direct or indirect) recursive or concurrent function call.<br></p><p>The following example illustrates this error:</p><pre class="language-clike"><code class="lang-clike">function f();
function f()   /* error 0xa223003c: recursive or concurrent function call */
{
f();
}
method main()
{
f();
}
</code></pre>                                                                                                                                                                                                                                                                                                         |
| 0xa223003d | Failed to wait for thread(s)                     | <p>The executor failed at the specified line to wait for one or more threads to be signaled.<br><br>The following example illustrates this error:</p><pre class="language-clike"><code class="lang-clike">function f()
{
}
 
method main()
{
variable handles[];
 
handles.AddAsLast( - Fork("f") );
Join(handles, hslInfinite);  /* error 0xa223003d: failed to wait for thread(s) */
}

</code></pre>                                                                                                                                                                                                                                                                       |
| 0xa223003e | Time-out interval elapsed                        | The time-out interval elapsed at the specified line.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| 1001       | Syntax error                                     | <p>The parser could not determine the meaning of an expression or statement within the source program.<br><br>The parser detected the syntax error at the specified line.<br></p><p>The following example illustrates this error:</p><pre class="language-clike"><code class="lang-clike">var v;  // error 1001: syntax error
method Main()
{
v = 1;
}
</code></pre>                                                                                                                                                                                                                                                                                                          |
| 1002       | Syntax error before                              | <p>The parser could not determine the meaning of an expression or statement within the source program.<br><br>The parser detected the syntax error at the specified line before the specified symbol.</p><p><br>The following example illustrates this error:</p><pre class="language-clike"><code class="lang-clike">method Main()
{
variable v;
v = 1 0; // error 1002: syntax error before number 0
}
</code></pre>                                                                                                                                                                                                                                                        |
| 1101       | Missing period                                   | <p>The parser detected that there is missing a period before the specified symbol. Ensure that the method contains a period before the symbol and compile again.<br></p><p>The following example illustrates this error:</p><pre class="language-clike"><code class="lang-clike">device d("SystemDeckLayout.lay", "ML_STAR", hslTrue);
d Plate1.GetCount(); // error 1101: missing '.' before identifier 'Plate1'
</code></pre>                                                                                                                                                                                                                                               |
| 1102       | Missing semicolon                                | <p>The parser expected a semicolon to appear before the specified symbol.<br><br>The following example illustrates this error:</p><pre class="language-clike"><code class="lang-clike">string posId, labId;
posId = "A1"  /* error 1102: missing ';' before identifier 'labId' */
labId = "Plate2";
</code></pre>                                                                                                                                                                                                                                                                                                                                                             |
| 1103       | Missing assignment                               | <p>The parser expected an assignment to appear before the specified symbol.<br></p><p>The following example illustrates this error: </p><pre class="language-clike"><code class="lang-clike">debug 1;  // error 1103: missing '=' before number 1
</code></pre>                                                                                                                                                                                                                                                                                                                                                                                                               |
| 1104       | Missing opening parenthesis                      | <p>The parser expected an opening parenthesis to appear before the specified symbol.<br></p><p>The following example illustrates this error:</p><pre class="language-clike"><code class="lang-clike">method main )  // error 1104: missing '(' before symbol ')'
{
variable i;
v = 1;
}
</code></pre>                                                                                                                                                                                                                                                                                                                                                                         |
| 1105       | Missing closing parenthesis                      | <p>The parser expected a closing parenthesis to appear before the specified symbol.<br><br>The following example illustrates this error:</p><pre class="language-clike"><code class="lang-clike">function foo()
{
return (1;  // error 1105: missing ')' before symbol ';'
}

</code></pre>                                                                                                                                                                                                                                                                                                                                                                                   |
| 1106       | Missing opening brace                            | <p>The parser expected an opening brace to appear before the specified symbol.<br><br>The following example illustrates this error:</p><pre class="language-clike"><code class="lang-clike">struct s long a;};  // error 1106: missing '{' before symbol 'long'
</code></pre>                                                                                                                                                                                                                                                                                                                                                                                                 |
| 1107       | Missing closing brace                            | The parser expected a closing brace to appear before the specified symbol.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| 1108       | Missing opening bracket                          | <p>The parser expected an opening bracket to appear before the specified symbol.<br><br>The following example illustrates this error:</p><pre class="language-clike"><code class="lang-clike">long a 10];  // error 1108: missing '[' before number 10
</code></pre>                                                                                                                                                                                                                                                                                                                                                                                                          |
| 1109       | Missing closing bracket                          | <p>The parser expected a closing bracket to appear before the specified symbol.<br><br>The following example illustrates this error:</p><pre class="language-clike"><code class="lang-clike">long a [10;  // error 1109: missing ']' before symbol ';'
</code></pre>                                                                                                                                                                                                                                                                                                                                                                                                          |
| 1110       | Missing comma or closing parenthesis             | <p>The parser expected a comma or a closing parenthesis to appear before the specified symbol.<br><br>The following example illustrates this error: </p><pre class="language-clike"><code class="lang-clike">function foo(p1, p2  // error 1110: missing ',' or ')' before symbol '{'
{
variable v;
v = 1;
}
</code></pre>                                                                                                                                                                                                                                                                                                                                                    |
| 1111       | Missing comma or semicolon                       | <p>The parser expected a comma or a semicolon to appear before the specified symbol.<br><br>The following example illustrates this error: </p><pre class="language-clike"><code class="lang-clike">variable v1 v2;  // error 1111: missing ',' or ';' before identifier 'v2'
</code></pre>                                                                                                                                                                                                                                                                                                                                                                                    |
| 1112       | Missing statement                                | <p>The parser expected a statement to appear before the specified symbol.<br><br>The following example illustrates this error:</p><pre class="language-clike"><code class="lang-clike">method main()
{
variable v;
?   // error 1112: missing statement before symbol '?'
}
</code></pre>                                                                                                                                                                                                                                                                                                                                                                                     |
| 1201       | Bad variable declaration                         | <p>The parser detected an error in a declaration of an array or structure tag variable before the specified symbol.<br><br>The following example illustrates this error:</p><pre class="language-clike"><code class="lang-clike">long [10];    // error 1201: error in variable declaration before symbol '['
struct s
{
long 1a; // error 1201: error in variable declaration before number 1
};
</code></pre>                                                                                                                                                                                                                                                               |
| 1202       | Bad argument list                                | <p>The parser detected an error in the function argument list before the specified symbol.<br><br>The following example illustrates this error:</p><pre class="language-clike"><code class="lang-clike">function foo(  // error 1202: error in function argument list before symbol ';'
{
variable i;
v = 1;
}
</code></pre>                                                                                                                                                                                                                                                                                                                                                  |
| 1203       | Bad function name                                | <p>The parser detected an error in the specified function name.<br><br>The following example illustrates this error:</p><pre class="language-clike"><code class="lang-clike">function 1foo() // error 1203: bad function name : number 1
{
variable i;
}
</code></pre>                                                                                                                                                                                                                                                                                                                                                                                                        |
| 1204       | Bad member function name                         | <p>The parser detected an error in the specified member function name.<br><br>The following example illustrates this error:</p><pre class="language-clike"><code class="lang-clike">string s;
s.Rigth(2);  // error 1204: bad member function name : identifier 'Rigth'
</code></pre>                                                                                                                                                                                                                                                                                                                                                                                         |
| 1205       | Bad argument name                                | <p>The parser detected an error in the specified function argument name.<br><br>The following example illustrates this error:</p><pre class="language-clike"><code class="lang-clike">function foo(p1, 2p) // error 1205: bad function argument name : number 2
{
variable v;
v = 1;
}
</code></pre>                                                                                                                                                                                                                                                                                                                                                                          |
| 1206       | Bad statement                                    | <p>The parser detected an error in the statement before the specified symbol.<br><br>The following example illustrates this error:</p><pre class="language-clike"><code class="lang-clike">variable v;
v = ;   // error 1206: error in statement before symbol ';'
</code></pre>                                                                                                                                                                                                                                                                                                                                                                                              |
| 1207       | Bad structure name                               | <p>The parser detected an error in the specified structure name.<br><br>The following example illustrates this error:</p><pre class="language-clike"><code class="lang-clike">struct
{
long a[10]; 
} 1s;   // error 1207: bad structure name : number 1
</code></pre>                                                                                                                                                                                                                                                                                                                                                                                                        |
| 1208       | Bad variable name                                | <p>The parser detected an error in the specified variable name.<br><br>The following example illustrates this error:</p><pre class="language-clike"><code class="lang-clike">variable v1, 2v; // error 1208: bad variable name : number 2
</code></pre>                                                                                                                                                                                                                                                                                                                                                                                                                       |
| 1209       | Bad subscript expression                         | <p>The parser detected an error in the subscript expression of an array before the specified symbol.<br><br>The following example illustrates this error:</p><pre class="language-clike"><code class="lang-clike">method Main()
{
variable v;
long a[1];
a[?] = 1;  // error 1209: error in subscript expression before symbol '?'
}
</code></pre>                                                                                                                                                                                                                                                                                                                            |
| 1210       | Bad member selection                             | <p>The parser detected an error in the selection a data member of a structure before the specified symbol.<br><br>The following example illustrates this error:</p><pre class="language-clike"><code class="lang-clike">struct
{
long a[10];
} s;
s.[0] = 1;  // error 1210: error in member-selection before symbol '['
</code></pre>                                                                                                                                                                                                                                                                                                                                        |
| 1211       | Bad argument statement                           | <p>The parser detected an error in the function argument statement before the specified symbol.<br><br>The following example illustrates this error:</p><pre class="language-clike"><code class="lang-clike">string s1, s2;
s1 = "ABCD";
s2 = s1.Mid(2,); // error 1211: error in function argument statement before symbol ')'
</code></pre>                                                                                                                                                                                                                                                                                                                                 |
| 1212       | Bad member declaration list                      | <p>The parser detected an error in the list of data member declarations of a structure before the specified symbol.<br><br>The following example illustrates this error: </p><pre class="language-clike"><code class="lang-clike">struct
{
LONG i;  // error 1212: error in member declaration list before identifier 'LONG'
} s;
</code></pre>                                                                                                                                                                                                                                                                                                                               |
| 1213       | Bad variable list                                | <p>The parser detected an error in the declarations list of variables before the specified symbol.<br></p><p>The following example illustrates this error:</p><pre class="language-clike"><code class="lang-clike">string "A";  // error 1213: error in variable declaration list before string "A"
</code></pre>                                                                                                                                                                                                                                                                                                                                                             |
| 1214       | Bad for expression                               | <p>The parser detected an error in one of the for-expressions before the specified symbol.<br><br>The following example illustrates this error: </p><pre class="language-clike"><code class="lang-clike">for (i = 1; i &#x3C; 10; +++i) // error 1214: error in for-expression before symbol '+'
a[i] = i;
</code></pre>                                                                                                                                                                                                                                                                                                                                                      |
| 1215       | Bad expression                                   | <p>The parser detected an error in the expression before the specified symbol.<br><br>The following example illustrates this error:</p><pre class="language-clike"><code class="lang-clike">variable v;
v = 2*;  // error 1215: error in expression before symbol ';'
</code></pre>                                                                                                                                                                                                                                                                                                                                                                                           |
| 1216       | Bad file name                                    | <p>The parser detected an error in the specified file name.<br><br>The following example illustrates this error:</p><pre class="language-clike"><code class="lang-clike">method main()
{
&#x3C;&#x3C; utils.hsl; // error 1216: bad file name : identifier 'utils'
}
</code></pre>                                                                                                                                                                                                                                                                                                                                                                                            |
| 1217       | Bad member declaration                           | <p>The parser detected an error in the data member declaration of a structure before the specified symbol.<br><br>The following example illustrates this error:</p><pre class="language-clike"><code class="lang-clike">struct
{
char c;
int x;  // error 1217: error in member declaration before identifier 'int'
} s;
</code></pre>                                                                                                                                                                                                                                                                                                                                        |
| 1218       | Bad block                                        | <p>The parser detected an error in the block before the specified symbol.<br></p><p>The following example illustrates this error:</p><pre class="language-clike"><code class="lang-clike">method main()
begin   // error 1218: error in block before identifier 'begin'
variable v;
v = 1;
end 
</code></pre>                                                                                                                                                                                                                                                                                                                                                                 |
| 1219       | Bad number                                       | <p>The parser detected an error in the number before the specified symbol.<br><br>The following example illustrates this error:</p><pre class="language-clike"><code class="lang-clike">debug = -1;  // error 1219: bad number before symbol '-' 
</code></pre>                                                                                                                                                                                                                                                                                                                                                                                                               |
| 1220       | Bad program                                      | <p>The parser detected an error in the structure of the program before the specified symbol.<br><br>The following example illustrates this error:</p><pre class="language-clike"><code class="lang-clike">file f;
f.Open("worklist.txt", "r"); // error 1220: error in program structure at identifier 'f'
method main()
{
variable v;
v = 1;
}
</code></pre>                                                                                                                                                                                                                                                                                                                 |
| 1221       | Bad array size                                   | <p>The parser detected an error in the size of an array before the specified symbol.<br><br>The following example illustrates this error:</p><pre class="language-clike"><code class="lang-clike">long a[]; // error 1221: error in array size before symbol ']'
</code></pre>                                                                                                                                                                                                                                                                                                                                                                                                |
| 1222       | Bad string expression                            | <p>The parser detected an error in string expression before the specified symbol.<br><br>The following example illustrates this error:</p><pre class="language-clike"><code class="lang-clike">string s;
s = 'a'; // error 1222: error in string expression before number 97 
</code></pre>                                                                                                                                                                                                                                                                                                                                                                                   |
| 1223       | Bad function reference                           | <p>The parser detected a reference of the method. The method marks the beginning and end of program execution and therefore cannot be referenced.<br></p><p>The following example illustrates this error:</p><pre class="language-clike"><code class="lang-clike">method main()
{
Trace("main");
}
 
function foo()
{
main();  // error 1223: bad function reference
} 
</code></pre>                                                                                                                                                                                                                                                                                         |
| 1224       | Bad sequence expression                          | <p>The parser detected an error in the sequence expression before the specified symbol.<br><br>The following example illustrates this error:</p><pre class="language-clike"><code class="lang-clike">sequence s;
s = 0;   // error 1224: error in sequence expression before number 0 
</code></pre>                                                                                                                                                                                                                                                                                                                                                                          |
| 1225       | Bad array expression                             | <p>The parser detected an error in the array expression before the specified symbol.<br><br>The following example illustrates this error:</p><pre class="language-clike"><code class="lang-clike">variable v, va[];
va = v;  // error 1225: error in array expression before symbol ';' 
</code></pre>                                                                                                                                                                                                                                                                                                                                                                        |
| 1226       | Bad array type                                   | <p>The parser detected an error in the array type before the specified symbol.<br><br>The following example illustrates this error:</p><pre class="language-clike"><code class="lang-clike">function f(varArray[]) // error 1226: bad type of array identifier before varArray
{
variable index;
for (index = 0; index &#x3C; varArray.GetSize(); index++)
varArray[index] = 0;
} 
</code></pre>                                                                                                                                                                                                                                                                              |
| 1227       | Bad constant                                     | <p>The parser detected an error in the specified constant.<br><br></p><p>The following example illustrates this error:</p><pre class="language-clike"><code class="lang-clike">#define D -1  // error 1227: bad constant : symbol '-' 
</code></pre>                                                                                                                                                                                                                                                                                                                                                                                                                          |
| 1228       | Bad namespace name                               | <p>The parser detected an error in the specified namespace name.<br><br>The following example illustrates this error:</p><pre class="language-clike"><code class="lang-clike">namespace 1A() // error 1228: bad namespace name : number 1
{
variable i;
} 
</code></pre>                                                                                                                                                                                                                                                                                                                                                                                                      |
| 1229       | Bad object expression                            | <p>The parser detected an error in the object expression before the specified symbol.<br><br>The following example illustrates this error:</p><pre class="language-clike"><code class="lang-clike">object o;
o = 0; // error 1229: error in object expression before number 0 
</code></pre>                                                                                                                                                                                                                                                                                                                                                                                  |
| 1230       | Bad timer expression                             | <p>The parser detected an error in the timer expression before the specified symbol.<br><br>The following example illustrates this error:</p><pre class="language-clike"><code class="lang-clike">timer t;
t = 0; // error 1230: error in timer expression before number 0 
</code></pre>                                                                                                                                                                                                                                                                                                                                                                                     |
| 1231       | Bad event expression                             | <p>The parser detected an error in the event expression before the specified symbol.<br><br>The following example illustrates this error:</p><pre class="language-clike"><code class="lang-clike">event e;
e = 0; // error 1231: error in event expression before number 0 
</code></pre>                                                                                                                                                                                                                                                                                                                                                                                     |
| 1302       | Undeclared identifier                            | <p>The specified identifier was not declared. A variable must be specified in a declaration before it can be used.<br><br>* Make sure the identifier name is spelled correctly.<br>* Make sure the identifier is using the correct upper- and lowercase letters.<br><br>The following example illustrates this error:</p><pre class="language-clike"><code class="lang-clike">method main()
{
 i = 0;  // error 1302: 'i' undeclared identifier
} 
</code></pre>                                                                                                                                                                                                              |
| 1303       | Redefined identifier                             | <p>The specified identifier has already been declared. A variable must be specified once in a declaration before it can be used.<br></p><p>The following examples illustrate this error:</p><pre class="language-clike"><code class="lang-clike">{
variable s;
sequence s;         // error 1303: identifier 's' has already been defined
}
 
function foo(variable v) // error 1303: identifier 'v' has already been defined
{
variable v;
} 
</code></pre>                                                                                                                                                                                                                  |
| 1304       | Redefined formal parameter                       | <p>The specified identifier has already been defined as a formal parameter.<br><br>The following example illustrates this error:</p><pre class="language-clike"><code class="lang-clike">function foo(variable v, variable v) // error 1304: redefinition of formal parameter 'v'
{
} 
</code></pre>                                                                                                                                                                                                                                                                                                                                                                          |
| 1305       | Nested function definition                       | <p>Function definitions cannot be nested.<br><br>The following example illustrates this error:</p><pre class="language-clike"><code class="lang-clike">function f0()
{
Trace("+f0");
function f1() // error 1305: can't have nested function definitions
{
return;
}
return;
Trace("-f0");
} 
</code></pre>                                                                                                                                                                                                                                                                                                                                                                   |
| 1306       | Nested comments                                  | <p>The parser detected nested comments.<br><br>The following example illustrates this error:</p><pre class="language-clike"><code class="lang-clike">/*
 A
 /* B */      // error 1306: can't have nested comments
 C
*/ 
</code></pre>                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| 1307       | Unterminated character constant                  | <p>The parser detected an unterminated character constant.<br></p><p>The following example illustrates this error:</p><pre class="language-clike"><code class="lang-clike">variable c;
c = 'a;  // error 1307: unterminated character constant 
</code></pre>                                                                                                                                                                                                                                                                                                                                                                                                                 |
| 1308       | Unterminated string                              | <p>The parser detected an unterminated string.<br><br>The following example illustrates this error:</p><pre class="language-clike"><code class="lang-clike">string s;
s = "a;  // error 1308: unterminated string 
</code></pre>                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| 1309       | No method                                        | <p>The method keyword marks the beginning and end of program execution. A HSL program must have one method.<br><br>The method cannot have arguments.<br><br>The following example illustrates this error:</p><pre class="language-clike"><code class="lang-clike">function main()
{
Trace("main");
}
   // error 1309: no method 
</code></pre>                                                                                                                                                                                                                                                                                                                               |
| 1310       | Redefined method                                 | <p>The method keyword marks the beginning and end of program execution. An HSL program must have exactly one method.<br><br>The following example illustrates this error:</p><pre class="language-clike"><code class="lang-clike">method A()
{
Trace("A");
}
 
method B()
{
Trace("B");
}   // error 1310: method has already been defined 
</code></pre>                                                                                                                                                                                                                                                                                                                     |
| 1311       | Unexpected end of file                           | <p>The parser detected an unexpected end of the file.<br><br>The following example illustrates this error:</p><pre class="language-clike"><code class="lang-clike">method main()
{
Trace("main ");
// error 1311: unexpected end of file found 
</code></pre>                                                                                                                                                                                                                                                                                                                                                                                                                 |
| 1312       | Include file not found                           | <p>The parser could not find the specified include file.<br><br>The following example illustrates this error:</p><pre class="language-clike"><code class="lang-clike">#include "c:\\nonexist.hsl" // error 1312: cannot open include file: 'c:\nonexist.hsl' 
</code></pre>                                                                                                                                                                                                                                                                                                                                                                                                   |
| 1313       | Internal error                                   | The parser failed to recover the parser's internal state following the detection of a syntax error in the program. In most cases, fixing the errors reported in the code and recompiling will solve the problem.                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| 1314       | Empty statement                                  | <p>The parser detected an empty statement.<br><br>The following example illustrates this error:</p><pre class="language-clike"><code class="lang-clike">method main()
{
;  // error 1314: empty statement
} 
</code></pre>                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| 1315       | Too many arguments                               | <p>The parser detected a function or an initialization of an object with too many arguments.<br><br>The following example illustrates this error:</p><pre class="language-clike"><code class="lang-clike">method main(arg) // error 1315: 'main' : too many arguments
{
variable v;
v = 1;
} 
</code></pre>                                                                                                                                                                                                                                                                                                                                                                   |
| 1316       | Not a member function                            | <p>The parser detected a function reference which is not a member function of the calling object.<br><br></p><p>The following example illustrates this error:</p><pre class="language-clike"><code class="lang-clike">string s;
s.IStr(1);  // error 1316: 'IStr' : not a member function 
</code></pre>                                                                                                                                                                                                                                                                                                                                                                      |
| 1317       | Wrong member function                            | <p>The parser detected a function reference which is not a member function of the calling object.<br><br>The following example illustrates this error:</p><pre class="language-clike"><code class="lang-clike">string s;
s.Close();  // error 1317: 'Close' : wrong member function 
</code></pre>                                                                                                                                                                                                                                                                                                                                                                            |
| 1318       | Not a data member                                | <p>The parser detected a data reference which is not a data member of the calling object.<br><br>The following example illustrates this error:</p><pre class="language-clike"><code class="lang-clike">device d("SystemDeckLayout.lay", "ML_STAR", hslTrue);
method main()
{
sequence s;
s = d.Plate; // error 1318: 'Plate' : not a data member
} 
</code></pre>                                                                                                                                                                                                                                                                                                             |
| 1319       | L-value is not a structure identifier            | <p>The parser detected a data reference which is not a structure.<br><br>The following example illustrates this error:</p><pre class="language-clike"><code class="lang-clike">method Main()
{
variable i;
struct s
{
long x;
};
i.x = 5; // error 1319: 'i' : l-value is not a structure identifier
} 
</code></pre>                                                                                                                                                                                                                                                                                                                                                         |
| 1320       | L-value is not an array identifier               | <p>The parser detected a data reference which is not an array.<br><br>The following example illustrates this error:</p><pre class="language-clike"><code class="lang-clike">method main()
{
variable i;
i[3] = 5; // error 1320: 'i' : l-value is not an array identifier
} 
</code></pre>                                                                                                                                                                                                                                                                                                                                                                                    |
| 1321       | L-value is an array identifier                   | <p>The parser detected a data reference which is an array.<br><br>The following example illustrates this error:</p><pre><code>method main()
{
variable v;
long i[5];
i = 5;  // error 1321: 'i' : l-value is an array identifier
} 
</code></pre>                                                                                                                                                                                                                                                                                                                                                                                                                             |
| 1322       | L-value is structure identifier                  | <p>The parser detected a data reference which is a structure.<br><br>The following example illustrates this error:</p><pre class="language-clike"><code class="lang-clike">method main()
{
variable v;
struct
{
long i;
} s;
s = 0;  // error 1322: 's' : l-value is a structure identifier
} 
</code></pre>                                                                                                                                                                                                                                                                                                                                                                  |
| 1323       | Integer divide by zero                           | <p>The parser detected an integer divided by zero.<br><br>The following example illustrates this error:</p><pre class="language-clike"><code class="lang-clike">method main()
{
variable v;
v = 1 / (2-2); // error 1323: integer divide by zero
} 
</code></pre>                                                                                                                                                                                                                                                                                                                                                                                                             |
| 1324       | Not an l-value                                   | <p>The parser detected a left operand that is not an l-value.<br><br>The following example illustrates this error:</p><pre class="language-clike"><code class="lang-clike">#define d1 1
#define d2 "a"
#define d3 'a'
 
method Main()
{
d1 = 2;    // error 1324: 'd1' : not an l-value
d2 = "b";  // error 1324: 'd2' : not an l-value
d3 = 'b';  // error 1324: 'd3' : not an l-value
} 
</code></pre>                                                                                                                                                                                                                                                                      |
| 1325       | Handler undefined                                | <p>The parser detected an <strong>onerror goto</strong> label, but the specified handler did not exist in the same function.<br><br>The following example illustrates this error:</p><pre class="language-clike"><code class="lang-clike">method Main()
{
onerror goto MainError;
DoSomething();
return;
} // error 1325: handler 'MainError' was undefined 
</code></pre>                                                                                                                                                                                                                                                                                                    |
| 1326       | Handler redefined                                | <p>The parser detected a handler that appeared before more than one statement in the same function.<br><br>The following example illustrates this error:</p><pre class="language-clike"><code class="lang-clike">method Main()
{
onerror goto MainError;
DoSomething();
return;
 
MainError :
{
abort;
}
 
MainError :
{
abort;  // error 1326: 'MainError' : handler redefined
}
} 
</code></pre>                                                                                                                                                                                                                                                                            |
| 1327       | Type mismatch                                    | <p>The parser detected a mismatch between the types of an actual and the corresponding formal initializer of a variable.<br><br></p><p>The following example illustrates this error:</p><pre class="language-clike"><code class="lang-clike">string s(1); // error 1327: type mismatch 
</code></pre>                                                                                                                                                                                                                                                                                                                                                                         |
| 1328       | Layout file not found                            | <p>The parser could not find the specified layout file.<br><br>The following example illustrates this error:</p><pre class="language-clike"><code class="lang-clike">device d("nonExistingLayoutFile.lay", "ML_STAR", hslTrue);
// error 1328: cannot open layout file: 'nonExistingLayoutFile.lay' 
</code></pre>                                                                                                                                                                                                                                                                                                                                                            |
| 1329       | Too few arguments                                | The parser detected a function or an initialization of an object with too few arguments.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| 1330       | Instrument not registered                        | <p>The parser could not find the specified instrument in the registry.<br><br>The following example illustrates this error:</p><pre class="language-clike"><code class="lang-clike">device d("nonExistingInstrument");
// error 1330: instrument 'nonExistingInstrument' not registered 
</code></pre>                                                                                                                                                                                                                                                                                                                                                                        |
| 1331       | Instrument needs a deck layout                   | <p>The specified instrument needs a deck layout.<br><br>The following example illustrates this error:</p><pre class="language-clike"><code class="lang-clike">device d("ML_STAR"); // error 1331: instrument 'ML_STAR' needs a deck layout
</code></pre>                                                                                                                                                                                                                                                                                                                                                                                                                      |
| 1332       | Instrument needs no deck layout                  | <p>The specified instrument needs no deck layout.<br><br>The following example illustrates this error:</p><pre class="language-clike"><code class="lang-clike">device d("vacuumBox.lay"); // error 1332: instrument 'VACUUM_BOX' needs no deck layout 
</code></pre>                                                                                                                                                                                                                                                                                                                                                                                                          |
| 1334       | Skipped block initialization                     | <p>The initialization of a block is skipped by an onerror goto statement.<br></p><p>The following example illustrates this error:</p><pre class="language-clike"><code class="lang-clike">method Main()
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
</code></pre>                                                                                                                                                                                                                                                                                                                   |
| 1335       | Parser token buffer overflow                     | The Parser runs out of memory for the state stack.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| 1336       | Name too long                                    | <p>The specified name is too long. Enter a shorter name.<br><br>Names cannot be longer than 255 characters (including any namespace qualifiers).</p>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| 1337       | Type mismatch in formal parameter                | <p>The parser detected a mismatch between the types of an actual and the corresponding formal parameter of a function.<br><br>The following example illustrates this error:</p><pre class="language-clike"><code class="lang-clike">function f(timer t) void
{
// ...
}
method M() void
{
variable v;
f(v); // error 1337: type mismatch in formal parameter 1 of function 'f'
} 
</code></pre>                                                                                                                                                                                                                                                                               |
| 1338       | Type mismatch in return value                    | <p>The parser detected a mismatch between the types of the return value of a function declaration and the corresponding function definition.<br><br>The following example illustrates this error:</p><pre class="language-clike"><code class="lang-clike">function f();
function f() void  // error 1338: type mismatch in return value of function 'f'
{
} 
</code></pre>                                                                                                                                                                                                                                                                                                    |
| 1339       | Must return a value                              | <p>The specified function must return a value.<br><br>The following example illustrates this error:</p><pre class="language-clike"><code class="lang-clike">function f(timer t) variable
{
t.SetTimer(2);
t.WaitTimer(hslFalse);
} // error 1339: function 'f' must return a value 
</code></pre>                                                                                                                                                                                                                                                                                                                                                                             |
| 1340       | Redefined workflow                               | <p>The workflow keyword marks the beginning and end of program execution. An HSL program can have at most one workflow.<br><br>The following example illustrates this error:</p><pre class="language-clike"><code class="lang-clike">workflow A()
{
Trace("A");
}
workflow B()
{
Trace("B");
}    // error 1340: workflow has already been defined 
</code></pre>                                                                                                                                                                                                                                                                                                             |
| 1341       | Not schedulable                                  | The specified statement is not schedulable.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| 1342       | Private object reference                         | <p>The specified private object cannot be referenced outside of its definition file.<br><br>The following example illustrates this error:</p><pre class="language-clike"><code class="lang-clike">File A.hsl:
 
private variable v;
 
File B.hsl:
 
#include "A.hsl"
function f() void
{
v; // error 1342: private object 'v' cannot be referenced outside of its definition file
} 
</code></pre>                                                                                                                                                                                                                                                                            |
| 1343       | Private function reference                       | <p>The specified private function cannot be referenced outside of its definition file.<br><br>The following example illustrates this error:</p><pre class="language-clike"><code class="lang-clike">File A.hsl:
 
private function f() void
{
 
}
 
File B.hsl:
 
#include "A.hsl"
function g() void
{
f(); // error 1343: private function 'f' cannot be referenced outside of its definition file
} 
</code></pre>                                                                                                                                                                                                                                                          |
| 1344       | Analyzing completed with error                   | Analyzing completed with errors. In most cases, fixing the errors reported in the code and recompiling will solve the problem.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| 1345       | Lexer string buffer overflow                     | The constant string exceeds the Lexer's string buffer. Split the string into smaler pieces.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| 1346       | Obsolete statement                               | The specified statement is obsolete.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
