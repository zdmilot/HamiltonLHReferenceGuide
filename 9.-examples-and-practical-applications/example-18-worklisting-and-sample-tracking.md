---
description: >-
  Perform a serial dilution utilizing worklisting.  Sample location and volumes
  are obtained from the worklist.
---

# Example 18: Worklisting and Sample Tracking

\*Note - Read over the whole assay first to see what you need to set up at the beginning.

1. Build a new deck layout first -       &#x20;
   1. Sample Carrier with 24 sample tubes.
   2. Reagent Carrier with 3 reagent tubs.
   3. An L5MD Plate Carrier with 1x Source 96-Well plate on one and 3 x Target 96-Well plates.
   4. A Tip carrier with appropriately sized tips.
2. Using Notepad.exe, create and save a worklist file with two comma separated columns: Save this file as “DilutionWorklist.xls”.\
   ![](<../.gitbook/assets/image (256).png>)
3. Start the Method by asking User to select the worklist.
4. Use the File: Open step to open the worklist using the Excel tab, then cycle through the records to create:
   1. Sample Volume array.
   2. A second Diluent Volume array where: Diluent Volume = 300µL – Sample Volume (Use Assignment with Calculation).
   3. A Source Sequence that uses the PositionID from the worklist and the name of the sample carrier (from the deck layout) for the LabwareID. &#x20;
5. Close file when done.
6. Fill one of the 96-Well plates with diluent using the Diluent volume array.  This will become the Dilution Plate (name the sequence DilutionPlate).
7. Aspirate the samples using the Sample Volume array and the Source Sequence generated from the worklist.
8. Proceed with the serial dilution over the DilutionPlate.  Dispensing the samples, then aspirating the Sample volume with mixing before moving to the next column.  Use 150 µL as the mix volume.  At the end, eject the tips with the aspirated liquid from the last column into the waste.
9. Transport the plate to an off-deck incubator location and wait 10 seconds for incubation to complete. Then transport the plate back to the original position. Use a User Output step to simulate the incubation time.\
   ![](<../.gitbook/assets/image (255).png>)
10. Transfer 80% of the liquid from the dilution plate to every third column on the target plates (Column 1 dilution plate goes to column 1 of the target plate; Column 2 dilution plate goes to column 4 of target plate; Column 3 dilution plate goes to column 7 of target plate and so on….).
11. Save and launch Run Control.  Simulate the method and correct any errors.  Create a Sample Tracking Report for the three final plates and verify that pipetting has occurred correctly.
