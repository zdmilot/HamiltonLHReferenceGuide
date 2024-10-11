# Data Types

What Are the HSL Data Types?

The main types are variables (**variable**), sequences (**sequence**), strings (**string**), devices (**device**), dialogs (**dialog**), automation objects (**object**), timers (**timer**), events (**event**), files (**file**)and errors (**error**).

&#x20;

## String Data Type

Strings are delineated by double quotation marks. A string is an object, with special element functions. The following are examples of strings:

### valid:

```clike
"This is a \n multi-line text "
"\"This is a text in double quotes""
"42"
```

### invalid:

```clike
""Text"" // error: double quotes in character string
```

A string can contain zero or more characters. When it contains zero, it is called a zero-length string "".&#x20;

&#x20;

## Number Data Type

HSL supports both integer and floating-point numbers. Integers can be positive, 0, or negative; a floating-point number can contain either a decimal point, an uppercase E, which is used to represent "ten to the power of" in scientific notation, or both. The following are examples of numbers:

&#x20;

### valid:

```clike
-1
0x1A
010
172
1.5
1.523E-1
```

### invalid:

```clike
.5         // error: missing integer part
1.523E-1.5 // error: exponent not an integer
1.5 E 2    // error: space before(after) character E
```



Integers can be represented in base 10 (decimal), and base 16 (hexadecimal).&#x20;

Hexadecimal integers are specified by a leading **0x** (the x must be lowercase) and can contain digits 0 through 9 and letters A through F (either uppercase or lowercase). The letter **E** is a permissible digit in hexadecimal notation and does not signify an exponential number. The letters A through F are used to represent, as single digits, the numbers that are 10 through 15 in base 10. That is, 0xF is equivalent to 15, and 0x10 is equivalent to 16.

Hexadecimal numbers can be negative, but cannot be fractional. A number that begins with a single 0 and contains a decimal point is a decimal floating-point number; a number that begins with 0x and contains a decimal point generates an error.&#x20;

### Some example numbers:

```clike
0.0001, 1E-4, 1.0E-4  // Three floating-point numbers, equivalent to each other
3.45e2                // A floating-point number, equivalent to 345
42                    // An integer number
0377                  // An integer number
0xff                  // A hexadecimal integer, equivalent to 255
0x37CF                // A hexadecimal integer, equivalent to 14287
```



#### Booleans

In a comparison, any expression that evaluates to 0 is taken to be false, and any statement that evaluates to a number other than 0 is taken to be true.

&#x20;

For more information on comparisons, see controlling program flow.
