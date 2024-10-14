---
icon: dev
---

# Whileloop

## While loop

## Statements

&#x20;

The following statements exist: the simple, the compound, the jump, the control statement and the error handler. Statements are executed sequentially.

&#x20;

statement :

simple\_statement ';'

compound\_statement

flow\_control\_statement ';'

control\_statement ';'

error\_handler

&#x20;

#### Simple Statement

A simple statement is an assignment or the calculation of an expression.

&#x20;

simple\_statement :

assignment\_expression

sequence\_expression

string\_expression

device\_expression

resource\_expression

dialog\_expression

object\_expression

array\_expression

timer\_expression

event\_expression

file\_expression

expression

&#x20;

Assignment:

As assignment statement, only the simple assignment operator = is supported.

&#x20;

assignment\_expression :

id '=' simple\_statement

dmemid '=' simple\_statement

&#x20;

The left operand must always be an l-value. It must not be a vector, not a structure and not a function. Either both operands must be of the integer or floating point types or both operands are string types. The type of the result of the assignment is that of the left operand and the value is that, which is after the assignment in the left operand.

&#x20;

Examples:

&#x20;

v1 = 1

v2 = v1

v3 = v1 == v2

v4 = Sin(v1 + v2)

arr\[v1] = (v1 + v2)^2

point.x = point.y = v1

&#x20;

String expressions:

As string expressions, only the simple assignment and the concatenation are supported.

&#x20;

string\_expression :

stringid '=' string\_expression

stringid '=' function\_reference '+' string\_expression

stringid '=' cstring '+' string\_expression

stringid '=' id '+' string\_expression

stringid '=' function\_reference

stringid '=' cstring

stringid '=' id

stringid '+' string\_expression

stringid '+' function\_reference

stringid '+' cstring

stringid '+' id

stringid

&#x20;

Both operands of the operators = and + must always be of string types. The type of the result of the assignment and the concatenation is that of the left operand and the value is that, which is after the assignment or the concatenation in the left operand.

&#x20;

Sequence expressions:

As sequence expressions, the simple assignment, the increment and the decrement operator are supported.

&#x20;

sequence\_expression :

sequenceid '=' sequence\_expression

sequenceid '=' function\_reference

sequenceid '++'

sequenceid '--'

sequenceid

&#x20;

Both operands of the assignment operator must always be of the sequence type. The type of the result of the assignment is that of the left operand and the value is that, which is after the assignment in the left operand.

The operand of the ++ operator must always be of the type sequence. The ++ operator increments the current position of the calling object by (used - current + 1) positions in iteration order (see element functions).

The operand of the -- operator must always be of the type sequence. The -- operator decrements the current position of the calling object by (used - current + 1) positions in iteration order (see element functions).

&#x20;

Device expressions:

As device expressions, only names are supported.

&#x20;

device\_expression :

deviceid

&#x20;

Resource expressions:

As resource expressions, only names are supported.

&#x20;

resource\_expression :

resourceid

&#x20;

Dialog expressions:

As dialog expressions, only names are supported.

&#x20;

dialog\_expression :

dialogid

&#x20;

Object expressions:

HSL supports the following object expressions:

&#x20;

object\_expression :

objectid '=' object\_expression

objectid '=' function\_reference

objectid

objectid '.' id '=' expression

objectid '.' id '=' object\_expression

&#x20;

Array expressions:

As dynamic array expressions, the simple assignment operator = and the subscription operator \[ ] are supported.

&#x20;

array\_expression :

arrayid '=' arrayid

arrayid '=' function\_reference

arrayid '\[' expression ']' '=' simple\_statement

arrayid '\[' expression ']'

arrayid

&#x20;

Both operands of the assignment operator must always be of the type of a dynamic array. The type of the result of the assignment is that of the left operand and the value is that, which is after the assignment in the left operand.

An indexed reference to an element of a dynamic array is an expression followed by an expression in square brackets. The first expression must be a dynamic array and the second expression must have an integer type. A reference to an element of a dynamic array is an l-value.

&#x20;

Timer expressions:

As timer expressions, only names are supported.

&#x20;

timer\_expression :

timerid '=' timer\_expression

timerid

&#x20;

Event expressions:

As event expressions, only names are supported.

&#x20;

event\_expression :

eventid '=' event\_expression

eventid

&#x20;

File expressions:

As file expressions, only names are supported.

&#x20;

file\_expression :

fileid

&#x20;

Variable expressions:

See expressions.

&#x20;

#### Compound Statement

A compound statement is either a selection, an iteration or a block statement.

&#x20;

compound\_statement:

if\_statement

iteration\_statement

block

&#x20;

Selection statement:

Selection statements select one of several continuation possibilities in the program.\


if\_statement :

if '(' expression ')' statement

if '(' expression ')' statement else statement

&#x20;

The expression expression must be of the integer or floating point type. The expression expression is evaluated. If it is not equal to 0, the first sub-expression is executed. In production with else the second sub-expression is executed, if the expression evaluates to 0. The else ambiguity in nested if statements is resolved, by assigning the else to the last else-loose if.

&#x20;

Example:

&#x20;

if (v2 != 0)

v3 = v1 / v2;

else

Trace("Division by zero !");

&#x20;

Iteration statement:

Iteration statements specify loops. Loops can be nested or chained.

Two types of loops are distinguished:

* conditional loops (while and for)
* loops with counter (loop)

&#x20;

iteration\_statement :

while '(' expression ')' statement

loop '(' expression ')' statement

for '('opt\_init\_expression ';' opt\_expression ';' opt\_for\_expression ')' statement

&#x20;

opt\_init\_expression :

assignment\_expression

&#x20;

opt\_expression :

expression

&#x20;

opt\_for\_expression :

assignment\_expression

&#x20;

&#x20;

In the while loop, the sub-statement statement is repeatedly executed until the value of the expression expression is 0. The expression must be of the integer or a floating point type. The while loop is executed as follows:

1\. The expression expression is calculated.

2\. If expression is initially false (zero), the sub-statement statement is never executed and the control flow goes from the while loop to the next statement in the program. If expression is true (not zero), the sub-statement statement is executed before the program is continued with step 1.

In the loop statement, the sub-statement statement will be executed N times, whereby N is the initial value of the expression expression. The expression expression must be of the integer type. The loop statement is executed as follows:

1\. An (anonymous) loop counter is initialized to zero.

2\. The expression expression is calculated and assigned to an (anonymous) loop limiter.

3\. The expression loop counter < loop limiter is calculated.

4\. If the expression calculated in step 3 is initially false (zero), the sub-statement statement is never executed and the control flow goes from the loop statement to the next statement in the program. If the expression calculated in step 3 is true (not zero), first the sub-statement statement is executed, then the loop counter is incremented and finally the program is continued with step 3.

In the for loop, the sub-statement statement is repeated executed, until the value of the expression opt\_expression is 0 (if available). The expression opt\_expression must be of the integer or the floating point type. The for loop is executed as follows:

&#x20;

1\. The expression opt\_init\_expression is calculated (if available).

2\. The expression opt\_expression is calculated (if available). If the expression opt\_expression is missing, then its value is considered as true (not zero).

3\. If the expression opt\_expression is initially false (zero), the sub-statement statement is never executed and the control flow goes from the for loop to the next statement in the program. If the expression opt\_expression is true (not zero), first the sub-statement statement is executed, then the expression opt\_for\_expression is calculated and finally the program is continued with step 2.

&#x20;

An iteration statement is also terminated if the sub-statement statement contains one of the jump statements break, return or abort.

&#x20;

Examples:

&#x20;

\#define MAX 12

&#x20;

variable v;

v = 0;

while (v < MAX)

{

...

v++;

}

&#x20;

while (1)  /\* forever \*/

{

...

}

&#x20;

loop (12)

{

...

}

&#x20;

for (v = 0; v < MAX; v++)

{

...

}

&#x20;

for ( ; ; )  /\* forever \*/

{

...

}

&#x20;

Block Statement:

Blocks serve to combine several statements into a statement. The body of a function is a block.

&#x20;

block :

'{' opt\_control\_line opt\_locals opt\_statement\_list '}'

&#x20;

opt\_control\_line :

opt\_control\_line control\_line

&#x20;

opt\_locals :

locals

&#x20;

locals :

locals type variable\_list ';'

locals declaration ';'

locals control\_line

type variable\_list ';'

declaration ';'

&#x20;

declaration:

structure

array

function\_declaration

&#x20;

variable\_list :

variable\_list ',' typeid opt\_initializer

typeid opt\_initializer

&#x20;

opt\_statement\_list :

statements

&#x20;

statements :

statements statement

statements control\_line

statement

&#x20;

Example:

&#x20;

{

variable v;

v = 1;

//...

}

&#x20;

#### Jump Statement

Jump statements result in non-conditional program execution.

&#x20;

flow\_control\_statement :

break

return

return '(' simple\_statement ')'

abort

pause

onerror goto id

onerror goto '0'

onerror resume next

resume next

lock

unlock

&#x20;

Break Statement:

A break statement may only be within an iteration statement. The program is continued with the statement, which follows directly after the abandoned statement, if one is available.

&#x20;

Example:

&#x20;

\#define MAX 12

&#x20;

variable v;

v = 0;

while (1)

{

//...

if (MAX <= v)

break;

v = v + 1;

}

&#x20;

Return Statement:

The return statement consists of the symbol return, which possibly follows an expression in parentheses. It signals that the execution of a function is terminated. The expression specifies the value returned by a function. A function returns with a return statement to the calling context. The normal termination of a function is equivalent to a return statement.

&#x20;

Abort Statement:

Terminates the program abnormally, by controlled aborting the execution.

&#x20;

Pause Statement:

Suspends the program execution at the next position where the lock and unlock statements match exactly.

&#x20;

Onerror Statement:

The onerror statement syntax can have any of the following forms:

&#x20;

| **Statement**         | **Description**                                                                                                                                                                                                                                                                                                                                       |
| --------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| onerror goto id       | Enables the error handler that starts at the specified label. If a runtime error occurs, the control branches to the label, activating the error handler. The specified label must be in the same function or method as the onerror statement; otherwise, a syntax error occurs.                                                                      |
| onerror resume next   | Specifies that when a runtime error occurs, the control goes to the statement immediately following the statement where the error occurred where execution continues. The err object's properties are reset to zero or zero-length strings ("") after an onerror resume next statement. The err.Clear() function can be used to explicitly reset err. |
| onerror goto 0        | Disables any enabled error handler in the current function or method.                                                                                                                                                                                                                                                                                 |

&#x20;

Resume Statement:

The resume next statement syntax has the following form:

&#x20;

| **Statement** | **Description**                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| ------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| resume next   | Resumes execution after an error handler is finished. If the error occurred in the same function as the error handler, execution resumes with the statement immediately following the statement that caused the error. If the error occurred in a called function, execution resumes with the statement immediately following the statement that last called out of the function containing the error-handler (or onerror resume next statement). |

&#x20;

Lock and Unlock Statement:

lock and unlock are control-of-flow language keywords that enclose a series of HSL statements so that a group of HSL statements can be executed without interruption. lock ... unlock blocks can be nested.

&#x20;

Example:

&#x20;

lock;

onerror goto Unexpected;

ML\_STAR.Aspirate();

ML\_STAR.Dispense();

onerror goto 0;

unlock;

//...

&#x20;

Unexpected:

{

unlock;

//...

}

&#x20;

#### Control Statement

A control statement of the form

&#x20;

control\_statement :

'<<' cstring

'<<' stringid

&#x20;

activates the parser at runtime. The current input stream of the parser as well as the current interpreter data are stacked. The file with the name cstring becomes the new input stream of the parser. The character eof causes the parser to close the file with the name cstring and to continue the translation with the preceding input stream. The file name specified in cstring can be relative or absolute. The specified file will be searched in the following directories in the following sequence:

1\) in the current directory.

2\) in the directory that is listed under the registry key Methods.

3\) in the directory that is listed under the registry key Library.

4\) in the directories that are listed in the PATH environment variable.

In contrast to the control directive #include cstring, the control statement << cstring starts a new translation at run-time. Control statements can be nested.

&#x20;

Example:

&#x20;

method Main()

{

Trace("+Main()");

//...

<< "c:\\\vector\\\methods\\\utils.hsl";

//...

f1();

Trace("-Main()");

}

&#x20;

File: utils.hsl

&#x20;

function f1()

{

Trace("+f1()");

//...

Trace("-f1()");

}

&#x20;

#### Error Handler

To transfer program control on a runtime error directly to a given error handler, the error handler must be labeled. The appearance of an identifier label in the source program declares an error handler. Only an onerror goto statement can transfer control to an error handler.

&#x20;

error\_handler :

id ':' block

&#x20;

Example:

&#x20;

method Main()

{

variable v;

onerror goto UnhandledError;

//...

return;

&#x20;

UnhandledError :

{

//...

err.Clear();

abort;

}

}

&#x20;

***

_Created with the Personal Edition of HelpNDoc:_ [_Easy EBook and documentation generator_](https://www.helpndoc.com)
