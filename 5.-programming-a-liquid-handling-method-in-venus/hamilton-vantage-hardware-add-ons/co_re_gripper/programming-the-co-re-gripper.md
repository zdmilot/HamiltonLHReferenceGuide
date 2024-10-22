# Programming the CO-RE Gripper

The following example demonstrates the use of the CO-RE gripper robotic plate handler with ML STAR. A set of plates are taken from the input carrier and brought to the barcode reading position of a third party barcode reader. Then, the plate is placed on another carrier for further actions (that are not part of this example).&#x20;

Reading of the plate’s barcode is done by a third party barcode reader. In the example, a comment to simulate this is used. In real life, this could be a Metrologic Orbit reader that is controlled through the HSLBarcodereader library. Please activate this library to read the barcode when working on a real system.

The positions where to get the plates and where to put it after reading are not specified directly, but in an array. An array can be imaged as a table with two columns. In column one, the index is stored. This value is not changeable by the user. It always starts at one. The second column of the array can be filled by the user. Either a variable of type integer, float, and string can be stored or a sequence name can be stored in this cell.

<figure><img src="../../../.gitbook/assets/image (119) (1) (1) (1).png" alt="" width="375"><figcaption></figcaption></figure>

Far ahead in the method, these arrays can be read out and the values from e.g. the second column can be used as pipetting volumes, number of loops etc. (in case of an array of variables) or these values specify where to aspirate, where to get a plate etc. (in case of an array of sequences).

<table data-header-hidden><thead><tr><th width="125"></th><th></th></tr></thead><tbody><tr><td><img src="../../../.gitbook/assets/image (10) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" data-size="original"></td><td><p>NOTE</p><p>The CO-RE gripper works on the base of sequences. Plates are moved from one sequence to another. The sequences remain fixed on the deck, but the plates change sequences.</p></td></tr><tr><td><img src="../../../.gitbook/assets/image (10) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" data-size="original"></td><td><p>NOTE</p><p>Target and source plate positions must be of the same labware type.</p></td></tr></tbody></table>

Creating the Deck Layout&#x20;

To work through this example, create the Deck Layout by following these steps:&#x20;

1. Click the “Labware“ Tab in the Method Editor.&#x20;
2. Add two plate carriers “PLT\_CAR\_L5MD\_A00” from the ML STAR carriers under the Plate carrier folder onto the deck.&#x20;
3. Add three plates on each carrier. The plate type could be “Nun\_96\_Fl\_Lb (low border)”. Name these plates ‘Input1’ to ‘Input3’ on one carrier and ‘Output1’ to ‘Output3’ on the other carrier.&#x20;
4. Add a plate “Nun\_96\_Fl\_Lb (low border)” directly on the deck. The coordinates should be x = 1100 / y = 150 / z = 150. This will be our position to read the plate’s barcode. Name it "ReadPosition". External in this case means that is not built in the ML STAR, but of course it must be located on the track area so the CO-RE gripper is able to reach the position.
5. Add the COREGripTool\_AtWaste\_1000μl to the waste (it will snap).&#x20;

<figure><img src="../../../.gitbook/assets/image (120) (1) (1).png" alt=""><figcaption></figcaption></figure>

\


### **Creating the Sequences**

In this example, only the default generated sequences were used.





### Command description

The following tables give a brief overview of the available ML STAR –specific CO-RE gripper commands.

{% tabs %}
{% tab title="Easy Steps" %}
<table><thead><tr><th>Command</th><th width="183">Icon</th><th>Action Performed</th></tr></thead><tbody><tr><td>1000µl Channel CO-RE Grip Transport</td><td><p><br><img src="../../../.gitbook/assets/image (108) (1) (1) (1).png" alt=""></p><p></p></td><td>Transports a plate from start sequence to end sequence using the 1000μl-pipetting hannels and the 1000μl CO-RE Grip tool.</td></tr><tr><td>5ml Channel CO-RE Grip Transport</td><td><p><br><img src="../../../.gitbook/assets/image (109) (1) (1) (1).png" alt=""></p><p></p></td><td>Transports a plate from start sequence to end sequence using the 5ml-pipetting channels and the 5ml CO-RE Grip tool.</td></tr></tbody></table>
{% endtab %}

{% tab title="Single Steps" %}
| Command                                | Icon                                                                                         | Action Performed                                                                                         |
| -------------------------------------- | -------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- |
| 1000µl Channel CO-RE Grip Get Plate    | ![](<../../../.gitbook/assets/image (114) (1) (1) (1).png>)                                  | Picks up a plate from the defined position.                                                              |
| 1000µl Channel CO-RE Grip Place Plate  | <img src="../../../.gitbook/assets/image (111) (1) (1) (1).png" alt="" data-size="original"> | Sets a plate down in a defined position.                                                                 |
| 1000µl Channel CO-RE Grip Move Plate   | ![](<../../../.gitbook/assets/image (112) (1) (1) (1).png>)                                  | Transfers a plate to another sequence.                                                                   |
| 1000µl Channel CO-RE Grip Read Barcode | <p><br><img src="../../../.gitbook/assets/image (113) (1) (1) (1).png" alt=""></p><p></p>    | Barcode of the plate held is read (after unloading the carrier that the CO-RE gripper will be moved to). |
| 5ml Channel CO-RE Grip Get Plate       | <img src="../../../.gitbook/assets/image (115) (1) (1) (1).png" alt="" data-size="original"> | Picks up a plate from the defined position.                                                              |
| 5ml Channel CO-RE Grip Place Plate     | <img src="../../../.gitbook/assets/image (116) (1) (1) (1).png" alt="" data-size="original"> | Sets a plate down in a defined position.                                                                 |
| 5ml Channel CO-RE Grip Move Plate      | <img src="../../../.gitbook/assets/image (117) (1) (1) (1).png" alt="" data-size="original"> | Transfers a plate to another sequence.                                                                   |
| 5ml Channel CO-RE Grip Read Barcode    | <img src="../../../.gitbook/assets/image (118) (1) (1) (1).png" alt="" data-size="original"> | Barcode of the plate held is read (after unloading the carrier that the CO-RE gripper will be moved to). |
{% endtab %}
{% endtabs %}





### **Creating the Method**

The resulting method should look like shown below:

![](<../../../.gitbook/assets/image (121) (1) (1).png>)\


1. The method will start with an initialization step. This step is always needed if a method does not start with a Smart Step or an Easy Step.
2. Steps 3 and 4 are used to create two empty arrays, one for the source- and one for the target sequences. The array: Declare / Set Size step shows that an array of sequences is generated and shall be empty.
3.  Empty array means that the number of entries the array will have is unknown. However, if the number of entries is already known, specify the array with the corresponding size. To do this, use the \[New size] field.

    <figure><img src="../../../.gitbook/assets/image (122) (1).png" alt=""><figcaption></figcaption></figure>

    \

4.  The next sets of steps (6-8 and 10-12) are used for filling both the array of GetPlatePositions and the array of PlacePlatePositions. Using the option “Add to the end of the array” will store the sequences in order of adding:

    <figure><img src="../../../.gitbook/assets/image (123) (1).png" alt=""><figcaption></figcaption></figure>

    \

5. Steps 6 to 8 and 11 to 12 are writing sequences into the newly declared arrays of sequences.
6.  Step 13 is used to find out how many entries are stored in an array. It will store the number of array entries into the variable NumOfEntries. This is especially used if the number of entries is unknown (e.g. if reading values or sequences from a file).\
    ![](<../../../.gitbook/assets/image (124) (1).png>)

    \



7.  The number of entries can be used as the number of loop runs:

    <figure><img src="../../../.gitbook/assets/image (125) (1).png" alt=""><figcaption></figcaption></figure>

    \

8. The GetPlate step in line 15 does not have a sequence included. The sequence is read out of the array ‘GetPlatePositions’ and the position where to read is given by the LoopCounter1 variable.
9.  Click the ![](<../../../.gitbook/assets/image (127) (1).png>) sign to set the array index seen below.

    ![](<../../../.gitbook/assets/image (128) (1).png>)\

10. In the first loop round, the GetPlate step is using the sequence stored in the array under position 1 (specified by the loopCounter1).
11. The MovePlate in step 16 will move the  to the barcode reader position. In the trace file, the barcode of the plate can be seen.
12. Step 17 will place the plate on a specific position. This position is defined by a sequence and stored in the second array. All of these must be done similar to the GetPlate step in line 16: simply define the array and the index then the sequence will be read out of the array.\
    ![](<../../../.gitbook/assets/image (129) (1).png>)

\


## CO-RE Gripper Transport: Avoiding Z-Step Loss

Keep in mind that the CO-RE gripper for the 5ml-pipetting channel needs more space than the 1000μl-pipetting channel CO-RE gripper tools. This can lead to Z-Step Loss when a Deck Layout is not properly set up (see below).\


<figure><img src="../../../.gitbook/assets/image (130) (1).png" alt=""><figcaption></figcaption></figure>

Side view of the instrument (turned towards the waste)



### CO-RE Gripper Transport: Avoiding Y-Step Loss

The 5ml-pipetting channels are less flexible than the 1000μl-pipetting channels due to their massive construction. Therefore, it makes sense to try low grip forces for labware transports.

In the event of heavy labware (e.g. filled Deep Well Plates), switching to higher grip forces can be done.

### CO-RE Gripper Transport: Adding the Suitable Tool

The Deck Layout Editor shows several tools for the CO-RE Gripper. The next statement is the correct use of the labware.

COREGripTool OnWaste 1000μl uses a holder for the paddles mounted on top of the waste block. This is a holder that is capable to hold both 1000μl-pipetting channel and 5ml-pipetting channel paddles.

Using this labware will create the default sequence for 1000μl-pipetting channel paddles.

\


<figure><img src="../../../.gitbook/assets/image (131) (1).png" alt=""><figcaption></figcaption></figure>

\


COREGripTool OnWaste 5ml uses a holder for the paddles mounted on top of the waste block. This is a holder that is capable to hold both 1000μl-pipetting channel and 5ml-pipetting channel paddles. Using this labware will create the default sequence for 5ml-pipetting channel paddles.

\


<figure><img src="../../../.gitbook/assets/image (132) (1).png" alt=""><figcaption></figcaption></figure>

\


COREGripTool AtWaste 1000μl uses a holder for the paddles mounted on the side of the waste block (only available for 1000μl-pipetting channels).

\


<figure><img src="../../../.gitbook/assets/image (133) (1).png" alt=""><figcaption></figcaption></figure>

\


CORE Grip Tool (landscape) uses a holder for the paddles on a landscape plate position (only available for 1000μl-pipetting channels).

\
![](<../../../.gitbook/assets/image (134) (1).png>)

CORE Grip Tool (portrait) uses a holder for the paddles on a portrait plate position (only available for 1000μl-pipetting channels).

\


<figure><img src="../../../.gitbook/assets/image (135) (1).png" alt=""><figcaption></figcaption></figure>

\


### Use Various Channels for CO-RE Gripper Transports

\


By default, pipetting channels 7 and 8 are used to execute CO-RE gripper transports. Having a method with many transport steps, these two pipetting channels are stressed more than the others. The input field “Used Front Channel” was designed to use different pipetting channels for the transports, which shares the applied load to all pipetting channels of an instrument.

The following program lines make sure that first, pipetting channels 1+2 are used. In the next “Get Plate” Command, pipetting channels 3+4 will be used (and so on). In this manner, the pickup commands are spread over all the pipetting channels and the mechanical system of all pipetting channels are strained to the same degree.

\


<figure><img src="../../../.gitbook/assets/image (136) (1).png" alt=""><figcaption></figcaption></figure>

\


1. Create a sub-method called “CalculateFrontChannel”
2. Make an assignment with calculation: “FrontChannel = FrontChannel + 2”
3. **Make an if statement: “If FrontChannel is greater than 8\*  FrontChannel = 2”**
4. Having a different number of pipetting channels on the instrument, enter e.g. 4, 12, 16
5. Now, make sure that the “FrontChannel” Variable is global and valid in all sub-methods:
6. Click on “Method  Export Local Variables” and select _FrontChannel_, then click \[OK].
7.  The sub-method should look like this:

    \


    <figure><img src="../../../.gitbook/assets/image (137) (1).png" alt=""><figcaption></figcaption></figure>

    \

8.  All that remains to be done is to set a start value in the main method:

    \


    ![](<../../../.gitbook/assets/image (138) (1).png>)\

9.  Insert the CalculateFrontChannel sub method in the method right before the GetPlate, as seen below.

    \


    <figure><img src="../../../.gitbook/assets/image (139) (1).png" alt=""><figcaption></figcaption></figure>

    \

10. In the CO-RE gripper “Get Plate” Command, set the “FrontChannel” Variable.

<figure><img src="../../../.gitbook/assets/image (140) (1).png" alt=""><figcaption></figcaption></figure>



## Read Plate Barcode using the CO-RE Gripper (only available with Autoload)

If the command “CO-RE gripper Read Barcode” is used, like this:

![](<../../../.gitbook/assets/image (141) (1).png>)\


Six tracks on the left side of the barcode reading position (inclusive) have to be empty, otherwise the plate will crash into the carriers on these positions. For example, if the track number of the barcode reader (Autoload) is set to 8, track numbers 3-8 have to be empty. The following sketch shows the situation:

<figure><img src="../../../.gitbook/assets/image (143) (1).png" alt=""><figcaption></figcaption></figure>

\


<table data-header-hidden><thead><tr><th width="125"></th><th></th></tr></thead><tbody><tr><td><img src="../../../.gitbook/assets/image (10) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" data-size="original"></td><td><p>NOTE</p><p>It is recommended to use the pipetting channels closest to the front for transporting plates to the barcode reader.</p></td></tr></tbody></table>

