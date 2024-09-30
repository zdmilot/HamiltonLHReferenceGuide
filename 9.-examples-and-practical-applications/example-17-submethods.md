---
description: >-
  Modify the previous method to incorporate a Submethod.  The Submethod will
  trace out the contents of the Array and Sequence.
---

# Example 17: Submethods

1. Open the method FileHandling.med, Select File - Save As and name it Submethod.
2. Add a new Submethod:
   1. Right click within the Method Bar and select “Add” from the drop down. \
      ![](<../.gitbook/assets/image (314).png>)
   2. Within the “Name” field name the Submethod TraceData.
   3. Add a Parameter named subArray, with type as Array of Variables, direction as Input and Output, and description as “Array to trace to logfile”
   4. Add a second Parameter named subSequence, with type as Sequence, direction as Input and Output, and description as “Sequence to trace to logfile”.\
      ![](<../.gitbook/assets/image (315).png>)
   5. Click OK to close the submethod’s parameter window
3. To the TraceData submethod add the Utils2 Libray command Debug::TraceArray to trace the array subArray

<figure><img src="../.gitbook/assets/image (316).png" alt="" width="326"><figcaption></figcaption></figure>

4. To the TraceData submethod add the Utils2 Libray command Debug::TraceSequence to trace the sequence subSequence
5. Back on the main Method tab, replace the Debug::TraceArray and Debug::TraceSequence steps with the Local Sub-methods step TraceData.  Provide the sequence \_Source and the array \_Volumes

<figure><img src="../.gitbook/assets/image (317).png" alt="" width="375"><figcaption></figcaption></figure>

6. Save and launch Run Control.  Simulate the method and correct any errors.

&#x20;

&#x20;

&#x20;

&#x20;

&#x20;

&#x20;

&#x20;

&#x20;

&#x20;

&#x20;

&#x20;

&#x20;
