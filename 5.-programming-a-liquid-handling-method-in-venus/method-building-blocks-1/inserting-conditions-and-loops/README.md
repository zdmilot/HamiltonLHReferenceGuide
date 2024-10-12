---
description: How to automate decision-making and repeated actions in Venus.
---

# Inserting Conditions and Loops

![](<../../../.gitbook/assets/0 (1).png>)

### ![](<../../../.gitbook/assets/1 (1).jpeg>)Loops <a href="#slide-number-2" id="slide-number-2"></a>

Found under the General Tab, the **Loop** Step is used to repeat specific steps (also known as _iterate_)

**Four ways to control the looping:**

Repeat a fixed number of times

Repeat while some logic expression is true

Repeat until the controlling & selected sequence has reached its end

Repeat until the selected file has reached its end: no more records

### ![](<../../../.gitbook/assets/2 (1).jpeg>)Using Loops <a href="#slide-number-3" id="slide-number-3"></a>

![](<../../../.gitbook/assets/3 (1) (1).png>)Add the General Step **Loop** to your Method and the **Loop** dialogue window appears

![](<../../../.gitbook/assets/4 (1) (1).png>)Select the way to Loop, provide any info needed, and click **OK**

![](<../../../.gitbook/assets/5 (1) (1).png>)An empty **Loop**-**End Loop** step combo is added to the Method

Steps added between the **Loop** and **End Loop** will be repeated when the Method runs

Examples:

### Loops

1. ![](<../../../.gitbook/assets/6 (1) (1) (1).png>)Repeat the step 12 times
2. Repeat forever or until the step Loop-Break is encountered

![](<../../../.gitbook/assets/7 (1) (1).png>)

1. Repeat the pipetting steps until all sequence positions in

![](<../../../.gitbook/assets/8 (1) (1).png>)TargetPlatesX4 are processed

1. ![](<../../../.gitbook/assets/9 (1) (1).png>)Read each record from the work list until the end-of-file is reached

### Loops <a href="#slide-number-5" id="slide-number-5"></a>

**“Iterate over sequence” =** Repeat the steps inside the loop until the “**Controlling**” sequence runs out of positions (i.e. reaches it’s **End Position)**

![](<../../../.gitbook/assets/10 (1) (1) (1).png>)

**=**

![](<../../../.gitbook/assets/11 (2).png>)![](<../../../.gitbook/assets/12 (2).png>)

**never** = no change in the **current position**

**before loop** = **current position** set to 1 _before_ Loop step starts

**after loop** = **current position** set to 1 _after_ Loop step is finished

![](<../../../.gitbook/assets/13 (1).png>)**before & after loop** = **current position** set to 1 _before & after_ Loop step

When more than one sequence is checked as **Controlling** then the Loop will end when the first sequence runs out of positions

### Loops <a href="#slide-number-6" id="slide-number-6"></a>

![](<../../../.gitbook/assets/14 (1).jpeg>)To force a **Loop** to end prematurely, use the **Loop Break** step. Processing continues with the next step after the **End Loop.**

![](<../../../.gitbook/assets/15 (1) (1).jpeg>)**Loop counter variable** created by the **Loop** step automatically keeps count of the number of iterations. **Loop counter variable** = **0** before **Loop** execution starts, and is incremented by **1** every time the **Loop** body is entered

![](<../../../.gitbook/assets/16 (1) (1).png>)**Loops** can contain other **Loops**

Example: an 8 channel STAR with 300uL tips can Dispense 100uL into 3 wells for each 300uL Aspiration. So it will need to repeat the Aspirate and Dispense steps 4 times to completely fill a 96 well plate **(Note: for Part Volume Dispenses, the volume for the first and last dispense will be off)**

### Demo: Loop over a Sequence <a href="#slide-number-7" id="slide-number-7"></a>

1. Add a **Loop** step to the end of the **Training\_Demo** Method:

Iterate over sequence **SMP\_CAR\_24\_15x75\_A00\_0001 (controlling)**

Also set the **Cos\_96\_Rd\_0001** sequence to _reset before & after loop_

1. Select the existing **Tip Pickup**, **Aspirate, Dispense**, and **Tip Eject** steps and drag them inside this **Loop-End Loop** step
2. Now add a **Tip Pick Up** single step: **MlStar1000ulHighVolumeTip** to the end of the Method
3. Add a **Aspirate** single step**:** from **rgt\_cont\_120ml\_a00\_0001** aspirate **500uL** using **1000ul High Volume Tips.** Set Sequence counting to Manual & use the **HighVolume\_Water\_DispenseJet\_Part** liquid class.
4. **Dispense 100uL** back into reagent tub 90mm from bottom and set Sequence counting to Manual
5. ![C:\Users\vienneau\_b\AppData\Local\Microsoft\Windows\Temporary Internet Files\Content.IE5\BE0QONK0\MC900434799\[1\].png](broken-reference)Add a Loop to iterate 3 times and in the loop **Dispense 100uL** into the

**Cos\_96\_Rd\_0001** sequence 10mm from the bottom

1. After the loop, add a **Tip Eject** single step

![MPj04003520000\[1\]](../../../.gitbook/assets/18.jpeg)Challenge 5:

Repeat steps with Loop- End Loop

![](<../../../.gitbook/assets/19 (1).jpeg>)Challenge 6:

Repeat steps with Loop- End Loop

### Variables <a href="#slide-number-9" id="slide-number-9"></a>

**Variables** are containers created to represent information that changes or is unknown at the time when the Method is written (e.g. the number of samples to process or the volume to be dispensed into each well)

**Variables** are created by providing a name and an initial value. Use general steps: **Assignment** and **Assignment with Calculation** to do this

![](<../../../.gitbook/assets/20 (1) (1).png>)

**Variables** can also be created directly within many steps



It’s recommended to provide descriptive names and not just X, Y, & Z

### Variables <a href="#slide-number-10" id="slide-number-10"></a>

* Names are case-sensitive and must begin with a letter. Spaces are not allowed, underscores (“\_”) are OK
* Once defined, variables show up in the drop-down list of input fields
* Inside text strings, a single backslash = Escape Character (i.e. the character that follows a backslash can have special meaning:

**“\t” = “tabs” “\n” = “new line” “\\\” = “\” “\”” =** quote marks

Example: **"C:\\\Program Files (x86)\\\HAMILTON\\\Methods\\\Examples\\\Worklist.xls"**

* Three types of variables: **Integers** (no decimals), **Floats** (floating point), and

**Strings** (text in quotes)

* For variables in calculations:
  * Two integers will result in an integer:**\*\***

_if A = 5 and B = 2, then A/B = 2, A\*B = 10_

*
  * An integer and a float will result in a float:

_if A = 5.0 and B = 2 then A/B = 2.5, A\*B = 10.0_

_**\*\*** VenusTwo provides this as a choice_

### User Input and User Output <a href="#slide-number-11" id="slide-number-11"></a>

*
  *
    * Dialog window that prompts user for information and assign values to variables for later use



*
  *
    * Square brackets “**\[ ]**” indicate that entering a value in that field is **optional**
    * Place double quotes **“ ”** around all text
    * Click the **Add** button to add more lines
    * Default for Type **String** is a pair of empty quotes “”
    * Type **String** displays a button during the run to open a “Browse for File” window



### User Input and Output <a href="#slide-number-12" id="slide-number-12"></a>

Title for the dialog window that appears



Button to include with the dialog window 1=OK, 2=Cancel, 3=Abort, 4=Retry, 5=Ignore, 6=Yes, 7=No



Create a variable to stores the value of the clicked button Sound to be played when dialog window appears



Seconds to wait before dialog box closes and

&#x20;default value are used. Dialog box waits for user to close when the **infinite** check box is checked

&#x20;Icon to be displayed in the User Output dialog

### Demo: User Input, Output, and Variables <a href="#slide-number-13" id="slide-number-13"></a>

1. Add a **User Input** step to the beginning of the **Training\_Demo** Method Set **Dialogue title** to : "METHOD PARAMETERS“

Add these **Input requests**:{Variable, Prompt, Type, Default, Min, Max}

**{varSamples**, "How many Samples are there?“, Integer, 8, 1, 24}

**{varSampleVolume**, "Sample Volume?“, Float, 100, 50, 200}

**{varDiluentVolume**, "Diluent Volume?“, Float, 100, 50, 200}

1. Next add a **Sequence: Set End Position** step and set the position to

**varSamples** for **SMP\_CAR\_24\_15x75\_A00\_0001** sequence

1. Modify the **Aspirate** and **Dispense** steps for the Sample pipetting to pipette the Sample volume (**varSampleVolume**) entered
2. Before the Diluent (reagent) pipetting, add the step **Assignment with Calculations** and set **varTotalDiluentVolume** = **varDiluentVolume \* 5**
3. Modify the Aspirate and Dispense steps for the Diluent pipetting to use the diluent volumes **varTotalDiluentVolume** & **varDiluentVolume**
4. Add a **User Output** step at the end to display the sample & diluent volumes

Challenge 7:

User Input and Aliquot Dispense



*
  * Compare expressions and make decisions
  * Can be nested to check multiple conditions
  * **Else** part of **If-Else** step is optional

When the **If** condition is **true**, steps between **If** and **End If** are executed. When **not true**, these steps are skipped and the Method continues onto

1. the next step after the **End If** or
2. the steps between the **Else** and the **End If**

when the **Include Else block** is checked.

### Nested If-Else Method Branching Example <a href="#slide-number-16" id="slide-number-16"></a>

**1**



**2**

**3**

**4**

**5**

Challenge 8: Incorporating If/Else branching
