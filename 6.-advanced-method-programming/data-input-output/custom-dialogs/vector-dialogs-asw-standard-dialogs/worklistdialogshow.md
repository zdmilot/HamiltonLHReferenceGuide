# WorklistDialogShow

| WorklistDialogShow |   |
| ------------------ | - |
| �Syntax            |   |

| WorklistDialogShow ( | variable i\_intDialogHeight,   |   |
| -------------------- | ------------------------------ | - |
|                      | variable i\_intDialogWidth,    |   |
|                      | variable & o\_arrIDsToProcess, |   |
|                      | variable & o\_arrIDsToExclude, |   |
|                      | variable & o\_arrIDsToRemove   |   |
|                      | ) variable                     |   |

Shows the WorklistDialog und gets the result arrays.



Note that the WorklistDialog has to be initialized first by using following functions in correct order,

1 � 5 calling order is not important.

1\.       WorklistDialogSetResources ����������������������������� (optional)

2\.       WorklistDialogSetTextField ������������������������������� (optional)

3\.       WorklistDialogSetSelectedColumn �������������������� (optional)

4\.       WorklistDialogSetStatusColumn ������������ ������������(optional)

5\.       WorklistDialogSetEditMode������������������������������� (optional)

6\.       WorklistDialogSetLegendVisibility���������������������� (optional)

7\.       WorklistDialogSetColumns ������������������������������� (mandatory)

8\.       WorklistDialogAddRow ������������������������������������� (for each entry - mandatory)

9\.       WorklistDialogShow

| �Arguments & Return Values |   |
| -------------------------- | - |

| arguments              | range             | description                                       |
| ---------------------- | ----------------- | ------------------------------------------------- |
| i\_intDialogHeight     | integer \[0�5999] | the height of the dialog in pixel (0 auto sizing) |
| i\_intDialogWidth      | integer \[0�5999] | the width of the dialog in pixel (0 auto sizing)  |
| o\_arrIDsToProcess     | integer array     | returns the row ids of the sample to process      |
| o\_arrIDsToExclude     | integer array     | returns the row ids of the sample to exclude      |
| o\_arrIDsToRemove      | integer array     | returns the row ids of the sample to remove       |
| return value           | range             | description                                       |
| ASWGLOBAL::BOOL::TRUE  | boolean           | true if successfully set                          |
| ASWGLOBAL::BOOL::FALSE |                   |                                                   |

| Example of WorklistDialogShow |   |
| ----------------------------- | - |

For examples or demo please see also (Copy & Paste to Explorer Adress Field):

32Bit OS (WinNT/WinXP 32Bit) and below:

%PROGRAMFILES%\HAMILTON\Methods\Library Demo Methods\ASWStandardDialogs\\

64Bit OS (XP64/Vista/Windows7):

%PROGRAMFILES(X86)%\HAMILTON\Methods\Library Demo Methods\ASWStandardDialogs\\

| �� by Hamilton Bonaduz AG |   |
| ------------------------- | - |
