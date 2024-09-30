# Creating and Modifying Sequences

Sequences are essential for organizing and managing the operations of labware on the deck of an instrument. Whether system-generated or user-defined, these sequences dictate the order of operations and can be modified to suit specific workflows. This section will provide a detailed step-by-step guide for creating, modifying, and deleting sequences.

***

## **Creating a New Sequence**

Creating a new sequence allows users to define a custom workflow for their instrument deck. Here's how to create a new sequence:

**Step-by-Step Instructions for Creating a New Sequence:**

1. **Open the Deck Sequence Panel:**
   * Navigate to the instrument control interface and find the **Deck Sequences** panel, which lists both system-generated and user-defined sequences.
2. **Click on "New Sequence":**
   * Locate the **New Sequence** button, typically found at the bottom of the Deck Sequences panel. Clicking this button initiates the creation of a new empty sequence.
   * Alternatively, you can use the keyboard shortcut **Ctrl+N** to start a new sequence creation.
3. **Name the New Sequence:**
   * A dialog box will prompt you to enter a name for the sequence. Enter a descriptive and unique name to make it easier to identify later.
   * For example, you can name it according to the labware type or process, such as "Sample Prep 1" or "PCR Run."
4. **Save the Sequence:**
   * Once the name is entered, click **Save** to confirm and add the new sequence to the list.
   * You can also use the **F2** key to rename the sequence at any point later if needed.

**How to Enter and Save the Sequence with a New Name:**

* The newly created sequence will appear in the list of sequences, and you can now start adding positions and defining specific steps in your workflow.
* When saving an existing sequence with a new name, use the **Save As...** option, which allows you to keep a copy of the current sequence under a new name while preserving the original.

***

## **Modifying Existing Sequences**

Modifying sequences allows you to adjust positions, reorder steps, and fine-tune your workflow.

**Description of How to Edit Sequence Positions and Save Modifications:**

* Each sequence consists of specific positions, which correspond to the steps or placements of labware on the deck.
* You can modify the sequence by dragging and dropping items into new positions or changing the order of operations to optimize your experiment.

**Step-by-Step Instructions for Using the 'Advanced' Option and the 'Edit Positions Dialog':**

1. **Open the Sequence for Editing:**
   * In the Deck Sequences panel, double-click on the sequence you want to edit, or right-click and select **Edit**. This opens the **Edit Positions Dialog**.
2. **Use the 'Advanced' Option for Detailed Adjustments:**
   * In the Edit Positions Dialog, click on **Advanced** to access more granular controls for sorting and adjusting positions. This feature allows you to modify not only the order but also the specific parameters of each position.
   * For instance, you can adjust the timing of a step, the specific location of labware, or interaction settings with other instruments.
3. **Drag and Drop to Reorder:**
   * In the Edit Positions Dialog, you can drag items (such as plates, racks, or reagents) into new positions on the deck.
   * Ensure that the sequence reflects the correct order of operations for your experiment.
4. **Save Modifications:**
   * After making your changes, click **Save** to confirm the modifications. The updated sequence will overwrite the previous version unless you opt to save it with a new name using **Save As...**.

**Instructions for Saving or Renaming Sequences with Examples:**

* After editing, to save changes under a new name, use the **Save As...** option from the file menu or the sequence context menu. This will allow you to keep a copy of the original sequence intact while creating a new version.

**Example:**

* You have an existing sequence named "Sample Prep." After adjusting the order of labware placements, you can save it as "Sample Prep v2" to reflect the updated sequence without overwriting the original.

***

## **Deleting Sequences**

Deleting sequences helps keep your workspace organized by removing sequences that are no longer needed.

**Steps to Delete User-Defined Sequences:**

1. **Select the Sequence to Delete:**
   * In the Deck Sequences panel, locate the sequence you want to delete.
2. **Delete the Sequence:**
   * Right-click on the sequence and choose **Delete** from the context menu. Alternatively, select the sequence and press the **Delete (Del)** key on your keyboard.
   * Confirm the deletion when prompted. Be cautious when deleting, as this action cannot be undone.
3. **System-Managed Sequences:**
   * **Note:** System-managed sequences, which are automatically generated and controlled by the system, **cannot** be deleted or modified. These sequences are locked and are only viewable in read-only mode.

**Clarification on System-Managed Sequences:**

* System-managed sequences are integral to the function of the instrument deck. They manage the default behaviors of labware placements and movements, ensuring smooth operation of the deck.
* Users can view these sequences in the **Edit Positions Dialog** but cannot delete or rename them.
