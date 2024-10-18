# Managing Documents

The SoftMax Pro Software uses two basic document types: protocols and data documents. You save both protocols and data documents just like any other file you save to a computer. Use the Protocols tab in the Ribbon to define which computer system database folders display in the Protocol Library. You should name the folders in a way that allows you to easily find the protocols.

&#x20;Protocols contain the settings that the instrument uses to collect data and the formulas to analyze data. Protocols are useful when you repeat experiments and when you create new documents.

&#x20;Data documents contain the data the software collects when you run the experiment.

Data documents allow you to create reports and graphs from the data you collect.

SoftMax Pro Software - Standard edition version 7.1 (and later) can open documents from version 4.0 or later.

SoftMax Pro Software - GxP edition version 7.1.1 allows you to import documents from version 6.0 or later. You can update documents created in earlier versions to a versions 6 or version 7 document and then import the document into the SoftMax Pro Software - GxP edition database.&#x20;

**Note:** Before you open a document, make sure the instrument you select uses the same settings or compatible settings as the instrument used to create the document.



### Protocols

You can use predefined protocols and you can create your own protocols. Protocols contain plate well layout assignments, reduction parameters, and instrument settings, but no data. Protocols are useful when you want to repeat experiments because they save instrument experiment settings and formulas for reuse.&#x20;

When you open a new document, the settings from the default protocol appear in the Workspace. The default protocol settings help you get started when you create a new document. When you install the software, the Basic Endpoint protocol is set as the default protocol with the file name _default.spr_. Use the  Save As Default icon on the Protocols tab to change the default protocol settings.&#x20;

**Note:** When you save a data document as a protocol, the software creates a new protocol that saves the experiment settings without the data. Any data you collect in the current experiment remains unchanged and is saved with the data document.



The  Protocol Manager icon on the Home tab and on the Protocols tab provides access to the Protocol Library. The Protocol Library contains over 160 protocols that contain instrument settings and formulas. You can customize the protocols in the Protocol Library to facilitate the data analysis and report creation.

Use the  Folder Locations icon on the Protocols tab to add or remove the folders that display in the Protocol Library. This helps you find the protocols you use most often.&#x20;

The  Protocol Home Page icon on the Protocols tab provides access to the SoftMax Pro Software user community where you can share protocols, exchange tips and tricks, and network with other users.

**Protocol File Extensions**

You can open protocols that have the following file extensions.:

&#x20;.spr for SoftMax Pro Software - Standard edition version 6 and 7 protocols.  .sprx for SoftMax Pro Software - GxP edition version 6 and 7.0.x protocols.

&#x20;SoftMax Pro Software - GxP edition version 7.1.1 does not display file extensions for protocols.

### Data Documents

Data documents contain the instrument settings, the raw data the instrument collects, and the completed data analysis.

**Data Document File Extensions**

You can open data documents that have the following file extensions:

&#x20;.sda for SoftMax Pro Software - Standard edition version 6 and 7 data documents.  .sdax for SoftMax Pro Software - GxP edition version 6 and 7.0.x data documents.

&#x20;SoftMax Pro Software - GxP edition version 7.1.1 does not display file extensions for data documents.

When you create a data document for an Imaging mode experiment or a Western Blot experiment, the software creates a folder with the same name as the data document.

**Data Export Formats**

You can export the data to files with the following file extensions: See Exporting Data on page 36.

&#x20;.xml

&#x20;.txt (list)

&#x20;.txt (plate)  .xls (list)

&#x20;.xls (plate)

### Imaging Mode Data Documents

Before you start an image acquisition for an Imaging mode experiment or a Western Blot experiment, you must save the data document in a location with enough capacity for the image files. For best results, save Imaging mode data documents on the secondary hard drive inside the computer. Use of an external hard drive can slow the data acquisition and is not recommended. Use of a USB flash drive or saving to a network location is not supported.

When you create a data document for an Imaging mode experiment or a Western Blot experiment, the software creates a folder with the same name as the data document.

Example: If you save the data document with the name _Imaging\_Data_, the software creates a new folder named _Imaging\_Data_ in the same folder where you save the data document. This folder stores the images and results.

&#x20;Imaging\_Experiments  Imaging\_Data.sda  Imaging\_Data

&#x20;Expt1

&#x20;Plate1

&#x20;IMAGES  RESULTS

The software stores the images separately for each plate in the IMAGES folder in .tiff format. The software stores image analysis data in the RESULTS folder. Western Blot experiments do not create or use the RESULTS folder.

**Note:** Do not rename, move, or delete the related folders or files. If you change the structure of these files and folders, the software may not be able to open the data document or might display inaccurate results.



Use the  Application menu to copy or delete data documents, image files, and analysis data files.

To delete the images or the analysis data for an Imaging mode experiment:

1. In the Navigation Tree right-click the Plate section.
2. Select **Delete Images** or **Delete Cell Data**.

If you delete the .tiff file for a Western Blot experiment, the software recreates the .tiff image from the intensity data stored in the data document.

**Note:** When you save an Imaging mode data document as a protocol, the software saves only the settings and does not create other folders or files.



Acquisition of images in Imaging read mode requires significant computer memory and resources.

Each image file for an Imaging mode experiment can be larger than 2 megabytes. When you acquire the image of a single site in each well of a 96-well plate you can generate 300 megabytes of image data. A 384-well plate can generate 1 gigabyte of image data. When you acquire images of multiple sites, you increase the data storage requirement.

Before you start an Imaging read mode experiment, turn off all other programs to minimize the demands on computer memory and resources. When the software has limited access to computer memory and resources, image acquisition can take a long time. In some cases, images of some of the wells can be lost. See Optimizing the Computer for Image Acquisition on page 178.

For Imaging mode experiments, save the data to a .txt file format. If you use Auto Export to export multiple Imaging mode data documents, the software exports each new data document without the folders required to save images and results. See Auto Export on page 23.

### Creating Protocols and Data Documents <a href="#bookmark2" id="bookmark2"></a>

Use the Quick Access toolbar and the  Application menu to create a new document that you can save as a protocol or data document. The Protocol Library contains protocols that you can use to create a new protocol or data document.

To create a document:

**Note:** You should save and name the protocol before you collect data. For the SoftMax Pro Software - GxP edition, you must save the document before you can proceed. See Saving Protocols and Data Documents on page 22.



&#x20;For the SoftMax Pro Software - Standard edition, select **Protocol Files (\*.spr)** to save the settings with no data as a protocol.

&#x20;For the SoftMax Pro Software - Standard edition, select **Data Files (\*.sda)** to save the settings with no data as a data document.

&#x20;For the SoftMax Pro Software - GxP edition, select **Protocol Documents** to save the settings with no data as a protocol.

&#x20;For the SoftMax Pro Software - GxP edition, select **Data Documents** to save the settings with no data as a data document.

\*Can be done at any point in the process, before or after the initial read.

### Opening Protocols and Data Documents <a href="#bookmark3" id="bookmark3"></a>

Use the Quick Access toolbar and the  Application menu to open documents. The Protocol Library contains protocols you can use to create a new protocol or a blank data document.

The SoftMax Pro Software - Standard edition can open documents created by version 4.0 or later. When you open a document from an earlier version, the software converts it to the SoftMax Pro Software version 7.x format. After you save a document, only the current software version can open the new document.

The SoftMax Pro Software - GxP edition requires a few additional steps if you want to use documents that are from version 5 or earlier. See Importing Legacy Documents on page 42.

**Note:** Each instrument has different settings. Before you open a document, verify that the instrument used to create the document is the same as the instrument you select on the Home tab. Some instruments have incompatible settings.



To open documents:

1. Click  in the Quick Access toolbar or click  to open the Application menu and Select  **Open** to display the Open dialog.
2. Click the Data Files (\*.sda) drop-down (SoftMax Pro Software - Standard edition) or the **Open Type** drop-down (SoftMax Pro Software - GxP edition). SoftMax Pro Software - GxP edition version 7.1.1 documents do not display the file extension.

&#x20;For SoftMax Pro Software - Standard edition, select **Protocol Files (\*.spr)** to open a protocol with an .spr file extension.

&#x20;For SoftMax Pro Software - Standard edition, select **Data Files (\*.sda)** to open a data document with an .sda file extension.

&#x20;For SoftMax Pro Software - GxP edition, select **Protocol Documents** to open a version 7.1.1 protocol.

&#x20;For SoftMax Pro Software - GxP edition, select **Data Documents** to open a version

7.1.1 data document.

1. Navigate to the document and select it.
2. Click **Open**. A new Document tab displays above the Workspace with the document name.
3. Before you use a protocol to collect data, you should save it as a data document.

### Saving Protocols and Data Documents <a href="#bookmark4" id="bookmark4"></a>

Use the Quick Access toolbar and the  Application menu to save documents. Before you use a protocol, you should save the protocol as a data document. For the SoftMax Pro Software - GxP edition, use auto save settings to automatically save the document. See Auto Save on page 26.

To save documents:

*
  1. Select one of the following:

&#x20;Click  in the Quick Access toolbar or click  to open the Applications menu and select **Save** to save the open document with updated information in the same location with the same name.

&#x20;Click  in the Quick Access toolbar or click  to open the Applications menu and select **Save As** to rename a document, to save a protocol as a data document, to save a data document as a protocol, to move a document to a different location, or to give a new document a name. The Save As dialog displays.

&#x20;Click  to open the Applications menu and select **Save As PDF** to save the document in a .pdf format. See Saving Data as a PDF on page 32.

*
  1. For Save As, in the Save As dialog, navigate to where you want to save the document.
  2. In the **File Name** field, enter the document name.
  3. Click the **Save As Type** drop-down.

&#x20;For the SoftMax Pro Software - Standard edition, select **Protocol Files (\*.spr)** to save the document as a protocol.

&#x20;For the SoftMax Pro Software - Standard edition, select **Data Files (\*.sda)** to save the document as a data document.

&#x20;For the SoftMax Pro Software - GxP edition, select **Protocol Documents** to save the document as a protocol.

&#x20;For the SoftMax Pro Software - GxP edition, select **Data Documents** to save the document as a data document.

*
  1. Click **Save**.

### Auto Export <a href="#bookmark5" id="bookmark5"></a>

Use the Auto Export dialog to define how and where the software is to automatically export data immediately after each plate read completes. Auto export reduces the likelihood of lost data, particularly when you choose to export documents to corporate network file locations that are backed up on a regular basis. You can define multiple auto export instances. The software saves auto export settings with each document.

This feature helps prevent data loss when you do automated reads, such as with the StakMax Microplate Handling System.

For Imaging mode experiments, export the data to a .txt file format. If you use auto export to export multiple Imaging mode data documents, the software exports each new data document without the folders required to save images and results.

To automatically export a document:

1. Open the protocol or data document to export.
2. Click  to open the Application menu and select  **Auto Export** to display the Auto Export dialog.
3. Select the **Save Data After Read** check box to use auto export.
4. Click **Add** or select a document in the list and click **Edit** to display the Auto Export Properties dialog.

**Note:** Auto export properties settings are specific to the new export location or the export location you select to edit from the Auto Export dialog. Use this to customize the settings for each location to which you use auto export.



1. Select a **File Location** option.

&#x20;Select **Protocol's Folder** to export documents back to the folder that contains the originating document.

&#x20;Select **Assigned Folder** to export documents to a folder to which the computer has access. Click **Browse** to display the Browse For Folder dialog. Navigate to the folder or click **Make New Folder** to create a new folder where you want to export the document.

1. Select a **File Name** option.

&#x20;Select **Protocol's Name** to name the document with the protocol name.

&#x20;Select **Assigned Name** to assign a name to the document. In the text field, enter the name for the document. The text in this field is inserted at the start of each document name.

1. Click the **File Format** drop-down and select a file format.

&#x20;Select **.sda** or **.sdax** to export the file as a data document.

&#x20;Select **.xml** to export the file in .xml format. You should use the .xml format if you plan to import read data into other data collection and storage applications, specifically, LIMS (Laboratory Information Management System) or SDMS (Scientific Data Management System) packages.

&#x20;Select **.txt (list)** or **.txt (plate)** to export the document as a tab delimited text file that most word processor, spreadsheet, or database programs can open.

&#x20;Select **.xls (list)** or **.xls (plate)** to export the document in a format that Microsoft Excel can open. The Excel output has the same format as a tab delimited file with an

.xls file extension.

1. **Save Options**: The available save options depend on the file format you select.
2. Select an **Export Data** option.

&#x20;Select **Raw** to export only the raw data.

&#x20;Select **Reduced** to export only the reduced data.

&#x20;Select **Both** to export both the raw and the reduced data in the same file.

1. Select one of the following:

&#x20;Select **Create a New File** to create a new document after each read. When you select this option and do not select either of the following check boxes, the software numbers documents with the same name sequentially. For example, _Data 1_, _Data 2_, and so on.

&#x20;Select the **Append Date to File Name** check box to add the date after the document name. If you select to append only the date to the document name, the software indexes the runs for that day starting with _1_ and increments with each successive run. For example, the software names the first document named _Data_ that you export on January 22nd, 2019 _Data-01-22-19 1_ and names the second document you export _Data-01-22-19 2_, and so on.

&#x20;Select the **Append Time to File Name** check box to add the time after the document name.

If you select both the date and the time, the time follows the date.

&#x20;Select **Overwrite Existing File** to overwrite an existing document for each read. Use this carefully because this can cause data loss. A document can overwrite only itself. If a different document with the same name exists in the save file location, the software appends a number to the end of the document name.

1. Select **Append to File** to append the data from multiple plates into one document. Enter the maximum number of plates to append per document. This option is available when you select either the .txt or .xls format.

**Tip:** If you use the StakMax Microplate Handling System to read 10 plates, use this option to export the data from all 10 plates in a single document.



1. After you define each document name and location, click **OK**.

### Auto Save <a href="#bookmark6" id="bookmark6"></a>

For the SoftMax Pro Software - GxP edition, use the Auto Save dialog to define how and where the software is to automatically save data immediately after each plate read completes. Auto save reduces the likelihood of lost data, particularly when you choose to save documents to corporate network file locations that are backed up on a regular basis. Auto save settings are saved with each document.

To automatically save a document:



**Note:** If you select both check boxes, the time follows the date.

### Printing

Use the  Application menu to print the contents of the document that is open in the Workspace. You can print all sections or select the sections to print. You can preview the print out before you print and you can define the page header, footer, and print quality options.

### Print Options

Before you print, you can add a logo image, and define the header, footer, and print quality in the Printing Options dialog.

Click  to open the Application menu, click  **Print**, and then select  **Printing Options** to display the Printing Options dialog.

### Print

The Application menu provides several ways to print the document content. You can click a section in the Navigation Tree and click  to have a section not print or you can select the sections to print from the Application menu.

To print a document:

1. Open the protocol or data document to print.
2. Click  to open the Application menu.
3. Click  **Print** and select an option:

&#x20;Select  **Print All** to print all the included sections in the document. The Print dialog displays.

&#x20;Select  **Print Preview** to display the Print Preview dialog where you preview the print job before you print.

&#x20;Select  **Print Selected** to display the Print Selected dialog where you select the sections to print.

&#x20;Select  **Printing Options** to display the Printing Options dialog where you define the header and footer of the pages and the print quality for the print job.

1. In the Print dialog, select the printer to use and set the print settings, including the number of copies to print. To print to a .pdf file, select the **Molecular Devices (PDF Writer)** or open the Application menu and select  **Save As PDF**.

### Previewing Print Jobs <a href="#bookmark7" id="bookmark7"></a>

Use the Print Preview dialog to preview the print job before you print. Use the Print Options dialog to add a header, footer, and logo image.&#x20;

To preview the printed output:

To print to a .pdf file, select the **Molecular Devices (PDF Writer)**.&#x20;

*
  1. Click **Print**.

### Printing Select Sections <a href="#bookmark8" id="bookmark8"></a>

Use the Print Selected dialog to select the sections of the document to print. Use the Print Options dialog to add a header, footer, and logo image.

To print select sections of a document:

1. Open the protocol or data document to print.
2. Click  to open the Application menu, click  **Print**, and then select  **Print Selected** to display the Print Selected dialog.
3. Select the check box for each section to print. Clear the check box for each section to not print.

&#x20;To select all the check boxes, click **Select All**.  To clear all the check boxes, click **Deselect All**.

&#x20;To preview the print job before you print, click **Print Preview**.

1. Click **Print** to display the Print dialog.
2. Select the printer to use and set the print settings, including the number of copies to print.

To print to a .pdf file, select the **Molecular Devices (PDF Writer)**.

1. Click **Print**.

### Printing Options

Use the Printing Options dialog to define the contents of the header and footer and the quality of the printed output.

To define printing options:

1. Open the protocol or data document to print.
2. Click  to open the Application menu, click  **Print**, and then select  **Printing Options** to display the Printing Options dialog.
3. Define the page header:

&#x20;Select the **Experiment Name** check box to include the experiment name in the header.

&#x20;Enter text in the **Left**, **Center**, and **Right** text fields.

&#x20;Select the **Add Image** check box and click the **Browse** button to locate and select an image file (.jpg format). The software sizes the image to fit in the upper-right area of the page.

1. Define the page footer:

&#x20;Select the **File Path and Name** check box to include the document name and path in the printout.

&#x20;Select the **Date and Time** check box to include the date and time.

&#x20;Select the **SoftMax Pro** check box to include the version of the SoftMax Pro Software.

&#x20;Select the **Page Number** check box to include page numbers.

1. Drag the **Print Quality** slider to adjust the print quality.
2. Click **OK**.

### Saving Data as a PDF <a href="#bookmark10" id="bookmark10"></a>

You can save the contents of a document in .pfd format. Before you save the .pdf file, you can define the header and footer of the pages and the print quality in the Printing Options dialog and predefine the sections that you want to exclude from the .pfd file in the Navigation Tree.

To define .pdf settings:

Click  to open the Application menu and select  **Save As PDF**. You can also select the

**Molecular Devices (PDF Writer)** in the Print dialog.

The following tables define the settings for each of the tabs in the Molecular Devices (PDF Writer) - Create File dialog:

**General Tab**

| **Option**                             | **Description**                                                                                                               |
| -------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------- |
| Option Set                             | Select a pre-defined set of .pdf settings from this list. To define a new set, select \<Edit>.                                |
| Format                                 | To create a .pdf file, select .pdf from this list. You can also select from this list to create output in image file formats. |
| File Name                              | Enter the file name in the path or click  to browse for a folder and name the file.                                           |
| Append if output exists                | Select this check box to append this file to an existing file instead of overwriting an existing file.                        |
| Open destination folder after creation | Select this check box to open the folder where the file is saved after the file saves.                                        |
| Open the document after creation       | Select this check box to open the file after the file saves.                                                                  |

**Document Tab**

| **Option**          | **Description**                                                                                                                            |
| ------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| Author              | Enter the name of the author in this field to display in the document properties.                                                          |
| Title               | Enter the title of the document in this field to display in the document properties.                                                       |
| Subject             | Enter the subject of the document in this field to display in the document properties.                                                     |
| Keywords            | Enter keywords for the document in this field to display in the document properties.                                                       |
| Quality             | Select a quality to define the size of the .pdf file.                                                                                      |
| Initial zoom level  | Select a zoom level to define how the document displays each time it opens.                                                                |
| Compatibility Level | Select a format to make the .pdf file compatible with older versions of PDF readers. Some options might not be supported in older version. |
| PDF/A-1b            | Select this check box to use the .pdf/A-1b archiving standard.                                                                             |

**Image Tab**

| **Option**      | **Description**                                                                                 |
| --------------- | ----------------------------------------------------------------------------------------------- |
| DPI             | When you create an image file, select the resolution for the image in dots per inch.            |
| Text Alpha Bits | When you create an image file, select the number of bits to use for the alpha channel for text. |

**Watermark Tab**

| **Option**            | **Description**                                                                                                                                              |
| --------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Text                  | Enter the text to display in the watermark.                                                                                                                  |
| Font                  | Select the typeface for the watermark.                                                                                                                       |
| Color                 | Click  to select the color for the text.                                                                                                                     |
| Size                  | Enter the size of the text in points.                                                                                                                        |
| Outline width         | Enter the width of the text outline in pixels to have the text display in outlines. To have the text display as a solid color, leave this field blank.       |
| Layer                 | To have the watermark text display on top of the document text, select Stamp. To have the watermark text display behind the document text, select Watermark. |
| Rotation              | Select to display the text upward from the lower left corner or downward from the upper left corner.                                                         |
| Vertical position     | Select to display the text on the top, center, or bottom of the document.                                                                                    |
| Vertical adjustment   | Enter a percentage offset for the vertical watermark position.                                                                                               |
| Horizontal position   | Select to display the text on the left, center, or right of the document.                                                                                    |
| Horizontal adjustment | Enter a percentage offset for the horizontal watermark position.                                                                                             |

**Merge Tab**

| **Option**     | **Description**                                                                                                                                    |
| -------------- | -------------------------------------------------------------------------------------------------------------------------------------------------- |
| Append PDF     | Enter the name of the file to which to append this file. To browse for the file, click .                                                           |
| Position       | To append the new file to the end of the old file, select Bottom. To append the new file to the start of the old file, select Top.                 |
| Background PDF | To print the data on an existing file, enter the file name in this field. Use this to print on company letterhead. To browse for the file, click . |
| Layer          | To have the new file display on top of the old file, select Stamp. To have the new file display behind the old file, select Watermark.             |

**Security Tab**

| **Option**        | **Description**                                                                    |
| ----------------- | ---------------------------------------------------------------------------------- |
| Owner password    | Enter the password that gives owner permissions for the file.                      |
| User password     | Enter the password that gives user permissions for the file.                       |
| Key Length        | Select the length of the key to use for document encryption.                       |
| Set Permissions   | Select this check box to limit access to the document for the user level.          |
| Print             | Select whether to permit printing and the print quality to permit.                 |
| Copy to clipboard | Select this check box to permit users to copy text from the file to the clipboard. |

### Exporting Data <a href="#bookmark11" id="bookmark11"></a>

Use the Export dialog to export data to a .xml, .xls, or .txt format. The software exports data values with the maximum floating point arithmetic precision, regardless of the display settings you define.

**Note:** For instructions to export membrane data, see Viewing Western Blot Membrane Data on page 241 and for instructions to export Imaging data to Microsoft Excel or PowerPoint see Viewing Imaging Data in Wells on page 207.



To export data:

1. Open the data document that contains the data to export.
2. Click  to open the Application menu, click **Export**, and then select  **Export to XML XLS TXT** to display the Export dialog.
3. Select the following:

&#x20;Select the **All Plates** check box to export all Plate section data.

&#x20;Select the **All Groups** check box to export all Group section data.  Select the **All Notes** check box to export all Note section data.

&#x20;Select the check box for each section to export.

&#x20;Clear the check box for each section to not export.

1. If you select to export Plate section data, select a **Plate Data Option**:  Select **Raw** to export only the raw data.

&#x20;Select **Reduced** to export only the reduced data.

&#x20;Select **Both** to export both the raw and the reduced data in the same file.



**Note:** These options apply only to Plate sections.

1. Select an **Output Format** option:

&#x20;Select **Columns** to export data in a single column of text for each well.

&#x20;Select **Plate** to export data in a text matrix that corresponds to a plate grid.  Select **XML** to export data in an .xml format.



**Note:** These options apply only to Plate sections.

1. Click **OK** to display the Save As dialog.
2. Navigate to the folder where you want to save the data.
3. In the **File Name** field, enter the export file name.
4. Click the **Save As Type** drop-down and select the file type for the export file.

&#x20;If you select the XML Output Format, the only option is **.xml**. For a copy of the SoftMax Pro .xml schema, contact Molecular Devices.

&#x20;For details about the format and content of the .txt and .xls format export file, see Exporting File Details on page 356

1. Click **Save**.

### Importing Data

Use the  Application menu to import data into the software. Click  to open the Application menu, click **Import**:

&#x20;Select **Plate Format** to import tab delimited text data into a Plate section. See Importing Data in Plate Format on page 39.

&#x20;Select **XML Format** to import .xml data into a Plate section. See Importing Data in XML Format on page 41.

&#x20;Select **Import Legacy Files** to import SoftMax Pro Software - GxP edition version 6 and 7 documents into the SoftMax Pro Software - GxP edition version 7.1.1 database. See Importing Legacy Documents on page 42.

**Note:** The import data in Plate format feature and the import data in the .xml format feature require separate licenses. To obtain a license for the Plate format data import feature and the .xml format data import feature, contact Molecular Devices.



The software installation includes templates to import data in the Plate format and a schema to import data in the .xml format.

When you import plate data, the software creates a new Plate section with the section name from the import file. If the Plate section name already exists, then the import data overwrites the existing data in the section. See Plate Sections on page 76.

When you import plate data into an existing Plate section, the software preserves the template and reduction settings in the existing Plate section if the data you import data is compatible with the settings in the existing section.

To preserve the template and reduction settings, the name of the Plate section in the source file must match the name of the Plate section in the destination file. If the names do not match, the software creates a new Plate section.

Another way to preserve template and reduction settings is to copy the import data from the new Plate section and then paste the data into an existing Plate section to use the template and reduction settings in the section where you paste the data.

**Note:** To maximize the number of data points the software uses for reduction, the end time reduction parameter changes to match the read time from the import file.



### Importing Data in Plate Format <a href="#bookmark12" id="bookmark12"></a>

Use the  Application menu to import data in the Plate format.

Before you can import plate data that you export in the Plate format from SoftMax Pro Software version 5.x and 6.x or that you acquire from a different software program, you must first use that software program to export the data into a format that is compatible with the SoftMax Pro Software version 7.1.1. The SoftMax Pro Software installation includes templates to import data in the Plate format.

To import data in the plate format:

1. Open or create a new protocol.
2. Define a Plate section into which to import the plate data. Name the Plate section with the same name as the Plate section in the import file.
3. Click  to open the Application menu.
4. Click **Import** and select  **Plate Format** to import tab delimited text data.
5. In the Open dialog, navigate to and select the file to import.
6. Click **Open** to import the data. The Plate sections display the imported data.
7. Save the file.

After you import the data into the Plate sections, the Read Information area on the right indicates that the data was imported and shows the time and date of the import. For the SoftMax Pro Software - GxP edition, the Read Information includes the name of the user who imported the data.

### More Information

Import templates are in a sub-folder of the Program Files folder where the SoftMax Pro Software is installed. The default installation path is:

C:\Program Files (x86)\Molecular Devices\SoftMax Pro 7.1.1\Plugins\Import-PlateFormat\Templates

The templates have the .xlsx format, but you must save the file in the .txt format with tab- separated values before you import the data.

The cells in the template are color-coded.

| **Background Color** | **Description**                  |
| -------------------- | -------------------------------- |
| White                | Do not alter cell.               |
| Green                | Cell requires information entry. |
| Light Yellow         | Cell information entry optional. |

You can paste your data directly into the template or use the template as a model for a script that converts your data to the acceptable format for import.

### Plate Data Layout

The first line of an import template defines the number of Plate sections (or "Blocks") that are included in the document.

&#x20;\##BLOCKS= 1

Each Plate section has the following format:

&#x20;Header lines

The first header line contains descriptive titles for the data in the second header line. The second header line contains the type of section, Plate, and the title to be given to the Plate section in the document.

The fields in the header lines define the type of read, the number of wells in the plate, and the wavelengths used for the read, among other relevant information. The layout and format of the header lines are dependent on the read type. For more information, see the template for the read type of your data.

&#x20;Data lines

The data lines follow the header lines with a blank row between the header lines and data lines. The layout and format of the data lines are dependent on the read mode and read type.

&#x20;The first column shows the time points for a kinetic read, the data points in a well scan read, or the wavelengths in a spectrum read. For endpoint reads, this column is blank.

&#x20;The second column shows the temperature for the read, if an incubator is used for the read. If the incubator is off, the value is zero.

&#x20;The third column is where the read data starts.

The data displays in a table to indicate the columns and rows of the plate used for the read. The data for multiple time points for kinetic reads, multiple data points for well scan reads, or multiple wavelengths for spectrum reads is listed in separate tables below the previous table. For endpoint, kinetic, or well scan reads with multiple wavelengths, the data for each wavelength displays in separate tables to the right of the previous table.

**wavelength 1 wavelength 2**

Temperature

| 1     | 2     | 3     | **…** |
| ----- | ----- | ----- | ----- |
| 1.596 | 2.479 | 2.95  | **…** |
| 1.024 | 0.308 | 3.925 | **…** |
| 0.195 | 0.287 | 2.638 | **…** |
| **…** | **…** | **…** | **…** |

| 1     | 2     | 3     | **…** |
| ----- | ----- | ----- | ----- |
| 3.103 | 1.39  | 1.97  | **…** |
| 2.381 | 1.957 | 3.722 | **…** |
| 0.967 | 1.049 | 1.422 | **…** |
| **…** | **…** | **…** | **…** |

0:00:00 ##

0:01:58 ##

| 1.564 | 3.344 | 2.378 | **…** |
| ----- | ----- | ----- | ----- |
| 0.82  | 1.797 | 1.064 | **…** |
| 0.421 | 3.066 | 3.906 | **…** |
| **…** | **…** | **…** | **…** |

| 0.113 | 3.872 | 0.637 | **…** |
| ----- | ----- | ----- | ----- |
| 3.58  | 2.603 | 0.996 | **…** |
| 0.915 | 0.57  | 2.251 | **…** |
| **…** | **…** | **…** | **…** |

**…** ##

| 1.169 | 1.092 | 3.969 | **…** |
| ----- | ----- | ----- | ----- |
| 1.105 | 3.022 | 2.845 | **…** |
| 3.602 | 2.033 | 3.737 | **…** |
| **…** | **…** | **…** | **…** |

| 1.126 | 0.004 | 1.934 | **…** |
| ----- | ----- | ----- | ----- |
| 1.933 | 2.834 | 0.657 | **…** |
| 0.437 | 3.242 | 1.337 | **…** |
| **…** | **…** | **…** | **…** |

&#x20;End line

The end line follows the data lines with a blank row between the data lines and end line. The end line of each Plate section is defined by the text: **\~End**

To import data from more than one Plate section in a single text file, include the header lines, the data lines, and the end line for each Plate section after the end line of the previous Plate section.

The final line of an import file contains a single field with the original name given to the import file, and the date and time that the file was saved. This information follows the endline for the last Plate section in the file.

### Importing Data in XML Format

Use the  Application menu to import data in the .xml format.

To import data in .xml format, you must use the SoftMax Pro Software .xml schema from software version 6.4.1 or later to format the .xml file.

To import data in .xml format:

1. Open or create a new protocol.
2. Define a Plate section into which to import the plate data. Name the Plate section with the same name as the Plate section in the import file.
3. Click  to open the Application menu.
4. Click **Import** and select  **XML Format** to import .xml data.
5. In the Open dialog, navigate to and select the file to import.
6. Click **Open** to import the data. The Plate sections display the data you import.
7. Save the file.

After the data imports into the Plate sections, the Read Information area on the right indicates that the data was imported and shows the time and date of the import. For the SoftMax Pro Software - GxP edition, the Read Information includes the name of the user who imported the data.

### More Information

Before you can import plate data that you acquire from a different software program, you must first use that software program to export the data into a compatible format. The SoftMax Pro Software installation includes templates to import data in a schema for the .xml format.

The .xml schema file for data import (XMLImportSchema.xsd) is in a sub-folder of the Program Files folder where the SoftMax Pro Software program is installed. The default installation path is:

C:\Program Files (x86)\Molecular Devices\SoftMax Pro 7.1.1\Plugins\Import-XML\Schema

For information about the .xml elements and their usages, see the comments in the schema file.

To import data from more than one Plate section in a single .xml file, make sure that all the Plate sections are between the \<PlateSections> tags and you define each Plate section between a set of \<PlateSection> tags.

\<PlateSections>

\<PlateSection>

\[Data from the first Plate section]

\</PlateSection>

\<PlateSection>

\[Data from the second Plate section]

\</PlateSection>

\</PlateSections>

### Importing Legacy Documents

### Import SoftMax Pro Software - Standard Edition Version 4 and 5 Documents

The SoftMax Pro Software - Standard edition version 7.1 can open documents created by version 4.0 or later. To open documents created in a version earlier than version 4.0, you must first open the document in the SoftMax Pro Software 4.0 or later, and then save it as a version 4.0 or later document. The document must also meet instrument compatibility requirements.

To use a document from an earlier version of the SoftMax Pro Software, save the document with a different name or in a different location after you open the document with the current version.

After you open a document from an earlier version, review the document to make sure the conversion went well. The document conversion might change instrument settings, curve fits, or other items that have been updated for version 7.1.

Legacy documents have the following file extensions.

&#x20;.ppr for SoftMax Pro Software - Standard edition 4 and 5 protocols

&#x20;.pda for SoftMax Pro Software - Standard edition 4 and 5 data documents  .epr for SoftMax Pro Software - GxP edition 4 and 5 protocols

&#x20;.eda for SoftMax Pro Software - GxP edition 4 and 5 data documents

### Import Documents Into the SoftMax Pro Software - GxP Edition Database

For SoftMax Pro Software - GxP edition version 7.1.1 additional steps are required to import the document into the database. Use the Import Legacy Files dialog to import SoftMax Pro Software - GxP edition version 6.x and 7.0.x protocols and data documents into the SoftMax Pro Software - GxP edition version 7.1.1 database. Documents in the SoftMax Pro Software - GxP edition version 7.1.1 database do not display file extensions.

When you log on to the SoftMax Pro Software - GxP edition, you select a Project. The Import Legacy Files dialog displays only folders for that Project. To import documents into the folders for a different Project, you must log out and then select the different Project when you log back on.

**Note:** You cannot edit the documents you import into the SoftMax Pro Software - GxP edition version 7.1.1 database. If you choose to do anything with the document after you import it, you must open the document and use Save As to make a copy of the document.



To import legacy documents:

1. Click  to open the Application menu.
2. Click **Import** and select **Import Legacy Files** to display the Import Legacy Files dialog.
3. Select an **Import** option:

&#x20;Select **Single File** to import one document.

&#x20;Select **Files In Selected Folder** to import all the documents in the folder you select. If you select this option an additional check box displays.

Select the **Include Subfolders and Import Whole Folder Structure** check box to import all documents in the folder you select plus all documents in any subordinate folders. This copies the folder structure and all documents to the folder hierarchy for the Project you selected when you logged in.

1. Click the **File Type** drop-down:

&#x20;Select **SMP 6 & 7 Data (\*.sda)** to import SoftMax Pro Software - Standard edition data documents.

&#x20;Select **SMP 6 & 7 Protocol (\*.spr)** to import SoftMax Pro Software - Standard edition protocols.

&#x20;Select **SMP 6 & 7 Data (\*.sdax)** to import SoftMax Pro Software - GxP edition data documents.

&#x20;Select **SMP 6 & 7 Protocol Files (\*.sprx)** to import SoftMax Pro Software - GxP edition protocols.

1. Next to the **Selected Folder** field, click **Browse** to display either the Open dialog or the Select Folder dialog. The path displays in the Selected Folder field. The path and the file name can have a maximum of 256 characters.
2. Navigate to and select the document or folder to import and click **Open** or **Select Folder**

to return to the Import Legacy Files dialog.

1. In the **Files To Be Imported** field, select the documents you do not want to import and click **Remove** to remove the documents from the list.
2. Next to the **Destination Folder** field, click **Browse** to display the Select Folder for Import dialog.
3. Select the folder into which to import the documents and click **OK** to return to the Import Legacy Files dialog. The path displays in the Destination Folder field. The path and the file name can have a maximum of 256 characters.

**Note:** The path (including the file name) can have a maximum of 256 characters. The file name (without the path) can have a maximum of 50 characters. The file name cannot contain the following characters: < > | : \* ? \ /



1. Select the **Create Copy If Document Exists In Database** check box to create a new document in the database if a document with the same name exists. Leave this check box clear to prevent the software from importing duplicate documents. The import does not overwrite a document.
2. Click **Import** to import the documents. The List of Files dialog displays to indicate the status of the import.
3. In the Import List of Files dialog, click **Close** to finish the import.

### Application Options <a href="#bookmark15" id="bookmark15"></a>

Use the SoftMax Pro Options dialog to define application level preference options that affect documents holistically.

Click  to open the Application menu, and then click the **Options** button at the bottom of the menu to display the SoftMax Pro Options dialog.

The SoftMax Pro Options dialog contains settings for the following options:

&#x20;**Data Recovery** - The **Save Opened Files For Data Recovery Every 5 Minutes** check box is selected by default. The software saves unsaved documents to a temporary file every five minutes to assist with data recovery. If the software experiences an unexpected interruption, when the software restarts, the Document Recovery dialog displays the list of the documents that can be recovered. Recovered documents are saved to C:\Users\\\<windows user>\Documents\SMP\<nn>. You cannot turn this option off.

&#x20;**Web Browser** - Select the **Do Not Display the Web Browser (What’s New Website) On Startup** check box to stop the display of the What's New page of the Molecular Devices web site every time you start the software. This used to be the What's New tab that appeared in previous versions of the software. You can view the What's New page from the Help tab in the Ribbon.&#x20;

**Plate Setup Helper** - Select the **Disable Auto Opening of Helper On New Protocol** check box to prevent the display of the Plate Setup Helper dialog when you open a new document.&#x20;

**Plate Height Warning** - Select the **Disable Plate Height Warning On Protocol Run** check box to prevent the display of the plate height warning when you start a read. To prevent damage to the SpectraMax i3, i3x, iD3, iD5, Paradigm, and FilterMax F3 and F5 the plate height warning displays as a reminder to make sure that you correctly define the plate height.&#x20;

**Plate Eject After Read** - Select the **Plate Remains Inside Instrument After Completion of Read** to have the plate drawer remain closed after a read completes. Leave this check box clear to have the plate drawer open after a read completes.

**Remote Control** - Select the **Enable Remote Control** check box to use an Apple mobile device to control the software. If you select this option, download the SoftMax Pro Remote app from the Apple App Store. Verify that both the app and the software use the same Port. Enter the Host Name or IP address of the computer into the app settings.

**Calculation** -

&#x20;Select the **Calculate During Acquisition** check box to have the software perform data calculations of the kinetic data while a kinetic acquisition is in progress. In the **Calculate Every Cycles** field, enter the number of kinetic reads between successive calculations. This option allows for the fact that calculations may take any amount of time, depending on the complexity of the protocol and the speed of the computer.

&#x20;Select the **Legacy Rounding** check box to improve consistency with the SoftMax Pro Software version 5. This introduces a small factor to force rounding upward.

**SpectraMax iDx Control** - When you use the SpectraMax iD3 and SpectraMax iD5, select the **Enable Control of SpectraMax iDx Instruments** check box to use the software to connect to a specific IP address. If the Instrument Connection dialog does not detect the instrument automatically, enter the IP address of the instrument. You can enter up to five different IP addresses to connect the computer to multiple instruments on your network. To find the instrument IP address, on the instrument touchscreen touch **Maintenance** > **System Information**.&#x20;
