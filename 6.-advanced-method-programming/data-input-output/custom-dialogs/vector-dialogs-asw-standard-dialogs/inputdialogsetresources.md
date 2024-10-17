# InputDialogSetResources

## Syntax

| InputDialogSetResources ( | variable i\_arrInputListHeaderLocalization) variable |   |
| ------------------------- | ---------------------------------------------------- | - |

Sets the columns header descriptions (captions / localizations).

i\_ arrInputListHeaderLocalization must contain three and only three elements of type string for the default headers:

�         Type,

�         Value,

�         Description.\
\


## Arguments & Return Values

| arguments                         | range   | description                    |
| --------------------------------- | ------- | ------------------------------ |
| i\_arrInputListHeaderLocalization | string  | column headers for columns 1-3 |
| return value                      |         |                                |
| ASWGLOBAL::BOOL::TRUE             | boolean | if successfully                |
| ASWGLOBAL::BOOL::FALSE            |         |                                |

For examples or demo please see also (Copy & Paste to Explorer Address Field):

32Bit OS (WinNT/WinXP 32Bit) and below:

%PROGRAMFILES%\HAMILTON\Methods\Library Demo Methods\ASWStandardDialogs\\

64Bit OS (XP64/Vista/Windows7):

%PROGRAMFILES(X86)%\HAMILTON\Methods\Library Demo Methods\ASWStandardDialogs\\
