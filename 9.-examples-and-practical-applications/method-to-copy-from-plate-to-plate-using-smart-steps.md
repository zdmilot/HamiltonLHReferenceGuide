# Method to Copy from Plate to Plate using Smart Steps

The method described in the following “copies” wells and does the following:

* Aspirates liquids from wells on a plate
* Dispenses liquid to the corresponding wells on another plate (A1A1…H12H12)

The transferred volume is 20μl. The method is named “OnePlateToPlatePipette”. The method uses new CO-RE tips for every well. We will start with an empty target plate.

First, an appropriate Deck Layout must be created and saved as “OnePlateToPlatePipette.lay”. The Deck Layout for this method is shown in the following picture.\


<figure><img src="../.gitbook/assets/image (31).png" alt=""><figcaption></figcaption></figure>

***

## Creating the Deck Layout:

1. Start the method editor by clicking on the “Hamilton Method Editor” Shortcut on the desktop.
2. Select “File -> New -> Method” to create a new method. A window opens to save the new method.
3. Enter the same filename and click \[Save]. A new method window and system deck window are opened in the Method Editor. To activate, click the system deck window.
4. Make sure the stamp tool “1000μl Channels” is selected.\
   \
   ![](<../.gitbook/assets/image (32).png>)\

5. Click on the “Labware” Tab.
6. In the list above the tabs, click “ML STAR Carriers  Plate Carriers” and select “PLT\_CAR\_L5MD\_A00”. This is a carrier for microplates. An image of the selected carrier will then be shown in the right-hand box.\
   \
   ![](<../.gitbook/assets/image (33).png>)\

7. “Drag and Drop” the carrier from the box onto the deck.
8. Right-click on the carrier. From the Context Menu, select “Properties”. In the “Properties” Dialog, assign a LabwareID to the carrier, e.g. “SourceCarrier”.\
   \
   ![](<../.gitbook/assets/image (34).png>)\

9. Repeat the steps above to create a second carrier with the name (LabwareID) “TargetCarrier”.
10. Same as the previous steps, add a tip carrier with 300μl tips (without filter).
11. Click “ML STAR Carriers -> Tip Carriers 96”. “Drag and Drop” the TIP\_CAR480\_BC\_ST\_A00 onto the deck. Change the LabwareID of the carrier to “TipCarrier”.
12. Following the previous steps, add a plate from the “Plates -> 96 position plates” to the “SourceCarrier” and the “TargetCarrier”. Open the “Properties” through a right-click on the plate and rename the plates to “SourcePlate” and “TargetPlate”.
13. Select “File -> Save” to save the Deck Layout.

## Creating the Sequence

1. Click the “Sequences” Tab to start editing the sequences
2. The window will be switched to sequence editing
3. Use the magnifying glass to zoom to the region of interest – the two plates and the tip rack.\
   \
   ![](<../.gitbook/assets/image (35).png>)\

4. Click the tip rack entry in the “System Managed Sequences” List.\
   \
   ![](<../.gitbook/assets/image (36).png>)\

5. The positions of the selected sequences are highlighted in the System Deck View.
6. If the \[Play] Button is clicked![](<../.gitbook/assets/image (37).png>), observe that one column of dots at a time changes its color for a short time, beginning at the left column, running from left to right. Simply click the \[Stop] Button in the toolbar to stop the play.
7. The order in which the tips will be processed is optimal for an 8 pipetting channel ML STAR. Note that the default name is given to the sequence automatically. To change or define a sequence name, select the sequence and click the \[Save as] or \[F2] Button.
8. Now, click the source plate entry in the “Deck Sequences” List. Observe that in playing the process order, the single wells will also be processed column by column, from left to right. Stop the play.

## Creating the Method

1. Open the Steps View of the Method Editor through this icon:&#x20;
2.  Writing a method can easily be performed by dragging step icons from the toolbox and dropping them into the method window on the right section of the window. The resulting method will look like the picture shown below.\
    \
    ![](<../.gitbook/assets/image (38).png>)\
    \


    <table data-header-hidden><thead><tr><th width="98"></th><th></th></tr></thead><tbody><tr><td><img src="../.gitbook/assets/image (10) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" data-size="original"></td><td><p>NOTE</p><p><em>For safety reasons, explicit loading (specifying loading commands within the method) is recommended. If no loading commands are specified, no checking of the carrier positions is performed and the user must ensure that all carriers are positioned manually on the correct tracks.</em></p><p><em>The system will be initialized automatically when using Smart Steps.</em></p></td></tr></tbody></table>

    \

3. “Drag and Drop” the “Load” Smart Step into the method window.\
   \
   ![](<../.gitbook/assets/image (39).png>)\

4. Click on \[Add all sequences] to make sure that all carriers are going to be loaded onto the instrument deck.
5. Click on \[Show Details] and leave only the “Reducible” Checkbox for the source sequence enabled, if it is only during run time that the decision on which or how many of the wells of the source plate is to be transferred to the target plate will be made.\
   \
   ![](<../.gitbook/assets/image (40).png>)\

6. For an instrument with the Autoload option, this command loads the carriers automatically onto the instrument deck during run time. For a manual load instrument, this command requests the user to load the carriers for run time.
7. Click \[OK] to continue.\


## Program the Liquid Handling Details

1. Drag the Smart Step “1000μl Channel Pipette – Simple” to the line below the loading step (a simple transfer from plate to plate).
2. Activate the drop-down list and select the instrument used for pipetting. In this example, the “ML STAR” is selected.
3. Select the source and target sequence.\
   ![](<../.gitbook/assets/image (41).png>)\
   \
   or\
   \
   “Drag and Drop” the sequences from the Deck Layout into the input fields.\
   \
   ![](<../.gitbook/assets/image (42).png>)\

4.  Click \[Next >] to continue.\


    <table data-header-hidden><thead><tr><th width="98"></th><th></th></tr></thead><tbody><tr><td><img src="../.gitbook/assets/image (10) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" data-size="original"></td><td><p>NOTE</p><p><em>The “Aspirate” and “Dispense” Sequences can be selected in the Graphic Deck Layout View and then “Dragged and Dropped” onto the list fields in the “Step Wizard” Dialog (Use Ctrl + left mouse click to “Drag and Drop” from deck to step).</em></p><p><em>The two windows (Deck Layout View and Step Wizard) are interactive: when a sequence in the step wizard is clicked, this sequence is highlighted in the corresponding color. All aspirate / pick-up sequences are shown in blue, while all dispense/eject sequences are shown in green.</em></p><p><em>Having a sequence grid in the step (e.g. loading step), the inserted sequences will not only be highlighted but will also be flashing.</em></p></td></tr></tbody></table>
5. Here, the volume to be transferred is specified – 20μl; no additional volume should be aspirated. In this field, it is also possible to use a variable or an array.\
   \
   ![](<../.gitbook/assets/image (43).png>)\

6. In this step, select a tip sequence (e.g. “ML\_STAR.MlStar300ulStandardVolumeTip”) from the drop-down field or “Drag and Drop” it from the Deck Layout. The tip handling chosen here is to take new tips for each sample.\
   \
   ![](<../.gitbook/assets/image (44).png>)\

7. Click \[Next >] to continue.
8. In this example, the dispense mode is set to “Jet” because initially, the target plate is assumed to be empty. The liquid class used in this example is water.\
   ![](<../.gitbook/assets/image (45).png>)\

9. Click “Advanced” to go to the LLD Settings.\

10. On aspiration, capacitive-based LLD may be used.\
    ![](<../.gitbook/assets/image (47).png>)\

11. On dispense, set the dispense height from bottom to 5mm.\
    ![](<../.gitbook/assets/image (48).png>)\

12. Click \[OK].\

13. On the next step shown below, select the aspiration sequence as the controlling sequence.
14. Even if both sequences have the same length initially, it is reasonable to choose the aspiration sequence as the controlling one. Remember that on loading this sequence, the sequence may be reduced to less than 96 positions. Then, only the current number of wells is transferred to the target plate.\
    \
    ![](<../.gitbook/assets/image (49).png>)\

15. In the Aspirate details, set the reloading of the aspirate sequence to “No”.
16. Accept the defaults for the settings under \[Advanced…] and for the \[Error settings…].
17. Click \[Finish] to close the “Smart Step” Dialog.

## Unloading the Deck

1. Finally, drag the “Unload” Smart Step to the line below the pipette step:\
   ![](<../.gitbook/assets/image (50).png>)\

2. Click \[Add all sequences] to add all sequences to the unload step and click \[OK].\
   ![](<../.gitbook/assets/image (51).png>)\

3. Setting the Audit Trail (Always or Validation Only) will allow the possibility to enter change description.
4. Click “File -> Save” in the Method Editor to store the method.\
   ![](<../.gitbook/assets/image (52).png>)\

5. Enter the change description and click \[OK].

\
