---
description: >-
  Modify the Aliquot Method by including a “Cancel” button on the User Input
  step.  Use an If/Else Conditional to check if the User clicked the “Cancel”
  button to cancel the method run.
---

# Example 9: Incorporating If/Else Branching

1. Open the Aliquot.med method file.  From the “File” menu select “Save As” and save the method as Aliquot\_If\_Else.
2. At the top of the Method, add a Comment step with the text “Lame Comment”.
3. Edit the User Input step and type in the variable, intUserChoice in the Return Value field and select the ‘OK’ and ‘Cancel’ buttons from the “Buttons” dropdown.

<figure><img src="../.gitbook/assets/image (284).png" alt=""><figcaption></figcaption></figure>

4. After the User Input step, insert an If/Else step that compares intUserChoice to 2 (the cancel button, denoted in the “Help” for the User Input step).

<figure><img src="../.gitbook/assets/image (285).png" alt=""><figcaption></figcaption></figure>

5. Inside the If/Else step add a User Output step and inform the User they have clicked “cancel” so the Method will now end.
6. Following the User Output step, add the General step Return, which will function to end the method withoutcausing the method to abort.&#x20;

<figure><img src="../.gitbook/assets/image (286).png" alt=""><figcaption></figcaption></figure>

7. Save and launch Run Control. Simulate the method and correct any errors.

## Optional Expert Challenges&#x20;

GOAL:  Verify that the User selected the Cancel button during the User Input dialogue.  Modify the method by changing the User Output within the If/Else step. &#x20;

1\.    Add a variable to the User Output in its Return Value field (you can re-use intUserChoice since its value has been processed and is no longer needed)

2\.    Select “Yes and No” buttons from the “Buttons” dropdown. &#x20;

3\.    Change the wording of the output text to ask the User if they really wish to quit and end the Method run.

4\.    Use another If/Else step to check their answer and exit the method only if they click on “Yes”.

5\.    Save and launch Run Control.  Simulate the method and correct any errors.
