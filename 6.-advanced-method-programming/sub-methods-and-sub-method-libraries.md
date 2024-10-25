# Sub-Methods and Sub-Method Libraries

## Sub-Method Overview&#x20;

Sub-Methods are collections of steps and functions that can perform specific tasks or make a methodmore modular.  They have many uses, but in general, the step usage falls into one of five categories

1. To execute after an abort (manual, instrument, or program driven) condition is reached
2. Those that are not to be executed (Revision history, or ‘archived’ steps)
3. Executed exactly the same way each time the submethod is called – wether it’s once (simple organization) or repeatedly
4. Executed differently each time it’s called based on a parameter
5. Behave as a separate set of steps, acting as a lbrary (Sub-Method Library, .SMT)

<div>

<figure><img src="../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

 

<figure><img src="../.gitbook/assets/image (1) (1).png" alt=""><figcaption></figcaption></figure>

 

<figure><img src="../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>

</div>

<details>

<summary>Use Case 1 - OnAbort</summary>



OnAbort is a Sub-Method, but instead of being called on through Local Sub-Methods, is triggered by an error condition or forced through the “Abort” step.

<img src="../.gitbook/assets/image (3).png" alt="" data-size="original"><img src="../.gitbook/assets/image (4).png" alt="" data-size="original">

* Use for final Tip Counters
* Integrated device shut-down and accessibility
* Error Logging to trace file or report
* Do not use MLSTAR instrument commands (could be in error state)

</details>

<details>

<summary>Use Case 2 - Store program code that is NOT to be executed.</summary>



A Sub-Method can be used to store program code that is _NOT_ to be executed.  This is more safe than disabling.\


<img src="../.gitbook/assets/image (5).png" alt="" data-size="original"><img src="../.gitbook/assets/image (6).png" alt="" data-size="original">

* Program module (group of code) developed in the “Method” Tab
* New Sub-Method created with clear name (“DNU”, “Extra”, “Storage”, etc.)
* Program module copied/pasted into new subroutine
* “Method” tab module can be changed or modified, tested, and reverted from the Subroutine.
* Can also be used to store Revision Comments from the beginning of method for previous method versions

</details>

<details>

<summary>Use Case 3 - Code Blocks without parameters.</summary>



A Sub-Method can be used to store blocks of code that are executed, but without parameters.

Note – Sequence Current and End position statuses are global.

Calling on a submethod multiple times may run differently (even without parameters) if sequence positions are changing by counting!

Traced Comments entering and leaving submethods can help with trace troubleshooting.

<img src="../.gitbook/assets/image (7).png" alt="" data-size="original">

* Program modes that may run conditionally, once or many times
* Usually coded in “Method Tab”, copied into Sub-Method Tab
* Useful for when large blocks of code could be buried behind conditional blocks
* Requires Local Sub-Method Call in Method tab

</details>

<details>

<summary>Use Case 4 - PARAMETERS control what CHANGES each time the SubMethod is called</summary>



PARAMETERS are used to control what CHANGES each time the SubMethod is called

Note: Marking a parameter as \[in] means that any changes to the object (including sequence counting!) will not be visible outside of the submethod!

<img src="../.gitbook/assets/image (8).png" alt="" data-size="original">

* i\_ / o\_ / io\_ variable naming helpful – tracks what’s changing each time, and if a value is passed back into main method
* Parameters can be sequences, arrays, variables, file handles, etc.
* Can use Return Value for a functional output, or an error message

</details>

<details>

<summary>Use Case 5 - Submethods for easier access between programs – a type of Library.</summary>



A separate file (.SMT) for Submethods can be created for easier access between programs – this is a type of Library.

<img src="../.gitbook/assets/image (9).png" alt="" data-size="original">

* Allows use of one set of code for multiple methods (easier maintenance)
* Parameters are the ONLY link between .SMT Sub-methods and a .MED
* Useful for common steps/conditions in dealing with integration devices
* Example: Visual NTR library

</details>



## &#x20;Variable Scope

The ”Visibility” of a variable between a Method, Submethods, or Workflow (Scheduler object) is called Scope

<figure><img src="../.gitbook/assets/image (10).png" alt="" width="331"><figcaption></figcaption></figure>

* Variables created in the Method tab are Task-Local, and are visible to all Sub-Methods
* Variables created in a Submethod tab, are Local, and can not be seen outside of the tab
* Use ViewàVariables to check what variables are scoped per the current tab (method or submethod)
* It’s possible to have identical variable names with different scopes – the naming convention prefix t\_ and l\_ can avoid this
* Where identical variables are present, an output warning will occur:
  * `Warning: Variable 'x_fltVolume' is defined in sub-method 'Pipette' and in global scope (global variable or task-local variable). The local variable hides the global variable.`
* Global Scoped variables are generally only used for Scheduled methods

&#x20;

## Features

A separate file (.SMT) for Submethods can be created for easier access between programs – this is a type of Library.

<figure><img src="../.gitbook/assets/image (11).png" alt="" width="375"><figcaption></figcaption></figure>

* Allows use of one set of code for multiple methods (easier maintenance)
* Parameters are the ONLY link between .SMT Sub-methods and a .MED
* Useful for common steps/conditions in dealing with integration devices
* Example: Visual NTR library

### &#x20; Visibility

<figure><img src="../.gitbook/assets/image (12).png" alt="" width="375"><figcaption></figcaption></figure>

#### Exported sub-methods

* Functions that can be called when the SMT is added to a method
* Visible in the toolbox

<figure><img src="../.gitbook/assets/image (13).png" alt="" width="375"><figcaption></figcaption></figure>

#### Not Exported sub-methods

* Only used within the SMT&#x20;
* Not visible in the toolbox when the SMT is added to a method

&#x20;

### Return Value

If Variable is selected:\


<div>

<figure><img src="../.gitbook/assets/image (16).png" alt=""><figcaption></figcaption></figure>

 

<figure><img src="../.gitbook/assets/image (17).png" alt=""><figcaption></figcaption></figure>

</div>

* The sub-method must include a Return Step
* When the return step is executed, the sub-method immediately exits the sub-method
* The Return Step can be set equal to a specified value
* When you add a SMT function to a method, enter a variable to capture the return value\
  ![](<../.gitbook/assets/image (14).png>)

If No return value is selected:

* The sub-method may include a Return Step, but no  value can be applied

## &#x20;Considerations

### “Visibility”

* Can –only- see parameters passed into them – lose access to task-local variables and sequences compared to Sub Methods
* No exchange of info between Sub-Method Library subs either (except by parameter)
* Instrument must be passed in to have access to certain steps (ML\_STAR instrument commands)
* Can use Config files to store values temporarily between subs

### Library Inception

* Libraries may have libraries referenced within them

### Applications

* Library usefulness should be clear by now!

### Limitations

* Submethods can be used to “automate” programming tasks, like decision making.
* Every time a decision is automated, you limit the flexibility of your program because it’s assuming things to be true.  Enter these limitations as descriptions in the Sub.
* Too many parameters can lead to unpredictable interactions – avoid having the sub turn into a “black box” where you lose track of how or when it works!
* Good Programming Practices Rule of Thumb
* Use a maximum of 8 parameters/sub-method
* Use a maximum of 20 functions/SMT

## &#x20;Trace when Sub-Methods Start and Stop

Code to include at the start of the sub-method:

<figure><img src="../.gitbook/assets/image (19).png" alt=""><figcaption></figcaption></figure>

Code to include at the end of the sub-method:

![](<../.gitbook/assets/image (20).png>)



## Example - Submethods and Submethod Libraries

### Problem

* Assay has many pipetting actions with similar solutions, only varies by volume and tip size&#x20;
* Assay requires intermittent activities, such that all pipetting can’t be looped together (over an array of sequences or large custom sequences)&#x20;

### Solution

<figure><img src="../.gitbook/assets/image (21).png" alt=""><figcaption></figcaption></figure>

* Create a submethod library that will take a volume (INPUT) and provide a liquid class (OUTPUT), and pickup up tips.  An error code (RETURN VALUE) will trigger if the volume is out of range.
* Create a Pipetting submethod that will accept a source reagent trough (INPUT), destination plate (INPUT) and volume (INPUT), and process volumes whenever needed.
* Use a Return value within the Pipetting sub method&#x20;

&#x20;
