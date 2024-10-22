# Method for Hit Picking using Smart Steps

Assume that there is a source plate and a photometer reads the optical absorbance of the wells of the plate. Create a target plate with all the compounds in the source plate having an absorbance of A>1.0E.

The ‘hit picking’ method exactly does this. The photometric results are retrieved from a file, and a sequence of hits (A>1.0E) is created ‘on the fly’ according to the absorbencies that have been read. Pipetting then occurs according to the sequence.

For this method, a source containing the absorbencies of the 96 wells of the source microplate is needed. The database can be either of the following:

* ASCII text file
* Microsoft Excel file
* Microsoft Access database
* Vector database

In this example, the database used is a Microsoft Excel file. The name of the Excel sheet being used is “Absorbance”. The sheet contains three columns, as follows:

* “LabID” defining the plate name of the source plate (“Source\_1” for the first plate and “Source\_2” for the second plate)
* “PosID” defining the position in the microplate alphanumerically (A1, A2, …, H12)
* absorbance or optical density “OD” in mE

The worklist then has 193 lines, 1 header line and the entries from 2 plates with 96 wells each.\


<figure><img src="../.gitbook/assets/image (76) (1).png" alt=""><figcaption></figcaption></figure>

The Deck Layout contains (see picture below):

* One tip carrier “TIP\_CAR\_480\_ST\_A00.tml” preloaded with five standard volume tip racks
* One plate carrier “PLT\_CAR\_L5MD\_A00.tml” with two Nunc plates “Nun\_96\_Fl\_L.rck”, which are the source plates (change the properties such that one plate is called “Source\_1” and the other “Source\_2”)
* One plate carrier “PLT\_CAR\_L5MD\_A00.tml” with two Nunc plates “Nun\_96\_Fl\_L.rck”, which are the target plates

<figure><img src="../.gitbook/assets/image (77) (1).png" alt=""><figcaption></figcaption></figure>

1. Create the “Target” Sequence by activating the “Sequences” Tab in the Deck Layout Editor.
2. Click on \[Clear selected].
3. Activate the “Channels” Stamp Tool and create a sequence spanning the two target plates and name it as “Target”.
4. Switch to the Method Editor window.
5. Include the two libraries “HSLTrcLib.hsl” and “HSLSeqLib.hsl” in the method.

***

## Creating the Method

1. “Drag and Drop” the steps from the toolbox into the method, as shown below.\
   \
   ![](<../.gitbook/assets/image (78) (1).png>)\

2. The first step is to request the user to input a threshold value for the absorption. This is saved as a variable called “Threshold”.\
   \
   ![](<../.gitbook/assets/image (79) (1).png>)\

3. In the “Prompt” Field, type in the question to be asked to the user (do not forget to put the string in quotation marks for this is a text).
4. Specify the “Type” (integer, float, string) of the input required. In this case, use a float type because this value will be used in an SQL statement.
5. In the next fields, a default value that is already displayed when the dialog opens can be specified. Having an integer or float value, also minimum and maximum values can be defined.
6. Click \[OK] to finish the user input.
7. In the next step, create an SQL statement to get only the values with the specified OD or greater. The complete expression in the left field is:\
   \
   “SELECT \* FROM \[Absorbance$] WHERE OD >”\
   ![](<../.gitbook/assets/image (80) (1).png>)\

8. This will create a variable SQL\_Statement which depends on the user input, e.g. if the user types in 500 as threshold, the statement to open the excel file will be “SELECT \* FROM \[Absorbance$] WHERE OD > 500”
9. Here, “Absorbance$” refers to the name of the Excel sheet which is going to be opened during the next steps.
10. Drag the “Open File” Icon into the method to open the file holding the absorbance information. The file format is also defined within this step as follows:
11. Select the tab for opening “Microsoft Excel” Files.
12. Under “File name (\*.xls)”, enter the file name. When browsing for the file, the full absolute path is required with the filename. Note that the backslash must be written twice. To use a relative path, delete it or simply enter the path enclosed in quotation marks.\
    \
    ![](<../.gitbook/assets/image (81) (1).png>)
13. The file type is an Excel file (.xls) where the sheet name (sheet1 if not defined otherwise, language dependent) and the $ sign must be added within the quotation marks.
14. Define a file handle (here the default: “file1”) which is a name for the file used within the method. Later, data will be read from this file by referring to this file handle.
15. Select “Open File to Read” as the mode to read data from this file.
16. Now, define the file format. Here, a variable is assigned to each column of the file. Later, for each reading step, one record (one line) is read from the file, and the contents read are assigned to their corresponding variables automatically.
17. Now define the file structure. One line in the “Column specification” of the file opening dialog represents one column in the file. Click on the \[Add] Button to add the next line to the dialog.
18. Enter the data as given in the screenshot above. Assign a header, a variable and a variable type to each column.
19. Select the variable “sql\_statement” from the dropdown list as a command string.
20. Click \[OK] to finish the definition.
21. Create a loop after opening but before closing the input file. This will loop over the file until the file has been read completely.\
    \
    ![](<../.gitbook/assets/image (82) (1).png>)\

22. Within the loop, the first record of the file is read.\
    \
    ![](<../.gitbook/assets/image (83) (1).png>)\

23. As the file is being read, the variables defined in “Open File” will be filled with the information found.
24. Use the “SeqAdd” Library Function. This command will add positions to a sequence when giving the LabID/PosID information (see image below).\
    \
    ![](<../.gitbook/assets/image (84) (1).png>)\

25. In the sequence “Name” Field, insert a sequence name. Since in this example, a completely new sequence is being created for all the hits “AllHits”, a name can directly be typed in. The system will then create a new sequence with the specified name.
26. Because the SQL selection string automatically skips all records with absorption values less than or equal to the value of the “Threshold” Variable, no other selection statements such as IF/ELSE are required.
27. In the “LabwareId “/ “PositionId” fill the two variables from the file open.
28. After the loop, use the “TrcTraceSequence” Command to see which positions have been added to the “AllHits” Sequence. This command will list all sequence positions in the trace window.\
    \
    ![](<../.gitbook/assets/image (85) (1).png>)\

29. Add a “Load” Smart Step. After the file has been analyzed and the hit sequence has been generated, the loading of the sequences (carriers) onto the deck may start.\
    \
    ![](<../.gitbook/assets/image (86) (1).png>)\
    \


    <table data-header-hidden><thead><tr><th width="98"></th><th></th></tr></thead><tbody><tr><td><img src="../.gitbook/assets/image (10) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" data-size="original"></td><td><p>NOTE</p><p><em>The “AllHits” Sequence was created in the previous step and the current position of the sequence is undefined.</em></p><p><em>To set, use the SetCurrentPosition command from the General Steps or in the load step, set the start Position to 1.</em></p></td></tr></tbody></table>

    \
    \

30. Add the “1000μl Channel Pipette - Simple” Smart Step into the method to start pipetting.
31. In this step of the wizard, make sure that the control sequence is properly defined (see image below). The “AllHits” Aspiration Sequence is the controlling sequence and therefore is not reloadable. The target sequence is not reloadable either.\


    <figure><img src="../.gitbook/assets/image (88) (1).png" alt=""><figcaption></figcaption></figure>
32. The rest of the settings made are very similar to the previous example “OnePlateToPipette”.
33. To end with, add a step for unloading.

\
