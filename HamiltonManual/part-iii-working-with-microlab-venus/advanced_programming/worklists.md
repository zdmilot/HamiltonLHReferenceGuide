# Worklists

## ‌File Formats‌

Frequently, there will be a need to import and export worklists. The “Open file” Command of the method editor is designed to enable such file handling. The data source type (format) is identified by the extension of the worklist file name. The editor supports formats listed in the table presented below. No other extensions are supported.

| Microsoft Excel           | .xls                    |
| ------------------------- | ----------------------- |
| Microsoft Access Database | .mdb                    |
| Structured Text Files     | .txt, .csv, .tab, .asc. |
| Unstructured Text Files   | <p><br></p>             |

\


## Command Overview‌

| Command            | Icon                                                                                                                                                            | Action Performed                                                      | Parameters to be Specified                                                                                           |
| ------------------ | --------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------- |
| File: Open         | <p><br></p><p><img src="../../../.gitbook/assets/Image_672.gif" alt="17"></p>                                                                                   | Open a file before file access                                        | File type, name, handle (reference to file), mode, data exchange variable and other, file- type-dependent parameters |
| File: Read         | <p><br></p><p><img src="../../../.gitbook/assets/Image_673.gif" alt="18"></p>                                                                                   | Read data out of a file                                               | File handle                                                                                                          |
| File: Write        | <p><br></p><p><img src="../../../.gitbook/assets/Image_674.gif" alt="19"></p>                                                                                   | Write data into a file\*                                              | File handle                                                                                                          |
| File: Set Position | <p><br></p><p><img src="../../../.gitbook/assets/Image_675.gif" alt="20"></p>                                                                                   | Set the file-pointer to a specific position for reading               | New position parameters                                                                                              |
| File: Close        | <p><br></p><p><img src="../../../.gitbook/assets/Image_676.gif" alt="21"></p>                                                                                   | Close a file after file operation(s)                                  | File handle                                                                                                          |
| Import Worklist    | <p><br></p><p><img src="../../../.gitbook/assets/Image_677.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\BtnImportWorklist.bmp"></p> | Imports worklist data from files into the supported database columns. | Wizard-guided; filename, filetype, delete old data Y/N, table name, column mapping                                   |



The FileRead / WriteSteps will read or write only ONE LINE of the file. To read through a complete file, use a loop.

The example below shows how to use the file commands. First, the file is opened by using the File: Open step. The path (C:\Temp\Worklist.xls) and sheet name (Absorbance$) are specified. Columns (LabID / PosID / OD) are linked to variables (xls\_LabID / xls\_PosID / xls\_OD) respectively.

A loop is inserted to make sure that the file is read from the beginning to end. Inside the loop, the File: Read step reads line per line and assigns the values from the file into the variables.

In this case, the LabID and PosID are read out and are used to create sequence positions through the SeqAdd step.

To end, the file is closed (otherwise, it remains open and exclusively locked by the method).

<figure><img src="../../../.gitbook/assets/image (589).png" alt=""><figcaption></figcaption></figure>

## ‌Importing a Worklist‌

<table data-header-hidden><thead><tr><th width="145"></th><th></th></tr></thead><tbody><tr><td><img src="../../../.gitbook/assets/image (10) (1) (1) (1) (1) (1) (1) (1).png" alt="" data-size="original"></td><td><p>NOTE</p><p>Once a Deck Layout has been linked to a method, the instrument specific steps will be visible in the toolbox.</p></td></tr></tbody></table>

1. From the toolbox, drag the “Load and Match” Command into the method.
2.  The “Load and Match” Wizard Step 1 will start as shown below.

    \


    <figure><img src="../../../.gitbook/assets/image (590).png" alt=""><figcaption></figcaption></figure>

    \

3. Select the instrument and the sequence, to load all potential samples. To unload unused samples, which means samples without a worklist entry, check the box “Unload unused samples tubes”.
4.  Click \[Next >] to continue to the next step of the wizard.\
    \


    <table data-header-hidden><thead><tr><th width="145"></th><th></th></tr></thead><tbody><tr><td><img src="../../../.gitbook/assets/image (10) (1) (1) (1) (1) (1) (1) (1).png" alt="" data-size="original"></td><td><p>NOTE</p><p>It is recommended to use fixed paths in the “Worklist filename” Field. Using fixed paths will allow a preview of the file. Using variables only does not allow a file preview.</p></td></tr></tbody></table>


5.  Specify the sheet to be opened (when using Excel) and check the data preview.\


    <figure><img src="../../../.gitbook/assets/image (555).png" alt=""><figcaption></figcaption></figure>
6.  Link the columns of the worklist to the default columns of the database. If needed, use the filter options to restrict the amount of data. A sorting option is available to specify the order of appearance. Click \[Finish] to complete the worklist import command.\
    \
    \


    <figure><img src="../../../.gitbook/assets/image (556).png" alt=""><figcaption></figcaption></figure>



## Importing a Worklist Example

This example shows the application of a worklist import.

The “Load and Match” Command is used to load the sample carrier 1 and to read all the barcodes. These barcodes are compared to the ones in the database (from the worklist). If the values match, a sequence position will be created in the “AllMatchingPositions\_Source” Sequence into the target plate. The volume is taken from the array that was created in the Load and Match step. This array can be inserted directly in the Smart Step.

### Import a Worklist

1. First, a worklist is imported with the command Import Worklist as described above.
2. From the toolbox, drag the “Load and Match” Command into the method.
3.  The “Load and Match” Wizard Step 1 will start as shown below.

    <figure><img src="../../../.gitbook/assets/image (557).png" alt=""><figcaption></figcaption></figure>

    \

4. Select the instrument and the sequence to load all potential samples. To unload unused samples, which means samples without a worklist entry, check the “Unload unused samples tubes” Box. Click \[Next >] to continue.
5.  Select the source sequence ‘AllMatchingPositions\_Source‘ with all matching positions and the target volume array ‘Matching\_Volume\[\*]. Click \[Next >] to continue.



    <figure><img src="../../../.gitbook/assets/image (558).png" alt=""><figcaption></figcaption></figure>
6.  The “Load and Match” Wizard Step 3 will be shown.

    <figure><img src="../../../.gitbook/assets/image (559).png" alt=""><figcaption></figcaption></figure>

    \

7. Click on the highlighted button shown above. Select the “Optimized for parallel pipetting” Sorting Method. Click \[Finish] to end the wizard.
8. From the toolbox, drag the “1000μl Channel Pipette – Simple (1-1)” Command into the method.
9. The “1000μl Channel Pipette – Simple (1-1)” Wizard Step 1 will start.
10. Select the instrument “ML\_STAR”, the sequence to aspirate “ML\_STAR.ReagentTrough” and the sequence to dispense “AllMatchingPositions\_Source”. Click \[Next >] to continue.\


    <figure><img src="../../../.gitbook/assets/image (560).png" alt="" width="358"><figcaption></figcaption></figure>
11. The “1000μl Channel Pipette – Simple (1-1)” Wizard Step 2 will be shown.\


    <figure><img src="../../../.gitbook/assets/image (561).png" alt="" width="358"><figcaption></figcaption></figure>

    \

12. Select the volume array “Matching\_Volume” and click on the array assistant to select the ‘Use multiple array values’. Make sure the Automatic array index selection box is ticked.

    <figure><img src="../../../.gitbook/assets/image (562).png" alt=""><figcaption></figcaption></figure>

    \

13. Click on \[OK] to close the window.
14. Select \[No] to the question if an additional rest volume should be aspirated.
15. Click \[Next >] to continue.
16. The “1000μl Channel Pipette – Simple (1-1)” Wizard Step 3 will be displayed.

    <figure><img src="../../../.gitbook/assets/image (563).png" alt=""><figcaption></figcaption></figure>

    \

17. Select the desired tip type. The tip sequence window will show all available sequences of this tip type.
18. Decide if there is a need to replace tips and activate the corresponding radio button. Leave the rest of the values in the dialog with the default settings. Click \[Next >] to continue.
19. The “1000μl Channel Pipette – Simple (1-1)” Wizard Step 4 will be activated.

    <figure><img src="../../../.gitbook/assets/image (564).png" alt=""><figcaption></figcaption></figure>
20. Select the desired dispense mode and an applicable liquid class from the list. Leave the rest of the values in the dialog with the default settings. Click \[Next >] to continue.
21. The “1000μl Channel Pipette – Simple (1-1)” Wizard Step 5 will be shown.

    <figure><img src="../../../.gitbook/assets/image (565).png" alt=""><figcaption></figcaption></figure>

    \

22. Select the “Dispense” Sequence as the controlling sequence (to finish pipetting after the AllMatchingPositions\_Source sequence is used up). Leave the rest of the values in the dialog with the default settings. Click \[Finish], to complete the Pipette – Simple (1-1) command.

### Worklist Handling with Microsoft Excel‌

Specifying a subset of the available data can be done when a Microsoft Excel workbook file is open. It is possible to open either of the following:

* A single worksheet
* A named range anywhere in the workbook
* An unnamed range in a single worksheet

The following table lists the conventions for these settings.

\


| To open this object to read...                                  | ...use this syntax                                                                                                                                                                                             |
| --------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Entire worksheet in a workbook file                             | <p>Specify the sheet as sheetname$, where sheetname is the name of the worksheet.</p><p>Important: A worksheet name must end with a dollar sign ($).</p>                                                       |
| Named range of cells in a worksheet or workbook file            | <p>Specify the named range as NamedRange, where NamedRange is the name assigned to the range in Microsoft Excel.</p><p>Important: The range in Microsoft Excel must be named before attempting to open it.</p> |
| Unnamed range of cells in a single worksheet in a workbook file | Specify the sheet to be opened as sheetname$ and the range as FirstCellInRange:LastCellInRange. For example, to access cells A1 through Z256 in a worksheet called Sales, Sales$A1:Z256 is specified.          |
| To open this object to write...                                 | ...use this syntax                                                                                                                                                                                             |
| Entire worksheet in a workbook file                             | <p>Specify the sheet as sheetname, where sheetname is the name of the worksheet.</p><p>Important: Do not end the worksheet name with a dollar sign ($).</p>                                                    |
| To append to an object                                          | ...use this syntax                                                                                                                                                                                             |
| Append to an existing worksheet in a workbook file              | <p>Specify the sheet as sheetname$, where sheetname is the name of the worksheet.</p><p>Important: A worksheet name must end with a dollar sign ($).</p>                                                       |
| Append to a not yet existing worksheet in a workbook file       | <p>Specify the sheet as sheetname, where sheetname is the name of the worksheet.</p><p>Important: Do not end the worksheet name with a dollar sign ($).</p>                                                    |

\


<table data-header-hidden><thead><tr><th width="145"></th><th></th></tr></thead><tbody><tr><td><img src="../../../.gitbook/assets/image (10) (1) (1) (1) (1) (1) (1) (1).png" alt="" data-size="original"></td><td><p>NOTE</p><p>A value in a range that exceeds the maximum number of rows, columns, or sheets for the worksheet or workbook cannot be specified. For more information on these values, refer to the Microsoft Excel documentation.</p><p>The format of all entries within a column in the Excel file must be identical: text, number, etc.</p><p>The handling (open/read/write/… file) of Excel files using the VENUS Software files do not require the installation of Microsoft Excel.</p></td></tr></tbody></table>



