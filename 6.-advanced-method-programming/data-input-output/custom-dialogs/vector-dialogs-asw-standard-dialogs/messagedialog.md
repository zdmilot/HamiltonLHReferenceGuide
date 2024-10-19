# MessageDialog

## Syntax

| MessageDialog ( | variable i\_strDialogTitle,  |
| --------------- | ---------------------------- |
|                 | variable i\_intIconType,     |
|                 | variable i\_intButtonType,   |
|                 | variable i\_intDialogHeight, |
|                 | variable i\_intDialogWidth,  |
|                 | variable i\_intTimeOut,      |
|                 | variable i\_strMessage       |
|                 | ) variable                   |

Creates a message dialog (optional with timeout auto closing).

For i\_intTimeOut > 0:

a)     This dialog will be closed automatically if the timer counted down to 0 and there was no interaction by the user

(means moving mouse over dialog area or clicking header row).

b)    The Timer will be stopped as soon as there is an interaction by the user (example: mouse click or mouse move over dialog area).

In this case dialog have to be closed by the user.

<figure><img src="../../../../.gitbook/assets/image (10) (1) (1).png" alt=""><figcaption></figcaption></figure>

## Arguments & Return Values

| argument           | range              | description                                                                                                            |
| ------------------ | ------------------ | ---------------------------------------------------------------------------------------------------------------------- |
| i\_strDialogTitle  | string             | dialog title shown in the header                                                                                       |
| i\_intIconType     | integer \[0..3]    | used for icon (Enumerations R)                                                                                         |
| i\_intButtonType   | integer \[0..7]    | button type class (Enumerations R)                                                                                     |
| i\_intDialogHeight | integer \[0..5999] | the height of the dialog in pixel (0 auto sizing)                                                                      |
| i\_intDialogWidth  | integer \[0..5999] | the width of the dialog in pixel (0 auto sizing)                                                                       |
| i\_intTimeOut      | integer \[0..9999] | sets timeout for auto closing of dialog in seconds, 0 no Timeout                                                       |
| i\_strMessage      | string             | the dialog message displayed                                                                                           |
| return values      | integer \[-9..7]   | value of clicked dialog button (see also ASWGlobal.hsl) or error value (return value < 0, see also chapter Errorcodes) |

For examples or demo please see also (Copy & Paste to Explorer Adress Field):

32Bit OS (WinNT/WinXP 32Bit) and below:

%PROGRAMFILES%\HAMILTON\Methods\Library Demo Methods\ASWStandardDialogs\\

64Bit OS (XP64/Vista/Windows7):

%PROGRAMFILES(X86)%\HAMILTON\Methods\Library Demo Methods\ASWStandardDialogs\\
