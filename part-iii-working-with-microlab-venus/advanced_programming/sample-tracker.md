# Sample Tracker

_The sample tracker is a system to record all actions related to labware and liquids (such as pipetting, moving plates). It can generate a file for each piece of labware on the ML STAR, recording information about its history (pipetting patterns, barcodes, pipetting errors, etc.) during one method._

_With this information from the sample tracker, the user can:_

* _Know what happened on the ML STAR during the runs_
* _Know, whether the ML STAR did its work correctly or not_
* _Use the output to link it to a LIMS_
* _Use the output file for documentation (GLP)_

\


![Originalbild anzeigen](../../.gitbook/assets/Image\_655.gif)

_NOTE_

_To configure, collect and visualize tracker data, use the Generate Mapping File step from the Data handling step collection._

\


_Enabling the sample tracker through the System Configuration Editor creates a database where all relevant information will be stored._

_To change the settings, click from the “Tools  System Configuration Editor” Menu._

\


![image](../../.gitbook/assets/Image\_656.png)

\


_Mark the “Data Handling Steps_[_” Checkbox when linking the instrument or layout, to be able to use the functions accessing the sample tracker information (see_ ](sample-tracker.md#bookmark180)[_Section 7.2 Linking a Deck to_ ](sample-tracker.md#bookmark180)_a_[ ](sample-tracker.md#bookmark180)_Method)._

_Once the access functions are activated for a method, the group “Data Handling Steps” in the toolbox window of the Method Editor will contain the sample tracker steps._

\


![image](../../.gitbook/assets/Image\_657.jpg)

\


1.  #### _‌Data Handling Steps Toolbar‌_

    \


    <table data-header-hidden><thead><tr><th width="382"></th><th></th><th></th></tr></thead><tbody><tr><td>Command</td><td>Icon</td><td>Action Performed</td></tr><tr><td>Generate Mapping File</td><td><p><br></p><p><img src="../../.gitbook/assets/Image_658.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\BtnGenerateMappingFile.bmp"></p></td><td>Generates a mapping file with information for selected sequence(s).</td></tr><tr><td>Set Labware Barcode</td><td><p><br></p><p><img src="../../.gitbook/assets/Image_659.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\BtnSetLabwareBarcode.bmp"></p></td><td>Set barcode for labware which was or cannot be read by built in reader.</td></tr><tr><td>Remove Labware</td><td><p><br></p><p><img src="../../.gitbook/assets/Image_660.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\BtnRemoveLabware.bmp"></p></td><td>Remove labware data from the database stop generation of mapping information.</td></tr><tr><td>Import Worklist</td><td><p><br></p><p><img src="../../.gitbook/assets/Image_661.jpg" alt="image"></p></td><td>Imports an external worklist into the internal Hamilton database. Works in combination with “Load and Match”.</td></tr><tr><td>Update Job Status</td><td><p><br></p><p><img src="../../.gitbook/assets/Image_662.jpg" alt="image"></p></td><td>Changes the status of a job on the Hamilton database.</td></tr></tbody></table>
2.  #### _‌Generating a Mapping File‌_

    \


    _To use this step, select the following:_

    * _instrument_
    * _Sequence over which the data should be generated_

    _The step is able to filter (expand) the stored information by selecting additional sequences in such a way that the additional information is stored which are affected by the sequences._

    _Define the path and filename where the collected information will be stored. If there is no path specified, it will automatically be stored in the HAMILTON\Logfiles directory by default._

    _Make sure that the labware is loaded before calling this command._

    \


    ![image](../../.gitbook/assets/Image\_663.png)

    \


    _The “Generate Mapping File” Step collects data regarding the TARGET sequence and “looks” backwards as to what was pipetted into this sequence. Specify “Sequences of interest” to filter the information._

    _Example: Pipette from a tube carrier into the target plate (red to green). Afterwards, cover the samples in the plate with the reagent (blue to green)._

    _To track both pipetting, both of the source sequences have to be added as “Sequences of interest”._

    _To link only the barcode of the sample tube to the well ID of the target plate, only add the sample tube sequence to the “Sequences of interest”._
3.  #### _‌Customizing the Mapping File‌_

    \


    _The \[Customize] Button offers multiple options to customize the output mapping file. It is possible to:_

    *   _Filter the data by using the status of the sample._

        \


        ![image](../../.gitbook/assets/Image\_664.jpg)

        \


        ![Originalbild anzeigen](../../.gitbook/assets/Image\_665.gif)

        _NOTE_

        _When the aspirate step is mixing the liquid, it will create an entry in the database. To suppress this liquid transfer, check the checkbox “Exclude multiple entries if source is mixed”. Otherwise, at least two lines per sample will be found._

        \

    *   _Sort the data in line wise (A1 – A12) or column wise (A1 – H1)._

        \


        ![image](../../.gitbook/assets/Image\_666.gif)

        \


        _It is possible to link the default column name of the mapping files column to a user defined column name (see lines 2, 4, 8 in the image below). Simply change the name in the right column. Make sure that the quotes are present. Alternatively, variables can be used in the column name fields._

        \


        ![image](../../.gitbook/assets/Image\_667.gif)

        \

    * _To hide columns in the output file, deactivate the checkbox (see lines 3, 5 and 6 in the image above)._
    * _Activating the “Create one file for full sequence of interest” will create one single output file even if the sequence of interest covers more than one labware. Unchecking this box will create a single output file for every labware of the sequence of interest._
    * _The “Open file to append” will not overwrite an existing file with new data but add the new data to the end of the file._
    * _Per default, the output excel file is created in the LogFiles folder (under C:\Program Files\HAMILTON..  depending on the language of the operating system). To change this path and the default name of the output file, use the field: “String used to generate the mapping file name(s)”._

    \


    ![image](../../.gitbook/assets/Image\_668.gif)

    \

4.  #### _‌Set Labware Barcode‌_

    \


    _The step “Set Labware Barcode“ is used for labware that has been positioned on the deck but cannot be identified by the built-in barcode reader._

    _The labware which the barcode has to be set must be identified either by the LabwareID (created in the Deck Layout Editor) or by the sequence which was defined by the Sequence Editor._

    _The barcode to be set must either be a constant string or a variable. At run time, an error will be generated if the barcode passed is empty._
5.  #### _‌Remove Labware‌_

    \


    _The command “Remove Labware“ removes labware from the access of sample tracking. It is used for the labware which are removed from the deck. After this command has been executed, no more tracking data for the removed labware is accessible._

    \

6.  #### _‌Import Worklist‌_

    \


    _The import worklist step is used to import an external database. The file format can be in Access, Excel or a structured text. The data in the external worklist can be assigned to the columns of the internal Hamilton database. This allows the use of the imported data within the VENUS Software environment and e.g. use the “Load and Match_[_” Step to connect the loaded barcodes to a previously imported worklist. Refer to_ ](sample-tracker.md#bookmark312)_Section 11.11.3 Importing a Worklist for more information._

    \

7.  #### _‌Update Job Status‌_

    \


    _This command allows changing the status of a sequence position from 'Assigned' or 'Unprocessed' to ‘Processed’. The update is done on the current position of the given sequence._
