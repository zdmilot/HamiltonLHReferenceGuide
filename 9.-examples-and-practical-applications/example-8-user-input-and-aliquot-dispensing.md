---
description: >-
  Creating a Method that will aliquot reagent from a reagent tub to all wells in
  a plate using the 1000µL channels. The Method will pick up tips, Aspirate and
  Multi-dispense, then eject tips.
---

# Example 8: User Input and Aliquot Dispensing

\*Note - The Aliquot process involves multiple Dispenses for each Aspiration.  The aspirate volume required equals the dispense volume per well multiplied by the # of dispenses + 2.  The + 2 is for the pre & post dispenses.&#x20;

(e.g. _Aspirate Volume = Dispense Volume \* 14_   for a 12 column plate)

1. Using your Basic\_Deck layout that we’ve been adding to through the course of the challenges, create a new method, and name it Aliquot.
2. Transfer 50µL (our dispense volume) from Ham\_DW\_Rgt\_L\_0001 to all 12 columns of the first plate (Nun\_96\_Fl\_Lb\_0001) as an Aliquot (multi-dispense:
   1. First, calculate the aspirate volume required using the formula above with the General Step Assignment with Calculation, you can call the variable, intAspirateVolume.
   2. Aspirate the calculated volume from the source reagent plate Ham\_DW\_Rgt\_L\_0001 and set the Dispense Mode to Jet Part Volume. Make sure you select the correct, corresponding liquid class.\
      ![](<../.gitbook/assets/image (136).png>)\
      \

   3. Next, dispense 50µL back into the source reagent plate Ham\_DW\_Rgt\_L\_0001.
   4. Add a Loop step to iterate over the Nun\_96\_Fl\_Lb\_0001 sequence.
   5. Within the Loop, add the Dispense step to dispense to the Nun\_96\_Fl\_Lb\_0001 sequence.
   6. After the Loop, eject the tips which will have liquid left over inside (this is the post-dispense volume).  &#x20;
3. Save and launch Run Control.  Simulate the method and correct any errors.
4. Modify this method by adding a User Input step at the beginning.  Prompt for the dispense volume storing it in variable intDispenseVolume.

<figure><img src="../.gitbook/assets/image (137).png" alt=""><figcaption></figcaption></figure>

5. Re-calculate (Using the Assignment with Calculation step) the Aspirate volume and replace the specific volumes with the variables intAspirateVolume and intDispenseVolume in the respective Aspirate and Dispense steps.

<figure><img src="../.gitbook/assets/image (138).png" alt=""><figcaption></figcaption></figure>

6. Add a User Output step at the end of the Method that will output the Aspirate and Dispense volumes and their descriptions.

<figure><img src="../.gitbook/assets/image (139).png" alt=""><figcaption></figcaption></figure>

7. Save and launch Run Control. Simulate the method and correct any errors.

## Optional Expert Challenges

1\.    Using “Save As”, save a copy of the method, call it Aliquot\_Extra.med

2\.    Add an additional prompt to the User Input step to ask for the number of columns (1-12) to be dispensed to. &#x20;

3\.    Use this value to calculate the sequence index of the last well of the target plate.  Use the General Step Sequence: Set End Position to set the End Position of the target sequence.

4\.    Recalculate the aspirate volume based on the reduced number of aliquots.

5\.    Modify the Loop step to “Iterate over Sequence” and select the target sequence as the controllingsequence.\
