# Method to Copy from Plate to Plate using Single and Easy Steps

The method that will be discussed in this section does exactly the same as the method “OnePlateToPlatePipette” described in Section 12.3 Method to Copy from Plate to Plate using Smart Steps. The only difference is that the method is now written using Easy Steps instead of Smart Steps. Here, no sample reduction is possible.

This method uses the same Deck Layout as the method used with the Smart Steps.

1. Open this system Deck Layout and create the easy step version using the following guide:
2. Create a new method called “OnePlateToPlateEasySteps”.
3. The method can be written easily by “Dragging and Dropping” the icons from the toolbox into the method window. The resulting method looks like this:\
   \
   ![](<../.gitbook/assets/image (53) (1).png>)\

4.  The first step is an initialize step. In the “ML\_STAR” toolbar, drag “Initialize” to the main window. A window will be displayed.\
    \
    ![](<../.gitbook/assets/image (54) (1).png>)\


    <table data-header-hidden><thead><tr><th width="98"></th><th></th></tr></thead><tbody><tr><td><img src="../.gitbook/assets/image (10) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" data-size="original"></td><td><p>NOTE</p><p><em>In using a single step in the beginning of a method, the initialize command has to be added prior to the single step.</em></p><p><em>When using Smart Steps and Easy Steps, the initialization will be executed automatically.</em></p></td></tr></tbody></table>
5. Drag “Load Carrier” into the next line of the method.\
   \
   ![](<../.gitbook/assets/image (55) (1).png>)\

6. This command loads the carriers automatically onto the instrument deck during run time.
7. Specify the name of the carrier to be loaded.
8. Click \[Advanced…] to display the path where the plate barcodes are stored, under the default file name “barcode\_1.txt” (Note that the checkbox “barcode trace” within the configuration editor must be checked to generate the file). The positions on the deck are automatically retrieved from the Deck Layout during run time.\
   \
   ![](<../.gitbook/assets/image (56) (1).png>)\

9. Click \[OK] twice.
10. Repeat the “Load Carrier” Command for the target plate carrier and the source carrier.
11. To copy the whole source plate and not just the first 8 wells to the target plate, the steps “Tip pick-up”, “Aspiration”, “Dispense” and “Tip eject” have to be performed 12 times (96 wells divided by 8 pipetting channels). This can be achieved using a loop command.
12. The loop statement consists of two lines, a “begin loop” and an “end loop” statement. The codes is inserted between these two statements will be looped.
13. Drag the “Loop” Command from the General Steps into the next line of the method window.
14. The “Loop” Dialog window will appear as follows:\
    \
    ![](<../.gitbook/assets/image (57) (1).png>)\

15. A loop can be performed looping:
    * Over a fixed number of iterations
    * An expression (repeat which the statement in the expression is true)
    * A sequence
    * A file (until end-of-file is reached)
16. In this example, a looping over the “SourcePlate” Sequence is done. This means, that the loop will continue until all sequence positions (the 96 wells) of the “SourcePlate” have been used. Only then the loop will stop.
17. Choose the default “after loop” for the “Reset Sequence” Option, to reset the sequence “SourcePlate” to the initial position (1) after the loop is done. If a pipette with the same sequence “SourcePlate” will be performed once more at a later time, the sequence will then start at the first well again.\
    \


    <table data-header-hidden><thead><tr><th width="98"></th><th></th></tr></thead><tbody><tr><td><img src="../.gitbook/assets/image (10) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" data-size="original"></td><td><p>NOTE</p><p><em>Keep in mind that in looping over a sequence, the sequence has to be incremented within the loop.</em></p></td></tr></tbody></table>

    \

18. Now, drag the “1000μl Channel Aspirate (Easy Step)” to the line below the tip pick-up step. A dialog box, as shown below will appear. Specify the values indicated below the dialog box.

    * Aspirate from Sequence: “ML\_STAR.SourcePlate” (aspirate from source plate)
    * Volume: 100μlTip Type: 300ul Standard Volume Tip
    * Dispense Mode: Jet Empty Tip
    * Liquid Class: StandardVolumePlasmaDispenseJet\_Empty (For questions about these parameters, refer to Section 13.5 Pipetting)
    * Submerge Depth: 2mm\


    <figure><img src="../.gitbook/assets/image (58) (1).png" alt="" width="211"><figcaption></figcaption></figure>
19. After completing all the fields, click \[OK].
20. Drag the “1000μl Channel Dispense (Easy Step)” to the position below the aspirate command. A dialog box, as shown below will appear. Specify the values indicated below the dialog box.\
    \
    ![](<../.gitbook/assets/image (59) (1).png>)\
    \

    * Dispense to Sequence: “ML\_STAR.TargetPlate” (target plate)
    * Sequence Counting: “Auto increment”
    * Volume: 100μl
    * Dispense Position: 5mm, “Fix height from container bottom” (which corresponds to a height of 2mm above the container bottom for dispensing)
21. After completing all the fields, click \[OK]. The loop is now complete.\
    \


    <table data-header-hidden><thead><tr><th width="98"></th><th></th></tr></thead><tbody><tr><td><img src="../.gitbook/assets/image (10) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" data-size="original"></td><td><p>NOTE</p><p><em>Keep in mind that in looping over a sequence, the sequence has to be incremented within the loop.</em></p></td></tr></tbody></table>

    \

22. Finally, the carrier must be unloaded outside the loop.
23. To unload the carriers, drag the “Unload” Command (with the carrier name as a parameter) into the method and drop it after the end loop.
24. The “Unload” Dialog appears:\
    \
    ![](<../.gitbook/assets/image (61) (1).png>)\

25. Click \[OK].
26. Insert “Unload” Commands for all three carriers.
27. The method is now complete. Save the method and exit by selecting “File  Exit” in the Method Editor.

