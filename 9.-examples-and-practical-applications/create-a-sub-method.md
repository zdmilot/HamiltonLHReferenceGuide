# Create a Sub-Method

The following example demonstrates how to:

* Build sub-methods into the method.
* Activate a sub-method library for a particular function

This example sub-method will be performing the pipetting from a source to a target plate.

Since sub-methods are created in the ‘main’ – method, it is not necessary to define a Deck Layout for the sub-method(s).

1. To create a local sub-method, right-click on the “Method” in the method window and select “Local Sub-methods”. Name the sub-method “CheckLoadedTubeCarrier”.\
   ![](<../.gitbook/assets/image (124).png>)\

2.  The parameter window shown below appears. Supply the following parameters with the following values:

    * Sub method name: “CheckLoadedTubeCarrier”
    * Description: optional
    * Parameters: “CarrierToLoad” of type “ Sequence”
    * Sub-method name: “Pipetting”\


    <figure><img src="../.gitbook/assets/image (125).png" alt=""><figcaption></figcaption></figure>
3. The empty sub-method will then appear.\
   \
   ![](<../.gitbook/assets/image (126).png>)\

4. Create the sub-method by “Dragging and Dropping” Steps from the toolbox to the step editor.\
   \
   ![](<../.gitbook/assets/image (127).png>)\

5. The pathname settings for the unformatted text file (step 7 of the image above), the formatted Excel file (Step 8 of the image above) and the sheet name of the Excel file (Step 9 of the image above) are all set using the “Assignment” Command from the General Steps.
6. Then the new carrier is then loaded.\
   \
   ![](<../.gitbook/assets/image (128).png>)\

7. Use the “CarrierToLoad“ Variable from the parameter window as the carrier name.
8. In the “Advanced settings”, set the barcode file name to the variable “BarcodeFileText” that has been defined in the previous step.\
   \
   ![](<../.gitbook/assets/image (129).png>)\

9. The “Load” Step creates a barcode file in TXT format under the specified pathname (step 7). The file will be formatted (Step 13) after the carrier has been loaded. To use this step, its library must be included first. To do this, follow the steps below:
10. Add the library “HSLML\_STARlib.hsl” to be able to use the “FormatBarcodeFile” Command.
11. Also add the “HSLTrcLib.hsl” to be able to trace data.\
    \
    ![](<../.gitbook/assets/image (130).png>)\

12. Fill out the “FormatBarcodeFile” Dialog: the instrument and the two files must be used as parameters. A return value is not needed.\
    \
    ![](<../.gitbook/assets/image (131).png>)\

13. Note that the “BarcodeFileExcel” Variable must be handed over.
14. The next step is to open the formatted file. Because only the tube barcodes are of interest, the information in the file has to be filtered. SQL (Structured Query Language) offers a lot of these filter and sorting options. For more explanation, open Help of the “FileOpen” Step.

\


\


## Example

A filter string has to be defined. This is done in step 15 as shown in the snapshot below.

"SELECT \* FROM \[Sheet1$] WHERE \[Barcode] NOT LIKE 'No barcode' AND \[Specifier] NOT LIKE 'C'"

<figure><img src="../.gitbook/assets/image (132).png" alt=""><figcaption></figcaption></figure>

This means that the Excel file is opened using two filters:

* All “No barcode” Entries (which is the code for an empty carrier position) are not shown
* All Entries with “C” in the “Specifier” Column are not shown (this is the carrier barcode)

1. In the “File Open”, the name of the Excel file and all the columns have to be passed. For “File name”, use the variable specified in the header. For “Sheet name”, use “Barcodes1$”. The $ sign is needed to be able to read from the file.
2. Set the “File handle” to “formattedExcel”. Giving a name makes it easier to find and use (e.g. of several files).
3. Set the mode to “File Open to Read”.
4. Then, type in all the columns that appear in the file to be opened. Please note that the column name has to be enclosed in quotation marks. Link this name to a Read/Write variable and set its type. As seen below, all columns are of type String except the “Id”. This one is an integer.
5. Finally, select the variable for the SQL Filter query in the “Command string” Field.\
   \
   ![](<../.gitbook/assets/image (133).png>)\

6. Click \[OK] to close the “File Open” Step.
7. Add a loop and iterate over file1. This means that the loop will be executed until ”formattedExcel” ends.\
   \
   ![](<../.gitbook/assets/image (134).png>)\

8. In the loop, the data is read by a File read from the General Steps using the file handle Excel file1 to include the information in the trace file (C:\programm file\ HAMILTON\LogFiles).\
   \
   ![](<../.gitbook/assets/image (135).png>)\

9.  The Data in line 1 and 3 are in quotation marks. Therefore, they are displayed as text. Line 2 and 4 will show the variable’s value at run time. The result of this will be an entry for each valid barcode, as shown below.\
    \


    <figure><img src="../.gitbook/assets/image (137).png" alt=""><figcaption></figcaption></figure>
10. This is done for each entry in the file that matches the restrictions in the SQL statement.
11. The result of the second part of the method should look like this:\
    ![](<../.gitbook/assets/image (138).png>)
12. The file is closed in step 24.
13. Steps 25 and 26 will delete both the system created BarcodeTextFile and the formatted BarcodeExcelFile. To do this, use the DeleteFile command from the HSLMappingReport library.
14. The newly created local sub-method is now ready.\
    ![](<../.gitbook/assets/image (139).png>)

\


## Using the Sub-Method in the Main Method

This sub-method can be used as the next step in the main method.

1. Select the "Main Method" Tab and drag the “Sub-method” Icon into the main-method.
2. The following dialog opens and the parameter list has to be supplied as shown on the next page.\
   \
   ![](<../.gitbook/assets/image (140).png>)\

3. The sub-method dialog cannot be closed. It will load the carrier “SMP\_CAR\_24\_17x100\_A00\_0001” onto the deck, read the barcodes and display all valid barcodes in the trace file.
4. The sub-method can be used for 24 and 32 tube carriers, MD and AC plate carriers etc. To do this, simply change the carrier’s name in the sub-method call.



<table data-header-hidden><thead><tr><th width="98"></th><th></th></tr></thead><tbody><tr><td><img src="../.gitbook/assets/image (10) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" data-size="original"></td><td><p>NOTE</p><p><em>The system will always show all possible barcodes in simulation mode.</em></p></td></tr></tbody></table>

