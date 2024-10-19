# Serial Dilution with CO-RE 384 STP Probe Head

This section describes how to program a column wise serial dilution using the CO-RE 384 STP. The samples are in column 1 of the plate. The 384 Head pipettes diluent from the diluent container and transfers the mix to column 2. This is repeated until column 24, so there is a decreasing concentration of sample in every column.

Close all open windows and create a method called “Demo384SerialDilution.med”.



## Creating the Deck Layout

1. From the “Sequence” Tab, select the “Head 384 Column” Stamp Tool.\
   ![](<../.gitbook/assets/image (109).png>)
2. Activate the “Labware” Tab and add the “Core384SlideWaste” onto the deck.
3. Add a “TIP384\_CAR\_1920\_50ul” Carrier to the deck.
4. Add a “TIP\_CAR\_480\_A00” to the deck.
5. On the empty tip carrier, place a “TipSupport\_50ul\_384\_STP\_Head” in position 2.
6. Add a “PLT\_CAR\_L5AC\_A00” Carrier to the deck.
7. On the plate carrier, add a “Nun\_300ml\_384C\_Rgt\_L.rck” in position 3. With a right mouse click, enter the “Properties…” and change the “LabwareID” to “Diluent”.
8. On the plate carrier, add a “Nun\_384\_Sq.rck” in position 2. Change xathe “LabwareID” to “Target”.
9. The Deck Layout should look as shown below.\
   ![](<../.gitbook/assets/image (110).png>)
10. The final method should look like this:\
    ![](<../.gitbook/assets/image (111).png>)\
    \
    Step 1 is the initialization of the instrument.\
    \
    Steps 2 and 3: bring the tips from the tip rack to the tip support for column wise tip pick up. Steps 4 to 7: pipette the diluent over the full plate except column 1 (where the sample is). Steps 8 to 11: Aspirate from the previous column and mix with the following column.

## Creating the Sequences

Only one additional sequence is used in this method. Make sure the stamp tool is still set to “Head 384 Column”. Create a sequence over the target plate WITHOUT selecting column one. Name it “TargetPlate\_Diluent”.\


<figure><img src="../.gitbook/assets/image (112).png" alt="" width="436"><figcaption></figcaption></figure>



## Creating the Method

1. First, insert an “Initialize” Step, then use the “CO-RE 384 Head Tip Pick Up (Single Step)” to pick up the tips from the tip rack.\
   \
   ![](<../.gitbook/assets/image (113).png>)\

2. Move the tips to the TipSupport using the “CO-RE 384 Head Tip Pick Eject (Single Step)”. Set the input field to “(0) OFF” because the tips do not go to the default waste. For “Destination”, select the tip support sequence.\
   ![](<../.gitbook/assets/image (114).png>)
3. The next step is a “Loop” Step to make sure the distribution of diluent continues over the full “TargetPlate\_Diluent” Sequence (all columns except column 1). Use the option “Iterate over sequence and adjust sequence” and select “ML\_STAR.TargetPlate\_Diluent”.\
   ![](<../.gitbook/assets/image (115).png>)
4. The loop is followed by the aspiration of diluent (with only one column of tips). Use the “CO-RE 384 Head Aspirate” Step and use the following settings:\
   ![](<../.gitbook/assets/image (116).png>)\
   \
   Tip Mode: (0) All the column wise setting is made in the “Customize” later\
   Aspiration sequence: ML\_STAR.Diluent\
   Auto increment: Not ticked\
   Volume: 40ul\
   TipType: 50µl tip for 384
5. The liquid class is selected automatically after specifying the liquid “Water”.
6. The tip pickup sequence should be “ML\_STAR.CORE384\_TipSupport\_50ul\_L\_0001”.
7. Now, the column wise tip pickup must be specified in the “Customize” Tab, found in the “Channel Settings” Section.
8. Make sure the “Reduced pattern mode” is set to “(4) Column(s)”. The column 24 is then automatically activated to be used for the tip pick up.\
   ![](<../.gitbook/assets/image (117).png>)
9.  Other possible selections for “Reduced pattern mode” are: \
    \
    “(0) All” to pick up all tips\
    “(1) One Channel” to pick up one tip in the corner of the head\
    “(2) Quarter” to have ¼ of the tips picked up. Quarter selection has different rears as shown below.\
    \
    ![](<../.gitbook/assets/image (118).png>)\
    \
    “(3) Row(s)” for row-wise tip pickup and pipetting\
    \


    <table data-header-hidden><thead><tr><th width="98"></th><th></th></tr></thead><tbody><tr><td><img src="../.gitbook/assets/image (9) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" data-size="original"></td><td><p>ATTENTION</p><p><em>Ensure that all methods are tested. It is recommended to run a simulation first, fThis is the pattern of the CO-RE 384 Probe Head and NOT the pipetting pattern on the plate.</em></p></td></tr></tbody></table>

    \
    \

10. To pick up two columns of tips, activate column 23 by clicking on the column number 23 as well. Through this, several columns can be activated and will be picked up.\
    \


    <table data-header-hidden><thead><tr><th width="98"></th><th></th></tr></thead><tbody><tr><td><img src="../.gitbook/assets/image (10) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" data-size="original"></td><td><p>NOTE</p><p><em>It is not possible to have gaps (empty lines) in the pattern. To create such a pattern, use a second tip support and move the tips to the according columns, rows, quarters or single positions.</em></p></td></tr></tbody></table>


11. If a reduced pattern mode other than “(0) All” is used, please read about the risks and limitations in the Help of the step  CO-RE 384 Head Pattern Mode Limitations.
12. It is also possible to use a variable for the columns or rows to be used. Example for column variable: “000000000000000000000011”, where every character represents a column.
13. “0” (zero) stands for not used column, “1” (one) for used column. In the example, the columns 23 and 24 will be used for tip pick up. For rows, only 16 values must be passed.
14. After the aspiration, insert a “CO-RE 384 Head Dispense” Step and fill the input fields as follows:\
    \
    ![](<../.gitbook/assets/image (119).png>)\

15. Make sure that the “Auto increment” Box is ticked.
16. The volume should be as big as the aspiration volume, or simply activate the “Dispense remaining volume” Checkbox.

The tip pattern is taken from the aspiration step, so no changes are necessary here.

17. With this step, the distribution of the diluent over the plate is finished. There is a choice whether to throw away the tips or to keep them. Use the ‘Tip handling after dispense’ to apply the settings.
18. Now, a second loop is needed to perform the transfer from column to column. With 24 columns, 23 transfers are needed. Therefore, the second loop can iterate over the fixed number of times.\
    \
    ![](<../.gitbook/assets/image (120).png>)\
    \

19. Inside the second loop, the aspirate of the sample is executed. To do so, use a “CO-RE 384 Head Aspirate” Step with the settings shown below. If the step from line 5 of the method is copied, there is no need to repeat the tip pattern settings in the “Customize” Tab (to use only one column).\
    \
    ![](<../.gitbook/assets/image (121).png>)\

20. It is important that the “Auto increment” Box is ticked. This will ensure that the aspirated liquid is transported to the next column for dispensing.
21. In the lower section, use a fixed pipetting height of 3mm. Keep in mind that this height may differ if other plates are used.\
    \
    ![](<../.gitbook/assets/image (122).png>)\

22. The dispense step may now be programmed. Add (or copy from above) the “CO-RE 384 Head Dispense” using the settings below:\
    \
    ![](<../.gitbook/assets/image (123).png>)\

23. The target plate is used both as aspirate and dispense location to get the serial dilution. Since the “Auto increment” on the Aspirate step was checked, the dispense step always uses the next column and because the next aspiration should happen in the same column, the “Auto increment” Checkbox must be unchecked on the dispense step.
24. Again, set a fixed height for dispensing then switch to the “Customize” Section. The “Minimize z-move after step” can be activated since dispensing is performed on one plate only. This will prevent the head from moving up to traverse height, which is time saving.
25. Activate the mixing function when dispensing the diluent into the sample. Use the “Customize” Tab to enter the “Advanced Dispense” Section.
26. Enter the values for the mixing as follows:
    * Cycles = 4
    * Mix position = 2
    * Volume = 20
27. Close the step by clicking \[OK] twice.

\
