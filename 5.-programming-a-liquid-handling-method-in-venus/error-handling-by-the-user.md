# Error Handling by the User

This command allows the user to handle errors occurring at runtime (e.g. a step 'File Open' creates a runtime error if the file not can opened).

If a runtime error occurs, the command branches into a different program path.

&#x20;

The command generates three entries in the method:

| ![](<../.gitbook/assets/image (64).png>)  (1. entry):           | Begin Error Handling by the User.                     |
| --------------------------------------------------------------- | ----------------------------------------------------- |
|   ![](<../.gitbook/assets/image (1) (1) (1) (1).png>)(2. entry) | End Error Handling by the User / Begin Error Handler. |
|  ![](<../.gitbook/assets/image (2) (1) (1) (1).png>) (3. entry) | End Error Handler                                     |

All errors occurring during the steps execution in the observed part (steps between the 1. and the 2. entry) are handled by the user. This means, that in case of an error the program execution continues immediately at the first step in the error handler.

It is not possible to use another step of type 'Error handling by the User' in the observed part.

&#x20;

The steps in the error handler (steps between the 2. and the 3. entry) are only proceeded if an error occurs in the observed part. After execution of the error handler, the method execution continues with the next step after the 3. entry.

It is possible to encase steps of type 'Error handling by the User' in the error handler to observe any steps of the error handler.

**Note:**

Without any error handling by the user, a runtime error aborts the method execution immediately and an error information dialog will be displayed.

&#x20;

The 'Error Handling by the User' Step is working incorrectly in the OnAbort sub-method. This is also the case for steps executed in an abort handler (See RegisterAbortHandler function in Utils library).

&#x20;

A workaround for this limitation is to add a HSL statement to ignore subsequent errors. Use the 'Insert HSL Code' command from the Edit menu or from the context menu and add the following HSL code in the dialog box: onerror resume next;
