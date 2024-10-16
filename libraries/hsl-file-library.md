# HSL File Library

<figure><img src="../.gitbook/assets/image (829).png" alt=""><figcaption></figcaption></figure>

Include: HSLFilLib.hsl

&#x20;

| Function                                                                                               | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| ------------------------------------------------------------------------------------------------------ | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| <p> </p><p>FilEof(</p><p>file&#x26; fileObj)</p>                                                       | <p> </p><p>Indicates that the current record position is after the last record.</p><p> </p><p>Parameter:</p><p>fileObj</p><p>The file object.</p><p> </p><p>Return:</p><p>Nonzero if the current record position is after the last record, otherwise zero.</p><p> </p>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <p> </p><p>FilFindFile(</p><p>variable&#x26; fileName)</p>                                             | <p> </p><p>Member function to start a file search.</p><p> </p><p>Parameter:</p><p>fileNamej</p><p>Specifies a valid directory or path and file name and can contain wildcard characters (* and ?).</p><p> </p><p>Return:</p><p>If the function is successful, the return value is the path name of the first file found.</p><p> </p><p>Remarks:</p><p>The FilFindFile function is obsolete. This function is provided only for compatibility reasons with version 1.2 of HSL. Version 2.0 (and higher) based methods should use the FilSearchPath function.</p><p> </p>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <p> </p><p>FilFindNextFile( )</p>                                                                      | <p> </p><p>Continuation of a file search from a previous call to FilFindFile</p><p> </p><p>Return:</p><p>If the function succeeds, the return value is the path name of the next file found.</p><p> </p>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <p> </p><p>FilFormatBarcodeFile(</p><p>variable&#x26; dataSource,</p><p>variable&#x26; dataTarget)</p> | <p> </p><p>Converts the weakly formatted barcode file, written as ASCII text file during the LoadCarrier oepration, into a strongly formatted barcode file using the format as specified below. The strongly formatted barcode file may be an ASCII text file, a Microsoft Excel, or a Microsoft Access file.</p><p> </p><table data-header-hidden><thead><tr><th></th><th></th></tr></thead><tbody><tr><td>Column name</td><td>Meaning</td></tr><tr><td>Id</td><td>Record id (integer)</td></tr><tr><td>Specifier</td><td>Specifier (string), P = Position, C = Carrier</td></tr><tr><td>Position</td><td>Position (integer)</td></tr><tr><td>Barcode</td><td>Barcode (string)</td></tr><tr><td>Timestamp</td><td>Time-stamp, YYYY-MM-DD hh:mm:ss (string)</td></tr></tbody></table><p> </p><p>Parameter:</p><p>dataSource</p><p>The name of the weakly formatted barcode file written as ASCII text file during the LoadCarrier operation (string).</p><p> </p><p>dataTarget</p><p>The name of the strongly formatted barcode file written as an ASCII text file, a Microsoft Excel, or a Microsoft Access file (string). The name must include a table name for a Microsoft Excel file or a Microsoft Access database.</p><p> </p><p>Return:</p><p>Nonzero if the function terminated successfully, otherwise zero.</p><p> </p><p>Examples:</p><p> </p><p><code>variable logPath("\\Program Files\\Hamilton\\LogFiles\\");</code></p><p><br><code>FilFormatBarcodeFile(logPath + "barcode_1.txt",</code></p><p><code>logPath + "barcode__1.txt");</code></p><p></p><p><code>FilFormatBarcodeFile(logPath + "barcode_1.txt",</code></p><p><code>logPath + "barcode__1.xls barcode_1");</code></p><p></p><p><code>FilFormatBarcodeFile(logPath + "barcode_1.txt",</code></p><p><code>logPath + "barcode__1.mdb barcode_1");</code></p><p> </p> |
| <p> </p><p>FilGetBinPath( )</p>                                                                        | <p> </p><p>The GetMethodsPath function retrieves the Vector binary path.</p><p> </p><p>Return:</p><p>The Vector binary path (fully qualified, e.g. C:\Program Files\HAMILTON\Bin).</p><p> </p>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <p> </p><p>FilGetCommState(</p><p>file&#x26; port)</p>                                                 | <p> </p><p>The FilGetCommState function retrieves the configuration information for a specified communication resource. The structure that contains the configuration information is as shown below. The entries of the structure that retrieves the configuration information must be accessible in the global scope.</p><p> </p><p>Parameter:</p><p>port</p><p>The communication resource opened during the file-Open operation (file).</p><p> </p><p>Return:</p><p>Nonzero if the function succeeds, otherwise zero.</p><p> </p>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <p> </p><p>FilGetCommTimeouts(</p><p>file&#x26; port)</p>                                              | <p> </p><p>The FilGetCommTimeouts function retrieves the time-out parameters for all read and write operations for a specified communication resource. The structure that contains the time-out information is as shown below. The entries of the structure that retrieve the configuration information must be accessible in the global scope.</p><p> </p><p>Parameter:</p><p>port</p><p>The communication resource opened during the file-Open operation (file).</p><p> </p><p>Return:</p><p>Nonzero if the function succeeds, otherwise zero.</p><p> </p>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <p> </p><p>FilGetConfigPath( )</p>                                                                     | <p> </p><p>The FilGetConfigPath function retrieves the Vector configuration path.</p><p> </p><p>Return:</p><p>The Vector configuration path (fully qualified, e.g. C:\Program Files\HAMILTON\Config).</p><p> </p>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <p> </p><p>FilGetLabwarePath( )</p>                                                                    | <p> </p><p>The FilGetLabwarePath function retrieves the Vector labware path.</p><p> </p><p>Return:</p><p>The Vector labware path (fully qualified, e.g. C:\Program Files\HAMILTON\Labware).</p><p> </p>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <p> </p><p>FilGetLibraryPath( )</p>                                                                    | <p> </p><p>The GetLibraryPath function retrieves the Vector library path.</p><p> </p><p>Return:</p><p>The Vector library path (fully qualified, e.g. C:\Program Files\HAMILTON\Library).</p><p> </p>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <p> </p><p>FilGetLogFilesPath( )</p>                                                                   | <p> </p><p>The FilGetLogFilesPath function retrieves the Vector log files path (contains runtime generated log files).</p><p> </p><p>Return:</p><p>The Vector log files path (fully qualified, e.g. C:\Program Files\HAMILTON\LogFiles).</p><p> </p>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <p> </p><p>FilGetMethodsPath( )</p>                                                                    | <p> </p><p>The FilGetMethodsPath function retrieves the Vector methods path (contains deck layout and method files).</p><p> </p><p>Return:</p><p>The Vector methods path (fully qualified, e.g.</p><p>C:\Program Files\HAMILTON\Methods).</p><p> </p>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <p> </p><p>FilGetSystemPath( )</p>                                                                     | <p> </p><p>The FilGetSystemPath function retrieves the Vector system path (contains system files).</p><p> </p><p>Return:</p><p>The Vector system path (fully qualified, e.g. C:\Program Files\HAMILTON\System).</p><p> </p>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <p> </p><p>FilIsNull(</p><p>variable&#x26; value)</p>                                                  | <p> </p><p>Returns non-zero if the variable is a null value (SQL style Null).</p><p> </p>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <p> </p><p>FilReadString(</p><p>file&#x26; fileObj)</p>                                                | <p> </p><p>Reads the next record from the file data source as string-valued data. Row data, but no schema data, is saved to the string. After you call FilReadString, the next unread record becomes the current record, or the Eof property is set to hslTrue if there are no more records.</p><p> </p><p>Parameter:</p><p>fileObj</p><p>The file object.</p><p> </p><p>Return:</p><p>The contents of the next field in the file data source as string-valued data (string) or a run time error in case of an error.</p><p> </p>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <p> </p><p>FilRemoveFields(</p><p>file&#x26; fileObj)</p>                                              | <p> </p><p>Removes all fields from a record definition.</p><p> </p><p>Parameter:</p><p>fileObj</p><p>The file object.</p><p> </p>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <p> </p><p>FilSearchPath(</p><p>variable&#x26; fileName)</p>                                           | <p> </p><p>The FilSearchPath function searches for the specified file.</p><p> </p><p>Parameter:</p><p>fileName</p><p>The name of the file to search for (string). Receives the path and file name of the file found.</p><p>The name of the file can be relative or absolute. The file will be searched in the following directories in the following sequence:</p><p>1) in the current directory.</p><p>2) in the directory that is listed under the registry key Methods.</p><p>3) in the directory that is listed under the registry key Library.</p><p>4) in the directories that are listed in the PATH environment variable.</p><p> </p><p>Return:</p><p>If the function succeeds, the return value is the path name of the first file found (may be an empty string if the file was not found).</p><p> </p>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <p> </p><p>FilSetCommState(</p><p>file&#x26; port,</p><p>variable&#x26; cfgFile)</p>                   | <p> </p><p>The FilSetCommState function configures a communication resource according to the specifications in a structure that contains the configuration information. The structure that contains the configuration information must be structured as shown below. Each entry in the structure is optional and overwrites the default value in parentheses.</p><p> </p><p>Parameter:</p><p>port</p><p>The communication resource opened during the file-Open operation (file).</p><p> </p><p>cfgFile</p><p>The name of the file that contains the configuration information (string). If this parameter is empty, the entries in the structure that contains the configuration information must be accessible in the global scope.</p><p> </p><p>Return:</p><p>Nonzero if the function succeeds, otherwise zero.</p><p> </p>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <p> </p><p>FilSetCommTimeouts(</p><p>file&#x26; port,</p><p>variable&#x26; cfgFile)</p>                | <p> </p><p>The FilSetCommTimeouts function sets the time-out parameters for all read and write operations on a specified communication resource. The structure that contains the time-out information is as shown below. Each entry in the structure is optional and overwrites the default value in parentheses.</p><p> </p><p>Parameter:</p><p>port</p><p>The communication resource opened during the file-Open operation (file).</p><p> </p><p>cfgFile</p><p>The name of the file that contains the time-out information (string). If this parameter is empty, the entries in the structure that contains the time-out information must be accessible in the global scope.</p><p> </p><p>Return:</p><p>Nonzero if the function succeeds, otherwise zero.</p><p> </p>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <p> </p><p>FilUpdateRecord(</p><p>file&#x26; fileObj)</p>                                              | <p> </p><p>Updates the current record of the file object with the values of the variable objects specified in the record definition. The current record remains current after you call the FilUpdateRecord function. The provider must support UPDATE.</p><p> </p><p>Parameter:</p><p>fileObj</p><p>The file object.</p><p> </p><p>Return:</p><p>Nonzero if the function terminated successfully, otherwise zero.</p><p> </p>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <p> </p><p>FilWriteString(</p><p>file&#x26; fileObj,</p><p>variable&#x26; stringObj)</p>               | <p> </p><p>Writes a string to the end of the file data source. After you call the FilWriteString function, the new record becomes the current record.</p><p> </p><p>Parameter:</p><p>fileObj</p><p>The file object.</p><p> </p><p>stringObj</p><p>The string to be written.</p><p> </p><p>Return:</p><p>Nonzero if the function terminated successfully, otherwise zero (e.g. timeout for a communications resource).</p><p> </p>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |

&#x20;

Structure that contains the configuration and time-out information, respectively:

```clike
namespace SerialCommunicationsControlSettings

{

variable BaudRate (9600);          /* current baud rate  */

variable fBinary (1);              /* binary mode, no EOF check  */

variable fParity (0);              /* enable parity checking  */

variable fOutxCtsFlow (0);         /* CTS output flow control  */

variable fOutxDsrFlow (0);         /* DSR output flow control  */

variable fDtrControl (0);          /* DTR flow control type  */

variable fDsrSensitivity (0);      /* DSR sensitivity  */

variable fTXContinueOnXoff (1);    /* XOFF continues Tx  */

variable fOutX (0);                /* XON/XOFF out flow control  */

variable fInX (0);                 /* XON/XOFF in flow control  */

variable fErrorChar (0);           /* enable error replacement  */

variable fNull (0);                /* enable null stripping  */

variable fRtsControl (0);          /* RTS flow control  */

variable fAbortOnError (0);        /* abort on error  */

variable XonLim (2048);            /* transmit XON threshold  */

variable XoffLim (512);            /* transmit XOFF threshold  */

variable ByteSize (8);             /* number of bits/byte, 4-8  */

variable Parity (0);               /* 0-4=no,odd,even,mark,space  */

variable StopBits (0);             /* 0,1,2 = 1, 1.5, 2  */

variable XonChar (17);             /* Tx and Rx XON character  */

variable XoffChar (19);            /* Tx and Rx XOFF character  */

variable ErrorChar (0);            /* error replacement character */

variable EofChar (0);              /* end of input character  */

variable EvtChar (0);              /* received event character  */

}

 

namespace SerialCommunicationsTimeoutSettings

{

/* maximum time between read chars */

variable ReadIntervalTimeout (hslInfinite);

/* multiplier of characters */

variable ReadTotalTimeoutMultiplier (hslInfinite);

/* constant in milliseconds */

variable ReadTotalTimeoutConstant (10.000);

/* multiplier of characters */

variable WriteTotalTimeoutMultiplier (0.000);

/* constant in milliseconds */

variable WriteTotalTimeoutConstant (10.000);

}


```

## Remarks:

&#x20;

A value of hslInfinite for ReadIntervalTimeout, combined with zero values for both the ReadTotalTimeoutConstant and ReadTotalTimeoutMultiplier members, specifies that the read operation is to return immediately with the characters that have already been received, even if no characters have been received.

&#x20;

If an application sets ReadIntervalTimeout and ReadTotalTimeoutMultiplier to hslInfinite and sets ReadTotalTimeoutConstant to a value greater than zero and less than hslInfinite, one of the following occurs when the ReadRecord function is called:

If there are any characters in the input buffer, ReadRecord returns immediately with the characters in the buffer.

If there are no characters in the input buffer, ReadRecord waits until a character arrives and then returns immediately.

If no character arrives within the time specified by ReadTotalTimeoutConstant, ReadRecord times out.

&#x20;

## Examples:

### Example 1

```clike
method Main()

{

file port;

variable io;

port.SetDelimiter(hslAsciiText);

port.AddField(1, io, hslString);

port.Open("COM2 9600,S,7,2,N,LF", hslWrite);

FilSetCommState(port, "DCB.hsl"); // init from configuration file

 

// ...

}
```

### Example 2

```clike
variable ReadIntervalTimeout(hslInfinite);

variable ReadTotalTimeoutMultiplier(hslInfinite);

variable ReadTotalTimeoutConstant(20000);

 

method Main()

{

file port;

variable io;

port.SetDelimiter(hslAsciiText);

port.AddField(1, io, hslString);

port.Open("COM2 9600,S,7,2,N,LF ", hslWrite);

SetCommTimeouts(port); // init from global scope

 

// ...

}

 

```

### Example 3

```clike
variable BaudRate (-1);

variable Parity (-1);

variable StopBits (-1);

 

variable ReadIntervalTimeout (-1);

variable ReadTotalTimeoutMultiplier (-1);

variable ReadTotalTimeoutConstant (-1);

variable WriteTotalTimeoutMultiplier (-1);

variable WriteTotalTimeoutConstant (-1);

 

method Main()

{

file port;

variable io;

port.SetDelimiter(hslAsciiText);

port.AddField(1, io, hslString);

port.Open("COM2 9600,S,7,2,N,LF ", hslWrite);

 

FilGetCommState(port);

FilGetCommTimeouts(port);

 

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



## Runtime Errors

|                         |                                                                                   |
| ----------------------- | --------------------------------------------------------------------------------- |
| Shell Out Delete Failed | The library failed at the specified line to shell out the 'DELETE' command.       |
| Shell Out Dir Failed    | The library failed at the specified line to shell out the 'DIR' command.          |
| Shell Out Delete Failed | The library failed at the specified line to shell out the 'DELETE' command.       |
| Add Field Failed        | The library failed at the specified line to add a field to the record definition. |
| Read Record Failed      | The library failed at the specified line to read a record from a file.            |
| Open File Failed        | The library failed at the specified line to open the specified file.              |
| Close File Failed       | The library failed at the specified line to close the specified file.             |



