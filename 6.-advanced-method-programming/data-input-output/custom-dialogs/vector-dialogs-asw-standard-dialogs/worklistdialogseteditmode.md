# WorklistDialogSetEditMode

## Syntax

| WorklistDialogSetEditMode( | variable i\_intEditMode | )variable |
| -------------------------- | ----------------------- | --------- |

Set the edit mode of the work list view. According to the selected edit mode the visibility of the radio buttons and buttons will changed.

![](<../../../../.gitbook/assets/image (15) (1) (1) (1) (1).png>)\
\


## Arguments & Return Values

| arguments              | range   | description                                                                                                                                                          |
| ---------------------- | ------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| i\_intEditMode         | enum    | <p>WorklistEditMode::ProcessExcludeRemove</p><p>WorklistEditMode::ProcessExclude</p><p>WorklistEditMode::ProcessRemove</p><p>used for edit mode (Enumerations R)</p> |
| return value           |         |                                                                                                                                                                      |
| ASWGLOBAL::BOOL::TRUE  | boolean | if successfully                                                                                                                                                      |
| ASWGLOBAL::BOOL::FALSE |         |                                                                                                                                                                      |

## Example of WorklistDialog

For examples or demo please see also (Copy & Paste to Explorer Adress Field):

32Bit OS (WinNT/WinXP 32Bit) and below:

%PROGRAMFILES%\HAMILTON\Methods\Library Demo Methods\ASWStandardDialogs\\

64Bit OS (XP64/Vista/Windows7):

%PROGRAMFILES(X86)%\HAMILTON\Methods\Library Demo Methods\ASWStandardDialogs\\
