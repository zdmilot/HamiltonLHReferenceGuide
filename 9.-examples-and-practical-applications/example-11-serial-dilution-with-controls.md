# Example 11: Serial Dilution with Controls

GOAL: Modify the previous method to skip over the first column when aliquotting diluent, and additionally to skip over the last row when pipetting Samples, providing for a control column of samples and a control row of Diluent.

1. Open Serial Dilution.med and save it as Serial Dilution with Controls.
2. Add the General step Sequence: Set Current Position to just before the first loop and set it to 9.  Also set the Reset to after loop in the loop step.

<figure><img src="../.gitbook/assets/image (294).png" alt=""><figcaption></figcaption></figure>

3. Run in Simulation Mode to make sure it works properly – the first column should remain empty.
4. Continue to modify the Method.  Insert an Assignment step just after the “Begin Serial Dilution Loop” Comment step to create a new variable, strChannelPattern equal to the string value “11111110”.&#x20;
5. Modify the sample Aspirate step outside the loop to use “Channel Selection as Variable” under the Channel Settings button.  Channel Use is set to Channel Pattern.  Set Sequence Counting to Manual.

<figure><img src="../.gitbook/assets/image (295).png" alt=""><figcaption></figcaption></figure>

6. Copy the Dispense step from the Loop and paste it just below the Aspirate step just before the loop. Modify this Dispense step setting Sequence counting to Automatic and use the new channel pattern.
7. Copy the previous Aspirate step and paste it right after this Dispense Step.
8. Modify the both the Dispense and Aspirate steps in the loop to use the same channel pattern. &#x20;
9. Save and launch Run Control.  Simulate the method and correct any errors.

## Optional Expert Challenges

GOAL: Dynamically build a Channel Pattern variable based on User Input.

1\.    Save a copy of this Method (File -> Save As..) and call it Serial Dilution with Control\_Extra.med

2\.    Add a prompt to the User Input asking which Row (1-8) should be the Diluent control.

3\.    Then add an Assignment step to set strPattern = “” (an empty string, allows for reassignment later!).

4\.    Then add a Loop step with a fixed iteration of 8 to build the variable string.

5\.    Use the IF/Else step to build a string of characters by selectively placing a “0” or a “1” in the correct order to reflect the Users choice of control row.&#x20;

6\.    In the Serial Dilution Loop, modify the Assignment with Calculations step to set strChannelPattern = strPattern.

7\.    Save and launch Run Control.  Simulate the method and correct any errors.

&#x20;

\
\
