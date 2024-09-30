---
description: >-
  Build a Method that will transfer liquid from sample tubes to the first column
  of a 96-well plate using 1000µL channels.
---

# Example 3: Putting together Steps for a Method

The Method will pick-up tips, aspirate from sample tubes, dispense to plate, and eject tips.

1. With your previous method Basic\_Deck still open, go to File –> New -> Method from the toolbar dropdown.  When asked for a name, give it the name Tubes\_to\_Plates.
2.  The new method will default to the Method Editor view. \


    <figure><img src="../.gitbook/assets/image (50) (1) (1).png" alt=""><figcaption></figcaption></figure>
3.  Add the Initialize step which is required before any other pipetting or transport steps.\


    <figure><img src="../.gitbook/assets/image (51) (1) (1).png" alt=""><figcaption></figcaption></figure>
4. Pick up 300µL Standard Volume Tips using the 1000µL Channel Tip Pick Up (Single Step).
5.  Think about manual pipetting, once we have picked up tips, what do we need to do?  We need to aspirateliquid.  Go ahead and add a 1000µL Channel Aspirate (Single Step).  We need to tell the STAR where the liquid is coming from, so select your Sample Tubes Sequence.\


    <figure><img src="../.gitbook/assets/image (52) (1) (1).png" alt="" width="248"><figcaption></figcaption></figure>
6.  Now we need to tell the STAR where the liquid needs to go, so now add a 1000µL Channel Dispense (Single Step). Where does the challenge ask for the liquid to go? Into one of our MTPs, so select the appropriate sequence, our Nun\_96\_Fl\_Lb\_0001 plate sequence.\
    \


    <figure><img src="../.gitbook/assets/image (53) (1) (1).png" alt="" width="233"><figcaption></figcaption></figure>
7. To avoid “contamination” we need to eject the tips.  Add a 1000µL Channel Tip Eject (Single Step).  For now, use the default parameters.\
   \

8. Check that your method’s steps are in the correct order of operations and then save your work. &#x20;

<figure><img src="../.gitbook/assets/image (54) (1).png" alt=""><figcaption></figcaption></figure>

9.  Now we need to tell the STAR to run the method. This is accomplished through Hamilton Run Control. You can launch Run Control from the traffic-signal type icon. Test Run the Method in simulation, and correct any errors.\


    <figure><img src="../.gitbook/assets/image (56) (1).png" alt=""><figcaption></figcaption></figure>
10. Once Run Control is launched, make sure Run Control is in Simulation mode. This is indicated by the Green (Instrument Mode) or Yellow (Simulation Mode) section of the toolbar. If Run Control is in Instrument Mode, you will get an error (unless you are actually connected to an instrument). The Error will appear as:\


    <figure><img src="../.gitbook/assets/image (57) (1).png" alt=""><figcaption></figcaption></figure>

    If this occurs, simply abort the method, go to the Settings drop down at the top of the screen and select “Simulation”. Once the instrument’s connection has been successfully simulated, the status toolbar will turn yellow and will read Idle (Simulator).\
    \


    <figure><img src="../.gitbook/assets/image (59) (1).png" alt=""><figcaption></figcaption></figure>



**\*Note – ALWAYS** be cautious of what status the instrument is in.  If you need to simulate the method before running, make sure that it is functioning correctly _before_ running on the physical instrument. &#x20;
