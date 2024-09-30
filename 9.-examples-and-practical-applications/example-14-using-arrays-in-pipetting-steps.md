---
description: >-
  Create a new Method with an array of volumes and then use this array to
  pipette the volumes from sample tubes to a plate.
---

# Example 14: Using Arrays in Pipetting Steps

1. Using our Basic\_Deck, create a new method and name it Volume\_Arrays.
2. Use the General Step Array: Declare/Set Size to declare an empty array called arrIntVolumes.
3. Add an Assignment step and set intSomeVolume = 95.
4. Add a Loop step to loop 8 times.\
   ![](<../.gitbook/assets/image (298).png>)
5. Add an Assignment with Calculations and increment intSomeVolume by 5.
6. Add the step Array: Set At to add intSomeVolume to the end of arrIntVolumes
7. Use Sequence: Set End Position and set the end of SMP\_CAR\_24\_15X75\_0001 to 8.
8. Add a Loop to iterate over the sequence SMP\_CAR\_24\_15X75\_0001.
9. Add the steps to the loop to pipette from Sample Carrier to the first plate.  For the Aspirate and Dispensesteps incorporate arrIntVolumes.   Select  “Use multiple array values” and start at index 1.\
   ![](<../.gitbook/assets/image (300).png>)
10. Run the Method and check Trace file to see if the correct volumes were pipetted.
11. Now modify your method.  Change the Number of iterations from 8 to 12 so you have a total of 12 values in arrIntVolumes.
12. Modify the Sequence: Set End Position step and set the end of SMP\_CAR\_24\_15X75 to 12.&#x20;
13. After the Sequence:  Set End Position step, add the Assignment step to assign intIndexStart = 1.&#x20;
14. At the end of the loop, add the Assignment with Calculation step to increment intIndexStart by 8 (i.e. the number of channels).\
    ![](<../.gitbook/assets/image (301).png>)
15. Modify the Array Index of the Aspirate and Dispense steps to have the volumes pipetted reflect the additional values in the array.
16. Save and launch Run Control.  Simulate the method and correct any errors.  Check the trace file to see if the correct volumes were pipetted.

\
\
