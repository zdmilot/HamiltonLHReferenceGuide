---
description: >-
  Using our previous method, expand the functionality to move from the sample
  tubes to all of the plates using sequences.
---

# Example 4: Defining and Using Sequences for the 1000uL Channel

Here we will learn to transfer liquid from the first 8 sample tubes to the first 8 wells on all 96-well plates. &#x20;

\* Note:  Because the first 8 positions of the Sample Tubes sequence are being reused, the Sequence counting for all Aspirate steps needs to be set to Manual.



<figure><img src="../.gitbook/assets/image (209).png" alt=""><figcaption></figcaption></figure>

1. Begin work on your previous method, Tubes\_to\_Plates.  Go ahead and select “Save As” from the File dropdown menu.  Save this file as Tube\_to\_Plates\_Part\_B.
2. Once you’ve saved the file, go to the 1000µL Channel Aspirate (Single Step) and change the Sequence counting according to the note above. &#x20;
3. Now copy the existing Aspirate and Dispense steps.  Paste them between the Dispense and Tip Ejectsteps and make sure the order of operations is correct. &#x20;
4. Do this until you have 4 pairs of Aspirate and Dispense steps.  Make sure the order of operations is correct. &#x20;
5. Modify the second Dispense step to dispense to the second plate (Nun\_96\_Fl\_Lb\_0002)
6. Modify the third and fourth Dispense steps to dispense to the third and fourth plates respectively (Nun\_96\_Fl\_Lb\_0003, Nun\_96\_Fl\_Lb\_0004)
7. Save your work.  Test Run Method in Simulation and correct any errors.

&#x20;

Now looking at this example, it seems a little messy.  Let’s use a sequence to clean up our method, allowing the computer to keep track of where the pipetting needs to be, instead of us manually managing it. &#x20;

&#x20;

&#x20;

GOAL:  Using our previous method, expand the functionality to move from the sample tubes to all of the plates using one sequence.

&#x20;

8. To create a new sequence, toggle to the Deck Layout view.  Look for the “Sequences” tab (next to the labware tab from our first challenge).&#x20;

<figure><img src="../.gitbook/assets/image (210).png" alt=""><figcaption></figcaption></figure>

9. Create a new Sequence by selecting the first column on each of the four 96-Well Plates.  Once selected, select “Save As” and name it Column1x4.  It will now appear in the Deck Sequences scrollable-list. &#x20;

\*Pro Tip – Make sure your Stamp Tool is set to 1000µL Channels. Then you can select the sequence easily by clicking on the first well (A1) on each of the plates.  4 clicks, and you’ve built the whole sequence. &#x20;

10. Modify all four Dispense steps to dispense to this new Column1x4 sequence. Sequence Countingshould still be set to Automatic for the Dispense step.
11. Save your work.  Test run in Simulation and fix any errors.

&#x20;

## Optional Expert Challenge

1. Create a new Sequence that consist of the first 8 wells on all four 96-well plates, but starting with the 4thplate and then the 3rd, 2nd, and 1st plates.  Save it as Column1x4\_Reverse.&#x20;
2. Create a new Sequence that consist of the first 8 tubes of all four sample tube carriers, then the next 8 tubes of all four sample tube carriers, and finally the last 8 tubes of all four sample tube carriers.  Save it as Tubes\_Combined and use the Play Sequence button to play and check these two new sequences.

<figure><img src="../.gitbook/assets/image (211).png" alt=""><figcaption></figcaption></figure>
