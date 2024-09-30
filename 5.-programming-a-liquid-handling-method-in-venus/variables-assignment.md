# Variables Assignment

## &#x20;Assignment

This command specifies a variable and assigns a value to it.

### Variable

Defines the variable to which the entered value shall be assigned.

**Format:**

* New variable name
  *   A valid variable name is a sequence of letters, digits or the special character '\_' (underscore).

      **Additional rules:**

      * First character has to be a letter.
      * Variable names are case-sensitive.
      * Variable names are restricted to the length of 255 characters.
      * Variable names must be unique.
      * HSL keywords cannot be used as variable names.

      **Examples:**

      * MyVarable1
      * my\_variable\_2
      * barcodesFile
      * incubationTimer
* New array element reference
  *   An array element reference is composed of an array name followed by a '\[' (an open bracket) followed by an index which is either a positive integer or a variable name followed by a ']' (a close bracket).

      &#x20;

      The array name is composed with the same rules as a variable name.

      **Additional rules:**

      * The index is one-based (array index 1 refers to the first array element)!
      * It is not possible to use another array element as array index.

      **Examples:**

      The following array element reference references the seventh element in the array anArray:

      * anArray\[7]

      The following array element reference references the element at the position denoted by the value of the variable index in the array myArray:

      * myArray\[index]

      &#x20;
* Entry from the given list

### Value

Defines the value to be assigned.

**Format:**

* Signed number
* String constant
  *   A valid string constant is a sequence of ASCII characters, enclosed by two quotation marks (").

      Note that control characters with ASCII code below 32 are NOT allowed (e.g. a carriage return with ASCII code 13)!

      **Special Characters**

      Some special characters are provided that allow the inclusion of characters which cannot be directly typed into strings. Each of these characters begins with a backslash. The backslash is an escape character used to indicate that the next character is special.

      &#x20;

      | Escape Sequence | Description           |
      | --------------- | --------------------- |
      | \n              | Line feed (newline)   |
      | \t              | Horizontal tab        |
      | \\'             | Single quotation mark |
      | \\"             | Double quotation mark |
      | \\\\            | Backslash             |

      &#x20;

      Notice that since the backslash itself is used as the escape character, it should not be used directly within a string. For any backslash to be included in a string, two of them together (\\\\) must be typed.

      **Examples:**

      * "" (empty string)
      * "Hello world"
      * "On/Off"
      * "BC73295xx734ABC"
      * "This is a text with more than 10 words and \n it could have still more words if you want\n\n..."
* Entry from the given list
* New variable name
  *   A valid variable name is a sequence of letters, digits or the special character '\_' (underscore).

      **Additional rules:**

      * First character has to be a letter.
      * Variable names are case-sensitive.
      * Variable names are restricted to the length of 255 characters.
      * Variable names must be unique.
      * HSL keywords cannot be used as variable names.

      **Examples:**

      * MyVarable1
      * my\_variable\_2
      * barcodesFile
      * incubationTimer
* New array element reference
  *   An array element reference is composed of an array name followed by a '\[' (an open bracket) followed by an index which is either a positive integer or a variable name followed by a ']' (a close bracket).

      &#x20;

      The array name is composed with the same rules as a variable name.

      **Additional rules:**

      * The index is one-based (array index 1 refers to the first array element)!
      * It is not possible to use another array element as array index.

      **Examples:**

      The following array element reference references the seventh element in the array anArray:

      * anArray\[7]

      The following array element reference references the element at the position denoted by the value of the variable index in the array myArray:

      * myArray\[index]

**Translatable String**

Values of type constant string may be defined as translatable string.

Such translatable strings may be translated into different languages by using the Translation Support System provided by the Hamilton Company.

The Translation Support System allows to translate string values (out of Workflows, Methods or Submethod-Libraries) that are displayed during execution time without changing the method.

If you have entered a string constant the option Translatable String is available
