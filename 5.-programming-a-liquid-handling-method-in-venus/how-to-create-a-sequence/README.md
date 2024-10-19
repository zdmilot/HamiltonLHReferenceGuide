# How to Create a Sequence

The sequence editor is part of the system deck editor. It is activated by clicking the “Sequences” Tab. With the sequence editor, the programmer declares series of cavities (containers) in an order in which they are processed by the instrument.

## Automatic Creation of a Sequence

1. If a labware is added to the deck, a default sequence is generated automatically (as long as the ‘Generate default deck sequence’ checkbox is activated).
2.  The system checks which stamp tool is activated. The active stamp tool will be used for the sequence creation in the "Stamp Tool" Tab. To change the stamp tool, click the appropriate Probe Head Type.

    \


    ![stamp](../../.gitbook/assets/Image\_446.gif)

    \

3.  To enable the automatic sequence generation, click on the “Labware” Tab, used when adding labware. Tick the “Generate default deck sequence” Box as highlighted on the image below.

    <figure><img src="../../.gitbook/assets/Image_447.png" alt=""><figcaption></figcaption></figure>
4. Dependent to the active stamp tool, the automatic generated deck sequence on the new labware will be created.

<figure><img src="../../.gitbook/assets/Image_448.jpg" alt=""><figcaption></figcaption></figure>

\


### Creating a Sequence Manually

Besides automatic created sequences, the Hamilton VENUS Software also allows the creation of sequences manually. This gives maximum flexibility and allows total control of the pipetting process. As a simple example, pipetting into every odd column of a plate shall be done. Instead of jumping around in an automatic sequence by only setting a current and end position, create a sequence that only contains all desired wells for the aspiration.



### To create a new sequence, perform the following steps:

1. Open the system deck and select the “Sequences” Tab.
2. Click the \[Clear Select] Button to make sure no sequence is selected.
3.  In the system deck window, select by clicking on the wells to add these labware positions to a sequence. The selected positions are highlighted in dark brown as shown below.



    Nun\_96\_Fl\_Lb\_000\
    ![image](../../.gitbook/assets/Image\_449.gif)\

4. Left click and do not release. Continue by moving over the desired positions, when the positions are covered by the rectangular parameter, release the button.\
   \
   It is possible to use the rubber band action to add positions to a sequence. Please notice that the selected stamp tool will be used to sort the sequence when the rubber band action is being used.\


<table data-header-hidden><thead><tr><th width="145"></th><th></th></tr></thead><tbody><tr><td><img src="../../.gitbook/assets/image (10) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" data-size="original"></td><td><p>NOTE</p><p>To select a labware position, click on it once. If a labware position is clicked the second time, it will be added to the sequence again.</p></td></tr></tbody></table>

5.  Once all the positions belonging to a sequence have been selected, click the \[Save as] Button found on the upper left side of the window. A save dialog where the name for the sequence is specified will be prompted.\
    ![image](../../.gitbook/assets/Image\_451.jpg)


6. Make sure to use relevant names such as “TargetPlateOddColumns” instead of “MySequence1”. Enter a name for the sequence and click \[OK]. The sequence is shown with the name in the “Deck sequences” List at the top center of the deck layout section, and the color changes from dark brown (draft sequence) to light brown (saved sequence).
7. In creating sequences on stacked labware (e.g. a stack of plates), select the Stack Z-Height Order in the Stamp Tool box first. The sequence will then be sorted top-down (descending) or bottom-up (ascending), depending on the chosen sorting method.

![image](../../.gitbook/assets/Image\_452.png)

\


### Checks

To envision the created sequence, select the sequence name from the “Deck sequences” List. The name of the sequence appears in blue, and the positions belonging to this sequence are highlighted in light brown.

1.  To have the sequences checked by the system, click \[Validate] on the lower left side. A dialog will appear listing the invalid positions; otherwise it will state the following message: “All sequences for this instrument are valid”.

    ![checks](../../.gitbook/assets/Image\_453.gif)

    or
2.  Use the “Play Sequence” Function to see the sequence being processed. The “Play” Function is controlled by three buttons above the tabs in the upper half of the method editor screen. The \[Play] Button first deselects all positions in the sequence and then plays the sequence. As each position is selected, it is at the same time coated in the deck-layout view and highlighted in the grid and tree views. Play can be paused at any time and can be resumed by clicking on the \[Play] Button again.\


    ![play sequence](../../.gitbook/assets/Image\_454.gif)

    \
    Play continuously, Stop, Play the sequence step by step
3. Select the sequence to be played in the Deck Sequence list by making use of the buttons below.



### Advanced Sequence editing

To see all positions of a sequence in a list, double click the sequence or select the sequence and click \[Advanced] found on the left side of the “Deck sequences” List window. The position of the selected sequence will be displayed, as shown in the image below.

![image](../../.gitbook/assets/Image\_458.jpg)

The grid contains one row for each labware position in the sequence.

### Editing positions

The “Advanced” Window offers several sorting options.

1. **Sort by column:** This allows sorting the sequence by LabwareID, PositionID, x, y and z. It is possible to specify up to three sorting options. Sorting will be executed as soon as the \[Sort All] Button is clicked.
2. **Sort by direction:** This allows sorting the whole sequence from top-down or left-right. Sorting will be executed as soon as the \[Sort] Button is clicked.
3. **Apply Stamp Tool:** This sorting option refers to the selected stamp tool in the stamp tool panel. When for example the “Head 96” stamp tool is activated, the sequence will be sorted to process the positions with the Head 96.
4. _**Delete Selected Positions**_ is used to delete one or more positions from the sequence. Click on the index (the number on the left side) of the position(s) to delete and click the \[Delete Selected Positions] Button.

<figure><img src="../../.gitbook/assets/image (75) (1) (1).png" alt=""><figcaption></figcaption></figure>

The \[CTRL] Button can be used to select several specific positions in the sequence. All selected sequence positions are highlighted in the deck layout.

\


<div>

<figure><img src="../../.gitbook/assets/image (76) (1) (1).png" alt=""><figcaption></figcaption></figure>

 

<figure><img src="../../.gitbook/assets/image (77) (1) (1).png" alt=""><figcaption></figcaption></figure>

</div>



### Saving the Sequence

Once the labware positions in the sequence are in the desired order, save the sequence by clicking the \[Save as] Button.

Saving affixes the order of each row in the grid as the order of the labware positions in the sequence. Upon saving, a prompt will request a name for the sequence.

Any existing sequence in the Deck Layout can be activated for viewing and/or editing by selecting the sequence name in the Drop-Down Menu.

Additional labware positions can be inserted in the active sequence by selecting them in the Deck Layout View. Existing positions can be removed. Positions can be reordered as described above. The sequence can be resaved to fix its positions according to the new order.

\
