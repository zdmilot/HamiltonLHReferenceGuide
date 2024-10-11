# Variables

Variables are used to store values. They are a way to retrieve and manipulate values using names. When used effectively they can help understanding what a program does.&#x20;

&#x20;

## Declaring Variables

It is required to declare variables before using them. This is done by using the **variable**, **sequence**, **string**, **device**, **dialog**, **object**, **timer**, **event** or **file** keywords. Variables can be global or local to a block. Local variables are those that are only within the block.

The following code examples are of variable declaration:&#x20;

&#x20;

```clike
variable count, less, factor;
string barcode;
barcode = "12345"; // The value stored in barcode is of string type. The sentence in quotes,
                   // the value of which is assigned to barcode, is a string literal
count = 5;         // The value stored in count has numeric type
less = count < 10; // The value stored in less has Boolean type
factor = 2.71;     // The value stored in factor has numeric type
```



&#x20;

## Naming Variables

HSL is a case-sensitive language, so naming a variable _Counter_ is different from naming it _counter_. In addition, variable names, which are restricted to the length of 255 charachters (including any namespace qualifiers), must follow certain rules:

The first character must be a letter (either uppercase or lowercase) or an underscore \_.

Subsequent characters can be letters, numbers, underscores.&#x20;

The variable name cannot be a keyword.&#x20;



### Some examples of valid variable names:

```clike
_count
Part9
Number_Of_Items
```

### Some invalid variable names:

```clike
96_nunc_flat       // Starts with a number
S&W                // Ampersand & is not a valid character for variable names
```



If a variable is declared without assigning any value to it, the variable will exist, however, its value is undefined.

```clike
variable index;
index = index + 1; // The value in index is undefined
```

It is not possible to use a variable that has never been declared; if tried to use such a variable, an error is generated at parse time.&#x20;

&#x20;

```clike
count = 1;         // The variable count has not been declared
```



&#x20;

### Conversion

Since HSL is a loosely-typed language, objects of the type **variable** have no fixed type. Instead, they have a type equivalent to the type of the value they contain. It is possible to convert a variable into a different type; for this, explicit conversion functions, IStr(), FStr(),IVal() and FVal() are provided.&#x20;

```clike
variable start, end;
string text;
start = 1;
end = 10;
text = "Count from ";
text = text + IStr(start);
text = text + " to ";
text = text + IStr(end);
```

After this code is executed, the text variable contains "Count from 1 to 10". The number data have been converted into string form.
