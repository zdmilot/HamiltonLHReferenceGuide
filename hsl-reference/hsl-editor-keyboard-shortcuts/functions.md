# Functions

## Functions

## Functions

&#x20;

What Is a Function?

HSL functions perform actions. They can also return results. Sometimes these are the results of calculations or comparisons.&#x20;

Functions combine several operations under one name and enable the streamlining of the written code. It is possible to write a set of statements, name it, and then execute the entire set at any time, just by calling it and passing to it the information it needs.&#x20;

Information is passed to a function by enclosing the information in parentheses after the function’s name. Pieces of information that are being passed to a function are called arguments or parameters. Some functions do not take any arguments at all; some functions take one argument; some take several. There are even functions for which the number of arguments depends on how the function is used.&#x20;

HSL supports two kinds of functions: those that are built into the language, and those created by the programmer.&#x20;

&#x20;

Special Built-in Functions

The HSL language includes several built-in functions. Some of them enable the handling of expressions and special characters, and convert strings to numeric values. For example, IStr() and FStr() are used to convert numbers to strings.&#x20;

Consult the library functions and element functions for more information about these and other built-in functions.&#x20;

&#x20;

Creating Own Functions

Programmers can create their own functions and use them wherever needed. A function definition consists of a function header and a block of HSL statements.&#x20;

The TrimLeadingZeros function in the following example takes as its argument a barcode string, and trims leading zero characters from the string before returning with the number representation of the barcode.&#x20;

&#x20;

**function** TrimLeadingZeros     // Function keyword followed by function name

(**string** barcode)              // Formal arguments

{

**variable** index, length;  // Variable declarations

**string** null;

null = "0";              // HSL statements

length = barcode.GetLength();

**for** (index = 0; index < length; index++)

if (null.Compare(barcode.Mid(index, 1)) != 0)

break;

**return**(IVal(barcode.Mid(index,length)));

}                             // Function body

&#x20;

***

_Created with the Personal Edition of HelpNDoc:_ [_Free HTML Help documentation generator_](https://www.helpndoc.com)
