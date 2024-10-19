# ErrorDialog

## Syntax

| <p> </p><p>ErrorDialog (</p> | <p> </p><p>variable i_strDialogTitle, </p> |
| ---------------------------- | ------------------------------------------ |
|                              | variable i\_intIconType,                   |
|                              | variable i\_intButtonType,                 |
|                              | variable i\_intDialogHeight,               |
|                              | variable i\_intDialogWidth,                |
|                              | variable i\_intTimeOut,                    |
|                              | variable i\_strMainMessage,                |
|                              | variable i\_strSupplementMessage           |
|                              | ) variable                                 |
|                              |                                            |

## Description

Creates a ErrorDialog.

&#x20;

![](blob:https://app.gitbook.com/573527e1-d594-4948-a4c3-496ae291f9b5)

&#x20;

&#x20;

&#x20;

## Arguments & Return Values

| argument                | range              | description                                                                                                            |
| ----------------------- | ------------------ | ---------------------------------------------------------------------------------------------------------------------- |
| i\_strDialogTitle       | string             | dialog title shown in the header                                                                                       |
| i\_intIconType          | integer \[0..3]    | used icon ([Enumerations R](chm://9c15f7be7941d7f53742b745f35e8edc/Enums.htm))                                         |
| i\_intButtonType        | integer \[0..7]    | button type class ([Enumerations R](chm://9c15f7be7941d7f53742b745f35e8edc/Enums.htm))                                 |
| i\_intDialogHeight      | integer \[0..5999] | the height of the dialog in pixel (0 auto sizing)                                                                      |
| i\_intDialogWidth       | integer \[0..5999] | the width of the dialog in pixel (0 auto sizing)                                                                       |
| i\_strMainMessage       | string             | Main messafe of the error (bold)                                                                                       |
| i\_strSupplementMessage | integer \[0..1]    | Extend message information                                                                                             |
| return values           | integer \[-9..7]   | value of clicked dialog button (see also ASWGlobal.hsl) or error value (return value < 0, see also chapter Errorcodes) |

&#x20;

&#x20;

## Example of FileBrowserDialog

For examples or demo please see also (Copy & Paste to Explorer Adress Field):

&#x20;

32Bit OS (WinNT/WinXP 32Bit) and below:&#x20;

%PROGRAMFILES%\HAMILTON\Methods\Library Demo Methods\ASWStandardDialogs\\

&#x20;

64Bit OS (XP64/Vista/Windows7):&#x20;

%PROGRAMFILES(X86)%\HAMILTON\Methods\Library Demo Methods\ASWStandardDialogs\\
