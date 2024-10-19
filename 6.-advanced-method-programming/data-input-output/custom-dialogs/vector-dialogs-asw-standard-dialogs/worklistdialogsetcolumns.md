# WorklistDialogSetColumns

## Syntax

| WorklistDialogSetColumns ( | variable i\_arrColumnNames\[] ) variable |
| -------------------------- | ---------------------------------------- |

Sets the columns names of the worklist view.\
\
![](<../../../../.gitbook/assets/image (14).png>)

## Arguments & Return Values

| arguments              | range        | description                                                                                                                                                                                      |
| ---------------------- | ------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| i\_arrColumnNames\[]   | string array | <p>array with column names of the worklist view<br>the columns names are the captions (headline),<br>except status and selected column, please use<br>different and namely discernable words</p> |
| return values          |              |                                                                                                                                                                                                  |
| ASWGLOBAL::BOOL::TRUE  | boolean      | if successful                                                                                                                                                                                    |
| ASWGLOBAL::BOOL::FALSE | boolean      |                                                                                                                                                                                                  |

## Example of WorklistDialog

For examples or demo please see also (Copy & Paste to Explorer Adress Field):

32Bit OS (WinNT/WinXP 32Bit) and below:

%PROGRAMFILES%\HAMILTON\Methods\Library Demo Methods\ASWStandardDialogs\\

64Bit OS (XP64/Vista/Windows7):

%PROGRAMFILES(X86)%\HAMILTON\Methods\Library Demo Methods\ASWStandardDialogs\\
