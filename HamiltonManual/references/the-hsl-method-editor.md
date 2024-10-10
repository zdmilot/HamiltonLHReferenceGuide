# The HSL Method Editor

HSL or Hamilton Standard Language is the underlying programming language that the VENUS Software is operated from. HSL is a C/C++ style programming language. To use HSL, the HSL Method Editor must be started. It is a separate program that is located in “C:\Program Files\Hamilton\Bin\HxHslMetEd.exe” (depending on the language/installation settings).

The editor is an acclaimed and outstanding text editor. An hsl file can be written using a text editor however the checksum lines have to be checked personally.\


<figure><img src="../../.gitbook/assets/image (52) (1) (1).png" alt="" width="563"><figcaption></figcaption></figure>

Before an HSL file is run, it has to be compiled (translated) into a basic computer language. This is done by the “MICROLAB STAR Run” Program, which should already be familiar.

Unlike a C/C++ program, the file is compiled just before it is run. This is done every time it is run. The Hamilton Method Editor is actually a code generator that creates an HSL code simultaneously. The Run Engine (compiler) runs the HSL file, not the ‘.med’ file.

<figure><img src="../../.gitbook/assets/image (55) (1).png" alt=""><figcaption></figcaption></figure>

## HSL File Types

HSL is usually used to create libraries. There are actually 2 HSL file types that may be encountered:

Files with a file extension of “.hsl” are known as header files while files with an extension of “.hs\_” are known as Source Files or Implementation Files.

Typically header files will contain only declarations of functions and variables while source files contain the actual code that is in the function (known as the function implementation).

There are three main reasons to split into header and source files:

1. It allows another person to look only at the header file and know what the functions do. It is not necessary to analyze they work.
2. Sometimes there is a need to create additional functions, for the functions in the header to work but, may not want others to see them. Anything declared in the implementation file is not visible when the declaration file is included.
3. It enhances the speed of the VENUS Method Editor.

\


## HSL Syntax

Most lines of code must end with a semicolon (;). Generally a new line is started after a semicolon. But this does not need to be done (just makes the code easier to read).

The space between lines is known as whitespace and has no function.

Use of a double forward slash (//) indicates that the following characters in this line are comments only. A forward slash followed by a star (/\*) together with the star followed by a forward slash (\*/) indicates a comment block which can be separated over multiple lines. This will be interpreted as comment text and is not executed at runtime.

\


## Code Block

A code block contains the actual coding in the HSL files. The following can be seen here:

* Variable declaration and calculation
* Conditional processing (loops and if, else statements)
* Function calls
* A Variety of other things

Code blocks always begin and end with curly brackets { … }.



## Keywords

Keywords are reserved words that perform specific actions in HSL such as declaring variables and functions. It is forbidden to name anything else with the same name as the keyword, e.g. it is not possible to name a variable ‘abort’ within HSL.

A list of keywords is shown in the table below:

| Keywords |           |              |
| -------- | --------- | ------------ |
| abort    | function  | pragma       |
| break    | global    | private      |
| char     | goto      | quit         |
| const    | if        | return       |
| device   | ifdef     | resume       |
| debug    | ifndef    | sequence     |
| define   | include   | short        |
| dialog   | lock      | static       |
| echo     | long      | struct       |
| else     | loop      | string       |
| endif    | method    | synchronized |
| error    | namespace | timer        |
| exit     | next      | unlock       |
| event    | object    | variable     |
| file     | once      | void         |
| float    | onerror   | while        |
| for      | pause     |   filename   |

\


## Operators

Operators represent logical operations such as addition and subtraction. Operators can be used in variable calculations or in conditional processing (if, else statements) to compare data and make decisions. HSL has a full range of operators, including arithmetic, logical, bit-wise, and assignment operators. Listed below are the different operators.

| Symbol      | Operator                 | Associativity | Symbol | Operator             | Associativity |
| ----------- | ------------------------ | ------------- | ------ | -------------------- | ------------- |
| ‖           | logical OR               | Left          | %      | remainder            | Left          |
| &&          | logical AND              | Left          | +      | add                  | Left          |
| <p><br></p> | <p><br></p>              | <p><br></p>   | -      | subtract             | Left          |
| \|          | bitwise OR               | Left          | \*     | multiply             | Left          |
| &           | bitwise AND              | Left          | /      | divide               | Left          |
| <           | less than                | Left          | !      | not                  | Right         |
| <=          | less than or equal to    | Left          | ^      | power                | Right         |
| ==          | Equal                    | Left          | -      | unary minus operator | Right         |
| !=          | not equal                | Left          | ++     | increment            | Left          |
| >=          | greater than or equal to | Left          | --     | decrement            | Left          |
| >           | greater than             | Left          | =      | assignment           | Right         |

\


## Variables and Objects

Variables are the basic components of a source code. They are used to store/represent information. A variable can be named according to preferences, except for a predefined HSL keyword or a function. It is possible to perform calculations with variables just like in the graphical Method Editor.

There are different types of variables. The most common one only holds a value, e.g. a pipetting volume. But since variables are objects, these objects could also store other information more than just a value. A variable can also hold a sequence, a file, etc.

\


### Variable Declaration

To declare a variable, use this code:

* Variable myVariable;

This will create a new variable named myVariable, and assigns zero (0) as the default value to it. To initialize a variable with a specific value, use the following syntax:

* Variable myVariable(5); // Now, the variable holds the integer value 5
* Variable myVariable(“Hello”); // this variable holds the string value Hello
* Variable myVariable(hslTrue); // boolean declaration – true or false

Variables always need to be declared before being used at the start of the code block. They cannot be declared in the middle of the code.



### Variable Scope

As stated previously, variables need to be declared at the beginning of a code block. These variables are local to that code block. In other words, they only exist in that section of code. There are a few other options however:

* _Global variables_ are declared at the beginning of a source file with the keyword ‘global’. These variables can be used all throughout the code – even in a different library or namespace.
* _Static variables_ are similar to a global variable but are global only to that certain library/namespace. They are declared using the keyword ‘static’.

All other variables are local to the code block in which they are declared.

\


### Array Declaration

Arrays are used to access a list of objects through the array name and the array index. An array can be of any sort of object (e.g. array of variables, array of files, array of sequences, etc…).

To declare an array:

1. Start by using the keyword of the type of the array (i.e. variable, file, sequence, etc…)
2. Specify a name to it, just like a variable.
3. Add a set of square brackets, \[ ] right after the name.
4. An empty set of brackets creates an empty, undeclared length array.
5. If a number is enclosed in brackets, \[5] it sets the size of the array.
6. Unlike in the graphical Method Editor, arrays in HSL are zero based, not one based.

A few examples:

* Variable ArrayOfVariables\[ ]; // an empty array
* Variable ArrayOfVariables\[100]; // an array with 100 elements
* Sequence ArrayOfSequences\[ ]; // an empty array of sequences



### If / Else Statements

HSL has the ability to compare things and make decisions. This is done with ‘If, Else’ statements. These are used in the exact same manner as they are in the graphical Method Editor, which should already be familiar.

They can be nested within each other to check multiple conditions.

They are more powerful than they are in the graphical Method Editor since multiple conditions at the same time can be checked. This eliminates the need for multiple nested ‘If, Else’ statements.

‘If’ and ‘If, Else’ statements will look like shown below.

```
If(var1 == 2)
var2 = 5;
Else
var2 = 10;
```

This example starts a new code block for multiple instructions&#x20;

```
If(var1 == 2)
{
var2 = 5;
var3 = 10;
}
```



Checking multiple conditions can also be as follows&#x20;

```
If(var1 == 5 && var2 == 10)
{
DoSomething();
}
Else
{
DoSomethingElse();
}
```

The above checks if both expressions are true. It is also possible to check other conditions such as ‘Or’ expressions. See the HSL Operators to know which operators can be used.

\


## Loops

Just like in the graphical Method Editor, loops can be used in HSL to do certain things multiple times.

There are 2 types of loops in HSL:

* ‘for’ loops: These are used to do something a predetermined number of times.
* ‘while’ loops: These are used to do something while an expression is true.

The expression is similar to the ‘if, else’ statements.



There is also a ‘break’ command to break a loop when a certain condition is met.

_For loop_ statements look like this:&#x20;

```
for(i = 0; i <= 100; i++)
{
/*…do something…*/
}

```

The ‘i’ here is a loop variable.

It is originally assigned a value. In this example it is declared with a 0 value.

The second section of the _for_ statement instructs the loop to keep going until i is greater than 100. The last part of the statement increments the loop variable by 1 every time the loop is executed.

_While loops_ look like this:&#x20;

```
while(myVar < 2000)
{
/*…do something…*/
}
```

The expression in the while loop is just like the expressions that are used in ‘If, Else’ statements. Usually the code block of the loop performs some action to change the result of the expression.

\


## Functions



Functions are pieces of code that perform repetitive tasks. Functions are analogous to sub- methods in graphical Method Editor files. Functions can (but don’t have to) accept variables and other objects as inputs. Similarly, functions can return a value of some sort (variable, sequence, file, etc.).

A function call looks like the following:

_myFunction(); // This function does not return anything var1 = myFunction(); // this function returns a variable_

_var1 = myFunction(5); // this function returns a variable and has a variable as an input_

\


### Function Declaration

A function declaration is just a statement allowing the compiler to know what functions are in existence. A function implementation is the actual code of the function. This tells the compiler how the function actually works.

The declaration and implementation can be done at the same time but is usually split into separate parts. The declaration can be seen in the header file (.hsl) while the implementation can be seen in the source file (.hs\_).

A function declaration looks like this:

```
function myFunction(variable var1) variable
```

The parts of the declaration are as follows:

* _function_: This tells the compiler that this is a function.
* _myFunction_: This is the name of the function (however wanted).
* _variable_: This first one is telling the compiler that ‘myFunction’ takes in one variable called ‘var1’. There can be multiple type declarations here!
* _variable_: The second variable declaration is telling the compiler and the programmer that this function returns a variable type object.

The variable declarations can be replaced with any type of object, e.g. sequence, file, etc….

A function does not have to return a variable. Some functions return other objects such as sequences or files while other functions can return nothing at all (this is marked by the keyword void). Sometimes an “&” can be seen after the word variable in the list of passed in variables/objects:

```
function myFunction(variable& var1) void
```

This ampersand is telling the compiler that the variable that is passed in is also passed out with a value that has potentially changed. This is called passing a variable by reference.

If there is no ampersand then the variable that is passed in is not changed by the function.

\


## Namespaces

A namespace is a way to protect the functions of the library/sourcecode. This is a way to distinguish where a function comes from. For instance, when using 2 libraries and they both contain a function called ‘Init’, the compiler would not be able to distinguish between the 2 and would produce an error. If a namespace is used for each library, the compiler gets information about the origin of the function.

Namespaces are declared using the ‘namespace’ keyword.

All the code belonging to the namespace has to be enclosed by opening and closing curly brackets.

\


### Using Libraries in HSL

Just like in the graphical Method Editor, other HSL libraries can be used in the code in order to access all of the functions that have already been created. Libraries are always included at the beginning of the source file. The preprocessor is used to include these files.

The preprocessor is a ‘macro’ that runs before the source code is compiled. This allows the compiler to get instructions on what is needed for the code to compile correctly.

\


### Preprocessor Syntax

Preprocessor commands are always prefixed with a ‘#’ sign.

These are usually seen at the beginning of an HSL file but also sometimes at the end. Typically in HSL 2 types of preprocessor commands can be seen:

_Include commands_. These are used to tell the compiler that some features from another HSL file (library) are used.

Include commands look like this:&#x20;

```
#include “HSLMthLib.hsl”
```

_Inclusion guards_. These are used to tell the compiler to check whether a particular library is already included through some other bit of source code. This is important because trying to include the same library more than once will cause an error.

Inclusion guards look like this:&#x20;

```
#ifndef   HSLMthLib_hsl  
#define   HSLMthLib_hsl  1
/* ….
…. hsl code which implements the MthLib
…. */ #endif
```



### HSL Runtime Inclusion Guard

In every library there is a special inclusion guard that looks like the following:

* _#ifndef HSL\_RUNTIME_
* _code here_
* _#endif_
* _#ifdef HSL\_RUNTIME_
* _code here_
* _#endif_

This is an inclusion guard that is checking to see if it is programming in VENUS or if the run engine is running. The library header will be presented in the ‘#ifndef’ section and the implementation will be presented in the ‘#ifdef’ section. It is located in these sections so that the actual commands are not compiled while programming in VENUS. This makes the editor tools faster.



### Add Bitmaps

Adding those little icons to the library commands (seen while programming in VENUS) is easy. First, draw or download a bitmap image. The dimensions need to be either 16 x 16 or 32 x 32 pixels. Save the bitmap image with the same name as the library in the library directory. VENUS will do the rest of the steps and automatically load the icon when the library is included.

To create a separate picture for a particular function, save the bitmap image with the library name and the function name separated with a period (_libraryname.functionname.bmp_).



### Add a Help File

Adding a help file for the library is just as easy as adding an icon. VENUS Help Files are CHM or HLP file structures. Only an appropriate editor is needed to create CHM or HLP files. A number of free editors can be found on the web.

Either create a file using an editor or write it in word and then use the CHM Editor to translate it. Save the help file with the same name as the library in the library folder just like bitmaps. It is highly recommended to create help files for a library. No one else will be able to support it otherwise.

\
