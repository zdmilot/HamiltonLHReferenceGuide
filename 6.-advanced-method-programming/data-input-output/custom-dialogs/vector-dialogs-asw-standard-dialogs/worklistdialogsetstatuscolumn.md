# WorklistDialogSetStatusColumn

## Syntax

| WorklistDialogSetStatusColumn ( | variable i\_blnIsColumnVisibility, |   |
| ------------------------------- | ---------------------------------- | - |
|                                 | variable i\_strStatusColumnName    | ) |

Set the header and visibility of the "Status" column.\
\
![](<../../../../.gitbook/assets/image (18) (1) (1) (1).png>)

## Arguments & Return Values

| arguments                | range   | description                                                               |
| ------------------------ | ------- | ------------------------------------------------------------------------- |
| i\_blnIsColumnVisibility | boolean | <p>is column visible, true it is, false do not show</p><p>that column</p> |
| i\_strStatusColumnName   | string  | header of column status                                                   |
| return values            |         |                                                                           |
| ASWGLOBAL::BOOL::TRUE    | boolean | if successful                                                             |
| ASWGLOBAL::BOOL::FALSE   | boolean |                                                                           |

## Example of WorklistDialog

For examples or demo please see also (Copy & Paste to Explorer Adress Field):

32Bit OS (WinNT/WinXP 32Bit) and below:

%PROGRAMFILES%\HAMILTON\Methods\Library Demo Methods\ASWStandardDialogs\\

64Bit OS (XP64/Vista/Windows7):

%PROGRAMFILES(X86)%\HAMILTON\Methods\Library Demo Methods\ASWStandardDialogs\\
