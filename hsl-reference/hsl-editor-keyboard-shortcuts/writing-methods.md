# Writing Methods

&#x20;The Hamilton Standard Language is written in text format, and is organized into statements, blocks consisting of related sets of statements, functions, one method and comments. Within a statement, the following can be used: variables, immediate data such as strings and numbers, and expressions.

The following diagram shows the general structure of an HSL program:

```cpp
#include "Utils.hsl"      // control directives
 
variable v1, v2;          // global declarations
timer t1, t2;
file f1, f2;
 
function f()              // function definitions
{
   //...
}
 
function g()
{
   //...
}
 
method myMethod()         // "main" program
{
 //...
 if (f() == 0)
 {
   //...
   Trace("f failed\n");
 }
 if (g() == 0)
 {
  //...
  Trace("g failed\n");
 }
 //...
 return;
}
```



## Method

The method marks the beginning and end of program execution. Every HSL program must have exactly one method. The method can call other functions. The method does not take any arguments and does not return a value.

The following example shows the definition of a method.

<pre class="language-clike"><code class="lang-clike">device Ml_Star("SystemDeckLayout.lay", "ML_STAR", hslTrue);  // Global variable declarations
 
method myMethod                 // Method keyword followed by method name
()                              // No formal arguments allowed
{
<strong> variable vol, currentPos;  // Local variable declarations
</strong> vol = 10;                  // HSL statements
 Initialize();
 TipPickUp();
 for (currentPos = Ml_Star.SourceA.SetCurrentPosition(1);
   currentPos != 0;
   currentPos = Ml_Star.SourceA++)
 {
  Aspirate();
  Dispense();
 }
 TipEject();
 Ml_Star.StandardTips++;
}   // Method body
</code></pre>



&#x20;

## Functions

A function is a collection of HSL statements. Functions can take any number of arguments and return a scalar value of type **variable**, **string** or **sequence** or an aggregate value of type **variable**, **string**, **sequence**, **dialog**, **object**, **timer**, **event** or **file** (see also Returning a value).

The following example shows the definition of a function, which consists of a block of six statements.&#x20;

```clike
function TrimLeadingZeros    // Function keyword followed by function name
(string barcode)             // Formal arguments
{
    variable index, length; // Variable declarations
    string null;
    null = "0";             // HSL statements
    length = barcode.GetLength();
    for (index = 0; index < length; index++)
        if (null.Compare(barcode.Mid(index, 1)) != 0)
            break;
    return(IVal(barcode.Mid(index,length)));
}   // Function body
```





&#x20;

## Statements

A statement consists of one or more items and symbols on a line. A semicolon terminates a statement.

```clike
count = 5;
barcodeStr = "12345";
```

A group of statements that is surrounded by braces { } is called a block. Blocks of statements are used, for example, in functions and conditionals.

&#x20;

## Comments

An HSL comment is written in one of the following ways:

The // (slash, asterisk) characters, followed by any sequence of characters (including new lines), followed by the characters.

The // (two slashes) characters, followed by any sequence of characters. A new line not immediately preceded by a backslash terminates this form of comment. Therefore, it is commonly called a ”single-line comment”.&#x20;

```clike
barcodeStr = "12345";
 
//
This is a multi-line comment that explains the preceding code statement.
The statement assigns a value to the barcodeStr variable. The value, which
is contained between the quotation marks, is called a literal. A literal explicitly and directly contains information; it does not refer to the information indirectly. (The quote marks are not part of the literal.)
*/
```



&#x20;

## Assignments and Equality

The equal sign = is used to indicate the action of assigning a value. That is, a statement could say

```clike
count = 5;
```

It means "Assign the value 5 to the variable count," or "count takes the value 5." If two valuesa are to be compared to determine whether they are equal, a pair of equal signs == should be used. This is discussed in detail in controlling program flow.&#x20;

&#x20;

## Expressions

An expression is something that a person can read as a Boolean or numeric expression. Expressions contain symbol characters like "+" rather than words like "added to". Any valid combination of values, variables, operators, and expressions constitutes an expression.

```clike
index = index + 1;
```
