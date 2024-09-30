---
description: >-
  Modify previous Method from Challenge 3 so they will repeatedly aspirate and
  dispense a fixed number of times using the Loop-End Loop step rather than
  having multiple copies of the same steps.
---

# Example 6: Repeat steps with Loop-End Loop

1. Navigate to the Sequence Tab, then to the Stamp Tool, reselect the 1000µl Channels as the Probe Head.
2. Open Tubes\_to\_Plates\_Part\_B.med from Challenge 3.  Select the “File” and “Save As” from the dropdown and save the method as Tubes\_to\_Plates\_LoopStep.
3. Add a Loop - End Loop step just above the first Aspirate step. Select Iterate a fixed number of times and set the Number of iterations to 4.

<div>

<figure><img src="../.gitbook/assets/image (271).png" alt="" width="140"><figcaption></figcaption></figure>

 

<figure><img src="../.gitbook/assets/image (273).png" alt="" width="209"><figcaption></figcaption></figure>

</div>

4. Move one pair of the Aspirate – Dispense steps into the Loop – End Loop step. &#x20;
5. Delete the other three Aspirate-Dispense steps outside the Loop.

<figure><img src="../.gitbook/assets/image (274).png" alt=""><figcaption></figcaption></figure>

6. Save and launch Run Control. Simulate the method and correct any errors.
7. Now that you’ve completed looping with a 1000µl Channel, let’s try it with our 384-Well plate stamp using the CO-RE 96 Head.  Open Plates96\_to\_Plate384 from Challenge 4.  Select the “File” and “Save As” from the dropdown and save the method as Plates96\_to\_Plate384\_LoopStep.
8. Add a Loop- End Loop step to the method just above the first Aspirate step.  Select Iterate a fixed number of times and set the Number of iterations to 4.
9. Move one pair of the Aspirate – Dispense steps into the Loop – End Loop step. &#x20;
10. Move the Tip Pickup and the Tip Eject into the Loop-End Loop step.&#x20;
11. Delete the other three Aspirate-Dispense steps.

<figure><img src="../.gitbook/assets/image (275).png" alt=""><figcaption></figcaption></figure>

12. Save and launch Run Control. Simulate the method and correct any errors.
