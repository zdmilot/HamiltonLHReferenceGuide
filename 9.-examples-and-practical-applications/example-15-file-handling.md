---
description: >-
  Modify the previous Method to open a file and create sequence and volume
  arrays from the file’s records.  Use the Sequence Library to manipulate
  sequences dynamically.
---

# Example 15: File Handling

1. With the previous Method (Volume\_Arrays.med) open, perform a File - Save As and save it as FileHandling.&#x20;
2. Modify the method by deleting the Assignment step through to the Sequence: Set End Position steps
3. Add the general step File: Open to the method just below the Array: Declare / Set Size step:&#x20;
   1. Click on the Microsoft Excel tab and browse to the file STU\_Worklist.xls (copy from thetraining drive).
   2. From the “Column Specification Helper” select Sheet1$ as the Sheet name and click “OK”. &#x20;
   3. Change the Position variable type to String with a Max column width of 255.   Click OK to close.
4. Next add a Loop step and iterate over the file.
5. To this loop add the General step File: Read.&#x20;

\*Note - This should always be the first step in a file read loop (otherwise how do we get the data from the file?)

6. Bring in the Sequence Library by selecting Libraries… from the Method menu.  Browse to and select HSLSeqLib.hsl.  Close the dialog window and a new dropdown will be added to your Toolbox.\
   ![](<../.gitbook/assets/image (307).png>)
7. In a similar manner, bring in the Utility Library, HSLUtilLib2.hsl.
8. Select the SeqAdd step from the Sequence Library and insert it into the Loop step below the File- Read:&#x20;
   1. Enter FilePickList for the Sequence Object, file1\_Labware\_ID as the LabwareID, and file1\_Position as the PositionID. &#x20;
   2. When you close the step, a window will pop up asking you to confirm the new sequence variable.  Click OK.\
      ![](<../.gitbook/assets/image (309).png>)
9. Next add the step Array: Set At and add file1\_Volume to the end of arrVolumes.
10. After the End-Loop add a File: Close step.



\*Note – Always add a File: Close step after the necessary data has been extracted from the file.  Otherwise there may be issues opening the file by other software, or Venus in the future. &#x20;

11. Modify the pipetting loop.  Select FilePickList as the controlling sequence and make sure to set Reset before loop.&#x20;
12. Modify the Aspirate step and set the aspirate sequence to FilePickList.
13. Modify the Dispense step and set the dispense sequence to Nun\_96\_Fl\_Lb\_0001.
14. Use the HSLUtilLib2.hsl Utility Library to trace the content of the sequence and array by adding the step Util2::Debug::TraceSequence and Util2::Debug::TraceArray after the File: Close step.
15. Save and launch Run Control.  Simulate the method and correct any errors.  Check that the correct volumes were pipetted in the trace file.  &#x20;
