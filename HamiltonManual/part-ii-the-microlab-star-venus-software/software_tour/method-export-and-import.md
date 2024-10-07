# Method Export and Import‌

Exporting and importing methods allow interchanging of methods between different PC’s. Once a method has been created and tested, it can then be packed in a single file with all the relevant information which includes the following:

* Method
* System Deck
* Required Labware
* Required Liquid Classes
* Included Libraries (standard and self-created)

It is also possible to add files to the package that are needed to execute the method but are not part of the Hamilton Software.

Example: an Excel sheet that is read to define the sample volumes.

To do so, select Method -> Dependencies and add all files that shall be part of the export package.

<figure><img src="../../.gitbook/manual-images/assets/image (133).png" alt="" width="272"><figcaption></figcaption></figure>



The advantage of such an export-import transfer is that not all labware, libraries, etc. have to be installed by default on another PC. Such transfer of files ensures that all information will be stored on the target PC when the package is imported.

Exporting methods is also a useful procedure for backing up the methods.

<table data-header-hidden><thead><tr><th width="145"></th><th></th></tr></thead><tbody><tr><td><img src="../../.gitbook/manual-images/assets/image (1) (1) (1).png" alt="" data-size="original"></td><td><p>NOTE</p><p>All data will be compressed, so a complete method can be transferred easily even through e-mail.</p></td></tr></tbody></table>

<details>

<summary>Exporting a Method</summary>

To collect all information used by a method, and to create one package file, follow the steps shown below.

<img src="../../.gitbook/manual-images/assets/image (134).png" alt="" data-size="original">

Choose “File -> Export…” within the method to be transferred. A dialog box will open, requesting for a filename.

![](<../../.gitbook/manual-images/assets/image (135).png>)\




Click the \[…] Button to select the package name including the path desired to export.

Click \[Finish] to complete the operation.

</details>

<details>

<summary>Importing a Method</summary>



The method in a package must be imported once received. To do this, perform the following steps:

1.  Start the “Graphical Method Editor”.

    ![](<../../.gitbook/manual-images/assets/image (136).png>)\

2.  Select among the “File -> Import…” Menu

    ![](<../../.gitbook/manual-images/assets/image (137).png>)\

3. Choose the desired package by clicking on \[…]
4. Once a package is selected, the comment written during the export process will be seen along with the name or path of the package.
5. If the selected package is not the desired one, click \[…] again to select another one.
6.  Click \[Next >] to determine the location in which the package shall be unpacked.

    There are four different possibilities:

    ![](<../../.gitbook/manual-images/assets/image (138).png>)\




    **Recovery:** A useful way to restore a destroyed method. If the method was exported for backup purposes, re-importing it while selecting the recovery option should be used. The same directory structure will be used to extract and store all the necessary files that were collected during the export procedure.\


    **Import into Default Directories:** Useful when data should be stored in the default directories as defined in VENUS Software. An example is by using the labware directory to save labware files.

    Import into Sub-Directories of Default Directories: Similar to the second possibility, however using this option will create sub-directories to the default directories with the names specified. This option guarantees that the existing files having the same names with the new files will not be overwritten.\


    **User-defined:** Gives the most flexibility in selecting the target directories. The next step will ask for a definition of the target directory for all groups of files, method files, library files, labware files and other files.\


    **Import Original Hamilton Files:** If this option is enabled, original Hamilton files are imported to a target environment, otherwise these files are skipped. This could however lead to non-working methods.

    \

7. Click \[Next >] again, to get to a summary of the current directories and, if necessary, further input fields and selection possibilities to change the desired directories. The summary will be updated on an ongoing basis with any changes that have been made.
8. Once the selections correspond to the requirements click \[Finish]. This will unpack and store all of the files.
9. The system imports all necessary files and prompts the dialog below upon completion. Click \[Close] to exit.\
   ![](<../../.gitbook/manual-images/assets/image (139).png>)



</details>

