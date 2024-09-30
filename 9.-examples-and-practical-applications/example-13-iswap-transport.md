---
description: >-
  Using the iSWAP, you will continue building on the previous Method and
  transport a plates from the carrier to an off-deck location and back again.
---

# Example 13: iSWAP Transport

1. Open Stacking Plates.med and create a Group called “CO-RE Transports”.  Place all the CO-RE Transport steps from the previous challenge into this group. &#x20;

<figure><img src="../.gitbook/assets/image (149).png" alt=""><figcaption></figcaption></figure>

2. Modify the deck layout by placing a Nunc plate (NUN\_96\_FL, low border) to the left of the Deck.  When the Adjust Labware Position dialogue window appears, update the location of the first position to:

<figure><img src="../.gitbook/assets/image (150).png" alt=""><figcaption></figcaption></figure>

3. Rename _(Right click -> Properties -> Labware ID)_ this plate to PlateReader.&#x20;
4. Switch back to the Method Editor and add a Loop Step to iterate over TargetCarrier.
5. Inside the loop -&#x20;
   1. Add a Gold Step iSWAP Transport to move a plate from TargetCarrier to PlateReader.
   2. The plate transport for this location is considered a Complex Movement because the robot is transporting off of the physical deck.  In the “Customize” tab select the “Complex Movement” tab.  Check the “Place plate is a complex movement” box and enter the settings as below.\
      ![](<../.gitbook/assets/image (152).png>)
   3. Add a User Output step that displays “_Reading Plate, please wait_” and set Timeout to 10seconds.
   4. Add another Gold Step iSWAP Transport to move the plate back to its original position on the carrier.  Make sure to set the “Get Plate is a complex movement” in the “Customize” tab with the same parameters as before!  This time, insure that the “Park iSWAP after labware is placed” has been selected to “(1) On”.\
      ![](<../.gitbook/assets/image (153).png>)
6. Create another Group and name it “iSWAP Transports”.  Place  the iSWAP steps for this challenge into this group. &#x20;
7. Save and launch Run Control.  Simulate the method and correct any errors.
