# LoadingDialog

| �LoadingDialog |   |
| -------------- | - |
| �Syntax        |   |

| LoadingDialog ( | variable i\_strDialogTitle,           |            |
| --------------- | ------------------------------------- | ---------- |
|                 | variable i\_intButtonType,            |            |
|                 | variable i\_intDialogHeight,          |            |
|                 | variable i\_intDialogWidth,           |            |
|                 | variable i\_intTimeOut,               |            |
|                 | variable i\_strTopText,               |            |
|                 | variable i\_strBottomText,            |            |
|                 | variable i\_strTopImage,              |            |
|                 | variable i\_strBottomImage,           |            |
|                 | variable i\_intMaxImageWidth,         |            |
|                 | variable i\_arrLabwarePositions\[],   |            |
|                 | variable i\_arrLabwareQuantities\[],  |            |
|                 | variable i\_arrLabwareDescriptions\[] | ) variable |
|                 |                                       |            |

Creates a Loading Dialog (optional with timeout auto closing).

For i\_intTimeOut > 0:

a)    This dialog will be closed automatically if the timer counted down to 0 and there was no interaction by the user

(means moving mouse over dialog area or clicking header row).

b)    The Timer will be stopped as soon as there is an interaction by the user (example: mouse click or mouse move over dialog area).

In this case dialog have to be closed by the user.

To customize the column captions of the list, use the function LoadingDialogSetResources.

The nominal height and width of an image is 100x100.



| �Arguments & Return Values |   |
| -------------------------- | - |

| argument                     | range              | description                                                                                                            |
| ---------------------------- | ------------------ | ---------------------------------------------------------------------------------------------------------------------- |
| i\_strDialogTitle            | string             | dialog title shown in the header                                                                                       |
| i\_intButtonType             | integer \[0..7]    | button type class (Enumerations R)                                                                                     |
| i\_intDialogHeight           | integer \[0..5999] | the height of the dialog in pixel (0 auto sizing)                                                                      |
| i\_intDialogWidth            | integer \[0..5999] | the width of the dialog in pixel (0 auto sizing)                                                                       |
| i\_intTimeOut                | integer \[0..0999] | sets timeout for auto closing of dialog in seconds, 0 no Timeout                                                       |
| i\_strTopText                | string             | the text at the top of the dialog (forced line break with \n)                                                          |
| i\_strBottomText             | string             | the text at the bottom of the dialog (forced line break with \n)                                                       |
| i\_strTopImage               | string             | full qualified image file (supported images are JPG, PNG)                                                              |
| i\_strBottomImage            | string             | full qualified image file (supported images are JPG, PNG)                                                              |
| i\_intMaxImageWidth          | integer            | max width for both images                                                                                              |
| i\_arrLabwarePositions\[]    | string array       | defines array for column of labware positions                                                                          |
| i\_arrLabwareQuantities\[]   | string array       | defines array for column of labware quantities                                                                         |
| i\_arrLabwareDescriptions\[] | string array       | defines array for column of labware descriptions                                                                       |
| return values                | integer \[-9..7]   | value of clicked dialog button (see also ASWGlobal.hsl) or error value (return value < 0, see also chapter Errorcodes) |

For examples or demo please see also (Copy & Paste to Explorer Adress Field):

32Bit OS (WinNT/WinXP 32Bit) and below:

%PROGRAMFILES%\HAMILTON\Methods\Library Demo Methods\ASWStandardDialogs\\

64Bit OS (XP64/Vista/Windows7):

%PROGRAMFILES(X86)%\HAMILTON\Methods\Library Demo Methods\ASWStandardDialogs\\

| �� by Hamilton Bonaduz AG |   |
| ------------------------- | - |
