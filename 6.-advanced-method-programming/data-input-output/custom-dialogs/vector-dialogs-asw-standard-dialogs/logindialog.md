# LoginDialog

## Syntax

| LoginDialog ( | variable i\_strDialogTitle,           |
| ------------- | ------------------------------------- |
|               | variable i\_intButtonType,            |
|               | variable i\_intDialogHeight,          |
|               | variable i\_intDialogWidth,           |
|               | variable i\_strMessage,               |
|               | variable i\_intEncryption,            |
|               | variable i\_intEncoding,              |
|               | variable i\_intEncodingCodepage,      |
|               | variable& o\_strUserName,             |
|               | variable& o\_strUserPassword,         |
|               | variable& o\_arrUserPasswordBytes\[], |
|               | ) variable                            |

Creates an LoginDialog.

<figure><img src="../../../../.gitbook/assets/image (9) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

## Arguments & Return Values

| argument                | range              | description                                                                                                            |
| ----------------------- | ------------------ | ---------------------------------------------------------------------------------------------------------------------- |
| i\_strDialogTitle       | string             | dialog title shown in the header                                                                                       |
| i\_intButtonType        | integer \[0..7]    | button type class (Enumerations R)                                                                                     |
| i\_intDialogHeight      | integer \[1..5999] | the height of the dialog in pixel (0 auto sizing)                                                                      |
| i\_intDialogWidth       | integer \[1..5999] | the width of the dialog in pixel (0 auto sizing)                                                                       |
| i\_strMessage           | string             | the text of the dialog (forced line break with \n)                                                                     |
| i\_intEncryption        | int \[1-6]         | encryption algorithm (Enumerations R)                                                                                  |
| i\_intEncoding          | int \[1-8]         | encoding to use (Enumerations R)                                                                                       |
| i\_intEncodingCodepage  | int                | Codepage for user defined encoding                                                                                     |
| o\_strUserName          | string             | Given user name                                                                                                        |
| o\_strUserPassword      | string             | Given user password as encrypted hex string or plain text in case of no encryption                                     |
| o\_arrUserPasswordBytes | array of byte      | Given user password as encrypted byte array                                                                            |
| return values           | integer \[-9..7]   | value of clicked dialog button (see also ASWGlobal.hsl) or error value (return value < 0, see also chapter Errorcodes) |

For examples or demo please see also (Copy & Paste to Explorer Address Field):

32Bit OS (WinNT/WinXP 32Bit) and below:

%PROGRAMFILES%\HAMILTON\Methods\Library Demo Methods\ASWStandardDialogs\LoginDialog\TestMethod\_LoginDialog.med

64Bit OS (XP64/Vista/Windows7):

%PROGRAMFILES(X86)%\HAMILTON\Methods\Library Demo Methods\ASWStandardDialogs\LoginDialog\TestMethod\_LoginDialog.med
