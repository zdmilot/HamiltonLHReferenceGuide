# WorklistDialogSetResources

## Syntax

| WorklistDialogSetResources ( | variable i\_strDialogTitle,                    |   |
| ---------------------------- | ---------------------------------------------- | - |
|                              | variable i\_strSaveAndCloseCaption,            |   |
|                              | variable i\_strResetCaption,                   |   |
|                              | variable i\_strCaptionSelectedRows             |   |
|                              | variable i\_strSampleModeProcessText,          |   |
|                              | variable i\_strSampleModeExcludeText,          |   |
|                              | variable i\_strSampleModeRemoveText,           |   |
|                              | variable i\_strSetAllToProcessButtonText,      |   |
|                              | variable i\_strSetAllToExcludeButtonText,      |   |
|                              | variable i\_strSetAllToRemoveButtonText        |   |
|                              | variable i\_strLegendRowStatusOKText           |   |
|                              | variable i\_strLegendRowStatusWarningText      |   |
|                              | variable i\_strLegendRowStatusErrorText        |   |
|                              | variable i\_strLegendProcessingModeProcessText |   |
|                              | variable i\_strLegendProcessingModeExcludeText |   |
|                              | variable i\_strLegendProcessingModeRemoveText  |   |
|                              | ) variable                                     |   |

Sets the generic resources in the work list view like dialog titles, labels, the button text and the button tooltips.

![](<../../../../.gitbook/assets/image (17) (1).png>)\
\


## Arguments & Return Values

| arguments                             | range   | description                                 |
| ------------------------------------- | ------- | ------------------------------------------- |
| i\_strDialogTitle                     | string  | dialog title                                |
| i\_strSaveAndCloseCaption             | string  | caption of the button �confirm�             |
| i\_strResetCaption                    | string  | caption of the button �reset�               |
| i\_strCaptionSelectedRows             | string  | caption of the label �Items to process�     |
| i\_strSampleModeProcessText           | string  | label of the radio button �Process�         |
| i\_strSampleModeExcludeText           | string  | label of the radio button �Exclude�         |
| i\_strSampleModeRemoveText            | string  | label of the radio button �Remove�          |
| i\_strSetAllToProcessButtonText       | string  | text of the button �Process all�            |
| i\_strSetAllToExcludeButtonText       | string  | text of the button �Exclude all�            |
| i\_strSetAllToRemoveButtonText        | string  | text of the button �Remove all�             |
| i\_strLegendRowStatusOKText           | string  | text for the icon description in the legend |
| i\_strLegendRowStatusWarningText      | string  | text for the icon description in the legend |
| i\_strLegendRowStatusErrorText        | string  | text for the icon description in the legend |
| i\_strLegendProcessingModeProcessText | string  | text for the icon description in the legend |
| i\_strLegendProcessingModeExcludeText | string  | text for the icon description in the legend |
| i\_strLegendProcessingModeRemoveText  | string  | text for the icon description in the legend |
| return value                          |         |                                             |
| ASWGLOBAL::BOOL::TRUE                 | boolean | if successful                               |
| ASWGLOBAL::BOOL::FALSE                |         |                                             |
|                                       |         |                                             |

## Example of WorklistDialog

For examples or demo please see also (Copy & Paste to Explorer Adress Field):

32Bit OS (WinNT/WinXP 32Bit) and below:

%PROGRAMFILES%\HAMILTON\Methods\Library Demo Methods\ASWStandardDialogs\\

64Bit OS (XP64/Vista/Windows7):

%PROGRAMFILES(X86)%\HAMILTON\Methods\Library Demo Methods\ASWStandardDialogs\\
