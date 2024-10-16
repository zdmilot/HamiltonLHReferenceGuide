# ListDialog

| �ListDialog |   |
| ----------- | - |
| �Syntax     |   |

| ListDialog ( | variable i\_strDialogTitle,  |   |
| ------------ | ---------------------------- | - |
|              | variable i\_intIconType,     |   |
|              | variable i\_intButtonType,   |   |
|              | variable i\_intDialogHeight, |   |
|              | variable i\_intDialogWidth,  |   |
|              | variable i\_intTimeOut,      |   |
|              | variable i\_strTopText,      |   |
|              | variable i\_intBottomText,   |   |
|              | variable i\_arrList\[]       |   |
|              | ) variable                   |   |

Creates an List Dialog.

Each entry of i\_arrList\[] will be shown in a row of the ListDialog.

For i\_intTimeOut > 0:

a)    This dialog will be closed automatically if the timer counted down to 0 and there was no interaction by the user

(means moving mouse over dialog area or clicking header row).

b)    The Timer will be stopped as soon as there is an interaction by the user (example: mouse click or mouse move over dialog area).

In this case dialog have to be closed by the user.



| �Arguments & Return Values |   |
| -------------------------- | - |

| argument           | range              | description                                                                                                            | key |
| ------------------ | ------------------ | ---------------------------------------------------------------------------------------------------------------------- | --- |
| i\_strDialogTitle  | string             | dialog title shown in the header                                                                                       | b)  |
| i\_intIconType     | enum \[0..3]       | icon type (Enumerations R)                                                                                             | c)  |
| i\_intButtonType   | integer \[0..7]    | button type class (Enumerations R)                                                                                     | c)  |
| i\_intDialogHeight | integer \[0..5999] | the height of the dialog in pixel (0 auto sizing)                                                                      | f)  |
| i\_intDialogWidth  | integer \[0..5999] | the width of the dialog in pixel (0 auto sizing)                                                                       | g)  |
| i\_intTimeOut      | integer \[0..9999] | sets timeout for auto closing of dialog in seconds, 0 no Timeout                                                       |     |
| i\_strTopText      | string             | the text at the top of the dialog (forced line break with \n)                                                          | h)  |
| i\_strBottomText   | string             | the text at the bottom of the dialog (forced line break with \n)                                                       | i)  |
| i\_arrList\[]      | string array       | array of strings with data rows (single column)                                                                        | j)  |
| return values      | integer \[-9..7]   | value of clicked dialog button (see also ASWGlobal.hsl) or error value (return value < 0, see also chapter Errorcodes) |     |

For examples or demo please see also (Copy & Paste to Explorer Adress Field):

32Bit OS (WinNT/WinXP 32Bit) and below:

%PROGRAMFILES%\HAMILTON\Methods\Library Demo Methods\ASWStandardDialogs\\

64Bit OS (XP64/Vista/Windows7):

%PROGRAMFILES(X86)%\HAMILTON\Methods\Library Demo Methods\ASWStandardDialogs\\

| �� by Hamilton Bonaduz AG |   |
| ------------------------- | - |
