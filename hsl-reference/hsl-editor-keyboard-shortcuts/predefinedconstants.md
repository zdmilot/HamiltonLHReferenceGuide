# Predefinedconstants

## Predefined constants

## Predefined Constants

&#x20;

Since the following constants are built into HSL, i.e. it is not necessary to explicitly define them before use. These constants can be used anywhere in the code to represent the values shown.

&#x20;

| **Name**            | **Value**  | **Meaning**                                                                                                                                       |
| ------------------- | ---------- | ------------------------------------------------------------------------------------------------------------------------------------------------- |
| hslTrue             | 1          | True                                                                                                                                              |
| hslFalse            | 0          | False                                                                                                                                             |
| hslInfinite         |            | Infinite time-out value.                                                                                                                          |
| hslOKOnly           | 0          | Display OK button only.                                                                                                                           |
| hslOKCancel         | 1          | Display OK and Cancel button.                                                                                                                     |
| hslAbortRetryIgnore | 2          | Display Abort, Retry and Ignore button.                                                                                                           |
| hslYesNoCancel      | 3          | Display Yes, No and Cancel button.                                                                                                                |
| hslYesNo            | 4          | Display Yes and No button.                                                                                                                        |
| hslRetryCancel      | 5          | Display Retry and Cancel button.                                                                                                                  |
| hslDefButton1       | 0          | The first button is the default button. hslDefButton1 is the default unless hslDefButton2, or hslDefButton3 is specified.                         |
| hslDefButton2       | 256        | The second button is the default button.                                                                                                          |
| hslDefButton3       | 512        | The third button is the default button.                                                                                                           |
| hslError            | 16         | Display Error Message icon.                                                                                                                       |
| hslQuestion         | 32         | Display Warning Query icon.                                                                                                                       |
| hslExclamation      | 48         | Display Warning Message icon.                                                                                                                     |
| hslInformation      | 64         | Display Information Message icon.                                                                                                                 |
| hslOK               | 1          | OK button was selected.                                                                                                                           |
| hslCancel           | 2          | Cancel button was selected.                                                                                                                       |
| hslAbort            | 3          | Abort button was selected.                                                                                                                        |
| hslRetry            | 4          | Retry button was selected.                                                                                                                        |
| hslIgnore           | 5          | Ignore button was selected.                                                                                                                       |
| hslYes              | 6          | Yes button was selected.                                                                                                                          |
| hslNo               | 7          | No button was selected.                                                                                                                           |
| hslInteger          | "i"        | The input value is an integer.                                                                                                                    |
| hslFloat            | "f"        | The input value is a float.                                                                                                                       |
| hslString           | "s"        | The input value is a string.                                                                                                                      |
| hslRead             | "r"        | Opens the file for reading. The file must exist.                                                                                                  |
| hslWrite            | "w"        | Opens an empty file for writing. If the file already exists, its contents is deleted.                                                             |
| hslAppend           | "a"        | Opens the file for writing at the end of the file. If the file does not exist, a new file is created.                                             |
| hslHide             | 1          | Hides the window and activates another window.                                                                                                    |
| hslShow             | 2          | Activates the window and displays it in its current size and position.                                                                            |
| hslShowMaximized    | 3          | Activates the window and displays it as a maximized window.                                                                                       |
| hslShowMinimized    | 4          | Activates the window and displays it as a minimized window.                                                                                       |
| hslSynchronous      | 1          | The execution of the running HSL program will be blocked until the program to execute terminates.                                                 |
| hslAsynchronous     | 2          | The execution of the running HSL program will not be blocked until the program to execute terminates.                                             |
| hslCSVDelimited     | ","        | Fields in the file data source are delimited by commas (default).                                                                                 |
| hslTabDelimited     | "\t"       | Fields in the file data source are delimited by tabs.                                                                                             |
| hslFixedLength      | ""         | Fields in the text file are of a fixed width.                                                                                                     |
|                     | "\*"       | Fields in the file data source are delimited by asterisks. The asterisk can be substituted by any character except the double (") quotation mark. |
| hslAsciiText        | "\n"       | Fields in the file data source are delimited by newline characters.                                                                               |
| hslCurrent          | 0          | Starts at the current row (default).                                                                                                              |
| hslFirst            | 1          | Starts at the first row.                                                                                                                          |
| hslLast             | 2          | Starts at the last row.                                                                                                                           |
| HSL\_RUNTIME        |            | Parser constant, always defined at run-time, but not at edit-time (see remark below).                                                             |

&#x20;

#### Remarks

The Parser constant HSL\_RUNTIME will always be defined at run-time, but not at edit-time, i.e the parsing at edit-time can be sped up by using the predefined constant HSL\_RUNTIME as follows:

&#x20;

Split the HSL library into two files. The first file defines the library functions with an empty implementation. The second file, which is included by the first file, provides the real implementation of all functions defined in the first file. The implementation being used at edit-time and at run-time, respectively, is controlled by the predefined constant HSL\_RUNTIME.

&#x20;

#### Example

&#x20;

\#ifndef \_\_HSLMthLib\_hsl\_\_

\#define \_\_HSLMthLib\_hsl\_\_ 1

&#x20;

// #define MTH\_DEVELOP 1

&#x20;

\#ifdef MTH\_DEVELOP

\#ifndef HSL\_RUNTIME

\#define HSL\_RUNTIME 1

\#endif

\#endif

&#x20;

// Interface to Math functions

\#ifndef HSL\_RUNTIME

function MthMin(variable number1, variable number2)  {}

function MthMax(variable number1, variable number2)  {}

function MthRound(variable number, variable numDecimalPlaces) {}

function MthSin(variable number)  {}

function MthCos(variable number)  {}

function MthTan(variable number)  {}

// ...

\#endif

&#x20;

// Implementation of Math functions

\#ifdef HSL\_RUNTIME

\#include "HSLMthLibImpl.hsl"

\#endif

&#x20;

\#endif

***

_Created with the Personal Edition of HelpNDoc:_ [_Produce online help for Qt applications_](https://www.helpndoc.com/feature-tour/create-help-files-for-the-qt-help-framework)
