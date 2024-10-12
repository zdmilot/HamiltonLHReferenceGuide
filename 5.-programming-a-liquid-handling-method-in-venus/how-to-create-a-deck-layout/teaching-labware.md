# Teaching Labware

## Teaching Labware with the 1000µl-Pipetting Channels

Teaching means:

* Manually guiding a pipetting channel to a particular location on the deck with tools in the VENUS Software.
* Assigning the name to the location
* Instructing the ML STAR to “remember” it.

\


The precise position (the x-y-z coordinates) of labware items can be “taught” in this way, using the needle from the teaching station.

Later, the only need is to specify the Lab ID and the STAR instrument instantly “remembers” exactly where it is positioned on the deck.

The image below shows a teaching station on the waste block with all needles loaded.

| <img src="../../.gitbook/assets/image (45) (1) (1).png" alt="" data-size="original"> | To teach the labware, only the 2nd needle is picked up by the pipetting channel. Make sure that at least this needle is loaded before activating the “Move Probe” Function. |
| ------------------------------------------------------------------------------------ | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |



<table data-header-hidden><thead><tr><th width="125"></th><th></th></tr></thead><tbody><tr><td><img src="../../.gitbook/assets/image (10) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" data-size="original"></td><td><p>NOTE</p><p><em>The teaching needles are optionally available and not part of the standard delivery package. They are also used in the maintenance methods.</em></p></td></tr></tbody></table>



If the labware to teach is not on the deck, add it.&#x20;

To teach a labware position:

1. By drag and drop, pre-position the plate on the deck.
2.  The “Adjust Labware Position” Dialog will be displayed, as seen on the picture below.\


    <figure><img src="../../.gitbook/assets/image (47) (1) (1).png" alt=""><figcaption></figcaption></figure>

* The red colored well (in the top row) indicates the “first position”.
* The gray colored well (in the bottom row) indicates the “last position”.
* Location: The default x/y/z- coordinate is determined by the mouse-cursor when dropping the labware onto the deck. Keep in mind that the Z-Axis has an offset of 100mm
* Rotation: The labware can be rotated and aligned as required. The rotation functions, the orientation of the labware can also be adjusted.

<table data-header-hidden><thead><tr><th width="125"></th><th></th></tr></thead><tbody><tr><td><img src="../../.gitbook/assets/image (9) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" data-size="original"></td><td><p>ATTENTION</p><p><em>Before the pipetting channel with the teaching needle is moving from the waste block (picking up position) to the rough position of the labware, make sure there is no danger of collision with objects higher than 140 mm (from the deck surface).</em></p></td></tr></tbody></table>



Normally only the first position has to be taught. If the rows and columns of a chosen labware do not correspond to the x/y-movements of the pipetting channels, there is a possibility to teach the first and the last position. This will allow compensating the slightest inaccuracy between the labware and the pipetting channel.

### The Move Probe Function

1.  Click on the \[Move Probe] and the following screen will be displayed.\


    <figure><img src="../../.gitbook/assets/image (48) (1) (1).png" alt=""><figcaption></figcaption></figure>
2. Select “1000μl Channel”
3. The pipetting channel will be moved to the waste block to pick up the teaching needle. With the teaching needle, the instrument moves to the x/y- coordinate of the position to be taught.
4.  The “Move Probe – Key Control” Dialog will appear.\


    <figure><img src="../../.gitbook/assets/image (52) (1).png" alt=""><figcaption></figcaption></figure>
5. As an alternative to step 2, select \[Move to Position...] from the “Tools” Menu.
6. When \[Cancel] is clicked, the pipetting channel is lifted in Z-direction first (to the traverse- height) before moving to the waste block. At the waste block, the pipetting channel ejects the teaching needle. No new positions are stored.\
   \
   The keyboard (arrow keys, page up, page down) can guide the pipetting channel to the labware position. The step size is 1 mm per default. Use +/- keys to increase / decrease the step size.



<table data-header-hidden><thead><tr><th width="125"></th><th></th></tr></thead><tbody><tr><td><img src="../../.gitbook/assets/image (9) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" data-size="original"></td><td><p>ATTENTION</p><p><em>Make sure that the chosen step size will not trigger a crash. The system can be seriously damaged when colliding with the</em> pipetting <em>channels. All collision control must be made by the user</em>.</p></td></tr></tbody></table>



7.  The correct position is reached when the pipetting channel is at the bottom of the first or last well (corresponding with the red / gray position of the labware as seen in the picture of step 2) of the labware. Prevent the pipetting channel from crashing the labware.\
    \


    <table data-header-hidden><thead><tr><th width="125"></th><th></th></tr></thead><tbody><tr><td><img src="../../.gitbook/assets/image (10) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" data-size="original"></td><td><p>NOTE</p><p><em>The reference point for “teaching” is the lower end of the teaching needle and the reference well of the rack which is usually marked in red (upper- and left- most well = A1).</em></p></td></tr></tbody></table>



The actual position and increment step size is displayed.

<figure><img src="../../.gitbook/assets/image (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

<table data-header-hidden><thead><tr><th width="125"></th><th></th></tr></thead><tbody><tr><td><img src="../../.gitbook/assets/image (9) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" data-size="original"></td><td><p>ATTENTION</p><p><em>Make sure that the step size is appropriate. When moving the x-arm with a step size of 100 mm, make sure to decrease the step size first. Otherwise, the pipetting channel will move 100 mm downwards and will possibly crash</em>.</p></td></tr></tbody></table>



8.  Once the position is reached, click \[OK]. The coordinates are then stored. The stored x, y, z coordinates are displayed in the “Adjust Labware Position” Window as shown below.\
    \


    <figure><img src="../../.gitbook/assets/image (2) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>
9. Click \[OK], to transfer the data to the deck layout.

<table data-header-hidden><thead><tr><th width="125"></th><th></th></tr></thead><tbody><tr><td><img src="../../.gitbook/assets/image (9) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" data-size="original"></td><td><p>ATTENTION</p><p><em>Do not use</em> [Move Probe] <em>in the simulation mode. The computer will try to establish a connection to an instrument several times otherwise will prompt a communication error after approximately 10 seconds.</em></p></td></tr></tbody></table>



## Teaching Labware with 5ml-Pipetting Channels

Teaching Labware with the 5ml-pipetting channels is very similar to teaching with 1000µl-pipetting channels. The teaching needle is located on the waste block, in front of the waste bag for tips. Follow the same rules and instructions as given in the Section 6.6 Teaching Labware with the 1000µl- Channels.



<table data-header-hidden><thead><tr><th width="125"></th><th></th></tr></thead><tbody><tr><td><img src="../../.gitbook/assets/image (10) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" data-size="original"></td><td><p>NOTE</p><p><em>The teaching needle is available optionally and not part of the standard delivery package. It is also used in the maintenance methods.</em></p></td></tr><tr><td><img src="../../.gitbook/assets/image (9) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" data-size="original"></td><td><p>ATTENTION</p><p><em>Before the pipetting channel with the teaching needle is moving from the waste block (picking up position) to the approximate position of the labware, make sure there is no danger of collision with objects higher than 140 mm (above the deck surface):</em></p></td></tr></tbody></table>



## Teaching Labware with iSWAP

If the ML STAR is configured with an iSWAP, positions of the plates can be “taught” to it. In order to teach the position of the iSWAP, the labware which will handle is required.

In the following example, a microplate carrier with at least one labware position is used.

<table data-header-hidden><thead><tr><th width="125"></th><th></th></tr></thead><tbody><tr><td><img src="../../.gitbook/assets/image (10) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" data-size="original"></td><td><p>NOTE</p><p><em>For the teaching process, the software requires a defined labware position. For this reason, at least one dummy position for the labware is required.</em></p><p><em>Place the carrier with the labware to the instrument. In the software add the corresponding labware to the deck layout.</em></p></td></tr></tbody></table>



The following steps describe how to teach a position with the iSWAP is done:

1. If the labware to teach is not on the deck, add it now.
2. Using the “Drag and Drop” technique, pre-position the labware on the deck.
3.  After dropping the labware onto the deck the window, as shown below will appear.\
    \


    <figure><img src="../../.gitbook/assets/image (3) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>
4. Clicking \[Move Probe…] will prompt the dialog shown below.
5.  Select “iSWAP” and click \[OK]\
    \


    <figure><img src="../../.gitbook/assets/image (4) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

<table data-header-hidden><thead><tr><th width="125"></th><th></th></tr></thead><tbody><tr><td><img src="../../.gitbook/assets/image (9) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" data-size="original"></td><td><p>ATTENTION</p><p><em>If the iSWAP is moving with the plate to the approximate position, make sure that there is no danger of collision with other objects higher than 140 mm (above the deck surface).</em></p></td></tr></tbody></table>

\


6. Click \[OK] to proceed. The “Teaching with iSWAP” Screen appears.
7. In the “Use labware from sequence” Drop Down List, enter a sequence of a plate that is already in a valid position. Select the labware that the iSWAP has to pick-up for the next steps of teaching. The default x/y-coordinate “Approximate target position” is determined by the mouse-cursor when dropping the labware to the deck.
8.  The iSWAP picks up the selected labware and moves to the x/y - coordinate of the position to be taught.\


    <figure><img src="../../.gitbook/assets/image (5) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>
9. The keyboard (arrow keys, page up, page down) can guide the iSWAP to the labware. The correct position is reached if the labware is touching the bottom of the transfer position. Prevent the iSWAP from crashing.
10. Click \[OK] to proceed.\


    <figure><img src="../../.gitbook/assets/image (6) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>
11. When \[Cancel] is clicked, the iSWAP puts the labware back to the picking-up position and moves to its park position.\


    <figure><img src="../../.gitbook/assets/image (7) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>
12. The taught coordinates are now stored. If the iSWAP cannot move up to the traverse height (e.g. shelving position where the iSWAP would collide with the shelf above it).
13. Click \[OK] if the iSWAP is in a collision-free position.\


    <figure><img src="../../.gitbook/assets/image (8) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>
14. The coordinates have been stored. The taught x/y/z coordinates are displayed in the “Adjust Labware Position” Window.
15. Press \[OK] to transfer the data to the deck layout.\
    \


    <figure><img src="../../.gitbook/assets/image (10) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>
16. The iSWAP places the labware back to the pick-up position and returns to its park position.

\
