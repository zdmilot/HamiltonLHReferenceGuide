---
description: >-
  Building on the previous Method, perform a Serial Dilution across a 96-Well
  plate using 1000µL channels.  Column 1 will contain the first dilution
---

# Example 10: Performing a Serial Dilution

\*Note - Mixing occurs during the Aspirate step, and the volume in the last column ends up the same as the others.

1. Open the method, Aliquot.med.  Using “File” – “Save As”, save the method as Serial\_Dilution.&#x20;
2. Modify the method.  After the Tip Eject step, add a Comment step (“Begin Serial Dilution Loop”).
3. After the Comment step add a Tip Pick Up to pick up 1000µL High Volume Tips.
4. Add an Aspirate step and aspirate from a Sample Tube Carrier (SMP\_CAR\_24\_15x75\_0001).  Use intDispenseVolume from the User Input step for the volume.
5. Add a Loop Step to iterate over the target sequence, Nun\_96\_Fl\_Lb\_0001 (What is the controlling sequence?). &#x20;
6. Within the Loop:
   1. Dispense intDispenseVolume to the target Sequence with a Fixed Height of 5 mm and Sequence counting to Manual.
   2. Aspirate intDispenseVolume from the same location but set Sequence counting to Automatic and under the “Advanced…” button, set the number of Mixing Cycles to 2 and the Mixing Volume to the intDispenseVolume.  Reduce the Mix Position to 0 mm.

<figure><img src="../.gitbook/assets/image (287).png" alt=""><figcaption></figcaption></figure>

7. After the Loop, eject the tips (with the liquid from the last aspirate) into the waste. &#x20;
8. Save and launch Run Control.  Simulate the method and correct any errors.

## Optional Expert Challenges

GOAL: Perform a row by row serial dilution by using the CO-RE 96 MPH as the pipetting tool.

1. Using “Save As”, save a copy of the method, call it Serial Dilution\_Extra.
2. In the Deck Layout Editor select the “Labware” tab, delete the 300µL Standard Volume tips in position 4 & 5 of the first tip carrier.  Replace position 5 with the TipSupport\_1000µlHighVolumeTip tip rack.
3. Create a sequence, Tips96 over a new rack of 1000µL High Volume Tips.
4. Under the “Sequence” tab, select Head 96 Row as the stamp tool.
5. Create 3 new sequences: one for the target plate (TargetByRow), one for the tip adapter (Tips1000Row), and one for the source plate (SamplesByRow – use Ham\_DW\_Rgt\_96 as the source).
6. Delete the last 1000µL Channel Tip Pick-Up step. Add a CO-RE 96 Head Tip Pickup to pick up 96 tips from Tips96 and add a tip eject to eject the tips into the Tip Support.
7.  Add a tip pickup using the CO-RE 96 Head and the sequence Tips1000Row.

    \*Note - select (2) Row(s) as the “Reduced pattern mode” under the Channel Settings of the CO-RE 96 Head Tip Pickup.&#x20;

<figure><img src="../.gitbook/assets/image (288).png" alt=""><figcaption></figcaption></figure>

8. Modify the serial dilution task to add the new sequences above. &#x20;
9. Save and launch Run Control.  Simulate the method and correct any errors.  Reset the Stamp tool to 1000µL Channels after completion. &#x20;
