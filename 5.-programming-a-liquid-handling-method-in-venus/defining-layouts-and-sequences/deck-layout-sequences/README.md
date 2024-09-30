# Deck Layout Sequences

<figure><img src="../../../.gitbook/assets/image (344).png" alt=""><figcaption></figcaption></figure>

**Deck Sequences list:**

This list shows all sequences of the current instrument deck. Included are default deck sequences generated automatically for new labware, and any user defined deck sequences. These sequences can be created, modified, deleted and renamed by the user.

**System Managed Sequences list:**

These sequences are automatically created and managed by the system deck and cannot be modified, nor deleted, nor renamed. The contained sequence positions can be viewed using the Edit Positions Dialog in read-only mode.

**Using the 'Stamp Tool':**

Usage is described in the section of Stamp Tool Panel.

**Using Deck Sequences:**

All labware objects have got a default sequence, if default sequence generation is enabled (see generation of default deck sequences).

* **Clear Selected**\
  Clear any active sequence selection in the instrument view.
* **Advanced...**\
  Allows detailed sorting and position adjustments. See Edit Positions Dialog.\
  System defined sequences can only be viewed (read-only mode).\
  Double left click a sequence in the lists opens the Edit Positions Dialog too.
* **Save**\
  Save the currently selected sequence.
* **Save As...**\
  Save a new sequence or an existing sequence under a new name.
* **New Sequence**\
  Creates a new empty sequence, a name must be entered.
* **Delete**\
  Delete the currently selected deck sequence (system defined sequences cannot be deleted manually).\
  The key "Del" can be used to delete a selected sequence too.
* **Rename**\
  Renames the currently selected deck sequence (system defined sequences cannot be renamed).\
  The key "F2" or the context menu can be used to rename a selected sequence.

A deck sequence can be dragged & dropped into an input field of an open step dialog. Press and hold the CTRL key while dragging the sequence with the mouse to desired input field. Note: the step must support drag & drop of sequences.

**Play Sequence:**

These buttons will help you visualize a sequence by playing, stopping or single stepping through the sequences definition in the instrument view.

**Validate Sequences:**

see Invalid Deck Positions

## Stamp Tool Panel

<figure><img src="../../../.gitbook/assets/image (345).png" alt=""><figcaption></figcaption></figure>

**Stamp Tool Preview:**

When moving the mouse over the instrument deck, the labware positions at the current location of the mouse pointer are highlighted using the selected Probe Head. A single left mouse click then selects the positions as shown by the Preview.

Note: The _Sequence Panel_ must be active to use the preview.

**Labware Z-Height Order:**

Defines creation order of sequences using positions having different z-heights (Stacks for example).

* _Bottom up_ will be used for (empty) target stacks, allowing to stack plates from the bottom to the top.
* _Top down_ will be used for (full) source stacks, where the plates are picked from top to bottom.

### Edit Positions Dialog

**Sorting:**

Sorting may be performed using a "sort by column" method or a "sort by direction" method.

The sort button will apply the sort selection to all or the currently selected grid positions.

**Apply Stamp Tool:**

The Stamp Tool currently selected on the Sequences Panel is applied to the sequence.

**Delete Selected Positions:**

Pressing this button deletes the selected positions from the sequence.

See Also: Advanced Positions Sorting using Excel.

Note: this dialog has a read-only mode where sequence positions can be viewed, but no changes can be saved to the sequence. System defined sequences can be viewed in read-only mode for example.

### Advanced Positions Sorting using Excel

**Overview:**

The Edit Position Dialog provides copy and paste integration with Excel.

1. Copy selected sequence data from the Edit Position Dialog to Excel.
2. Sort the selected sequence items in Excel.
3. Copy the data back to the Edit Position Dialog.

This feature provides a way to execute advanced sorts inside of Excel that are not provided by the Vector software. There are a number of constraints that the user must be aware of when using this feature.

**Illustrated Step by step instructions for Advanced Sorting using Excel:**

**Step 1: Copy Sequence Data from Edit Position Dialog**

From the Edit Positions Dialog select the sequence positions that shall be adjusted using Excel. Selecting the items in the table and press CTRL+C. This will copy the sequence items into the Windows clipboard.

Note: Edit Position Dialog will not accept a paste action until a copy has been initiated.

The image below shows the copy from the Edit Positions Dialog.

**Step 2: Prepare Excel**

If Excel is not currently running then start it. Select an empty cell in Excel were the sequence data should be pasted.

The image below shows the empty Excel worksheet.

**Step 3: Paste Sequence Data from Edit Position Dialog to Excel**

The data from Sequence Edit Position dialog should currently be in the Windows clipboard. Using the CTRL+V (Paste Action; this can also be done from the Edit Menu of Excel) paste the sequence data into Excel.

The image below shows the past into Excel.

**Step 4: Sort Sequence Data using Excel**

The illustration sorts the sequence by position in ascending order. The user is free to use any of the Excel sorting features.

The image below shows the sequence list being sorted in Excel.

**Step 5: Copy Sequence Data from Excel**

At this point it is assumed that the sequence positions have been sorted according to the users specifications. We must now copy the sequence data back to the Edit Positions Dialog. Select the sorted items and press CTRL+C (or by using the Edit menu of Excel). This will copy the sequence items back into the Windows clipboard.

The image below shows the sorted items being copied from Excel.

**Step 6: Paste Sequence Data from Excel into Edit Positions Dialog**

We now return to the Edit Position Dialog, the original selected sequence items should still be selected. Press CTRL+V to paste the sorted items from Excel. This action will both remove the old sequence positions and replace them with the new sequence positions.

The image below shows the copied sequence from Excel being pasted into the Edit Positions Dialog.

## Invalid Deck Positions

## Delete Invalid Deck Positions

This dialog shows any invalid sequence positions on the current deck layout.

**Delete Selected:**

Any selected sequence position is deleted when the button "Delete Selected" is pressed.

Multiple positions to be deleted can be selected by holding the CTRL key pressed while selecting the positions with the mouse.

**Select All:**

By pressing the button "Select All" all invalid positions in the list are selected for deletion.

## Defining Labware Sequences

## What is a Sequence?

A sequence is a List of Positions that consist of:

<mark style="background-color:purple;">INDEX</mark> = order in which the positions are processed - this column is fixed

<mark style="background-color:red;">LABWARE ID</mark> = rackname - could be a plate name or sample tube carrier name

<mark style="background-color:green;">POSITION ID</mark> = specific well on a plate, or a specific tube position a sample carrier

<figure><img src="../../../.gitbook/assets/image (246).png" alt=""><figcaption></figcaption></figure>

## Advantage of Sequence concept

* Flexable & Limitless
* Can be sorted any way possible\
  ![](<../../../.gitbook/assets/image (247).png>)
* Not limited to one labware or one labware type\
  ![](<../../../.gitbook/assets/image (248).png>)
* Can have multiple entries of the same position
* Can be modified during the Method run by commands\
  ![](<../../../.gitbook/assets/image (249).png>)\
  ![](<../../../.gitbook/assets/image (251).png>)

## Creating a Sequence

![](<../../../.gitbook/assets/image (252).png>)

* When labware is added to the deck, a default Sequence is created with the same name as the labware.\
  ![](<../../../.gitbook/assets/image (253).png>)
* Another way is to select all the desired positions for your self made sequence and save it with a new name. E.g. SourcePlate, DestinationPlate, Dilutant\_A, ReagentB, SourceStack, My\_1000ul\_Tips....\
  ![](<../../../.gitbook/assets/image (254).png>)\\

To select the positions for your self made Sequence:

1. Click the Clear Selected button ![](<../../../.gitbook/assets/image (257).png>)
2. Do one of the following:
   1. Select (“Rubber Band“) the desired positions\
      ![](<../../../.gitbook/assets/image (258).png>)
   2. Click on labware to select the Stamp Tool “pattern“\
      ![](<../../../.gitbook/assets/image (259).png>)
   3. Click on the Single position select button and then individually click on the desired positions to select.\
      ![](<../../../.gitbook/assets/image (260).png>)
3. Click Save As... and provide a name ![](<../../../.gitbook/assets/image (261).png>)

* Continuing to Rubber Band or to click on positions continues to append those positions to your list
* When starting a new Sequence, click the Clear Selected button first or your list may contain unwanted positions ![](<../../../.gitbook/assets/image (262).png>)

<figure><img src="../../../.gitbook/assets/image (263).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (264).png" alt=""><figcaption></figcaption></figure>

Creating a Sequence: Stamp Tool

Type of pipetter to use that dictates how positions are sorted when Sequences are first created and what pattern is selected when labware is clicked.

<figure><img src="../../../.gitbook/assets/image (266).png" alt=""><figcaption></figcaption></figure>

Pattern examples from clicking A1 well on a 384 well plate:

<figure><img src="../../../.gitbook/assets/image (267).png" alt=""><figcaption></figcaption></figure>

## Editing and Sorting Sequences

Click the Advanced button to bring up the Edit Positions window ![](<../../../.gitbook/assets/image (268).png>)\\

<figure><img src="../../../.gitbook/assets/image (269).png" alt=""><figcaption></figcaption></figure>

Note: the order of adding the positions to your sequence is the order they appear in the sequence list

<figure><img src="../../../.gitbook/assets/image (271).png" alt=""><figcaption></figcaption></figure>

From the Edit Positions window, the positions can be:

1. Sorted by Labware, Position, X, Y, and Z co-ordinates in either ascending or decending order
2. Sorted by starting corner and direction\
   ![](<../../../.gitbook/assets/image (270).png>)
3. Sorted by the default Stamp Tool order
4. Positions can also be deleted from list

## Handling Sequences

<figure><img src="../../../.gitbook/assets/image (319).png" alt=""><figcaption></figcaption></figure>

* Clicking a sequence name from the list selects that sequence
* Right-click a sequence name to Rename it
* Properties will list the labware assciated with that sequence
* Click the red X to delete the selected sequence
* One System Defined sequence is created for each Tip Type that is added to the deck layout

## Playing and Validating a Sequence

The Sequence Player will animate the order a Sequence is processes by the Stamp Tool. Use this to test the sort order

<figure><img src="../../../.gitbook/assets/image (321).png" alt=""><figcaption></figcaption></figure>

The Validate button checks for invalid Sequences and provides the options to delete them

<figure><img src="../../../.gitbook/assets/image (322).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (323).png" alt=""><figcaption></figcaption></figure>

## Using Sequences

* Sequences are used within Method Steps to describe a source or a destination for pipetting and transport

<figure><img src="../../../.gitbook/assets/image (324).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (325).png" alt=""><figcaption></figcaption></figure>

*   When pipetting, 1st sequence position is assigned to channel 1, the 2nd position to channel 2 and so on until all channels or positions have been assigned and then the processing begins\
    Returning to the same sequence, the 9th position is assigned to channel 1, 10th position assigned to channel 2 and so on until all channels or positions have been assigned.\
    \\

    <figure><img src="../../../.gitbook/assets/image (326).png" alt=""><figcaption></figcaption></figure>
* Pointers keep track of the available positions in a Sequence\
  \
  ![](<../../../.gitbook/assets/image (327).png>)
  * The Current\_Position pointer always points to the next available position (set to index # 1 when first created)
  * The End\_Position pointer always points to the last available position (set to the last index # when first created)
* Actions, such as pipetting and transport, always start at the Current\_Position and follow the index order
  * If the Sequence Counting is set to Automatic, then the Current\_Position pointer will follow along as positions get processed\
    ![](<../../../.gitbook/assets/image (329).png>)
  * In the illustration below, the first eight positions were processed and the Currrent\_Position pointer now points to index #9\
    ![](<../../../.gitbook/assets/image (330).png>)\
    \\
  * If the Sequence Counting is set to Manual, then the Current\_Position pointer will not change as positions get processed\
    ![](<../../../.gitbook/assets/image (332).png>)\
    ![](<../../../.gitbook/assets/image (333).png>)
  * In the illustration below, the first eight positions were processed and the Currrent\_Position pointer continued to point to index #1 which means those first eight positions will be re-proccessed\
    ![](<../../../.gitbook/assets/image (334).png>)\
    \
    \
    \\
  *   Manual: "go back to same positions"

      Automatic: "Advance to next positions"\
      \
      ![](<../../../.gitbook/assets/image (335).png>)\
      \
      \\
  * When all positions are processed, the Current\_Position pointer has no next available position to point to and is set to zero\
    In the illustration below, all positions were processed and the Currrent\_Position pointer now points past the End\_Position pointer indicating that the Sequence has no positions left to process.\
    ![](<../../../.gitbook/assets/image (337).png>)\
    \
    \
    \
    \
    \\
  *   If all positions in a Sequence have been processed and you try to pipette to the same sequence then an error occurs and your Method is aborted.\\

      <figure><img src="../../../.gitbook/assets/image (339).png" alt=""><figcaption></figcaption></figure>

      To avoid this error or to start over from the beginning of a sequence: Use the Sequence: Set Current Position step\
      ![](<../../../.gitbook/assets/image (341).png>)\
      \\
  * Also, if positions from a Sequence (e.g. Reagent tub) are to be re-used then reset to the beginning by using the Sequence: Set Current Position step.\
    ![](<../../../.gitbook/assets/image (342).png>)\
    In fact, the Current Position can be set to any position within the Sequence. Processing will then start from that position.\
    ![](<../../../.gitbook/assets/image (343).png>)\
    Similarly, the End Position can be set to any position within the Sequence. Only positions between the Current Position and End Position can be processed.\\

## Sequence Counting

Manual: "go back to same positions"

Automatic: "Advance to next positions"\
\
![](<../../../.gitbook/assets/image (335).png>)
