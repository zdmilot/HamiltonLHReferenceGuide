# DirectoryBrowserDialog

## Syntax

| DirectoryBrowserDialog ( | variable i\_strDialogTitle,         |
| ------------------------ | ----------------------------------- |
|                          | variable i\_intButtonType,          |
|                          | variable i\_intDialogHeight,        |
|                          | variable i\_intDialogWidth,         |
|                          | variable i\_strMessage,             |
|                          | variable i\_strCaptionBrowseButton, |
|                          | variable i\_strFolderDialogMessage, |
|                          | variable i\_strInitialDirectory,    |
|                          | variable \&o\_strSelectedFolder,    |
|                          | ) variable                          |
|                          |                                     |

## Description

Creates a DirectoryBrowser Dialog.

<figure><img src="../../../../.gitbook/assets/image (831).png" alt=""><figcaption></figcaption></figure>

## Arguments & Return Values

| argument                  | range              | description                                                                                                            |
| ------------------------- | ------------------ | ---------------------------------------------------------------------------------------------------------------------- |
| i\_strDialogTitle         | string             | dialog title shown in the header                                                                                       |
| i\_intButtonType          | integer \[0..7]    | button type class (Enumerations R)                                                                                     |
| i\_intDialogHeight        | integer \[0..5999] | the height of the dialog in pixel (0 auto sizing)                                                                      |
| i\_intDialogWidth         | integer \[0..5999] | the width of the dialog in pixel (0 auto sizing)                                                                       |
| i\_strMessage             | string             | the text of the dialog (forced line break with \n)                                                                     |
| i\_strCaptionBrowseButton | string             | <p>the caption of the browse button (maybe “…” or “select file …”)</p><p>default is “browse”</p>                       |
| i\_strFolderDialogMessage | string             | The displayed message in the windows directory browser dialog                                                          |
| i\_strInitialDirectory    | string             | initial directory                                                                                                      |
| o\_strSelectedFolder      | string             | the selected directory, if selected, in case of cancel, the initial directory is returned                              |
| return values             | integer \[-9..7]   | value of clicked dialog button (see also ASWGlobal.hsl) or error value (return value < 0, see also chapter Errorcodes) |

## Example of DirectoryBrowserDialog

For examples or demo please see also (Copy & Paste to Explorer Address Field):

32Bit OS (WinNT/WinXP 32Bit) and below:

%PROGRAMFILES%\HAMILTON\Methods\Library Demo Methods\ASWStandardDialogs\\

64Bit OS (XP64/Vista/Windows7):

%PROGRAMFILES(X86)%\HAMILTON\Methods\Library Demo Methods\ASWStandardDialogs\\
