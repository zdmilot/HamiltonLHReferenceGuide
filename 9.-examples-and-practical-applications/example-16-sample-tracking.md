---
description: >-
  Modify the previous method to add sample tracking to output a report showing
  the well-to-well transfers and other labware related details.
---

# Example 16: Sample Tracking

1. Open the Serial Dilution with Control.med.
2. Make sure that Sample Tracking is “On” (Tools -> System Configuration Editor).

<figure><img src="../.gitbook/assets/image (305).png" alt=""><figcaption></figcaption></figure>

3. Assure Data Handling steps are visible (Method -> Instrument and Smart Steps)

<figure><img src="../.gitbook/assets/image (306).png" alt=""><figcaption></figcaption></figure>

4. Add a Smart Step Load after the Initialize step to load the Nun\_96\_Fl\_Lb\_0001, SMP\_CAR\_24\_15x75\_A00\_0001 and Ham\_DW\_Rgt\_L sequences.

<figure><img src="../.gitbook/assets/image (307).png" alt=""><figcaption></figcaption></figure>

5. Add the Data Handling step Generate Mapping File to your method after the first pipetting loop
   1. Generate mapping for the Nun\_96\_Fl\_Lb\_0001 and Ham\_DW\_Rgt\_L sequence. \
      ![](<../.gitbook/assets/image (308).png>)
   2. Use the Customize Button to report only wells “Without errors only” and to sort the output file by column (A1, B1, C1).
   3. Use the default report name and directory (\<LabID>\_\<BC>\_\<No>.xls).
6. Add a second Generate Mapping File to your method after the second pipetting loop to map the Nun\_96\_Fl\_Lb\_0001 and SMP\_CAR\_24\_15x75\_A00\_0001 transfers.  Use the same settings as the previous Generate Mapping File step.
7. Save and launch Run Control.  Simulate the method and correct any errors.  Check the mapping files have been created correctly.  Notice the reporting provided for the Serial Dilution pipetting action.
