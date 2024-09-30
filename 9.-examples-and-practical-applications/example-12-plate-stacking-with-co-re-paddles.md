---
description: >-
  Develop a method that will use the CO-RE Paddles to move plates from a stack
  to a carrier.
---

# Example 12: Plate Stacking with CO-RE Paddles

1. Using your Basic\_Deck layout from the beginning, create a new method and call it Stacking Plates.
2. On the Deep-Well carrier (PLT\_CAR\_L5AC\_A00) add one stack of 4 plates (NUN\_96\_FL, low border).  To do this add one plate to the carrier then right-click on the plate to select Add to Stack from the drop down menu

<figure><img src="../.gitbook/assets/image (147).png" alt=""><figcaption></figcaption></figure>

3. Add the CO-RE gripper paddles (COREGrip Tool OnWaste 1000uL)

<figure><img src="../.gitbook/assets/image (148).png" alt=""><figcaption></figcaption></figure>

4. Switch to the “Sequence” Tab.  Rubber band the A1 well from the stack of plates and save as SourceStack.  Use the “Advanced” button to sort this sequence from the top down.  This sequence should only have one position (A1 well) per plate.&#x20;
5. Create a sequence over the 4 plates on the plate carrier.  Save as TargetCarrier.&#x20;
6. Use the Gold Step 1000uL Channel CO-RE Grip Transport and a Loop step to move the stack of plates, one at a time, from SourceStack to TargetCarrier.  Leave Eject Gripper Tool when finished set to “Off” and remember to check the Auto Increment (same as setting Sequence Counting to Automatic in single steps).
7. And lastly to get rid of CO-RE paddles, add a Single Step Tip Eject and select the CORE Grip Toolsequence as the Eject destination.  Also, set the Channel Selection to match the channels with the paddles.
8. Save and launch Run Control.  Simulate the method and correct any errors.&#x20;

## Optional Expert Challenges

1\.    Save a copy of this Method (File -> Save as...) and call it Stacking Plates Optional.

2\.    Create a second sequence from the stack of plates but sort it from the bottom up.  Save it as StackReturn.

3\.    Create a second sequence over the plates on the carrier but in the reverse order.  Save as CarrierReturn.

4\.    Transport the plates back to their original positions from carrier to the stack using these sequences and a Loop step.
