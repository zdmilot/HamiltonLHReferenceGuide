# The HSL Method Editor

_HSL or Hamilton Standard Language is the underlying programming language that the VENUS Software is operated from. HSL is a C/C++ style programming language. To use HSL, the HSL Method Editor must be started. It is a separate program that is located in “C:\Program Files\Hamilton\Bin\HxHslMetEd.exe” (depending on the language/installation settings)._

_The editor is an acclaimed and outstanding text editor. An hsl file can be written using a text editor however the checksum lines have to be checked personally._

\\

![image](../.gitbook/manual-images/assets/Image\_1722.gif)

\\

_Before an HSL file is run, it has to be compiled (translated) into a basic computer language. This is done by the “MICROLAB STAR Run” Program, which should already be familiar._

![image](../.gitbook/manual-images/assets/Image\_1723.png)

\\

_behind is...._

_Unlike a C/C++ program, the file is compiled just before it is run. This is done every time it is run. The Hamilton Method Editor is actually a code generator that creates an HSL code simultaneously. The Run Engine (compiler) runs the HSL file, not the ‘.med’ file._

\\

![image](../.gitbook/manual-images/assets/Image\_1724.jpg)

\\

.med _.hsl_

1.  #### _‌HSL File Types‌_

    \\

    _HSL is usually used to create libraries. There are actually 2 HSL file types that may be encountered:_

    _Files with a file extension of “.hsl” are known as header files while files with an extension of “.hs\_” are known as Source Files or Implementation Files._

    _Typically header files will contain only declarations of functions and variables while source files contain the actual code that is in the function (known as the function implementation)._

    _There are three main reasons to split into header and source files:_

    1. _It allows another person to look only at the header file and know what the functions do. It is not necessary to analyze they work._
    2. _Sometimes there is a need to create additional functions, for the functions in the header to work but, may not want others to see them. Anything declared in the implementation file is not visible when the declaration file is included._
    3. _It enhances the speed of the VENUS Method Editor._

    \\
2.  #### _‌HSL Syntax‌_

    \\

    _Most lines of code must end with a semicolon (;). Generally a new line is started after a semicolon. But this does not need to be done (just makes the code easier to read)._

    _The space between lines is known as whitespace and has no function._

    _Use of a double forward slash (//) indicates that the following characters in this line are comments only. A forward slash followed by a star (/_) together with the star followed by a forward slash (_/) indicates a comment block which can be separated over multiple lines. This will be interpreted as comment text and is not executed at runtime._

    \\
3.  #### _‌Code Block‌_

    \\

    _A code block contains the actual coding in the HSL files. The following can be seen here:_

    * _Variable declaration and calculation_
    * _Conditional processing (loops and if, else statements)_
    * _Function calls_
    * _A Variety of other things_

    _Code blocks always begin and end with curly brackets { … }._
4.  #### _‌Keywords‌_

    \\

    _Keywords are reserved words that perform specific actions in HSL such as declaring variables and functions. It is forbidden to name anything else with the same name as the keyword, e.g. it is not possible to name a variable ‘abort’ within HSL._

    _A list of keywords is shown in the table below:_

    \\

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
    | for      | pause     | filename     |

    \\
5.  #### _‌Operators‌_

    \\

    _Operators represent logical operations such as addition and subtraction. Operators can be used in variable calculations or in conditional processing (if, else statements) to compare data and make decisions. HSL has a full range of operators, including arithmetic, logical, bit-wise, and assignment operators. Listed below are the different operators._

    | Symbol      | Operator                 | Associativity | <p><br></p> | Symbol               | Operator | Associativity |
    | ----------- | ------------------------ | ------------- | ----------- | -------------------- | -------- | ------------- |
    | ‖           | logical OR               | Left          | %           | remainder            | Left     |               |
    | &&          | logical AND              | Left          | +           | add                  | Left     |               |
    | <p><br></p> | <p><br></p>              | <p><br></p>   | -           | subtract             | Left     |               |
    | \|          | bitwise OR               | Left          |             | multiply             | Left     |               |
    | &           | bitwise AND              | Left          | /           | divide               | Left     |               |
    | <           | less than                | Left          | !           | not                  | Right    |               |
    | <=          | less than or equal to    | Left          | ^           | power                | Right    |               |
    | ==          | Equal                    | Left          | -           | unary minus operator | Right    |               |
    | !=          | not equal                | Left          | ++          | increment            | Left     |               |
    | >=          | greater than or equal to | Left          | --          | decrement            | Left     |               |
    | >           | greater than             | Left          | =           | assignment           | Right    |               |

    \\
6.  #### _‌Variables and Objects‌_

    \\

    _Variables are the basic components of a source code. They are used to store/represent information. A variable can be named according to preferences, except for a predefined HSL keyword or a function. It is possible to perform calculations with variables just like in the graphical Method Editor._

    _There are different types of variables. The most common one only holds a value, e.g. a pipetting volume. But since variables are objects, these objects could also store other information more than just a value. A variable can also hold a sequence, a file, etc._

    \\

    1.  _**‌Variable Declaration‌**_

        \\

        _To declare a variable, use this code:_

        *   _Variable myVariable;_

            _This will create a new variable named myVariable, and assigns zero (0) as the default value to it. To initialize a variable with a specific value, use the following syntax:_
        * _Variable myVariable(5); // Now, the variable holds the integer value 5_
        * _Variable myVariable(“Hello”); // this variable holds the string value Hello_
        * _Variable myVariable(hslTrue); // boolean declaration – true or false_

        _Variables always need to be declared before being used at the start of the code block. They cannot be declared in the middle of the code._
    2.  _**‌Variable Scope‌**_

        \\

        _As stated previously, variables need to be declared at the beginning of a code block. These variables are local to that code block. In other words, they only exist in that section of code. There are a few other options however:_

        * _Global variables are declared at the beginning of a source file with the keyword ‘global’. These variables can be used all throughout the code – even in a different library or namespace._
        * _Static variables are similar to a global variable but are global only to that certain library/namespace. They are declared using the keyword ‘static’._

        _All other variables are local to the code block in which they are declared._

        \\
    3.  _**‌Array Declaration‌**_

        \\

        _Arrays are used to access a list of objects through the array name and the array index. An array can be of any sort of object (e.g. array of variables, array of files, array of sequences, etc…)._

        _To declare an array:_

        1. _Start by using the keyword of the type of the array (i.e. variable, file, sequence, etc…)_
        2. _Specify a name to it, just like a variable._
        3. _Add a set of square brackets, \[ ] right after the name._
        4. _An empty set of brackets creates an empty, undeclared length array._
        5. _If a number is enclosed in brackets, \[5] it sets the size of the array._
        6.  _Unlike in the graphical Method Editor, arrays in HSL are zero based, not one based._

            _A few examples:_

            * _Variable ArrayOfVariables\[ ]; // an empty array_
            * _Variable ArrayOfVariables\[100]; // an array with 100 elements_
            * _Sequence ArrayOfSequences\[ ]; // an empty array of sequences_

        \\
    4.  _**‌If / Else Statements‌**_

        \\

        _HSL has the ability to compare things and make decisions. This is done with ‘If, Else’ statements. These are used in the exact same manner as they are in the graphical Method Editor, which should already be familiar._

        _They can be nested within each other to check multiple conditions._

        _They are more powerful than they are in the graphical Method Editor since multiple conditions at the same time can be checked. This eliminates the need for multiple nested ‘If, Else’ statements._

        _‘If’ and ‘If, Else’ statements will look like shown below._

        _If(var1 == 2)_

        _var2 = 5;_

        _Else_

        _var2 = 10;_

        _This example starts a new code block for multiple instructions If(var1 == 2)_

        _{_

        _var2 = 5;_

        _var3 = 10;_

        _}_

        \\

        _Checking multiple conditions can also be as follows If(var1 == 5 && var2 == 10)_

        _{_

        _DoSomething();_

        _}_

        _Else_

        _{_

        _DoSomethingElse();_

        _}_

        _The above checks if both expressions are true. It is also possible to check other conditions such as ‘Or’ expressions. See the HSL Operators to know which operators can be used._

        \\
7.  #### _‌Loops‌_

    \\

    _Just like in the graphical Method Editor, loops can be used in HSL to do certain things multiple times._

    _There are 2 types of loops in HSL:_

    _‘for’ loops: These are used to do something a predetermined number of times._

    _‘while’ loops: These are used to do something while an expression is true._

    _The expression is similar to the ‘if, else’ statements._

    \\

    _There is also a ‘break’ command to break a loop when a certain condition is met._

    _For loop statements look like this: for(i = 0; i <= 100; i++)_

    _{_

    _/…do something…/_

    _}_

    _The ‘i’ here is a loop variable._

    _It is originally assigned a value. In this example it is declared with a 0 value._

    _The second section of the for statement instructs the loop to keep going until i is greater than 100. The last part of the statement increments the loop variable by 1 every time the loop is executed._

    _While loops look like this: while(myVar < 2000)_

    _{_

    _/…do something…/_

    _}_

    \\

    _The expression in the while loop is just like the expressions that are used in ‘If, Else’ statements. Usually the code block of the loop performs some action to change the result of the expression._

    \\
8.  #### _‌Functions‌_

    \\

    _Functions are pieces of code that perform repetitive tasks. Functions are analogous to sub- methods in graphical Method Editor files. Functions can (but don’t have to) accept variables and other objects as inputs. Similarly, functions can return a value of some sort (variable, sequence, file, etc.)._

    _A function call looks like the following:_

    _myFunction(); // This function does not return anything var1 = myFunction(); // this function returns a variable_

    _var1 = myFunction(5); // this function returns a variable and has a variable as an input_

    \\

    1.  _**‌Function Declaration‌**_

        \\

        _A function declaration is just a statement allowing the compiler to know what functions are in existence. A function implementation is the actual code of the function. This tells the compiler how the function actually works._

        _The declaration and implementation can be done at the same time but is usually split into separate parts. The declaration can be seen in the header file (.hsl) while the implementation can be seen in the source file (.hs\_)._

        \\

        _A function declaration looks like this:_

        _function myFunction(variable var1) variable_

        \\

        _The parts of the declaration are as follows:_

        _function: This tells the compiler that this is a function._

        _myFunction: This is the name of the function (however wanted)._

        _variable: This first one is telling the compiler that ‘myFunction’ takes in one variable called ‘var1’. There can be multiple type declarations here!_

        _variable: The second variable declaration is telling the compiler and the programmer that this function returns a variable type object._

        _The variable declarations can be replaced with any type of object, e.g. sequence, file, etc…._

        _A function does not have to return a variable. Some functions return other objects such as sequences or files while other functions can return nothing at all (this is marked by the keyword void). Sometimes an “&” can be seen after the word variable in the list of passed in variables/objects:_

        _function myFunction(variable& var1) void_

        _This ampersand is telling the compiler that the variable that is passed in is also passed out with a value that has potentially changed. This is called passing a variable by reference._

        _If there is no ampersand then the variable that is passed in is not changed by the function._

        \\
9.  #### _‌Namespaces‌_

    \\

    _A namespace is a way to protect the functions of the library/sourcecode. This is a way to distinguish where a function comes from. For instance, when using 2 libraries and they both contain a function called ‘Init’, the compiler would not be able to distinguish between the 2 and would produce an error. If a namespace is used for each library, the compiler gets information about the origin of the function._

    _Namespaces are declared using the ‘namespace’ keyword._

    _All the code belonging to the namespace has to be enclosed by opening and closing curly brackets._

    \\
10. #### _‌Using Libraries in HSL‌_

    \\

    _Just like in the graphical Method Editor, other HSL libraries can be used in the code in order to access all of the functions that have already been created. Libraries are always included at the beginning of the source file. The preprocessor is used to include these files._

    _The preprocessor is a ‘macro’ that runs before the source code is compiled. This allows the compiler to get instructions on what is needed for the code to compile correctly._

    \\

    1.  _**‌Preprocessor Syntax‌**_

        \\

        _Preprocessor commands are always prefixed with a ‘#’ sign._

        _These are usually seen at the beginning of an HSL file but also sometimes at the end. Typically in HSL 2 types of preprocessor commands can be seen:_

        _Include commands. These are used to tell the compiler that some features from another HSL file (library) are used._

        _Include commands look like this: #include “HSLMthLib.hsl”_

        _Inclusion guards. These are used to tell the compiler to check whether a particular library is already included through some other bit of source code. This is important because trying to include the same library more than once will cause an error._

        _Inclusion guards look like this: #ifndef HSLMthLib\_hsl_

        _#define HSLMthLib\_hsl 1_

        _/\* …._

        _…. hsl code which implements the MthLib_

        _…. / #endif_
    2.  _**‌HSL Runtime Inclusion Guard‌**_

        \\

        _In every library there is a special inclusion guard that looks like the following:_

        * _#ifndef HSL\_RUNTIME_
        * _code here_
        * _#endif_
        * _#ifdef HSL\_RUNTIME_
        * _code here_
        * _#endif_

        _This is an inclusion guard that is checking to see if it is programming in VENUS or if the run engine is running. The library header will be presented in the ‘#ifndef’ section and the implementation will be presented in the ‘#ifdef’ section. It is located in these sections so that the actual commands are not compiled while programming in VENUS. This makes the editor tools faster._

        \\
    3.  _**‌Add Bitmaps‌**_

        \\

        _Adding those little icons to the library commands (seen while programming in VENUS) is easy. First, draw or download a bitmap image. The dimensions need to be either 16 x 16 or 32 x 32 pixels. Save the bitmap image with the same name as the library in the library directory. VENUS will do the rest of the steps and automatically load the icon when the library is included._

        _To create a separate picture for a particular function, save the bitmap image with the library name and the function name separated with a period (libraryname.functionname.bmp)._

        \\
11. #### _‌Add a Help File‌_

    \\

    _Adding a help file for the library is just as easy as adding an icon. VENUS Help Files are CHM or HLP file structures. Only an appropriate editor is needed to create CHM or HLP files. A number of free editors can be found on the web._

    _Either create a file using an editor or write it in word and then use the CHM Editor to translate it. Save the help file with the same name as the library in the library folder just like bitmaps. It is highly recommended to create help files for a library. No one else will be able to support it otherwise._
12. #### _‌VENUS Help Function‌_

    \\

    _To get more information about the HSL Editor, refer to the VENUS Help Function:_

    \\

    ![image](../.gitbook/manual-images/assets/Image\_1725.jpg)

    _It is located in the “Help Menu  Help Topics” and provides fundamental information in three categories:_

    * _HSL Method overview / Keyboard shortcuts / Modifying a method_
    * _All available menu options (File, Edit, View, Insert, Tools, Window, Help)_
    * _An HSL reference guide to cover all aspects of HSL programming_
