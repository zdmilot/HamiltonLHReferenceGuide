# ImageRadioButtonDialog

| ImageRadioButtonDialog |   |
| ---------------------- | - |
| �Syntax                |   |

| ImageRadioButtonDialog( | variable i\_strDialogTitle,     |   |
| ----------------------- | ------------------------------- | - |
|                         | variable i\_intButtonType,      |   |
|                         | variable i\_intDialogHeight ,   |   |
|                         | variable i\_intDialogWidth,     |   |
|                         | variable i\_strTopText,         |   |
|                         | variable i\_strBottomText,      |   |
|                         | variable i\_arrLabels\[],       |   |
|                         | variable i\_arrTooltips\[],     |   |
|                         | variable i\_arrIsEditable\[],   |   |
|                         | variable i\_arrImageSource\[],  |   |
|                         | variable i\_arrImageHeight\[],  |   |
|                         | variable i\_arrImageWidth\[],   |   |
|                         | variable \&io\_arrIsSelected\[] |   |
|                         | variable i\_arrGroupName\[],    |   |
|                         | variable i\_intWrapOrientation, |   |
|                         | variable i\_intSortDirection    |   |
|                         | ) variable                      |   |

Creates a n-ImageRadioButton Dialog.



| �Arguments & Return Values |   |
| -------------------------- | - |

| argument              | range              | description                                                                                                                                                                                                  |
| --------------------- | ------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| i\_strDialogTitle     | string             | dialog title shown in the header                                                                                                                                                                             |
| i\_intButtonType      | integer \[0..7]    | button type class (Enumerations R)                                                                                                                                                                           |
| i\_intDialogHeight    | integer \[0..5999] | the height of the dialog in pixel (0 auto sizing)                                                                                                                                                            |
| i\_intDialogWidth     | integer \[0..5999] | the width of the dialog in pixel (0 auto sizing)                                                                                                                                                             |
| i\_strTopText         | string             | message at the top of the dialog (optional)                                                                                                                                                                  |
| i\_strBottomText      | string             | message at the bottom of the dialog (optional)                                                                                                                                                               |
| i\_arrLabels\[]       | string array       | label / description of a rows                                                                                                                                                                                |
| i\_arrTooltips\[]     | string array       | the tooltip for a row / radiobutton (optional)                                                                                                                                                               |
| i\_arrIsEditable\[]   | integer array      | is the given radiobutton editable for the user (optional)                                                                                                                                                    |
| i\_arrImageSource\[]  | string array       | image source (fullpath) for the radiobutton                                                                                                                                                                  |
| i\_arrImageHeight\[]  | integer array      | image height for the radiobutton, between 40-500                                                                                                                                                             |
| i\_arrImageWidth\[]   | integer array      | image width for the radiobutton, between 40-500                                                                                                                                                              |
| io\_arrIsSelected\[]  | integer array      | defines the preselection of each checkbox / returns selected radiobutton/s                                                                                                                                   |
| i\_arrGroupName\[]    | string array       | defines the optional groups for different radiobutton groupings (optional)                                                                                                                                   |
| i\_intWrapOrientation | integer\[0..1]     | <p>sets the orientation of the group content layout container, horizontal or vertical</p><p>(Enumerations R)</p>                                                                                             |
| i\_intSortDirection   | integer \[0..2]    | <p>defines the sorting direction for the labels (important for the arrangement in a group)</p><p>if you choose �Unsorted� your given order by default (array i_arrLabels) is used</p><p>(Enumerations R)</p> |
| return values         | integer \[-9..7]   | value of clicked dialog button (see also ASWGlobal.hsl) or error value (return value < 0, see also chapter Errorcodes)                                                                                       |

| Example of RadioButtonDialog |   |
| ---------------------------- | - |

For examples or demo please see also (Copy & Paste to Explorer Address Field):

32Bit OS (WinNT/WinXP 32Bit) and below:

%PROGRAMFILES%\HAMILTON\Methods\Library Demo Methods\ASWStandardDialogs\\

64Bit OS (XP64/Vista/Windows7):

%PROGRAMFILES(X86)%\HAMILTON\Methods\Library Demo Methods\ASWStandardDialogs\\

| �� by Hamilton Bonaduz AG |   |
| ------------------------- | - |
