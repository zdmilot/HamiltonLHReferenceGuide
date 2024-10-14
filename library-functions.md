# Library Functions

Library functions are pre-defined. Their names are reserved. Library functions are:

&#x20;

<table><thead><tr><th width="170">Function</th><th>Description</th></tr></thead><tbody><tr><td><p> </p><p>Sin(x)</p></td><td><p> </p><p>Sine of x</p><p>x in radian, integer or float</p><p> </p></td></tr><tr><td><p> </p><p>Cos(x)</p></td><td><p> </p><p>Cosine of x</p><p>x in radian, integer or float</p><p> </p></td></tr><tr><td><p> </p><p>Tan(x)</p></td><td><p> </p><p>Tangent of x</p><p>x in radian, integer or float</p><p> </p></td></tr><tr><td><p> </p><p>ASin(x)</p></td><td><p> </p><p>Arcsine of x in [-1, 1]</p><p>x integer or float</p><p>Undefined, if x not in [-1, 1]</p><p> </p></td></tr><tr><td><p> </p><p>ACos(x)</p></td><td><p> </p><p>Arccosine of x in [-1, 1]</p><p>x integer or float</p><p>Undefined, if x not in [-1, 1]</p><p> </p></td></tr><tr><td><p> </p><p>ATan(x)</p></td><td><p> </p><p>Arctangent of x</p><p>x integer or float</p><p> </p></td></tr><tr><td><p> </p><p>Exp(x)</p></td><td><p> </p><p>Exponential function ex</p><p>x integer or float</p><p> </p></td></tr><tr><td><p> </p><p>Log(x)</p></td><td><p> </p><p>Natural logarithm ln( x), x > 0</p><p>x integer or float</p><p>Undefined, if x &#x3C;= 0</p><p> </p></td></tr><tr><td><p> </p><p>Log10(x)</p></td><td><p> </p><p>Logarithm to the base 10 log10(x), x > 0</p><p>x integer or float</p><p>Undefined, if x &#x3C;= 0</p><p> </p></td></tr><tr><td><p> </p><p>Ceiling(x [,returnFloat])</p></td><td><p> </p><p>Returns the smallest integral value, not smaller than x.</p><p> </p><p><strong>Parameter</strong></p><p>x</p><p>[in] Floating-point or integer value.</p><p> </p><p>returnFloat</p><p>[in] If not zero, the function return value has type float (integer, optional, defaults to 0).</p><p> </p></td></tr><tr><td><p> </p><p>Floor(x [,returnFloat])</p></td><td><p> </p><p>Returns the largest integral value, not larger than x.</p><p> </p><p><strong>Parameter</strong></p><p>x</p><p>[in] Floating-point or integer value.</p><p> </p><p>returnFloat</p><p>[in] If not zero, the function return value has type float (integer, optional, defaults to 0).</p><p> </p></td></tr><tr><td><p> </p><p>IStr(inum)</p></td><td><p>Converts the integer inum into the corresponding character string.</p><p> </p><p><strong>Parameter</strong></p><p>inum</p><p>The integer to be converted.</p><p> </p><p><strong>Return</strong></p><p>The string representation of the integer inum.</p><p> </p></td></tr><tr><td><p> </p><p>FStr(</p><p>fnum</p><p>[,languageSpecific]</p><p>[,precision])</p></td><td><p> </p><p>Converts the floating point number fnum into the corresponding character string.</p><p> </p><p><strong>Parameter</strong></p><p>fnum</p><p>The float to be converted.</p><p> </p><p>languageSpecific</p><p>Specifies whether the decimal symbol in the Regional Settings should be used to write the string representation of the floating point number (integer, hslTrue or hslFalse).</p><p> </p><p>precision</p><p>An integer that indicates the number of significant digits or significant decimal digits to be used for floating-point display. Default precision is set to seven. The precision indicates the total number of significant digits.</p><p> </p><p><strong>Return</strong></p><p>The string representation of the float fnum.</p><p> </p></td></tr><tr><td><p> </p><p>IVal(istr)</p></td><td><p> </p><p>Converts the sequence of digits, contained in the character string istr, into the corresponding integer. The sequence of digits is interpreted decimal. If the sequence begins with 0x, it is interpreted hexadecimal.</p><p>Conversion aborts at the first character in istr, which is not a digit or not one of the characters + or -.</p><p> </p><p><strong>Parameter</strong></p><p>istr</p><p>The string to be converted.</p><p> </p><p><strong>Return</strong></p><p>The numeric value of the sequence of digits contained in the character string istr (integer). Null, if the character string can not be converted into a number. LONG_MAX (LONG_MIN) if the conversion results in an overflow.</p><p> </p></td></tr><tr><td><p> </p><p>FVal(fstr)</p></td><td><p> </p><p>Converts the sequence of digits, contained in the character string fstr, into the corresponding floating point number. Conversion aborts with the first character in fstr, which is not a digit or not one of the characters +, -, e, E.</p><p> </p><p><strong>Parameter</strong></p><p>fstr</p><p>The string to be converted.</p><p> </p><p><strong>Return</strong></p><p>The numeric value of the sequence of digits contained in the character string fstr (float). Null, if the character string cannot be converted into a number. DBL_MAX (DBL_MIN) if the conversion results in an overflow.</p><p> </p></td></tr><tr><td><p> </p><p>Trace([...])</p></td><td><p> </p><p>Trace function with variable argument list.</p><p> </p><p><strong>Parameter</strong></p><p>The values to be traced (integers, floats and strings).</p><p> </p></td></tr><tr><td><p> </p><p>FormatTrace(</p><p>source,</p><p>action,</p><p>status</p><p>[, ... ])</p></td><td><p> </p><p>Function with variable argument list to trace formated strings.</p><p> </p><p><strong>Parameter</strong></p><p>source</p><p>Source (string), e.g. System.</p><p> </p><p>action</p><p>Action (string), e.g. Pipette.</p><p> </p><p>status</p><p>Action status (integer). It may be one of the following predefined values:</p><p> </p><table data-header-hidden><thead><tr><th></th><th></th></tr></thead><tbody><tr><td>Value</td><td>Meaning</td></tr><tr><td>1</td><td>start</td></tr><tr><td>2</td><td>complete</td></tr><tr><td>3</td><td>error</td></tr><tr><td>4</td><td>progress</td></tr><tr><td>5</td><td>completeWithError</td></tr></tbody></table><p> </p><p>[...]</p><p>Variable argument list of the details to be traced (integers, floats and strings).</p><p> </p></td></tr><tr><td><p> </p><p>InputBox(</p><p>prompt,</p><p>title,</p><p>type</p><p>[,default]</p><p>[,timeout])</p></td><td><p> </p><p>Displays the input request prompt in a dialog box and returns with the value of the specified type entered by the user.</p><p> </p><p><strong>Parameter</strong></p><p>prompt</p><p>The input request prompt to be displayed (string).</p><p> </p><p>title</p><p>The title of the dialog box (string).</p><p> </p><p>type</p><p>The parameter type specifies the type of the value to be entered by the user as follows:</p><p> </p><table data-header-hidden><thead><tr><th></th><th></th><th></th></tr></thead><tbody><tr><td>Name</td><td>Value</td><td>Meaning</td></tr><tr><td>hslInteger </td><td>"i"</td><td>The input value is an integer</td></tr><tr><td>hslFloat </td><td>"f"</td><td>The input value is a float</td></tr><tr><td>hslString </td><td>"s"</td><td>The input value is a string</td></tr></tbody></table><p> </p><p>default</p><p>The default value (optional; integer, float or string).</p><p> </p><p>timeout</p><p>Specifies the amount of time to wait before the input dialog box will be automatically dismissed without any user intervention, provided that each field has a value (in seconds, non-negative floating-point number, optional). The default timeout value is hslInfinite.</p><p> </p><p><strong>Return</strong></p><p>If the user selected OK, the value of the appropriate type entered by the user, i.e. the function GetType returns hslInteger, hslFloat or hslString.</p><p>If the user selected Cancel, the value returned has no type, i.e. the function GetType returns the empty string.</p><p> </p></td></tr><tr><td><p> </p><p>MessageBox(</p><p>message,</p><p>title</p><p>[, type]</p><p>[,timeout])</p></td><td><p> </p><p>Displays a message in a message box and returns with a value, which identifies the button selected by the user.</p><p> </p><p><strong>Parameter</strong></p><p>message</p><p>The message to be displayed (string).</p><p> </p><p>title</p><p>The title of the message box (string).</p><p> </p><p>type</p><p>The optional type of the message box is a numeric expression that is the sum of the values specifying the number and type of the buttons to display and the icon style to use (integer).</p><p> </p><table data-header-hidden><thead><tr><th></th><th></th><th></th></tr></thead><tbody><tr><td>Name</td><td>Value</td><td>Meaning</td></tr><tr><td>hslOKOnly</td><td>0</td><td>Display OK button only (default)</td></tr><tr><td>hslOKCancel</td><td>1</td><td>Display OK and Cancel button</td></tr><tr><td>hslAbortRetryIgnore</td><td>2</td><td>Display Abort, Retry and Ignore button</td></tr><tr><td>hslYesNoCancel</td><td>3</td><td>Display Yes, No and Cancel button</td></tr><tr><td>hslYesNo</td><td>4</td><td>Display Yes and No button</td></tr><tr><td>hslRetryCancel</td><td>5</td><td>Display Retry and Cancel button</td></tr><tr><td>hslError</td><td>16</td><td>Display Error Message icon</td></tr><tr><td>hslQuestion</td><td>32</td><td>Display Warning Query icon</td></tr><tr><td>hslExclamation</td><td>48</td><td>Display Warning Message icon</td></tr><tr><td>hslInformation</td><td>64</td><td>Display Information Message icon</td></tr></tbody></table><p> </p><p>To indicate the default button, specify one of the following values.</p><p> </p><table data-header-hidden><thead><tr><th></th><th></th><th></th></tr></thead><tbody><tr><td>Name</td><td>Value</td><td>Meaning</td></tr><tr><td>hslDefButton1 </td><td>0 </td><td><p>The first button is the default button.</p><p>hslDefButton1 is the default unless hslDefButton2, or hslDefButton3 is specified</p></td></tr><tr><td>hslDefButton2 </td><td>256 </td><td>The second button is the default button</td></tr><tr><td>hslDefButton3 </td><td>512 </td><td>The third button is the default button</td></tr></tbody></table><p> </p><p>timeout</p><p>Specifies the amount of time to wait before the output dialog box will be automatically dismissed without any user intervention (in seconds, non-negative floating-point number, optional). The default timeout value is hslInfinite.</p><p> </p><p><strong>Return</strong></p><p>If the function succeeds, one of the following values will be returned:</p><p> </p><table data-header-hidden><thead><tr><th></th><th></th><th></th></tr></thead><tbody><tr><td>Name</td><td>Value</td><td>Meaning</td></tr><tr><td>hslOK</td><td>1</td><td>OK button was selected</td></tr><tr><td>hslCancel</td><td>2</td><td>Cancel button was selected</td></tr><tr><td>hslAbort</td><td>3</td><td>Abort button was selected</td></tr><tr><td>hslRetry</td><td>4</td><td>Retry button was selected</td></tr><tr><td>hslIgnore</td><td>5</td><td>Ignore button was selected</td></tr><tr><td>hslYes</td><td>6</td><td>Yes button was selected</td></tr><tr><td>hslNo</td><td>7</td><td>No button was selected</td></tr></tbody></table><p> </p></td></tr><tr><td><p> </p><p>Shell(</p><p>pathname,</p><p>windowstyle,</p><p>concurrency</p><p>[,eventObj]</p><p>[,exitCode])</p></td><td><p> </p><p>Runs an executable (exe, com, bat) and returns a nonzero value if the function was successful, otherwise it returns zero. The Shell function runs other programs synchronously or asynchronously as specified by the parameter concurrency.</p><p> </p><p><strong>Parameter</strong></p><p>pathname</p><p>The name of the program to execute and any required arguments or command-line options; may include directory and drive (string).</p><p> </p><p>windowstyle</p><p>The parameter windowstyle specifies for graphical user interface (GUI) processes the style of the window in which the program is to be run as follows (integer):</p><p> </p><table data-header-hidden><thead><tr><th></th><th></th><th></th></tr></thead><tbody><tr><td>Name</td><td>Value</td><td>Meaning</td></tr><tr><td>hslHide</td><td>1</td><td>Hides the window and activates another window.</td></tr><tr><td>hslShow</td><td>2</td><td>Activates the window and displays it in its current size and position.</td></tr><tr><td>hslShowMaximized</td><td>3</td><td>Activates the window and displays it as a maximized window.</td></tr><tr><td>hslShowMinimized</td><td>4</td><td>Activates the window and displays it as a minimized window.</td></tr></tbody></table><p> </p><p>concurrency</p><p>The parameter concurrency specifies the concurrency of the program to execute as follows (integer):</p><p> </p><table data-header-hidden><thead><tr><th></th><th></th><th></th></tr></thead><tbody><tr><td>Name</td><td>Value</td><td>Meaning</td></tr><tr><td>hslSynchronous</td><td>1</td><td>The execution of the running HSL program will be blocked until the program to execute terminates.</td></tr><tr><td>hslAsynchronous</td><td>2</td><td>The execution of the running HSL program will not be blocked until the program to execute terminates.</td></tr></tbody></table><p> </p><p>eventObj</p><p>The optional reference to an event object allows the method to block until completion of the asynchronous executable completes (event).</p><p> </p><p>exitCode</p><p>A reference to a variable to retrieve the termination status of the executable (variable).</p><p> </p><p><strong>Return</strong></p><p>If the function succeeds, the return value is nonzero.</p><p>If the function fails, the return value is zero.</p><p> </p></td></tr><tr><td><p> </p><p>Fork(entryPoint)</p></td><td><p> </p><p>The Fork function creates a new thread for an HSL program. The creating thread must specify the entry point to the new thread. Typically, the entry point is the name of a function defined in the HSL source code. This function takes no arguments and returns no value. If a function has not been specified as synchronized, a program cannot have multiple threads simultaneously executing the same function.</p><p> </p><p><strong>Parameter</strong></p><p>entryPoint</p><p>The name of the entry point to the new thread (string).</p><p> </p><p><strong>Return</strong></p><p>If the function succeeds, the return value is a handle (type variable) to the new thread.</p><p>If the function fails, the return value is zero.</p><p> </p></td></tr><tr><td><p> </p><p>Join(</p><p>handles,</p><p>timeout)</p></td><td><p> </p><p>The Join function returns when one of the following occurs:</p><ul><li>All of the specified thread handles (or task identifiers) are in the signaled state.</li><li>The time-out interval elapses.</li></ul><p> </p><p><strong>Parameter</strong></p><p>handles</p><p>A reference to a single variable or to an array of variables containing thread handles (or task identifiers) returned by the Fork (or ActivateXxx) function (single variable, or array of variables).</p><p> </p><p>timeount</p><p>Specifies the amount of time to wait for all thread handles to be signaled (in seconds, non-negative floating-point number).</p><p> </p><p><strong>Return</strong></p><p>Nonzero if the function succeeds, otherwise zero (e.g. timeout).</p><p> </p></td></tr><tr><td><p> </p><p>GetBarcodeJoker(</p><p>barcodeJokerKey)</p></td><td><p> </p><p>Returns the value for the barcode joker mapped to the given key (string).</p><p> </p><p><strong>Parameter</strong></p><p>barcodeJokerKey</p><p>Specifies the key that identifies the barcode joker value (string).</p><p> </p></td></tr><tr><td><p> </p><p>GetType(var)</p></td><td><p> </p><p>The GetType function retrieves the type of the value of a variable.</p><p> </p><p><strong>Parameter</strong></p><p>var</p><p>A reference to a variable (integer, float or string).</p><p> </p><p><strong>Return</strong></p><p>One of the following string valued constants that indicates the type of the value of a variable:</p><p> </p><table data-header-hidden><thead><tr><th></th><th></th><th></th></tr></thead><tbody><tr><td>Name</td><td>Value</td><td>Meaning</td></tr><tr><td>hslInteger </td><td>"i"</td><td>The value is an integer</td></tr><tr><td>hslFloat </td><td>"f"</td><td>The value is a float</td></tr><tr><td>hslString </td><td>"s"</td><td>The value is a string</td></tr><tr><td> </td><td>""</td><td>The value has no type</td></tr></tbody></table><p> </p></td></tr><tr><td><p> </p><p>GetTime(format)</p></td><td><p> </p><p>The GetTime function returns a string that contains the formatted time.</p><p> </p><p><strong>Parameter</strong></p><p>format</p><p>A formatting string (string).</p><p>The value and meaning of the formatting codes for GetTime are listed below. If the formatting string is empty or of invalid format, the ISO format "%H:%M:%S" will be used.</p><p> </p><p>%H</p><p>Hour in 24-hour format (00 - 23).</p><p>%I</p><p>Hour in 12-hour format (01 - 12).</p><p>%M</p><p>Minute as decimal number (00 - 59).</p><p>%p</p><p>Current locale’s A.M./P.M. indicator for 12-hour clock.</p><p>%S</p><p>Second as decimal number (00 - 59).</p><p>%X</p><p>Time representation for current locale.</p><p> </p><p><strong>Return</strong></p><p>A string that contains the formatted time.</p><p> </p></td></tr><tr><td><p> </p><p>GetDate(format)</p></td><td><p> </p><p>The GetDate function returns a string that contains the formatted date.</p><p> </p><p><strong>Parameter</strong></p><p>format</p><p>A formatting string (string).</p><p>The value and meaning of the formatting codes for GetDate are listed below. If the formatting string is empty or of invalid format, the ISO format "%Y-%m-%d" will be used.</p><p> </p><p>%a</p><p>Abbreviated weekday name.</p><p>%A</p><p>Full weekday name.</p><p>%b</p><p>Abbreviated month name.</p><p>%B</p><p>Full month name.</p><p>%d</p><p>Day of month as decimal number (01 - 31).</p><p>%m</p><p>Month as decimal number (01 - 12).</p><p>%x</p><p>Date representation for current locale.</p><p>%y</p><p>Year without century, as decimal number (00 - 99).</p><p>%Y</p><p>Year with century, as decimal number.</p><p> </p><p><strong>Return</strong></p><p>A string that contains the formatted date.</p><p> </p></td></tr><tr><td><p> </p><p>GetMethodFileName( )</p></td><td><p> </p><p>The GetMethodFileName function retrieves the path and name of the topmost HSL source file that includes the current HSL source file. Usually, this is the name of the file containing the method.</p><p> </p><p><strong>Return</strong></p><p>The path and name of the topmost HSL source file that includes the current HSL source file.</p><p> </p></td></tr><tr><td><p> </p><p>GetFileName( )</p></td><td><p> </p><p>The GetFileName function retrieves the path and name of the current HSL source file.</p><p> </p><p><strong>Return</strong></p><p>The path and name of the current HSL source file.</p><p> </p></td></tr><tr><td><p> </p><p>GetFunctionName( )</p></td><td><p> </p><p>The GetFunctionName function retrieves the name of the current HSL function.</p><p> </p><p><strong>Return</strong></p><p>The name of the current HSL function.</p><p> </p></td></tr><tr><td><p> </p><p>GetLineNumber( )</p></td><td><p> </p><p>The GetLineNumber function retrieves the current line of the current HSL source file.</p><p> </p><p><strong>Return</strong></p><p>The current line of the current HSL source file (string).</p><p> </p></td></tr><tr><td><p> </p><p>GetRowNumber( )</p></td><td><p> </p><p>The GetRowNumber function retrieves the current row of the current HSL source file.</p><p> </p><p><strong>Return</strong></p><p>The current row of the current HSL source file (string; "0" if the current HSL source file contains no row information).</p><p> </p></td></tr><tr><td><p> </p><p>GetColumnNumber( )</p></td><td><p> </p><p>The GetColumnNumber function retrieves the the current column of the current HSL source file.</p><p> </p><p><strong>Return</strong></p><p>The current column of the current HSL source file (string; "0" if the current HSL source file contains no column information).</p><p> </p></td></tr><tr><td><p> </p><p>GetBinPath( )</p></td><td><p> </p><p>The GetBinPath function retrieves the Vector binary path.</p><p> </p><p><strong>Return</strong></p><p>The Vector binary path (fully qualified e.g. C:\Program Files\HAMILTON\Bin).</p><p> </p></td></tr><tr><td><p> </p><p>GetConfigPath( )</p></td><td><p> </p><p>The GetConfigPath function retrieves the Vector configuration path.</p><p> </p><p><strong>Return</strong></p><p>The Vector configuration path (fully qualified e.g. C:\Program Files\HAMILTON\Config).</p><p> </p></td></tr><tr><td>GetLabwarePath( )</td><td><p> </p><p>The GetLabwarePath function retrieves the Vector labware path.</p><p> </p><p>Return:</p><p>The Vector labware path (fully qualified, e.g. C:\Program Files\HAMILTON\Labware).</p><p> </p></td></tr><tr><td><p> </p><p>GetLibraryPath( )</p></td><td><p> </p><p>The GetLibraryPath function retrieves the Vector library path.</p><p> </p><p><strong>Return</strong></p><p>The Vector library path (fully qualified e.g. C:\Program Files\HAMILTON\Library).</p><p> </p></td></tr><tr><td><p> </p><p>GetMethodsPath( )</p></td><td><p> </p><p>The GetMethodsPath function retrieves the Vector methods path (contains deck layout and method files).</p><p> </p><p><strong>Return</strong></p><p>The Vector methods path (fully qualified, e.g. C:\Program Files\HAMILTON\Methods).</p><p> </p></td></tr><tr><td>GetLogFilesPath( )</td><td><p> </p><p>The GetLogFilesPath function retrieves the Vector log files path (contains runtime generated log files).</p><p> </p><p><strong>Return</strong></p><p>The Vector log files path (fully qualified, e.g. C:\Program Files \HAMILTON\LogFiles).</p><p> </p></td></tr><tr><td><p> </p><p>GetSystemPath( )</p></td><td><p> </p><p>The GetSystemPath function retrieves the Vector system path (contains system files).</p><p> </p><p><strong>Return</strong></p><p>The Vector system path (fully qualified, e.g. C:\Program Files \HAMILTON\System).</p><p> </p></td></tr><tr><td><p> </p><p>GetLanguage()</p></td><td><p> </p><p>The GetLanguage function retrieves the Vector language (returns a 3 letter symbol - refer to ISO standard 639 for list of symbols).</p><p> </p><p><strong>Return</strong></p><p>The Vector language.</p><p> </p></td></tr><tr><td><p> </p><p>GetIVDSystem( )</p></td><td><p> </p><p>The GetIVDSystem function retrieves the IVD System installed flag from the System Registry (integer).</p><p> </p><p><strong>Return</strong></p><p>Return value = 0 or 1 (default = 0, if not present).</p><p> </p></td></tr><tr><td><p> </p><p>GetUniqueRunId( )</p></td><td><p> </p><p>The GetUniqueRunId function returns the unique id of the current run (string), e.g. "42d75f353ff549ecb681121e81306741".</p><p> </p></td></tr><tr><td><p> </p><p>GetHWnd( )</p></td><td><p> </p><p>The GetHWnd function returns the application's main window handle (integer).</p><p> </p></td></tr><tr><td><p> </p><p>SearchPath(</p><p>fileName)</p></td><td><p> </p><p>The SearchPath function searches for the specified file.</p><p> </p><p><strong>Parameter</strong></p><p>fileName</p><p>The name of the file to search for (string). Receives the path and file name of the file found.</p><p>The name of the file can be relative or absolute. The file will be searched in the following directories in the following sequence:</p><p>1) in the current directory.</p><p>2) in the directory that is listed under the registry key Methods.</p><p>3) in the directory that is listed under the registry key Library.</p><p>4) in the directories that are listed in the PATH environment variable.</p><p> </p><p><strong>Return</strong></p><p>If the function succeeds, the return value is the path name of the first file found (may be the empty string if the file was not found).</p><p> </p></td></tr><tr><td><p> </p><p>AlignSequences(</p><p>maxOnly</p><p>[, ... ])</p></td><td><p> </p><p>Aligns the max. number of positions - allowed to process per step - of the given sequences, and optionally aligns the current total number of positions of the sequences, too.</p><p> </p><p><strong>Parameter</strong></p><p>maxOnly</p><p>Specifies whether only the max. number of positions - allowed to process per step - of the sequences should be aligned (integer; hslTrue or hslFalse). If maxOnly evaluates to false, the current total number of positions of the sequences are aligned, too. Thereby taking the smallst of the given sequences as the driving sequence.</p><p> </p><p>[...]</p><p>Variable argument list of comma separated sequence-multiplicity-pairs (integer).</p><p> </p><p><strong>Example</strong></p><p>AlignSequences(hslTrue, tips, 1, samples, 1, plate, 2);</p><p> </p></td></tr><tr><td><p> </p><p>GetUserName( )</p></td><td><p> </p><p>The GetUserName function retrieves the name of the current user. This is the name of the user currently logged onto the system.</p><p> </p><p><strong>Return</strong></p><p>If the function succeeds, the return value is the name of the user currently logged onto the system.</p><p> </p></td></tr><tr><td><p>AddCheckSum(</p><p>fileName,</p><p>commentDelimiter)</p></td><td><p> </p><p>The AddCheckSum function computes the checksum of the specified file and writes the checksum value to the end of the file.</p><p> </p><p><strong>Parameter</strong></p><p>fileName</p><p>The pathname of the file (string).</p><p> </p><p>commentDelimiter</p><p>The single-line comment delimiter(string), e.g. "//".</p><p> </p><p><strong>Return</strong></p><p>Nonzero if the function succeeds, otherwise zero.</p><p> </p><p><strong>Requirements</strong></p><p>Access right: AllAccess or Programmer.</p><p> </p><p><strong>Remarks</strong></p><p>A checksum can be used to test the validity of data.</p><p> </p></td></tr><tr><td><p> </p><p>VerifyCheckSum(</p><p>fileName)</p></td><td><p> </p><p>The VerifyCheckSum function verifies the checksum value of the specified file.</p><p> </p><p><strong>Parameter</strong></p><p>fileName</p><p>The pathname of the file (string).</p><p> </p><p><strong>Return</strong></p><p>Nonzero if the verification completed successfully, otherwise zero.</p><p> </p><p><strong>Remarks</strong></p><p>A checksum can be used to test the validity of data.</p><p> </p></td></tr><tr><td><p> </p><p>RegisterAbortHandler(</p><p>abortHandler)</p></td><td><p> </p><p>The RegisterAbortHandler function registers abortHandler as a custom HSL function called before a method will be aborted. One ore more abort handlers can be registered.</p><p>A custom HSL abort handler can take no arguments and should neither return a value nor raise an exception.</p><p> </p><p><strong>Parameter</strong></p><p>abortHandler</p><p>The name of the HSL function called before a method will be aborted (string).</p><p> </p><p><strong>Example</strong></p><p> </p><p>namespace MyLib</p><p>{</p><p>function OnAbortMyLib()</p><p>{</p><p>// cleanup</p><p>}</p><p>}</p><p> </p><p>function OnAbortMain()</p><p>{</p><p>// cleanup</p><p>}</p><p> </p><p>method Main()</p><p>{</p><p>RegisterAbortHandler("MyLib::OnAbortMyLib");</p><p>RegisterAbortHandler("OnAbortMain");</p><p>}</p><p> </p></td></tr><tr><td><p> </p><p>UnegisterAbortHandler(</p><p>abortHandler)</p></td><td><p> </p><p>The UnegisterAbortHandler function unregisters abortHandler as a custom HSL function called before a method will be aborted.</p><p> </p><p><strong>Parameter</strong></p><p>abortHandler</p><p>The name of the HSL function to be unregistered (string).</p><p> </p></td></tr><tr><td><p> </p><p>GetVectorDbTrackerObject( )</p></td><td><p> </p><p>Returns the Vector Database Tracker object (object == IHxVectorDbTracking*).</p><p> </p></td></tr><tr><td><p> </p><p>GetSimulationMode( )</p></td><td><p> </p><p>Returns the simulation mode (0 = simulation off, 1 = full simulation).</p><p> </p></td></tr><tr><td><p> </p><p>GetTimeScaleFactor( )</p></td><td><p> </p><p>Returns the current time scale factor (float; defaults to 1.0).</p><p>The time scale factor is used to scale:</p><p>- task dependencies</p><p>- activity durations</p><p><strong>Remark</strong></p><p>Timer durations may be scaled using the optional parameter 'scale' in the timer.SetTimer( ) function.</p><p> </p></td></tr><tr><td><p> </p><p>SetTimeScaleFactor(</p><p>timeScaleFactor )</p></td><td><p> </p><p>Sets the current time scale factor (float; defaults to 1.0).</p><p>If the simulation mode is switched on, the time scale factor is used to scale:</p><p>- task dependencies</p><p>- activity durations</p><p><strong>Parameter</strong></p><p>timeScaleFactor</p><p>[in] The new time scale factor (float; must be greater than zero).</p><p><strong>Remark</strong></p><p>Timer durations may be scaled using the optional parameter 'scale' in the timer.SetTimer( ) function.</p><p> </p></td></tr><tr><td><p> </p><p>IsDBNull(</p><p>value)</p></td><td><p> </p><p>Returns an indication whether the specified variable is of type null (VT_NULL).</p><p><strong>Parameter</strong></p><p>value</p><p>[in] A variable.</p><p><strong>Return</strong></p><p>Nonzero if the specified variable is of type null (VT_NULL), otherwise zero.</p><p> </p></td></tr><tr><td><p> </p><p>SetDBNull(</p><p>value)</p></td><td><p> </p><p>Sets the value of the specified variable to a null value (VT_NULL).</p><p><strong>Parameter</strong></p><p>value</p><p>[in/out] A variable.</p><p> </p></td></tr><tr><td><p> </p><p>GetCommState(port)</p></td><td><p> </p><p>The GetCommState function retrives the configuration information for a specified communications resource. The structure that contains the configuration information looks as shown below. The entries of the structure that retrive the configuration information must be accessible in the local scope.</p><p> </p><p><strong>Parameter</strong></p><p>port</p><p>The communications resource opened during the file-Open operation (file).</p><p> </p><p><strong>Return</strong></p><p>Nonzero if the function succeeds, otherwise zero.</p><p> </p></td></tr><tr><td><p> </p><p>SetCommState(</p><p>port,</p><p>cfgFile)</p></td><td><p> </p><p>The SetCommState function configures a communications resource according to the specifications in a structure that contains the configuration information. The structure that contains the configuration information must look as shown below. Each entry in the structure is optional and overwrites the default value in parentheses.</p><p> </p><p><strong>Parameter</strong></p><p>port</p><p>The communications resource opened during the file-Open operation (file).</p><p> </p><p>cfgFile</p><p>The name of the file that contains the configuration information (string; optional). If this parameter is omitted, the entries in the structure that contains the configuration information must be accessible in the local scope.</p><p> </p><p><strong>Return</strong></p><p>Nonzero if the function succeeds, otherwise zero.</p><p> </p></td></tr><tr><td><p> </p><p>GetCommTimeouts(</p><p>port)</p></td><td><p> </p><p>The GetCommTimeouts function retrives the time-out parameters for all read and write operations for a specified communications resource. The structure that contains the time-out information looks as shown below. The entries of the structure that retrive the configuration information must be accessible in the local scope.</p><p> </p><p><strong>Parameter</strong></p><p>port</p><p>The communications resource opened during the file-Open operation (file).</p><p> </p><p><strong>Return</strong></p><p>Nonzero if the function succeeds, otherwise zero.</p><p> </p></td></tr><tr><td><p> </p><p>SetCommTimeouts(</p><p>port,</p><p>cfgFile)</p></td><td><p> </p><p>The SetCommTimeouts function sets the time-out parameters for all read and write operations on a specified communications resource. The structure that contains the time-out information must look as shown below. Each entry in the structure is optional and overwrites the default value in parentheses.</p><p> </p><p><strong>Parameter</strong></p><p>port</p><p>The communications resource opened during the file-Open operation (file).</p><p> </p><p>cfgFile</p><p>The name of the file that contains the time-out information (string; optional). If this parameter is omitted, the entries in the structure that contains the time-out information must be accessible in the local scope.</p><p> </p><p><strong>Return</strong></p><p>Nonzero if the function succeeds, otherwise zero.</p><p> </p></td></tr><tr><td><p> </p><p>Translate(</p><p>text)</p><p> </p></td><td><p> </p><p>This function handles translation of a text. If there exists a translation of the text given by the text parameter, the function returns the translated string, else the original text is returned.</p><p> </p><p><strong>Parameter</strong></p><p>text</p><p>Text which is to be translated (string).</p><p> </p><p><strong>Return</strong></p><p>Returns the translated text if available, else returns the original text.</p><p> </p><p><strong>Example</strong></p><p>Assume that the method was written in English and the parameter text holds the English phrase "This is an English text".</p><p> </p><p>variable text;</p><p>variable translatedText;</p><p>text = "This is an English text";</p><p> </p><p>translatedText = Translate(text);</p><p> </p><p>If for example a German translation of the method's texts like "This is an English text" is available and the language is set to German, the function Translate() returns the translated phrase "Dies ist ein deutscher Text".</p><p>If no translation is found, Translate() returns the original phrase "This is an English text".</p><p> </p></td></tr><tr><td><p> </p><p>GetDeviceRef(</p><p>systemDeckLayoutName, instrumentDeckName)</p><p> </p><p>GetDeviceRef(</p><p>instrumentKeyName)</p><p> </p></td><td><p> </p><p>Returns a reference to the global device with the given system deck layout file name and contained instrument deck name.</p><p><strong>Parameter</strong></p><p>systemDeckLayoutName</p><p>The name of a system deck layout file (.lay) containing one or more single deck layouts (string; may be empty). The name of the system deck layout file can be relative or absolute.</p><p>The system deck layout file will be searched in the following directories in the following sequence:</p><ol><li>In the same directory of the file that contains the declaration of the device object, and then in the directories of whatever files that include that file.</li><li>In the directory that is listed under the registry key Methods.</li><li>In the directory that is listed under the registry key Library.</li><li>In the directories that are listed in the PATH environment variable.</li></ol><p>If the name of the system deck layout file is empty, the first device with a matching instrument deck name contained in its system deck layout file will be returned.</p><p> </p><p>instrumentDeckName</p><p>The name of a particular deck layout of in the system deck (string).</p><p> </p><p>instrumentKeyName</p><p>The key name of an instrument registered in the registry (string).</p><p><strong>Return</strong></p><p>The reference to the global device with the given system deck layout file name and contained instrument deck name if the function succeeds, otherwise the element function device.IsNullDevice( ) returns hslTrue.</p><p><strong>Example</strong></p><p></p><pre class="language-clike"><code class="lang-clike">device ML_STAR("SystemLayout.lay",
               "ML_STAR", hslTrue);
//...
function MyFunc() void
{
device ML_STAR_Ref("", "", hslTrue);
ML_STAR_Ref = GetDeviceRef("SystemLayout.lay", "ML_STAR");
if (!ML_STAR_Ref.IsNullDevice())
{
//...
}
//...
}
</code></pre><p></p><p> </p></td></tr></tbody></table>

&#x20;

Structure containing the configuration and time-out information, respectively:

```
namespace SerialCommunicationsControlSettings

{

variable BaudRate (9600);                            // current baud rate  

variable fBinary (1);                                // binary mode, no EOF check  

variable fParity (0);                                // enable parity checking  

variable fOutxCtsFlow (0);                           // CTS output flow control  

variable fOutxDsrFlow (0);                           // DSR output flow control  

variable fDtrControl (0);                            // DTR flow control type  

variable fDsrSensitivity (0);                        // DSR sensitivity  

variable fTXContinueOnXoff (1);                      // XOFF continues Tx  

variable fOutX (0);                                  // XON/XOFF out flow control  

variable fInX (0);                                   // XON/XOFF in flow control  

variable fErrorChar (0);                             // enable error replacement  

variable fNull (0);                                  // enable null stripping  

variable fRtsControl (0);                            // RTS flow control  

variable fAbortOnError (0);                          // abort on error  

variable XonLim (2048);                              // transmit XON threshold  

variable XoffLim (512);                              // transmit XOFF threshold  

variable ByteSize (8);                               // number of bits/byte, 4-8  

variable Parity (0);                                 // 0-4=no,odd,even,mark,space  

variable StopBits (0);                               // 0,1,2 = 1, 1.5, 2  

variable XonChar (17);                               // Tx and Rx XON character  

variable XoffChar (19);                              // Tx and Rx XOFF character  

variable ErrorChar (0);                              // error replacement character 

variable EofChar (0);                                // end of input character  

variable EvtChar (0);                                // received event character  

}

 

namespace SerialCommunicationsTimeoutSettings

{

variable ReadIntervalTimeout  (hslInfinite);          // maximum time between read chars 

variable ReadTotalTimeoutMultiplier (hslInfinite);    // multiplier of characters  

variable ReadTotalTimeoutConstant (10.000);           // constant in seconds  

variable WriteTotalTimeoutMultiplier (0.000);         // multiplier of characters  

variable WriteTotalTimeoutConstant (10.000);          // constant in seconds  

}


```

**Remarks**

A value of hslInfinite for ReadIntervalTimeout, combined with zero values for both the ReadTotalTimeoutConstant and ReadTotalTimeoutMultiplier members, specifies that the read operation is to return immediately with the characters that have already been received, even if no characters have been received.

&#x20;

If an application sets ReadIntervalTimeout and ReadTotalTimeoutMultiplier to hslInfinite and sets ReadTotalTimeoutConstant to a value greater than zero and less than hslInfinite, one of the following occurs when the ReadRecord function is called:

If the input buffer contains any characters, ReadRecord returns immediately with the characters in the buffer.

If the input buffer contains no characters, ReadRecord waits until a character arrives and then returns immediately.

If no character arrives within the time specified by ReadTotalTimeoutConstant, ReadRecord times out.

&#x20;

**Examples**

1\)

```clike
method Main()

{

file port;

variable io;

port.SetDelimiter(hslAsciiText);

port.AddField(1, io, hslString);

port.Open("COM2 9600,S,7,2,N,LF", hslWrite);

SetCommState(port, "DCB.hsl");                     // init from configuration file

 

// ...

}

```

2\)

```clike
method Main()

{

variable ReadIntervalTimeout(hslInfinite);

variable ReadTotalTimeoutMultiplier(hslInfinite);

variable ReadTotalTimeoutConstant(20.000);

file port;

variable io;

 

port.SetDelimiter(hslAsciiText);

port.AddField(1, io, hslString);

port.Open("COM2 9600,S,7,2,N,LF ", hslWrite);

SetCommTimeouts(port);                             // init from local scope

 

// ...

}
```

3\)

```clike
method Main()

{

variable BaudRate (-1);

variable Parity (-1);

variable StopBits (-1);

 

variable ReadIntervalTimeout (-1);

variable ReadTotalTimeoutMultiplier (-1);

variable ReadTotalTimeoutConstant (-1);

variable WriteTotalTimeoutMultiplier (-1);

variable WriteTotalTimeoutConstant (-1);

 

file port;

variable io;

port.SetDelimiter(hslAsciiText);

port.AddField(1, io, hslString);

port.Open("COM2 9600,S,7,2,N,LF ", hslWrite);

 

GetCommState(port);

GetCommTimeouts(port);

 

Trace("BaudRate = ", BaudRate);

Trace("Parity = ", Parity);

Trace("StopBits = ", StopBits);

 

Trace("ReadIntervalTimeout = ", ReadIntervalTimeout);

Trace("ReadTotalTimeoutMultiplier = ", ReadTotalTimeoutMultiplier);

Trace("ReadTotalTimeoutConstant = ", ReadTotalTimeoutConstant);

Trace("WriteTotalTimeoutMultiplier = ", WriteTotalTimeoutMultiplier);

Trace("WriteTotalTimeoutConstant = ", WriteTotalTimeoutConstant);

 

// ...

}

```

