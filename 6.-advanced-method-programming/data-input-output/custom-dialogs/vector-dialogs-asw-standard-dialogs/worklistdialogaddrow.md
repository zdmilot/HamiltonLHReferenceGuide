# WorklistDialogAddRow

## Syntax

| WorklistDialogAddRow ( | variable i\_intID,             |           |   |
| ---------------------- | ------------------------------ | --------- | - |
|                        | variable i\_intStatus,         |           |   |
|                        | variable i\_blnIsEditable,     |           |   |
|                        | variable i\_intProcessingMode, |           |   |
|                        | variable i\_arrValueColumns\[] | )variable |   |

Add a row in the work list view with default columns and custom columns.\
![](<../../../../.gitbook/assets/image (13) (1) (1) (1).png>)\


## Arguments & Return Values

| arguments              | range        | description                                                                                                                                       |
| ---------------------- | ------------ | ------------------------------------------------------------------------------------------------------------------------------------------------- |
| i\_intID               | integer      | id�s of the worklist view                                                                                                                         |
| i\_intStatus           | enum         | <p>WorklistStatus::Ok (Green)</p><p>WorklistStatus::Warning (Yellow)</p><p>WorklistStatus::Error (Red)</p><p>used for status (Enumerations R)</p> |
| i\_blnIsEditable       | boolean      | <p>true = row editable</p><p>false = row not editable</p>                                                                                         |
| i\_intProcessingMode   | enum         | <p>ProcessingMode::Process</p><p>ProcessingMode::Exclude</p><p>ProcessingMode::Remove</p><p>used for processing mode (Enumerations R)</p>         |
| i\_arrValueColumns\[]  | string array | string value rows                                                                                                                                 |
| return value           |              |                                                                                                                                                   |
| ASWGLOBAL::BOOL::TRUE  | boolean      | if successfully                                                                                                                                   |
| ASWGLOBAL::BOOL::FALSE |              |                                                                                                                                                   |

## Example of WorklistDialog

For examples or demo please see also (Copy & Paste to Explorer Adress Field):

32Bit OS (WinNT/WinXP 32Bit) and below:

%PROGRAMFILES%\HAMILTON\Methods\Library Demo Methods\ASWStandardDialogs\\

64Bit OS (XP64/Vista/Windows7):

%PROGRAMFILES(X86)%\HAMILTON\Methods\Library Demo Methods\ASWStandardDialogs\\
