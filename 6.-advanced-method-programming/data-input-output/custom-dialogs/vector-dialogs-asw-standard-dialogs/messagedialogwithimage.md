# MessageDialogWithImage

## Syntax

| MessageDialogWithImage ( | variable i\_strDialogTitle,  |
| ------------------------ | ---------------------------- |
|                          | variable i\_intIconType,     |
|                          | variable i\_intButtonType,   |
|                          | variable i\_intDialogHeight, |
|                          | variable i\_intDialogWidth,  |
|                          | variable i\_intTimeOut,      |
|                          | variable i\_strMessage,      |
|                          | variable i\_strImage,        |
|                          | Variable i\_intMaxImageWidth |
|                          | ) variable                   |
|                          |                              |

Creates message dialog with an image.

For i\_intTimeOut > 0:

a)    This dialog will be closed automatically if the timer counted down to 0 and there was no interaction by the user

(means moving mouse over dialog area or clicking header row).

b)    The Timer will be stopped as soon as there is an interaction by the user (example: mouse click on dialog area or any key).

In this case dialog have to be closed by the user.

<figure><img src="../../../../.gitbook/assets/image (11).png" alt=""><figcaption></figcaption></figure>

## Arguments & Return Values

| argument            | range              | description                                                                                                            | key |
| ------------------- | ------------------ | ---------------------------------------------------------------------------------------------------------------------- | --- |
| i\_strDialogTitle   | string             | dialog title shown in the header                                                                                       | a)  |
| i\_intIconType      | integer \[0..3]    | used for dialog icon (Enumerations R)                                                                                  | i)  |
| i\_intButtonType    | integer \[0..7]    | button type class (Enumerations R)                                                                                     | c)  |
| i\_intDialogHeight  | integer \[0..5999] | the height of the dialog in pixel (0 auto sizing)                                                                      | f)  |
| i\_intDialogWidth   | integer \[0..5999] | the width of the dialog in pixel (0 auto sizing)                                                                       | g)  |
| i\_intTimeOut       | integer \[0..9999] | sets timeout for auto closing of dialog in seconds, 0 no Timeout                                                       |     |
| i\_strMessage       | string             | message of the dialog                                                                                                  | h)  |
| i\_strImage         | string             | full qualified image file                                                                                              | j)  |
| i\_intMaxImageWidth | integer \[0..5999] | max displaying width of the image                                                                                      | j)  |
| return values       | integer \[-9..7]   | value of clicked dialog button (see also ASWGlobal.hsl) or error value (return value < 0, see also chapter Errorcodes) |     |

## Example of MessageDialogWithImage

For examples or demo please see also (Copy & Paste to Explorer Adress Field):

32Bit OS (WinNT/WinXP 32Bit) and below:

%PROGRAMFILES%\HAMILTON\Methods\Library Demo Methods\ASWStandardDialogs\\

64Bit OS (XP64/Vista/Windows7):

%PROGRAMFILES(X86)%\HAMILTON\Methods\Library Demo Methods\ASWStandardDialogs\\
