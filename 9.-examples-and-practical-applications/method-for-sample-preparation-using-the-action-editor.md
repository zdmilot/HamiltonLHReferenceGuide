# Method for Sample Preparation using the Action Editor

The action editor is a helpful tool for graphical method creation. It should be activated if the scheduling software is NOT installed. If scheduling software is installed, the same icon will start the activity editor.

This demo will:

* Aspirate buffer from a reagent trough
* Aliquot this over a Microplate, starting at A1
* Aspirate samples from three tube racks
* Dispense them into the same target plate and mix

The transferred volume will be 50μl of buffer and 100μl of the sample. The method is named “MixSampleAndBuffer”. The method uses new CO-RE tips for every well. Start with an empty target plate.

First, create a new method. This will also add a Deck Layout with the same name (“MixSampleAndBuffer”.lay). The Deck Layout for this method is shown in the picture below.

<figure><img src="../.gitbook/assets/image (26) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

***



## Creating the Deck Layout:

1. Start the Method Editor by clicking on the “Hamilton Method Editor” Shortcut on the desktop.
2. Select “File -> New -> Method” to create a new method. A window will open to be able to save the new method.
3. Enter the filename (MixSampleAndBuffer) and click \[Save]. A new method window and system deck window are opened in the Method Editor. To activate, click on the system deck window.
4. Click the “ML\_STAR” Tab in the lower left corner.
5. Make sure the “1000μl Channels” Stamp Tool is selected to define the sorting of the default sequences when adding labware.
6.  Click the on the “Labware” Tab.\
    \


    <figure><img src="../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>
7.  In the tree list right above the tabs, expand “ML STAR Carriers -> Plate Carriers” and select “PLT\_CAR\_L5MD\_A00”. This is a carrier for microplates.\
    \
    \
    An image of the selected carrier is shown in the right-hand box.

    <figure><img src="../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>
8. “Drag and Drop” the carrier from the box onto the deck.
9. Repeat the steps above to add a tip carrier with 300μl Tips (without filter). Click “ML STAR Carriers -> Tip Carriers 96” and “Drag and Drop” the TIP\_CAR480\_BC\_ST\_A00 onto the deck.
10. Following the previous steps, add three sample carriers to the deck. Click “ML STAR Carriers -> Sample Carriers -> 32 positions -> SMP\_CAR\_32\_12x95\_A00” and drag it onto the deck. Repeat this step until there are 3 sample carriers on the deck.
11. Same as the steps above, add a reagent carrier preloaded with 3 reagent troughs to the deck. Click “ML STAR Carriers -> Reagent Carriers -> RGT\_CAR\_3R\_A01” and drag it onto the deck.
12. Place the target plate on the plate carrier. Click “Plates ->  96 position plates -> Nunc\_96\_Fl\_Lb (low border)” and drag the plate to the carrier position 5.
13. Right click on the plate and select “Properties” in the Context Menu.
14. Change the LabwareID of the plate to “TargetPlate”.\


    <figure><img src="../.gitbook/assets/image (3) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>
15. Delete two of the three reagent troughs (they are not needed). Select a trough and press the Delete key on the keyboard or right-click the trough and select “Delete” from the Context Menu.
16. Click the “Sequences” Tab to start editing the sequences. The upper part of the window changes to sequence editing.
17. Click the \[Clear selected] Button to make sure that nothing is selected.
18. Click and hold the left mouse button at one corner of the sample carriers and move over all three sample carriers.\


    <figure><img src="../.gitbook/assets/image (4) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>
19. The positions appear in dark brown.\


    <figure><img src="../.gitbook/assets/image (5) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>
20. Click the \[Save as] Button and enter the sequences name as shown in the image.
21. Save by clicking \[OK].

## Creating the Method

1. Open the action editor by clicking on the icon in the toolbar:&#x20;
2.  The action editor window should appear as presented below.\


    <figure><img src="../.gitbook/assets/image (6) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>
3. Click the “Load” action and drag it in the right section of the window. The action dialog appears as follows:
4. Leave the default values for the “Display name”, “Color”, “Duration” and “Symbol” selection. In the “Insert Step” Field, the loading step can be included.
5. This dialog allows the creation of a method which will run on an instrument. Actions without steps can only be used for calculations.
6.  Select the “Load” Smart Step from the “Insert Step” List and Click \[OK].\
    \


    <table data-header-hidden><thead><tr><th width="98"></th><th></th></tr></thead><tbody><tr><td><img src="../.gitbook/assets/image (10) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" data-size="original"></td><td><p>NOTE</p><p><em>Inserting steps to an action offers the possibility to create running methods for instruments.</em></p><p><em>Inserting “No Step” to an action is used to create a ‘dummy’ method for throughput calculations.</em></p><p><em>Steps can also be inserted later.</em></p></td></tr></tbody></table>



    <figure><img src="../.gitbook/assets/image (7) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>
7.  The action dialog will be closed and the “Load” Smart Step Dialog will open as follows:\


    <figure><img src="../.gitbook/assets/image (8) (1) (1) (1) (1) (1) (1).png" alt="" width="472"><figcaption></figcaption></figure>
8. Add the sequences to load by clicking the \[Add] Button and selecting the required sequences.
9. Click \[OK] to close the “Load” Dialog
10. The “Load” Icon is now visible in the window as shown below.\


    <figure><img src="../.gitbook/assets/image (9) (1) (1) (1) (1) (1) (1).png" alt="" width="375"><figcaption></figcaption></figure>
11. Drag the action “Pipette 1000μl Channels” to the right window. The action data dialog will open.
12. Leave the default values for the “Display name”, “Color”, “Duration” and “Symbol” selection. To execute the pipetting, select the “1000μl Channel Pipette – Aliquot” for the liquid transfer from the buffer trough onto the target plate.\


    <figure><img src="../.gitbook/assets/image (10) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>
13. After clicking \[OK], the “Smart Step Pipette” Dialog opens.\


    <figure><img src="../.gitbook/assets/image (11) (1) (1) (1) (1) (1).png" alt="" width="239"><figcaption></figcaption></figure>
14. Fill out the sequences as shown above (by using the sequence list) and click \[Next >] to continue.
15. In the next step, specify the pipetting, pre- and post-aliquot volumes and click \[Next >].\


    <figure><img src="../.gitbook/assets/image (12) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>
16. Here, a tip is pre-selected. Since only one kind of tip is on the deck, this tip type will be selected automatically. Make sure the “Use one set for the full pipette” Radio Button is activated.\


    <figure><img src="../.gitbook/assets/image (13) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>
17. Click \[Next >] to continue.
18. Select the liquid class that shall be used for pipetting.
19. Click \[Next >] to continue.\
    \
    In this step of the “1000μl Channel Pipette – Aliquot” Dialog, make sure that the next pipette step will find available sequence positions on the target plate. Otherwise, the whole TargetPlate sequence is used up by the aliquot and no more positions are available for the samples.\

20. To do so, select the \[Advanced] Button in the “Dispense details” Section as highlighted below.\


    <figure><img src="../.gitbook/assets/image (14) (1) (1) (1) (1) (1).png" alt="" width="358"><figcaption></figcaption></figure>
21. On the next screen, activate the \[Used within this step] Radio Button. This will set the current position of the target plate back to 1 (which is Well A1), and pipetted the samples into the buffer.\


    <figure><img src="../.gitbook/assets/image (15) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>
22. Click \[OK] to close the “Dispense: Advanced Sequence Settings” Dialog.
23. Click \[Finish] to end the “1000μl Channel Pipette” Wizard.\
    \
    The pipetting from buffer to target plate step is now visible in the window as presented below.\


    <figure><img src="../.gitbook/assets/image (16) (1) (1) (1) (1) (1).png" alt="" width="563"><figcaption></figcaption></figure>

## Pipetting 1:1

Add another “Pipette 1000μl Channels” Action to the right section of the window.

<figure><img src="../.gitbook/assets/image (17) (1) (1) (1) (1) (1).png" alt="" width="317"><figcaption></figcaption></figure>

1. This time, change the display name to “Pipette Samples”, change the color to light blue, set the “Duration” to 300 seconds and insert a “1000μl Channel Pipette – Simple (1-1)” Step.
2. Click \[OK] to continue.
3. The “1000μl Channel Pipette – Simple (1-1)” Dialog will open.
4. Insert the aspirate- and dispense sequences as shown. Click \[Next >] to continue.\
   ![](<../.gitbook/assets/image (18) (1) (1) (1) (1) (1).png>)
5. Set the volume in the next window to 100μl and Click \[Next >] to continue.\
   ![](<../.gitbook/assets/image (20) (1) (1) (1) (1) (1).png>)\

6. Next, make sure that the \[After each dispense] Radio Button is activated.
7. Click \[Next >] to continue.\
   ![](<../.gitbook/assets/image (21) (1) (1) (1) (1) (1).png>)
8. Next, specify the dispense mode “Surface” and the liquid class “Plasma”.\
   ![](<../.gitbook/assets/image (22) (1) (1) (1) (1).png>)
9. Under “Dispense parameters”, click the \[Advanced…] Button and enter the following values found on the next page.\
   ![](<../.gitbook/assets/image (23) (1) (1) (1) (1).png>)
10. Click \[OK] to close this dialog and click \[Next >] to continue.
11. On the last step, activate the radio button to be used for the controlling sequence.\
    \
    ![](<../.gitbook/assets/image (25) (1) (1) (1) (1).png>)
12. Complete by clicking \[Finish].
13. Add the “Unload” Action. Follow the previous steps in adding the action. The final method should look the image below.\
    ![](<../.gitbook/assets/image (26) (1) (1) (1) (1).png>)

\


<table data-header-hidden><thead><tr><th width="98"></th><th></th></tr></thead><tbody><tr><td><img src="../.gitbook/assets/image (10) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" data-size="original"></td><td><p>NOTE</p><p><em>Running a method in simulator mode will consume the specified action</em></p><p><em>duration. Here, the setting will generate a timer of 120 seconds.</em> <br><img src="../.gitbook/assets/image (27) (1).png" alt=""><br><em>This can be switched off in the “Advanced setting of the action”.</em><br><img src="../.gitbook/assets/image (28) (1).png" alt=""><br><em>Uncheck the “Simulate actual time” Box to NOT consume the specified duration.</em></p></td></tr></tbody></table>

\
