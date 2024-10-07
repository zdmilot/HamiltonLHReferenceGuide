# Worklists

*   #### _‌File Formats‌_

    \


    _Frequently, there will be a need to import and export worklists. The “Open file” Command of the method editor is designed to enable such file handling. The data source type (format) is identified by the extension of the worklist file name. The editor supports formats listed in the table presented below. No other extensions are supported._

    \


    | Microsoft Excel           | .xls                    |
    | ------------------------- | ----------------------- |
    | Microsoft Access Database | .mdb                    |
    | Structured Text Files     | .txt, .csv, .tab, .asc. |
    | Unstructured Text Files   | <p><br></p>             |

    \

*   #### _‌Command Overview‌_

    \


    | Command            | Icon                                                                                                                                                         | Action Performed                                                      | Parameters to be Specified                                                                                           |
    | ------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------ | --------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------- |
    | File: Open         | <p><br></p><p><img src="../../.gitbook/manual-images/assets/Image_672.gif" alt="17"></p>                                                                                   | Open a file before file access                                        | File type, name, handle (reference to file), mode, data exchange variable and other, file- type-dependent parameters |
    | File: Read         | <p><br></p><p><img src="../../.gitbook/manual-images/assets/Image_673.gif" alt="18"></p>                                                                                   | Read data out of a file                                               | File handle                                                                                                          |
    | File: Write        | <p><br></p><p><img src="../../.gitbook/manual-images/assets/Image_674.gif" alt="19"></p>                                                                                   | Write data into a file\*                                              | File handle                                                                                                          |
    | File: Set Position | <p><br></p><p><img src="../../.gitbook/manual-images/assets/Image_675.gif" alt="20"></p>                                                                                   | Set the file-pointer to a specific position for reading               | New position parameters                                                                                              |
    | File: Close        | <p><br></p><p><img src="../../.gitbook/manual-images/assets/Image_676.gif" alt="21"></p>                                                                                   | Close a file after file operation(s)                                  | File handle                                                                                                          |
    | Import Worklist    | <p><br></p><p><img src="../../.gitbook/manual-images/assets/Image_677.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\BtnImportWorklist.bmp"></p> | Imports worklist data from files into the supported database columns. | Wizard-guided; filename, filetype, delete old data Y/N, table name, column mapping                                   |

    \


    _The FileRead / WriteSteps will read or write only ONE LINE of the file. To read through a complete file, use a loop._

    _The example below shows how to use the file commands. First, the file is opened by using the File: Open step. The path (C:\Temp\Worklist.xls) and sheet name (Absorbance$) are specified. Columns (LabID / PosID / OD) are linked to variables (xls\_LabID / xls\_PosID / xls\_OD) respectively._

    _A loop is inserted to make sure that the file is read from the beginning to end. Inside the loop, the File: Read step reads line per line and assigns the values from the file into the variables._

    _In this case, the LabID and PosID are read out and are used to create sequence positions through the SeqAdd step._

    _To end, the file is closed (otherwise, it remains open and exclusively locked by the method)._

    \


    ![image](../../.gitbook/manual-images/assets/Image\_678.jpg)

    \

*   #### _‌Importing a Worklist‌_

    \


    ![Originalbild anzeigen](../../.gitbook/manual-images/assets/Image\_679.gif)

    _NOTE_

    _Once a Deck Layout has been linked to a method, the instrument specific steps will be visible in the toolbox._

    \


    1. _From the toolbox, drag the “Load and Match” Command into the method._
    2.  _The “Load and Match” Wizard Step 1 will start as shown below._

        \


        ![image](../../.gitbook/manual-images/assets/Image\_680.jpg)

        \

    3. _Select the instrument and the sequence, to load all potential samples. To unload unused samples, which means samples without a worklist entry, check the box “Unload unused samples tubes”._
    4.  _Click \[Next >] to continue to the next step of the wizard._

        ![Originalbild anzeigen](../../.gitbook/manual-images/assets/Image\_681.gif)

        _NOTE_

        _It is recommended to use fixed paths in the “Worklist filename” Field. Using fixed paths will allow a preview of the file. Using variables only does not allow a file preview._

        \

    5.  _Specify the sheet to be opened (when using Excel) and check the data preview._

        \


        ![image](../../.gitbook/manual-images/assets/Image\_682.jpg)

        \

    6. _Link the columns of the worklist to the default columns of the database. If needed, use the filter options to restrict the amount of data. A sorting option is available to specify the order of appearance. Click \[Finish] to complete the worklist import command._

    \


    ![image](../../.gitbook/manual-images/assets/Image\_683.jpg)

    _Importing a Worklist Example_

    _This example shows the application of a worklist import._

    _The “Load and Match” Command is used to load the sample carrier 1 and to read all the barcodes. These barcodes are compared to the ones in the database (from the worklist). If the values match, a sequence position will be created in the “AllMatchingPositions\_Source” Sequence into the target plate. The volume is taken from the array that was created in the Load and Match step. This array can be inserted directly in the Smart Step._

    _Import a Worklist_

    1. _First, a worklist is imported with the command Import Worklist as described above._
    2. _From the toolbox, drag the “Load and Match” Command into the method._
    3.  _The “Load and Match” Wizard Step 1 will start as shown below._

        \


        ![image](../../.gitbook/manual-images/assets/Image\_684.jpg)

        \

    4. _Select the instrument and the sequence to load all potential samples. To unload unused samples, which means samples without a worklist entry, check the “Unload unused samples tubes” Box. Click \[Next >] to continue._
    5.  _Select the source sequence ‘AllMatchingPositions\_Source‘ with all matching positions and the target volume array ‘Matching\_Volume\[]. Click \[Next >] to continue._

        \


        ![image](../../.gitbook/manual-images/assets/Image\_685.jpg)
    6.  _The “Load and Match” Wizard Step 3 will be shown._

        \


        ![image](../../.gitbook/manual-images/assets/Image\_686.png)

        \

    7. _Click on the highlighted button shown above. Select the “Optimized for parallel pipetting” Sorting Method. Click \[Finish] to end the wizard._
    8. _From the toolbox, drag the “1000μl Channel Pipette – Simple (1-1)” Command into the method._
    9. _The “1000μl Channel Pipette – Simple (1-1)” Wizard Step 1 will start._
    10. _Select the instrument “ML\_STAR”, the sequence to aspirate “ML\_STAR.ReagentTrough” and the sequence to dispense “AllMatchingPositions\_Source”. Click \[Next >] to continue._

        \


        ![image](../../.gitbook/manual-images/assets/Image\_687.jpg)
    11. _The “1000μl Channel Pipette – Simple (1-1)” Wizard Step 2 will be shown._

        \


        ![image](../../.gitbook/manual-images/assets/Image\_688.jpg)

        \

    12. _Select the volume array “Matching\_Volume” and click on the array assistant to select the ‘Use multiple array values’. Make sure the Automatic array index selection box is ticked._

        \


        ![image](../../.gitbook/manual-images/assets/Image\_689.jpg)

        \

    13. _Click on \[OK] to close the window._
    14. _Select \[No] to the question if an additional rest volume should be aspirated._
    15. _Click \[Next >] to continue._
    16. _The “1000μl Channel Pipette – Simple (1-1)” Wizard Step 3 will be displayed._

        \


        ![image](../../.gitbook/manual-images/assets/Image\_690.jpg)

        \

    17. _Select the desired tip type. The tip sequence window will show all available sequences of this tip type._
    18. _Decide if there is a need to replace tips and activate the corresponding radio button. Leave the rest of the values in the dialog with the default settings. Click \[Next >] to continue._
    19. _The “1000μl Channel Pipette – Simple (1-1)” Wizard Step 4 will be activated._

        \


        ![image](../../.gitbook/manual-images/assets/Image\_691.jpg)
    20. _Select the desired dispense mode and an applicable liquid class from the list. Leave the rest of the values in the dialog with the default settings. Click \[Next >] to continue._
    21. _The “1000μl Channel Pipette – Simple (1-1)” Wizard Step 5 will be shown._

        \


        ![image](../../.gitbook/manual-images/assets/Image\_692.jpg)

        \

    22. _Select the “Dispense” Sequence as the controlling sequence (to finish pipetting after the AllMatchingPositions\_Source sequence is used up). Leave the rest of the values in the dialog with the default settings. Click \[Finish], to complete the Pipette – Simple (1-1) command._

    \

*   #### _‌Worklist Handling with Microsoft Excel‌_

    \


    _Specifying a subset of the available data can be done when a Microsoft Excel workbook file is open. It is possible to open either of the following:_

    * _A single worksheet_
    * _A named range anywhere in the workbook_
    * _An unnamed range in a single worksheet_

    _The following table lists the conventions for these settings._

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


    ![Originalbild anzeigen](../../.gitbook/manual-images/assets/Image\_693.gif)

    _NOTE_

    _A value in a range that exceeds the maximum number of rows, columns, or sheets for the worksheet or workbook cannot be specified. For more information on these values, refer to the Microsoft Excel documentation._

    _The format of all entries within a column in the Excel file must be identical: text, number, etc._

    _The handling (open/read/write/… file) of Excel files using the VENUS Software files do not require the installation of Microsoft Excel._
