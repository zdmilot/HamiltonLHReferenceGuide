# Programming the iSWAP

The following example demonstrates the use of iSWAP with Microlab STAR. A plate is transported from a stacker to a processing position. Here, its plate barcodes is also read. After pipetting some reagent, the plate is brought to a reader and read (simulated). Then, the plate is transported to an output stack.

## Creating the Deck Layout

<figure><img src="../../../.gitbook/assets/image (95) (1) (1).png" alt="" width="375"><figcaption></figcaption></figure>

<table data-header-hidden><thead><tr><th width="145"></th><th></th></tr></thead><tbody><tr><td><img src="../../../.gitbook/assets/image (10) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" data-size="original"></td><td><p>NOTE</p><p>To save deck space, the stacker carrier can be positioned 4 tracks to the left of the deck (track positions –3 to +3), and the plates will still be fully accessible by the iSWAP.</p></td></tr></tbody></table>



## Creating the Sequences

1. Click the “Sequences” Tab and create the following sequences:&#x20;
2. On the foremost plate stack, select only the well A1 of all 9 plates. Make sure the stamp tool is set to “Single position select” and the sorting option is “Top Down” as shown below. \
   ![](<../../../.gitbook/assets/image (96) (1) (1).png>)\

3. This means that the stack from top to bottom is used as a SOURCE stack. \
   ![](<../../../.gitbook/assets/image (97) (1) (1).png>)\

4. In the “Advanced” Window, check if the plate on top (the one with the highest z-coordinate is on sequence position one. Save the sequence as ‘InputStack’. \
   ![](<../../../.gitbook/assets/image (98) (1) (1).png>)\
   \

5. Do the same for the output stack on position 4. But this time, sort the sequence to start with the deepest position (sorting option is “Descending”).&#x20;
6. Save this sequence as “OutputStack”&#x20;
7. Rename the sequence “rgt\_cont\_120ml\_a00\_0001” to “Reagent”.



## Command Description

The following tables give a brief overview of the available ML STAR-specific iSWAP commands.

{% tabs %}
{% tab title="Easy Steps" %}
| Command         | Icon                                                                                                                            | Action Performed              |
| --------------- | ------------------------------------------------------------------------------------------------------------------------------- | ----------------------------- |
| iSWAP Transport | <p><br><img src="blob:https://app.gitbook.com/b9657d03-436a-449d-96a9-621d4ec5f8cb" alt="NewIMAGES/iswaptransport.bmp"><br></p> | Transport a plate with iSWAP. |
{% endtab %}

{% tab title="Single Steps" %}
| Command                        | Icon                                                                                                                                         | Action Performed                                                                                  |
| ------------------------------ | -------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------- |
| iSWAP Get Plate                | <p><br></p><p><img src="blob:https://app.gitbook.com/bcb46329-a13d-4496-b30c-a6f9b4463b2b" alt="NewIMAGES/cmdgetPlate.bmp"></p>              | Picks up a plate from the defined position.                                                       |
| iSWAP Place Plate              | <p><br></p><p><img src="blob:https://app.gitbook.com/2091b377-9f72-4378-9212-e599a8f0a9b2" alt="NewIMAGES/cmdplacePlate.bmp"></p>            | Sets a plate down in a defined position.                                                          |
| iSWAP Move Plate               | <p><br></p><p><img src="blob:https://app.gitbook.com/ba5b0661-9b7a-420d-a097-4d050139f6ca" alt="NewIMAGES/cmdmovePlate.bmp"></p>             | Transfers a plate to another sequence.                                                            |
| iSWAP Open Gripper             | <p><br></p><p><img src="blob:https://app.gitbook.com/6a8780f9-57e6-4363-8cdb-a9d2a4f021c5" alt="NewIMAGES/cmdopenGripper.bmp"></p>           | Spreads the fingers of iSWAP’s robotic hand.                                                      |
| iSWAP Close Gripper            | <p><br></p><p><img src="blob:https://app.gitbook.com/a7da62f6-32bf-4f67-9599-0e5d1245c0e3" alt="28"></p>                                     | Closes the fingers of iSWAP’s robotic hand.                                                       |
| iSWAP Read Plate Barcode       | <p><br></p><p><img src="blob:https://app.gitbook.com/e47ff9c1-f075-4b6b-a525-1ec41b22ed8e" alt="NewIMAGES/cmdreadBarcode.bmp"></p>           | iSWAP transports the labware item it is holding to the barcode reader so its barcode can be read. |
| iSWAP Get First Plate Position | <p><br></p><p><img src="blob:https://app.gitbook.com/4a48ac93-dc2c-4635-9fe3-602f798f5607" alt="NewIMAGES/CmdgetfirstPlatePosition.bmp"></p> | Sequence over several plates is checked for the first plate position.                             |
| iSWAP Park                     | <p><br></p><p><img src="blob:https://app.gitbook.com/09436efe-b9dc-4af2-970b-8da737ada2a7" alt="NewIMAGES/cmdparkiswap.bmp"></p>             | Parks the iSWAP under the pipetting arm.                                                          |
{% endtab %}
{% endtabs %}



## Creating the Method

To create the required method:&#x20;

1. Drag and drop an “iSwap Transport” Step into the method. Since this is an Easy Step, an initialize step is not needed to initialize the instrument. \
   ![](<../../../.gitbook/assets/image (99) (1) (1).png>)\

2. Set the ‘InputStack’ sequence as the get sequence. Activate the ‘Auto increment’ to make sure the current position points to the next plate after getting this one.&#x20;
3. Setting the ‘Search source labware first’ will force the iSWAP to check where the first free position is. This is especially helpful if the loading state of a stack is not known. The iSWAP will check this and set the current position according to the first free position.&#x20;
4. Activate the ‘Read plate barcode’ box to identify the plate. The Autoload will move to track 12 to read the plate’s barcode. If the default settings from this step are being used then there is no risk of collision. That means that the barcode reading with iSWAP is possible even on a fully loaded deck.&#x20;
5. Set the “Parking the iSWAP after labware is placed” to On.&#x20;
6. Use a “Aliquote” Smart Step to pipette 50μl of reagent over the full plate. Even if the sequence of the Reagent trough is used up, it will still restart at the beginning, since the Radio Button is set to \[No, reuse the sequence from the beginning if necessary]: ![](<../../../.gitbook/assets/image (100) (1) (1).png>)\

7. Also make sure the “Initial sequence manipulation” are set as follows: \
   ![](<../../../.gitbook/assets/image (101) (1) (1).png>)\

8. Because the sequence ‘Processing’ is used both for pipetting and transport, the “Final sequence manipulation” should be used as follows: \
   ![](<../../../.gitbook/assets/image (102) (1) (1).png>)\

9. Now, use an “iSwapTransport” Step to bring the plate from the “Processing” Position to the “Reader” Position. Do not park the iSWAP.&#x20;
10. Since there is no reader connected, a comment step is used to simulate this.&#x20;
11. After reading, the plate has to be taken at the reader position and brought to the output stack. Make sure the “Auto increment” is only set at the “Output Stack” Place Sequence.&#x20;
12. To have all plates processed, create a loop and move all steps inside. The loop limitation should be the sequence ‘InputStack’. \
    ![](<../../../.gitbook/assets/image (103) (1) (1).png>)\

13. To make the method perfect, add an iSWAP park step at the end (the transport step in line 6 was set to park iSWAP = Off).&#x20;
14. When all of the steps have been done, the method should look like this: \
    ![](<../../../.gitbook/assets/image (104) (1) (1).png>)\


## &#x20;
