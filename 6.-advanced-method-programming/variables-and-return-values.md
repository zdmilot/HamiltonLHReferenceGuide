# Variables and Return Values

## Variables

Within a method, the programmer will naturally define and process variables. There are two ways to specify variables:

1. Use the “Assignment / Assignment with calculation steps” from the “General Steps”.
2.  Type in the variable and the value needed and confirm with \[OK].

    \


    ![image](../.gitbook/assets/Image\_595.jpg)

    \

3. Activate the “Variables and Constants” Screen shown below in the “View  Variables” Menu or with \[ALT + F7].
4.  To create a new variable, trigger the Context Menu with a right click in the Variables and Constants scree, and select “New”.

    \


    ![image](../.gitbook/assets/Image\_596.png)
5.  Type in the name, type, scope, start value and the description (optional). Confirm the entries with \[OK].

    \


    ![image](../.gitbook/assets/Image\_597.jpg)

    \

6.  The new variable is now available in the method.

    \


    The method editor supports three kinds of variables with differing scope:

    \


    | Local variables:      | Valid only within a sub-method. All variables declared inside a sub-method automatically have a local scope. Local variables can be promoted to “Task local variables” through the “Method Export local variable” Menu.                                                                                                                                                                                                            |
    | --------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
    | Task local variables: | Valid within a method. All sub-methods have access to variables of this type. Local variables and Task local variables with identical names can coexist however, it is recommended to use naming conventions or prefixes. Such variables are generated when they are declared within the main program, or for example, within the method. When the method is scheduled, each task will have its own task local variable.            |
    | Global variables:     | <p>Can be accessed by all tasks using a method (see the Scheduler Manual). They can be declared in the Method Editor through the “Method  Global variables” Menu. This menu option can also promote a Task local variable to a global variable.</p><p>If a workflow contains a task local variable and a global variable with the</p><p>same name, a name conflict occurs. In this case, a syntax error hint will be signaled.</p> |



<table data-header-hidden><thead><tr><th width="145"></th><th></th></tr></thead><tbody><tr><td><img src="../.gitbook/assets/image (10) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" data-size="original"></td><td><p>NOTE</p><p>It is important to avoid mixing and confusing local and global variables. If possible, use naming conventions allowing the identification of each variable type:</p><p>GV&#x3C;variable name> for global variables used for all tasks of the same method</p><p>TV&#x3C;variable name> for task local variables used in one method</p><p>LV&#x3C;variable name> for local variables used in a sub-method</p><p>It is not possible to define variables which are valid in a method without being also valid in the related sub-methods. For this requirement, define task local variables with reserved names, e.g.:</p><p>MLV&#x3C;variable name> for local variables used in a method.</p></td></tr></tbody></table>

\


The Graphical Method Editor provides variables which can accommodate three sub-types of variables without explicit declaration:

* Integers (numbers)
* Floats (floating point numbers)
*   Strings (text variables and characters)

    Variables can be newly defined within the dialogs, if they occur in the following:
* Left-hand side of an equation (e.g. x=0, or x=t+1), or
* Within entry fields that hold only one variable

If not requested (as it is the case for the “Open File” Dialog), the variable types are identified automatically. For example, f=5 will generate a variable f of type integer.

\


<table data-header-hidden><thead><tr><th width="145"></th><th></th></tr></thead><tbody><tr><td><img src="../.gitbook/assets/image (10) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" data-size="original"></td><td>NOTE<br><em>To define a string (text) variable through the assignment step, the text must be enclosed in quotation marks, e.g. “s” = “Test”. The variable “s” is then of type string. Otherwise, the contents of a variable named “Test” and its contents will be assigned to s. If the “Test” variable does not exist, a warning will be prompted.</em><br><br><img src="../.gitbook/assets/image (536).png" alt=""></td></tr></tbody></table>

\


Variables once defined show up in the drop-down list of all input fields of a method. Syntax

For variable names, do not

− place numbers at the beginning

− use blanks or signs other than the underscore (“”) Variable names are case-sensitive.

To define a path within a string variable in the course of programming, use the double backslash (“\”) - e.g. “c:\programfiles\hamilton\methods\“. To define a path at run time by typing it into an input box, use single backslash (“\</b>“). The reason for this is that variables defined in the course of programming are analyzed for escape sequences (for example single backslash “\</b>”), and single backslash followed by n (““) means “new line”.

\


## Return Values‌

Often times, the steps used will return data when the step is executed. A typical example would be a mathematical function, like a simple assignment x=0.

Dialog functions or instrument steps can also return data:

* Dialog functions will provide a code of the button pressed upon exit enabling the method to continue depending on the button pressed in a particular dialog.
* Instrument steps can, for example, return a temperature for the TCC (Temperature- Controlled Carrier) or a pressure value for the BVS / CVS.

\


### Example 1 (Function Call)

Using the "Round" Function of the HLSMth library leads to the dialog below showing an entry field "Bind return value to:" which by default is empty. Select a variable listed in the dropdown list or enter a variable name, even one that does not yet exist. Leaving this field empty means that there is no variable where the rounded value of NumberOfCycles\_Float will be taken from.

<figure><img src="../.gitbook/assets/image (537).png" alt=""><figcaption></figcaption></figure>

Example 2 (Instrument Step Return Values)

In a similar way you can have access to the additional return value of, for example, the "GetTemperature" Function of the TCC. Some functions return more than one item of information.

If you use this "GetTemperature" Function, you will only be asked for the TCC you want to use. The value of interest, the returned temperature, needs to be bound in a separate task.

To do this perform these steps:

1. Right-click on the desired step.
2. Select "Bind Return values..." from the Context Menu that opens.

\


| <p></p><p><img src="../.gitbook/assets/image (538).png" alt="" data-size="original"></p> | The “Bind Return values…” Function is also available as a function button in the toolbar. The function is active for method steps which have additional return values. |
| ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------- |



<table data-header-hidden><thead><tr><th width="145"></th><th></th></tr></thead><tbody><tr><td><img src="../.gitbook/assets/image (10) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" data-size="original"></td><td><p>NOTE</p><p>The “Easy Steps” and “Smart Steps” do not have the “Bind Return values…” Function.</p></td></tr></tbody></table>



These pieces of information as presented in the image below can be stored in variables for further processing or to be used as output. The dialog generally lists the return values, each with an editable field “Variable Name”, to define the variable the return value is to bound to.

![](<../.gitbook/assets/image (539).png>)\




### When to Bind Variables‌

It is up to the programmer to choose whether to bind variables or not. Often times, the variables need to be handled in a different way from what are shown in the examples. For user defined error handling, there is a necessity to bind return values.

Functions with additional return values which have to be bound by the procedure, as shown above can be simply recognized in a method. The number of return values is given, even if it is not going to be handled (see in the topmost label of method 2, "Tip Pick Up" in the image below). The return value(s) assigned to the variables will also be shown (see the method Steps 3 and 4 in the image below).

![](<../.gitbook/assets/image (540).png>)\




