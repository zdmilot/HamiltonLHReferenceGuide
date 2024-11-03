# CheckBoxDialog

## Syntax

| <p> </p><p>CheckBoxDialog(</p> | <p> </p><p>variable i_strDialogTitle,</p>  |
| ------------------------------ | ------------------------------------------ |
|                                | variable i\_intButtonType,                 |
|                                | variable i\_intDialogHeight ,              |
|                                | variable i\_intDialogWidth,                |
|                                | variable i\_strTopText,                    |
|                                | variable i\_strBottomText,                 |
|                                | variable i\_arrLabels\[],                  |
|                                | variable i\_arrTooltips\[],                |
|                                | variable i\_arrIsEditable\[],              |
|                                | variable \&io\_arrIsSelected\[] ) variable |

## Description

Creates a n-CheckBox Dialog.

&#x20;![](<../../../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png>)

&#x20;

Arguments & Return Values\



| argument             | range              | description                                                                                                                                                                                                                                                                                        |
| -------------------- | ------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| i\_strDialogTitle    | string             | dialog title shown in the header                                                                                                                                                                                                                                                                   |
| i\_intButtonType     | integer \[0..7]    | button type class (Enumerations R)                                                                                                                                                                                                                                                                 |
| i\_intDialogHeight   | integer \[0..5999] | the height of the dialog in pixel (0 auto sizing)                                                                                                                                                                                                                                                  |
| i\_intDialogWidth    | integer \[0..5999] | the width of the dialog in pixel (0 auto sizing)                                                                                                                                                                                                                                                   |
| i\_strTopText        | string             | message at the top of the dialog (optional)                                                                                                                                                                                                                                                        |
| i\_strBottomText     | string             | message at the bottom of the dialog (optional)                                                                                                                                                                                                                                                     |
| i\_arrLabels\[]      | string array       | label / description of a rows                                                                                                                                                                                                                                                                      |
| i\_arrTooltips\[]    | string array       | the tooltip for a row / checkbox (optional)                                                                                                                                                                                                                                                        |
| i\_arrIsEditable\[]  | integer array      | <p>defines if the given checkbox is editable for the user (optional),</p><p>use the value 1 to set the concerned checkbox editable, with 0 the user cannot check or uncheck the checkbox with user interaction,</p><p>preselection is only possible with the array i_arrIsSelected (see below)</p> |
| io\_arrIsSelected\[] | integer array      | <p>defines the pre-selection of each checkbox (optional, only initialized array is required) and returns selected</p><p>use 1 to pre-select concerned checkbox, you can pre-select not editable checkboxes too, 0 means checkbox is not pre-selected</p>                                           |
| return values        | Integer \[-9..7]   | value of clicked dialog button (see also ASWGlobal.hsl) or error value (return value < 0, see also chapter ErrorCodes R)                                                                                                                                                                           |

&#x20;

&#x20;

## Example of CheckBoxDialog

For examples or demo please see also (Copy & Paste to Explorer Address Field):

32Bit OS (WinNT/WinXP 32Bit) and below:

%PROGRAMFILES%\HAMILTON\Methods\Library Demo Methods\ASWStandardDialogs\\

64Bit OS (XP64/Vista/Windows7):

%PROGRAMFILES(X86)%\HAMILTON\Methods\Library Demo Methods\ASWStandardDialogs\\

&#x20;
