# Method to Copy from Tubes to Plates using Smart Steps

This method copies tubes. It aspirates liquid from tubes in a carrier and dispenses them into wells of a Microplate. The maximum number of tubes to be processed is 96, corresponding to a maximum of four 24-tube carriers (1T).

1.  First the appropriate Deck Layout must be created and saved. In this case, it will be “TubesToPlatePipette.lay”. The Deck Layout for this method is shown in the following picture:\


    <figure><img src="../.gitbook/assets/image (62) (1).png" alt=""><figcaption></figcaption></figure>

***

## Creating the Deck Layout:

2. Start the Method Editor by clicking on the “Hamilton Method Editor” Shortcut on the desktop.
3. Select “File -> New -> Method” to create a new method. A window will open to be able to save the new method.
4. Enter the filename “TubesToPlatePipette.med” and click \[Save]. A new method window and system deck window are opened in the Method Editor. To activate, click the system deck window.
5.  Make sure the Stamp Tool “1000μl Channels” is selected, as shown below.\


    <figure><img src="../.gitbook/assets/image (63) (1).png" alt=""><figcaption></figcaption></figure>
6. Click on the “Labware” Tab.
7. In the list above the tabs, expand the “ML STAR Carriers” by clicking the “+” right next to the entry. Do the same to the “Sample carriers”. Select the “24 positions” Entry. A list of 24- position carriers is displayed.
8.  Select the carrier “SMP\_CAR\_24\_15x95\_A00” (rack holding 24 tubes with a 15mm diameter and a height of 75mm). An image of the selected carrier will then be shown in the right-hand box.\


    <figure><img src="../.gitbook/assets/image (64) (1).png" alt=""><figcaption></figcaption></figure>
9. “Drag and Drop” the carrier image onto the deck. Add the other three tube carriers onto the deck (adjacent to the first carrier).
10. Following the steps above, add a plate carrier from the “ML STAR Carriers  Plate Carriers” list.
11. Select “PLT\_CAR\_L5MD\_A00” or use the \[Browse] Button to search for “PLT\_CAR\_L5MD\_A00.tml” in the “ML\_STAR” Labware subdirectory.
12. Same as the previous steps, add a target plate from the “Plates  Nunc” group.
13. Select “Nunc 96 Fl Lb (low border)” and “Drag and Drop” the plate onto the deck.
14. Change the LabwareID of the plate to “TargetPlate”
15. Following the same steps above, add a tip carrier with 300μl tips (without filter).
16. Click “ML STAR Carriers  Carriers 96” and “Drag and Drop” the TIP\_CAR480\_BC\_ST\_A00 onto the deck.
17. Select “File  Save” to save the Deck Layout.
18. Click the “Sequences” Tab to start editing the sequences.
19. At this point, the sequence window should look like the image presented below.\


    <figure><img src="../.gitbook/assets/image (65) (1).png" alt="" width="286"><figcaption></figcaption></figure>
20. Zoom in using the zoom in/out toolbar or the “View” Menu:\


    <figure><img src="../.gitbook/assets/image (66) (1).png" alt="" width="214"><figcaption></figcaption></figure>
21. Rubber band all four tube carriers by performing a left click (do not release) followed by moving over all of the sample carriers. The 96 selected tubes of the four carriers are then highlighted.
22. Click the \[Advanced…] Button to see all the selected positions in a table. The table (presented below) shows the positions of the sequences holding all tubes.\


    <figure><img src="../.gitbook/assets/image (67) (1).png" alt="" width="317"><figcaption></figcaption></figure>
23. As long as no sorting option is selected, the sequence is sorted as follows: “SMP\_CAR\_24\_15x95\_A00\_0001”: Position 1 to 24\
    “SMP\_CAR\_24\_15x95\_A00\_0002”: Position 1 to 24\
    “SMP\_CAR\_24\_15x95\_A00\_0003”: Position 1 to 24\
    “SMP\_CAR\_24\_15x95\_A00\_0004”: Position 1 to 24
24. Click the \[OK] Button and give a name to the sequence.
25. Save the new sequence by clicking \[OK].\


    <figure><img src="../.gitbook/assets/image (68) (1).png" alt="" width="278"><figcaption></figcaption></figure>
26. Click the \[Clear selected] Button in the “Sequences” Tab.
27. Select “File  Save” to save the Deck Layout. This is the end of the Deck Layout and sequences creation.

\


## Creating the Method

1.  Open the Steps View of the Method Editor. Add all the steps by “Dragging and Dropping” icons from the toolbox into the method window. The resulting method should appear as presented below.\


    <figure><img src="../.gitbook/assets/image (69) (1).png" alt="" width="541"><figcaption></figcaption></figure>
2. Add the Smart Step “Load” by “Dragging and Dropping” it from the toolbar to the method window. The “Load” Dialog appears:
3. Click on the drop-down found in the “Sequence” Field and select the sequence “ML\_STAR.SampleCarrier1to4”.
4. Click \[Show details] in order to check the column “Reducible”.
5. Following the previous steps, add the “ML\_STAR.MlStar300ulStandardVolumeTips” and “ML\_STAR.TargetPlate” Sequences.
6.  To do so, use the \[Add] Button from the “Load” Dialog. Finish with \[OK].\


    <table data-header-hidden><thead><tr><th width="98"></th><th></th></tr></thead><tbody><tr><td><img src="../.gitbook/assets/image (10) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" data-size="original"></td><td><p>NOTE</p><p><em>Be reminded that the sequences to be loaded can be selected through the graphical Deck Layout View and by using the “Drag and Drop” technique on the list fields in the “Load” Dialog (with Ctrl + left mouse “Drag and Drop”). The two windows (Deck Layout View and “Load” Dialog) are interactive: when a sequence in the “Load” Dialog is clicked, this sequence flashes with a specific color in the Deck Layout View.</em></p></td></tr></tbody></table>

    \

7.  Drag the Smart Step “1000μl Channel Pipette – Simple (1-1)” to the next line in the method:\


    <figure><img src="../.gitbook/assets/image (70) (1).png" alt=""><figcaption></figcaption></figure>
8.  In the “Smart Step” Wizard screens, select the following:\


    | Step 1: | <ul><li>Aspiration sequence: “ML_STAR.SampleCarrier1to4”</li><li>Dispense sequence: “ML_STAR.TargetPlate”</li></ul>                                                                                                                                                                                                    |
    | ------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
    | Step 2: | - - Volume = 50μl, no additional residual volume                                                                                                                                                                                                                                                                       |
    | Step 3: | <ul><li>Tip sequence: “ML_STAR.MlStar300ulStandardVolumeTips”</li><li>Tip handling: “After each dispense”</li></ul>                                                                                                                                                                                                    |
    | Step 4: | <ul><li>Liquid Class: Water “StandardVolume_DispenseJet”</li><li>LLD on aspiration: settings are capacitive, sensitivity low, submerge depth 2mm</li><li>LLD on dispense: fixed height 2mm from bottom</li></ul>                                                                                                       |
    | Step 5: | <ul><li>Controlling sequence: “Aspiration sequence”</li><li>Aspiration details: no reload</li><li>Dispense details: reload may be selected. This is of no relevance here, since the aspiration sequence is controlling and as long as, or even shorter (by reduction on run time) than the dispense sequence</li></ul> |
9. Click \[Finish] to continue.
10. Drag the “Unload” Smart Step into the next line. Click on the list to add the three sequences into the list of sequences to unload. Finally, click \[OK] to add the “Unload” Step into the method.\


    <figure><img src="../.gitbook/assets/image (71) (1).png" alt="" width="320"><figcaption></figcaption></figure>

## What happens when running this Method?

11. Within the loading step, the sample sequence was chosen to be reducible. This means that, at run time, the following dialog is shown, enabling reduction of the number of samples (from any position). The user may reduce the number of samples down to 24. The altered sequence is immediately shown in the Deck View. The method processes 24 tubes (in this case, from the first carrier) to the plate and then stops.\


    <figure><img src="../.gitbook/assets/image (72) (1).png" alt=""><figcaption></figcaption></figure>

    <figure><img src="../.gitbook/assets/image (75).png" alt=""><figcaption></figcaption></figure>
12. It is also possible to deselect particular tubes from the sequence by clicking on the wells or by using the rubber band. These positions will then turn to grey. A \[Reset] Button is available to restore the original sequence.

\
