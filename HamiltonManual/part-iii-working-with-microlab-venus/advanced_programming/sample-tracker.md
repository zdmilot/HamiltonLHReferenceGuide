# Sample Tracker

The sample tracker is a system to record all actions related to labware and liquids (such as pipetting, moving plates). It can generate a file for each piece of labware on the ML STAR, recording information about its history (pipetting patterns, barcodes, pipetting errors, etc.) during one method.

With this information from the sample tracker, the user can:

* Know what happened on the ML STAR during the runs
* Know, whether the ML STAR did its work correctly or not
* Use the output to link it to a LIMS
* Use the output file for documentation (GLP)

<table data-header-hidden><thead><tr><th width="145"></th><th></th></tr></thead><tbody><tr><td><img src="../../../.gitbook/assets/image (10) (1) (1) (1) (1) (1) (1) (1).png" alt="" data-size="original"></td><td><p>NOTE</p><p>To configure, collect and visualize tracker data, use the Generate Mapping File step from the Data handling step collection.</p></td></tr></tbody></table>

\


Enabling the sample tracker through the System Configuration Editor creates a database where all relevant information will be stored.

To change the settings, click from the “Tools -> System Configuration Editor” Menu.

<figure><img src="../../../.gitbook/assets/image (552).png" alt="" width="563"><figcaption></figcaption></figure>

Mark the “Data Handling Steps” Checkbox when linking the instrument or layout, to be able to use the functions accessing the sample tracker information.

Once the access functions are activated for a method, the group “Data Handling Steps” in the toolbox window of the Method Editor will contain the sample tracker steps.

<figure><img src="../../../.gitbook/assets/image (553).png" alt="" width="464"><figcaption></figcaption></figure>



\


## Data Handling Steps Toolbar‌

\


<table><thead><tr><th width="246">Command</th><th>Icon</th><th>Action Performed</th></tr></thead><tbody><tr><td>Generate Mapping File</td><td><img src="../../../.gitbook/assets/Image_658.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\BtnGenerateMappingFile.bmp"></td><td>Generates a mapping file with information for selected sequence(s).</td></tr><tr><td>Set Labware Barcode</td><td><img src="../../../.gitbook/assets/Image_659.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\BtnSetLabwareBarcode.bmp"></td><td>Set barcode for labware which was or cannot be read by built in reader.</td></tr><tr><td>Remove Labware</td><td><img src="../../../.gitbook/assets/Image_660.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\BtnRemoveLabware.bmp"></td><td>Remove labware data from the database stop generation of mapping information.</td></tr><tr><td>Import Worklist</td><td><img src="../../../.gitbook/assets/Image_661.jpg" alt="image"></td><td>Imports an external worklist into the internal Hamilton database. Works in combination with “Load and Match”.</td></tr><tr><td>Update Job Status</td><td><img src="../../../.gitbook/assets/Image_662.jpg" alt="image"></td><td>Changes the status of a job on the Hamilton database.</td></tr></tbody></table>



## ‌Generating a Mapping File‌

To use this step, select the following:

* instrument
* Sequence over which the data should be generated

The step is able to filter (expand) the stored information by selecting additional sequences in such a way that the additional information is stored which are affected by the sequences.

Define the path and filename where the collected information will be stored. If there is no path specified, it will automatically be stored in the HAMILTON\Logfiles directory by default.

Make sure that the labware is loaded before calling this command.

<figure><img src="../../../.gitbook/assets/image (554).png" alt="" width="563"><figcaption></figcaption></figure>



The “Generate Mapping File” Step collects data regarding the TARGET sequence and “looks” backwards as to what was pipetted into this sequence. Specify “Sequences of interest” to filter the information.

Example: Pipette from a tube carrier into the target plate (red to green). Afterwards, cover the samples in the plate with the reagent (blue to green).

To track both pipetting, both of the source sequences have to be added as “Sequences of interest”.

To link only the barcode of the sample tube to the well ID of the target plate, only add the sample tube sequence to the “Sequences of interest”.



## ‌Customizing the Mapping File‌

The \[Customize] Button offers multiple options to customize the output mapping file. It is possible to:

*   Filter the data by using the status of the sample.\
    \
    ![](<../../../.gitbook/assets/image (585).png>)

    \


    <table data-header-hidden><thead><tr><th width="145"></th><th></th></tr></thead><tbody><tr><td><img src="../../../.gitbook/assets/image (10) (1) (1) (1) (1) (1) (1) (1).png" alt="" data-size="original"></td><td><p>NOTE</p><p>When the aspirate step is mixing the liquid, it will create an entry in the database. To suppress this liquid transfer, check the checkbox “Exclude multiple entries if source is mixed”. Otherwise, at least two lines per sample will be found.</p></td></tr></tbody></table>




*   Sort the data in line wise (A1 – A12) or column wise (A1 – H1).

    \
    ![](<../../../.gitbook/assets/image (587).png>)



    \


    It is possible to link the default column name of the mapping files column to a user defined column name (see lines 2, 4, 8 in the image below). Simply change the name in the right column. Make sure that the quotes are present. Alternatively, variables can be used in the column name fields.\


    ![image](../../../.gitbook/assets/Image\_667.gif)

    \

* To hide columns in the output file, deactivate the checkbox (see lines 3, 5 and 6 in the image above).
* Activating the “Create one file for full sequence of interest” will create one single output file even if the sequence of interest covers more than one labware. Unchecking this box will create a single output file for every labware of the sequence of interest.
* The “Open file to append” will not overwrite an existing file with new data but add the new data to the end of the file.
*   Per default, the output excel file is created in the LogFiles folder (under C:\Program Files\HAMILTON.. -> depending on the language of the operating system). To change this path and the default name of the output file, use the field: “String used to generate the mapping file name(s)”.\
    \


    <figure><img src="../../../.gitbook/assets/image (588).png" alt=""><figcaption></figcaption></figure>



## ‌Set Labware Barcode‌

The step “Set Labware Barcode“ is used for labware that has been positioned on the deck but cannot be identified by the built-in barcode reader.

The labware which the barcode has to be set must be identified either by the LabwareID (created in the Deck Layout Editor) or by the sequence which was defined by the Sequence Editor.

The barcode to be set must either be a constant string or a variable. At run time, an error will be generated if the barcode passed is empty.





## Remove Labware‌

The command “Remove Labware“ removes labware from the access of sample tracking. It is used for the labware which are removed from the deck. After this command has been executed, no more tracking data for the removed labware is accessible.

\


## ‌Import Worklist‌

The import worklist step is used to import an external database. The file format can be in Access, Excel or a structured text. The data in the external worklist can be assigned to the columns of the internal Hamilton database. This allows the use of the imported data within the VENUS Software environment and e.g. use the “Load and Match” Step to connect the loaded barcodes to a previously imported worklist.

\


## Update Job Status‌

This command allows changing the status of a sequence position from 'Assigned' or 'Unprocessed' to ‘Processed’. The update is done on the current position of the given sequence.
