# FileBrowserDialog

## Syntax

| FileBrowserDialog ( | variable i\_strDialogTitle,    |
| ------------------- | ------------------------------ |
|                     | variable i\_intButtonType,     |
|                     | variable i\_intDialogHeight,   |
|                     | variable i\_intDialogWidth,    |
|                     | variable i\_strMessage,        |
|                     | variable i\_intFileDialogType, |
|                     | variable i\_strFileFilter,     |
|                     | variable i\_intFilterIndex,    |
|                     | variable i\_strInitialFile,    |
|                     | variable \&o\_strSelectedFile  |
|                     | ) variable                     |

Creates a FileBrowser Dialog.

<figure><img src="../../../../.gitbook/assets/image (72) (1).png" alt=""><figcaption></figcaption></figure>

## Arguments & Return Values

| argument             | range              | description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| -------------------- | ------------------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| i\_strDialogTitle    | string             | dialog title shown in the header                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| i\_intButtonType     | integer \[0..7]    | button type class (Enumerations R)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| i\_intDialogHeight   | integer \[0..5999] | the height of the dialog in pixel (0 auto sizing)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| i\_intDialogWidth    | integer \[0..5999] | the width of the dialog in pixel (0 auto sizing)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| i\_strMessage        | string             | the text of the dialog (forced line break with \n)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| i\_intFileDialogType | integer \[0..1]    | the type of the file dialog (save, for new file or open for existing file) (Enumerations R)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| i\_strFileFilter     | string             | <p>defines the file filter</p><p></p><p></p><p>Examples:<br></p><pre><code>“{description_1}|{filename_1.fileextension_1}”
        
       "All files (*.*)|*.*" - for all files
</code></pre><p>or</p><pre><code>“{description_1}|{filename_1.fileextension_1}|
            {description_2}|{filename_2.fileextension_2}|
            {description_3}|{filename_3.fileextension_3}”
 
            "All files (*.*)|*.*|Only Text Files (*.txt)|*.txt|         Only Hamilton Methods (*.med)|*.med"
</code></pre><p>Result:<br><img src="../../../../.gitbook/assets/image (3) (1) (1) (1).png" alt=""></p> |
| i\_intFilterIndex    | int                | which defined file filter is default, with the last example from above and i\_intFilterIndex = 3 (1-based-index) \*.med is the default setting for the file browser                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| i\_strInitialFile    | string             | initial file                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| o\_strSelectedFile   | string             | the selected file, if selected                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| return values        | integer \[-9..7]   | value of clicked dialog button (see also ASWGlobal.hsl) or error value (return value < 0, see also chapter Errorcodes)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |

## Example of FileBrowserDialog

For examples or demo please see also (Copy & Paste to Explorer Adress Field):

32Bit OS (WinNT/WinXP 32Bit) and below:

%PROGRAMFILES%\HAMILTON\Methods\Library Demo Methods\ASWStandardDialogs\\

64Bit OS (XP64/Vista/Windows7):

%PROGRAMFILES(X86)%\HAMILTON\Methods\Library Demo Methods\ASWStandardDialogs\\
