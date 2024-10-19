# Initialize

### Syntax

**Initialize (** variable i\_strTitleDialog **)**

### Description

This function creates the com object ‘Hamilton.AswStatusDialogViewController’ and shows a dialog in the top right corner on the main screen.

### Hints:

It is very important to call this function whenever you use the object ‘Hamilton.AswStatusDialogViewController’. This function is always at the beginning.

### Arguments

| **Argument**      | **Type** | **Description**                                                                                                                                  |
| ----------------- | -------- | ------------------------------------------------------------------------------------------------------------------------------------------------ |
| i\_strTitleDialog | string   | Dialog Title to be displayed. This is an optional Parameter. If the parameter is empty is reported as the standard title dialog "Status Window". |

**Return Values**

Function returns ASWGLOBAL::BOOL::TRUE if successful, ASWGLOBAL::BOOL::FALSE in case an error occurred.
