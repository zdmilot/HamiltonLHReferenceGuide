# ListSelectDialog

## Syntax

| ListSelectDialog ( | variable i\_strDialogTitle,   |            |
| ------------------ | ----------------------------- | ---------- |
|                    | variable i\_intButtonType,    |            |
|                    | variable i\_intDialogHeight,  |            |
|                    | variable i\_intDialogWidth,   |            |
|                    | variable i\_strTopText,       |            |
|                    | variable i\_strBottomText,    |            |
|                    | variable i\_arrListValues\[], |            |
|                    | variable \&o\_strSelection    | ) variable |
|                    |                               |            |

Creates an List Select Dialog.

<figure><img src="../../../../.gitbook/assets/image (7) (1) (1).png" alt=""><figcaption></figcaption></figure>

## Arguments & Return Values

| argument           | range              | description                                                                                                            |
| ------------------ | ------------------ | ---------------------------------------------------------------------------------------------------------------------- |
| i\_strDialogTitle  | string             | dialog title shown in the header                                                                                       |
| i\_intButtonType   | integer \[0..7]    | button type class (Enumerations R)                                                                                     |
| i\_intDialogHeight | integer \[1..5999] | the height of the dialog in pixel (0 auto sizing)                                                                      |
| i\_intDialogWidth  | integer \[1..5999] | the width of the dialog in pixel (0 auto sizing)                                                                       |
| i\_strTopText      | string             | the text at the top of the dialog (forced line break with \n)                                                          |
| i\_strBottomText   | string             | the text at the bottom of the dialog (forced line break with \n)                                                       |
| i\_arrListVales\[] | string array       | array of strings with data rows (single column)                                                                        |
| \&o\_strSelection  | string             | the selected value, if selected                                                                                        |
| return values      | integer \[-9..7]   | value of clicked dialog button (see also ASWGlobal.hsl) or error value (return value < 0, see also chapter Errorcodes) |

## Example of ListSelectDialog

For examples or demo please see also (Copy & Paste to Explorer Adress Field):

32Bit OS (WinNT/WinXP 32Bit) and below:

%PROGRAMFILES%\HAMILTON\Methods\Library Demo Methods\ASWStandardDialogs\\

64Bit OS (XP64/Vista/Windows7):

%PROGRAMFILES(X86)%\HAMILTON\Methods\Library Demo Methods\ASWStandardDialogs\\
