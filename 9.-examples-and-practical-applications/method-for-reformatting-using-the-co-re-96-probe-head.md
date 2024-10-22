# Method for Reformatting using the CO-RE 96 Probe Head

This method copies four 96-well plates into a 384-well plate using the CO-RE 96 Probe Head.

First, make sure that the CO-RE 96 Probe Head is activated in the Hamilton System Configuration Editor.

Now, it is possible to create a new method named “Demo96To384.med”.

To create this Deck Layout perform the following steps:

1. Start the Method Editor.
2. Select “New  Method” from the File Menu in the Method Editor. A prompt will then ask for a name to be assigned to the new method.
3. Enter a name, e.g. “Demo96To384.med” and click the \[Save] Button. A new method window and a new “System Deck” Window are displayed, both empty.

<figure><img src="../.gitbook/assets/image (89) (1).png" alt=""><figcaption></figcaption></figure>

4.  Click the “Labware” Tab above the System Deck View. A list of labware is displayed on the left-hand side.\


    <figure><img src="../.gitbook/assets/image (90) (1).png" alt=""><figcaption></figcaption></figure>
5. Type “Slide” in the search labware field. Drag the “Core96SlideWaste” into the left bottom edge of the instrument deck. A frame will indicate the position where to release.
6. Type “L5 MD” in the “Search Labware” Field. “Drag and Drop” a “PLT\_CAR\_L5MD\_A00” onto the deck.
7. Set the Stamp Tool to “Head 96”.\
   \
   ![](<../.gitbook/assets/image (91) (1).png>)\

8. Key in ‘Nunc’ in the “Search Labware” Field. “Drag and Drop” four “Nunc 96 Fl lb (low border)” plates to position 1-4 of the plate carrier.
9. On the plate carrier’s position 5, place the plate “Nunc\_384\_Sq.rck”.
10. Key in “ST 48” in the “Search Labware” Field. Add the “TIP\_CAR\_480\_ST\_A00”.
11. Save the Deck Layout.

<table data-header-hidden><thead><tr><th width="98"></th><th></th></tr></thead><tbody><tr><td><img src="../.gitbook/assets/image (9) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" data-size="original"></td><td><p>ATTENTION</p><p>Be aware that the CO-RE 96 Probe Head may require more space to pick up tips than the single pipetting channels.</p></td></tr></tbody></table>



***

## Creating the Sequences

Now, define the necessary sequence to be used in this method. To define a sequence follow these:

1. Click the “Sequences” Tab in the Method Editor. In the upper section, the “Sequence Editor” Screen is displayed.
2. Zoom in by using the + zoom from zoom in/out toolbar ![](<../.gitbook/assets/image (93) (1).png>) , the “View” Menu in the Method Editor or by using the scroll wheel of the mouse.
3. Use the rubber band function over all four 96-well plates. All wells of the four selected plates are highlighted as seen in the image below.\
   \
   ![](<../.gitbook/assets/image (92) (1).png>)\

4. Save this sequence as “AllFour96WellPlates”.\
   ![](<../.gitbook/assets/image (94) (1).png>)
5. Save the new sequence by clicking \[OK]. All the necessary sequences for the method have been created.
6. Click on the “Method Editor” Icon to activate the Method Editor.

## Creating the Method

The next step is to write the method in the Method Editor. Add all steps by dragging icons from the toolbox and dropping them into the method window. Finally, the method should look as displayed below:\


<figure><img src="../.gitbook/assets/image (95) (1).png" alt=""><figcaption></figcaption></figure>

In more details, the necessary steps for the method are the following:

1. Add the “Load” Smart Step by dragging and dropping it from the toolbar into the method window: the “Load” Dialog appears as shown below.\
   ![](<../.gitbook/assets/image (96) (1).png>)
2. Click on the drop down list in the “Sequence” Section and select the “ML\_STAR.AllFour96WellPlates” Sequence.
3. Use the \[Add] Button to create two more lines. Add the “ML\_STAR.Nun\_384\_Sq\_0001” sequence and the “ML\_STAR.MlStar300ulStandardVolumeTip” Tip Sequence.
4.  Finish the “Load” Step with \[OK].\
    \


    <table data-header-hidden><thead><tr><th width="98"></th><th></th></tr></thead><tbody><tr><td><img src="../.gitbook/assets/image (10) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" data-size="original"></td><td><p>NOTE</p><p><em>The sequences to load can be selected in the Sequence View and then dragged and dropped into the list fields in the “Load” Dialog (Ctrl + left mouse drag and drop). The two windows (Deck Layout View and “Load” Dialog) are interactive: when a sequence in the “Load” Dialog is selected, this sequence flashes in a specific color in the Deck Layout View.</em></p></td></tr></tbody></table>

    \

5. Insert a “Loop” from the “General Steps”.
6. Activate the \[Iterate over sequences and adjust sequences] Radio Button and tick the box for the “ML\_STAR.AllFour96WellPlates”.\
   \
   ![](<../.gitbook/assets/image (97) (1).png>)\

7. Click \[OK] to close the “Loop” Step.
8. Add a “CO-RE 96 Head Aspirate” Step to the loop. Fill out the input fields as follows:\
   ![](<../.gitbook/assets/image (99) (1).png>)
   * Aspirate sequence: “ML\_STAR.AllFour96WellPlates”
   * Volume: 50ul
   * Liquid: “DMSO”, the Dispense mode is “Jet Empty Tip”
   * Liquid class: “StandardVolume\_96COREHead1000ul\_DMSO\_DispenseJetEmpty”
   * Tip pickup sequence: “ML\_STAR.MlStar300µlStandardVolumeTip”
9. Click \[OK] to close and save the aspirate step.
10. Add a “CO-RE 96 Head Dispense” Step after the aspirate step. Fill out the input fields as follows:\
    \
    ![](<../.gitbook/assets/image (101) (1).png>)
    * Dispense sequence: “ML\_STAR.Nun\_384\_Sq\_0001”
    * Volume: 50ul
    * Dispense position: “Fix height”, 5mm from container bottom
    * Tip handling after dispense: “Eject tip to default waste”\

11. Then add the “Unload” Smart Step into the method.

\
