---
description: >-
  Using the CO-RE 96 Head, create a new Method that will transfer liquid from
  four 96 well plates to a 384 well plate.
---

# Example 5: Defining and Using Sequences Using the CO-RE 96 Head

1. Create a new Method and save as Plates96\_to\_Plate384.\


<figure><img src="../.gitbook/assets/image (212).png" alt=""><figcaption></figcaption></figure>

2. Switch to the Deck Layout Editor. &#x20;
3. Switch to the Sequence Tab and select the Head 96 as the Probe Head.

\*Note – Make sure that you have clicked “Clear Selected” before selecting new sequences! Otherwise, the sequences you are selecting will be appended to whatever sequence was already selected.

<figure><img src="../.gitbook/assets/image (213).png" alt=""><figcaption></figcaption></figure>

4. Create a new Sequence encompassing all four 96-well plates and save it as PlatesX4
5. Use the “Advanced…” button to re-sort the 384-Well Plate sequence for use with the CO-RE 96 Head:
   1.  Select the existing 384-Well plate sequence from the list\


       <figure><img src="../.gitbook/assets/image (214).png" alt=""><figcaption></figcaption></figure>
   2. &#x20;Click the “Advanced…” button   &#x20;
   3.  Click the “Apply Stamp Tool” button\


       <figure><img src="../.gitbook/assets/image (215).png" alt=""><figcaption></figcaption></figure>
   4. Click “Ok”
6. Build the Method using the CO-RE 96 Head steps:
   1.  a. Pickup 300µL Standard Tips\


       <figure><img src="../.gitbook/assets/image (216).png" alt=""><figcaption></figcaption></figure>
   2. Aspirate and Dispense four times from PlatesX4 to Nun\_384\_sq\_0001 each time transferring 50µL   &#x20;
   3.  Eject tips


7. Save and launch Run Control. Simulate the method.



Optional Expert Challenges

1\.    Using “Save As”, save a copy of the method, call it Plates96\_to\_Plate384\_Extra.

2\.    Create a Sequence over the 384-Well plate that will follow the quadrant pattern A1, B2, A2, B1 and save it as Quad384.

3\.    Create another sequence that includes Nun\_96\_Fl\_Lb\_0001, Nun\_96\_Fl\_Lb\_0003, Nun\_96\_Fl\_Lb\_0002, Nun\_96\_Fl\_Lb\_0004 in that order and save it as MixedPlates.

4\.    Copy and paste the steps above to pipette with these new sequences.

5\.    Save and launch Run Control.  Simulate the method.

\* Note - During execution of a Method in the Run Control, if the Method aborts and this error message appears, check the step that caused the error.  Is the Sequence Counting set up to Automatic or Manual?

&#x20;

<figure><img src="../.gitbook/assets/image (275).png" alt=""><figcaption></figcaption></figure>
