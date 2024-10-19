# SetStatusText

### Syntax

**SetStatusText (** variable i\_strStatusDialogText **)**

### Description

Displays the given text in the status dialog window. The previous window content will be removed before displaying the given text. Call this method with an empty string to clean up the status dialog window.

### Arguments

| **Argument**            | **Type** | **Description**                                   |
| ----------------------- | -------- | ------------------------------------------------- |
| i\_str StatusDialogText | string   | Text associated with the control to be displayed. |

**Return Values**

Function returns ASWGLOBAL::BOOL::TRUE if successful, ASWGLOBAL::BOOL::FALSE in case an error occurred.
