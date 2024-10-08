# Helpful Hints

## Define Special Labware Data / Parameters Only Once

<table data-header-hidden><thead><tr><th width="145"></th><th></th></tr></thead><tbody><tr><td><img src="../../../.gitbook/assets/image (10) (1) (1) (1) (1).png" alt="" data-size="original"></td><td><p>NOTE</p><p>It is possible to unmark the “Generate default deck sequence” in the “Labware” Tab. In this case, no default sequences are created. This option is helpful if many special sequences have to be created.</p></td></tr></tbody></table>

If the default values for GripForce, GripWidth, GripHeigth, OpeningWidthBeforeAccess (because an own new plate labware has been created or the method must use different values) are not used, it would seem sensible to save these parameters in a variable. This can be done by selecting “View” -> “Variables” in the Method Editor.

<figure><img src="../../../.gitbook/assets/image (105).png" alt=""><figcaption></figcaption></figure>

1. To create a new variable, enter the Context Menu with a right mouse click and select “New”. The dialog box below will then appear and can be filled out.&#x20;
2. It is now possible to create many variables as needed.&#x20;
3. These variables can now be used in all iSWAP or CO-RE gripper commands for the special plate.&#x20;
4. If there are multiple grip commands for this plate in the method, it is much faster to change these values once in the variable definition. Of course, every plate type needs its own parameters.

## Move to Positions Outside of the Slot Area

The iSWAP is able to reach positions outside the slot area or below the deck’s surface (check the specifications for the exact range).&#x20;

Use the “AdjustPosition” Function (double click on the labware) to move a plate outside the slot area. Find the position using the \[Move Probe].&#x20;

<figure><img src="../../../.gitbook/assets/image (106).png" alt=""><figcaption></figcaption></figure>

If a collision is possible (e.g. with the housing of a reader), select “Complex Movement” as the “Movement Type” and define a “Retract Distance” greater than the plate length. Refer to the image below.

<figure><img src="../../../.gitbook/assets/image (107).png" alt=""><figcaption></figcaption></figure>

All bending and turning moves are now executed in a way which is directed away from the housing. The iSWAP will drive to the position using x-drive.
