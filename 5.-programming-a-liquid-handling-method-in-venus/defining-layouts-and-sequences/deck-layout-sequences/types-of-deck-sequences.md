# Types of Deck Sequences

## **System-Managed Sequences**

**Description of Sequences that are Automatically Generated and Managed by the System:** System-managed sequences are sequences created and maintained by the system to ensure the proper functionality and organization of deck operations. These sequences are automatically generated when new labware is added to the deck or during system initialization, ensuring consistent and reliable positioning for specific instruments or workflows. System-managed sequences are critical for maintaining the structural integrity of the instrument deck and ensuring that default operations are smoothly executed without manual intervention.

**Properties of System-Managed Sequences:** System-managed sequences have specific properties that distinguish them from user-defined sequences:

* **Immutable:** These sequences cannot be altered by the user. Their configuration is locked by the system to prevent any disruptions to core processes.
* **Read-only:** While users can view system-managed sequences, they cannot make modifications. The sequences are visible only in a read-only mode, ensuring that the default settings remain intact.
* **Non-deletable:** Unlike user-defined sequences, system-managed sequences cannot be deleted. This is a safeguard to prevent accidental removal of critical deck operations that might affect system performance or workflow execution.

**Instructions for Viewing System-Managed Sequences:** Although system-managed sequences are not modifiable, users can view their positions and details using the ‘Edit Positions Dialog’. Follow these steps to view system-managed sequences:

1. **Open the Deck Layout View:** Navigate to the deck layout where sequences are listed, including both system-managed and user-defined sequences.
2. **Select the Sequence to View:** In the 'System Managed Sequences' list, select the desired sequence. System-managed sequences are clearly labeled to differentiate them from user-defined sequences.
3. **Access the 'Edit Positions Dialog':** Once a sequence is selected, double-click on it or right-click to open the context menu. From the menu, choose the 'Edit Positions Dialog' option. The dialog box will display the sequence’s positions and details in read-only mode.
4. **View the Sequence:** In the 'Edit Positions Dialog', you can view all the positions contained in the system-managed sequence. No editing options will be available, as the system protects these sequences from modification.

By providing visibility into system-managed sequences without allowing alterations, the system ensures that essential configurations are not tampered with while giving users insight into how sequences are structured.

***

## **User-Defined Sequences**

**Overview of Sequences Created and Managed by the User:** User-defined sequences offer flexibility to adapt the deck layout to specific workflows or preferences. Unlike system-managed sequences, these are entirely customizable, giving users the ability to create new sequences that meet their unique requirements. Users can define, adjust, rename, and delete these sequences to fit the evolving needs of their lab operations.

**Properties of User-Defined Sequences:** User-defined sequences differ from system-managed sequences in several key ways:

* **Modifiable:** Users have complete control over the positions and contents of user-defined sequences. This flexibility allows users to optimize sequences for their specific tasks and workflows.
* **Renamable:** Users can rename sequences to better reflect their purpose or to follow specific naming conventions that enhance organization and clarity.
* **Deletable:** If a sequence is no longer needed, it can be deleted to streamline the sequence list. This helps users maintain an organized deck layout, ensuring that only relevant sequences are kept.

**How to Modify, Rename, or Delete User-Defined Sequences:**

1. **Modify a Sequence:**
   * Select the desired user-defined sequence from the 'Deck Sequences' list.
   * Double-click on the sequence or right-click to open the context menu, then choose the 'Edit Positions Dialog' option.
   * Modify the positions and contents as needed. The 'Advanced' option may provide further customization, such as sorting and precise position adjustments.
   * Once the changes are made, click 'Save' to update the sequence.
2. **Rename a Sequence:**
   * Select the user-defined sequence from the 'Deck Sequences' list.
   * Right-click the sequence and choose 'Rename' from the context menu, or simply press the F2 key.
   * Enter the new name and confirm the change by pressing 'Enter.' The sequence will now appear under the new name in the list.
3. **Delete a Sequence:**
   * Select the sequence to be deleted from the 'Deck Sequences' list.
   * Right-click the sequence and choose 'Delete,' or press the 'Del' key on your keyboard.
   * Confirm the deletion when prompted. The sequence will be removed from the deck layout, helping keep the sequence list clean and relevant.

**Examples of When a User Might Define a Custom Sequence:**

* **Task-Specific Sequences:** A user working on a specific experimental protocol may define a sequence to ensure that labware is placed in a particular order on the deck for easy access during the procedure.
* **Workflow Optimization:** When users need to frequently access a set of labware or instruments in a specific order, they can create custom sequences that streamline the workflow, reducing time spent searching for the correct labware position.
* **Personal Preferences:** Different users may have different preferences for how labware and instruments are arranged on the deck. Custom sequences allow users to tailor the deck layout to their own working style, improving efficiency and reducing errors.
* **Temporary Sequences:** For short-term projects or experiments, users may create custom sequences that only apply to the current task. Once the project is completed, these sequences can be easily deleted to reduce clutter.

User-defined sequences offer great flexibility and customization, empowering users to control and optimize their deck layout according to their needs. By providing the ability to modify, rename, and delete sequences, the system ensures that users can keep their deck organized and functional for a wide range of tasks.
