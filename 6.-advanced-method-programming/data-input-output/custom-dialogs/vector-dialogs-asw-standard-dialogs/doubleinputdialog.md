# DoubleInputDialog

## &#x20;Syntax

| <p> </p><p>LoginDialog (</p> | <p> </p><p>variable i_strDialogTitle,</p> |
| ---------------------------- | ----------------------------------------- |
|                              | variable i\_intButtonType,                |
|                              | variable i\_intDialogHeight,              |
|                              | variable i\_intDialogWidth,               |
|                              | variable i\_strMessage,                   |
|                              | variable i\_strMessage,                   |
|                              | variable i\_strErrorMessage,              |
|                              | variable \&o\_strBlindEntry               |
|                              | ) variable                                |
|                              |                                           |

## Description

Creates an DoubleInputDialog.

&#x20;

&#x20;

<figure><img src="../../../../.gitbook/assets/image (832).png" alt=""><figcaption></figcaption></figure>

Arguments & Return Values\
\



| argument           | range              | description                                                                                                              |
| ------------------ | ------------------ | ------------------------------------------------------------------------------------------------------------------------ |
| i\_strDialogTitle  | string             | dialog title shown in the header                                                                                         |
| i\_intButtonType   | integer \[0..7]    | button type class (Enumerations R)                                                                                       |
| i\_intDialogHeight | integer \[0..5999] | the height of the dialog in pixel (0 auto sizing)                                                                        |
| i\_intDialogWidth  | integer \[0..5999] | the width of the dialog in pixel (0 auto sizing)                                                                         |
| i\_strMessage      | string             | the text of the dialog (forced line break with \n)                                                                       |
| i\_strErrorMessage | string             | the error message for incorrect entered values                                                                           |
| o\_strBlindEntry   | string             | the return value is the validated blind entry                                                                            |
| return values      | integer \[-9..7]   | value of clicked dialog button (see also ASWGlobal.hsl) or error value (return value < 0, see also chapter ErrorCodes R) |

&#x20;

## &#x20;Example of DoubleInputDialog

For examples or demo please see also (Copy & Paste to Explorer Address Field):

&#x20;

32Bit OS (WinNT/WinXP 32Bit) and below:

%PROGRAMFILES%\HAMILTON\Methods\Library Demo Methods\ASWStandardDialogs\\

&#x20;

64Bit OS (XP64/Vista/Windows7):

%PROGRAMFILES(X86)%\HAMILTON\Methods\Library Demo Methods\ASWStandardDialogs\\
