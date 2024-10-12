# Initialize

Syntax

```clike
Initialize(variable i_strTitleDialog)
```

&#x20;

***

## Description

&#x20;

This function creates the com object ‘Hamilton.AswStatusDialogViewController’ and shows a dialog in the top right corner on the main screen.

&#x20;

### **Hints:**

It is very important to call this function whenever you use the object ‘Hamilton.AswStatusDialogViewController’. This function is always at the beginning.

&#x20;

***

## Arguments

&#x20;

| Argument          | Type   | Description                                                                                                                                      |
| ----------------- | ------ | ------------------------------------------------------------------------------------------------------------------------------------------------ |
| i\_strTitleDialog | string | Dialog Title to be displayed. This is an optional Parameter. If the parameter is empty is reported as the standard title dialog "Status Window". |

&#x20;

***

## Return Values

&#x20;

Function returns ASWGLOBAL::BOOL::TRUE if successful, ASWGLOBAL::BOOL::FALSE in case an error occurred.

&#x20;
