# SetStatusText

## Syntax

```clike
SetStatusText(variable i_strStatusDialogText)
```

***

## Description

&#x20;

Displays the given text in the status dialog window. The previous window content will be removed before displaying the given text. Call this method with an empty string to clean up the status dialog window.

&#x20;

***

## Arguments

&#x20;

| Argument                | Type   | Description                                       |
| ----------------------- | ------ | ------------------------------------------------- |
| i\_str StatusDialogText | string | Text associated with the control to be displayed. |

&#x20;

***

## Return Values

&#x20;

Function returns ASWGLOBAL::BOOL::TRUE if successful, ASWGLOBAL::BOOL::FALSE in case an error occurred.

&#x20;\
\
