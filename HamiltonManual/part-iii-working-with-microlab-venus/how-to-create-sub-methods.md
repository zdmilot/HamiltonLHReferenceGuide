# How to Create Sub-Methods‌

1.
   1.  ### Sub-Methods and Sub-Method Libraries‌

       \


       Parts of the existing methods can usually be re-used at a later time in the same method or in other methods. The VENUS Software enables grouping of useful command routines that are called sub- methods.

       Method 1

Sub-method 2

Sub-method 1

A local sub-method is part of a particular method and remains linked to it. It is displayed along with the method it belongs to.

\


Method 2

\


![image](../.gitbook/assets/Image\_464.png)

Method 2

Submeth-Lib 1

![image](../.gitbook/assets/Image\_465.png)

Method 1

Submeth-Lib 2

Submeth-Lib 1

Submeth-Lib 1

A sub-method library contains an independent sub-method that may be used in several independent methods. To make use of the advantages of sub-methods, the functions of the “Sub- method“ Library has to be included in a method.

\


Submeth-Lib 2

Although sub methods and sub method libraries are different in terms of scope, the programming is very similar.

1.
   1.  ### ‌How to Create Sub-Methods‌

       \


       1.  In a method, right-click in the top area beside the "Main Method" Tab / "OnAbort" Tab to open the Context Menu then click the \[Add...] Button to open a new dialog box where the interface of a sub-method can be defined.

           \


           ![right klick here](../.gitbook/assets/Image\_466.gif)

           \

       2.  The “Define Sub-method” Dialog, as shown below, will appear.

           \


           ![image](../.gitbook/assets/Image\_467.jpg)

           \

       3.  Specify a sub-method name.

           The "Visibility" Option can only be used in sub-method libraries. Such collection of steps may itself contain functions/procedures which will not be exported. In this case, they are of local nature and hence are not visible by the user of the library. Local sub-methods will always be visible in the method within which they are defined.
       4.  Enter a "Sub-method description" to briefly describe its use. This entry is optional but helpful to other programmers who may access the method. Note that quotation marks are not required and should not be used in this field.

           \


           ![image](../.gitbook/assets/Image\_468.jpg)

           One or more parameters can be assigned to a sub-method, to do this, perform the succeeding steps:
       5. Click \[Add] for each parameter to be assigned.
       6. For each parameter specify:
          * A name (which will be referenced throughout the sub-method),
          * A type (variable, sequence, etc.) selected from the list in the drop-down list available,
          * A direction (input, output or both)
            * “Direction” refers to whether the variable used to call the sub-method in the main method may be altered by the sub-method or not.
            * The “Input” Option means that the original variable is not to be altered.
            * The “Output” Option means that the original variable will be overwritten by the sub- method, and the value of the original variable cannot be used inside the sub-method.
            * The “Both” Option (both input and output) means that the original variable will be altered by the sub-method.
       7.  A short description of the parameter (without quotation marks).

           \


           Example:

           If the main method contains a variable par = 10 and the sub-method contains the operation par = par + 5:

           * The “Input” yields the result 10 (the value of the parameter is copied from the main method and overwrites the value in the sub-method)
           * The “Output” yields 5 (no value is read from the main method)
           *   Then “Both” yield 15 (the value of the parameter is copied from the main method and is added to the operation in the sub-method).

               To remove a parameter, click one of its description fields, and then click \[Remove]. To reorder parameters, select one and click \[Move Up] or \[Move Down].
       8.  Click \[OK] to store the sub-method interface. The system returns to the previous window, and the new sub-method is included in the “Local Sub-methods” Tab found in the toolbox window.

           \


           ![image](../.gitbook/assets/Image\_469.jpg)

           \

       9. Additional sub-methods will be added to the “Local Sub-methods” Tab. The main method itself is always on the first tab.

       \


       Modifying a Sub-Method

       To modify an existing sub-method (e.g. by adding or deleting steps), click on its tab in the method window and it will open for editing.

       \


       ![sub-methode](../.gitbook/assets/Image\_470.gif)

       \


       Variables in Sub-Methods

       [Just like in a method, variables can be created in a sub-method. However, unlike those in a method, sub-method variables remain local (see ](how-to-create-sub-methods.md#bookmark283)Section 11.1 Variables and Return Values).

       \


       Promoting Variables to Global Status

       A local variable defined inside a sub-method can be promoted to global status if it has to be used elsewhere.

       From the Menu, select “Methods” and choose “Export Local Variables…”. A dialog will prompt containing a list box that displays the local variables in the current sub-method.

       1. Tick the box of all variables that will be promoted to global status.
       2. Click \[Export] to promote the variables globally.

       \


       ![image](../.gitbook/assets/Image\_471.jpg)

       \

   2.  ### ‌Sub-Method OnAbort‌

       \


       The “OnAbort” Sub-method appears in every method. This sub-method is used to execute steps in case of an (instrument- or user caused) abort. It can contain indicated to do instructions when the method is aborted. If a method finishes successfully, the steps in the OnAbort sub method are not executed.

       \


       ![image](../.gitbook/assets/Image\_472.jpg)
