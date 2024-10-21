# Temperature Controlled Carrier (TCC)

The temperature controlled carrier (TCC) is a device for heating and cooling of microplates. It has four positions for microplates which are all of the same temperature. The TCC can heat microplates up to 60°C or cool them down to 22°C below ambient temperature.

A maximum of two TCCs can be placed on one ML STAR and controlled by the VENUS Software. Activate the Temperature Controlled Carrier in the System Configuration Editor (ML STAR Tab).

<figure><img src="../../.gitbook/assets/image (36) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

The method is also using the sample tracker to store the pipetting data to a file. It can be activated in the System Configuration Editor (System Tab) as well.

<figure><img src="../../.gitbook/assets/image (38) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

\


## Command Description

The table below gives a brief overview of the available commands for the TCC.

<table><thead><tr><th>Command</th><th width="175">Icon</th><th></th></tr></thead><tbody><tr><td>Set Carrier Temperature</td><td><img src="../../.gitbook/assets/image (42) (1) (1) (1) (1) (1) (1).png" alt="" data-size="original"></td><td>Sets the temperature of a TCC.</td></tr><tr><td>Get Carrier Temperature</td><td><img src="../../.gitbook/assets/image (41) (1) (1) (1) (1) (1) (1).png" alt="" data-size="original"></td><td>Retrieves the temperature of a TCC.</td></tr></tbody></table>



Typical times (at 40% rel. humidity) to heat and cool a Microplate are (Tambient ≈ 20°C):

| Tambient to 60°C:  | 20 min |
| ------------------ | ------ |
| 60 °C to Tambient: | 20 min |
| Tambient to 4°C:   | 15 min |
| 4°C to 60°C:       | 25 min |



## Programming the TCC / Sample Tracking

The following example makes use of the TCC and shows the additional functionality of the ML STAR user software. It can be found under the name “Example”.



### Creating the Deck Layout

Create the Deck Layout holding the following:

* Tip carrier (TIP\_CAR\_480\_ST\_A00).
* 6 tube carriers (SMP\_CAR\_32\_12x75\_A00) for 32 sample tubes each.
* Temperature-controlled carrier (Car\_TCC\_1).
* Two standard Nunc plates (Nun\_96\_Fl\_L) on the TCC.\


<figure><img src="../../.gitbook/assets/image (44) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>



## Creating the Sequences

Under the “Sequences” Tab, select the “Channels” Stamp Tool and create the following:

* A sequence over all six tube carriers named “AllSamples”.
* A sequence over the two plates named ‘Target’.

### Creating the Method

In order to use the “Generate Mapping File” Step, which will create an output file with source / target / volume information, the “Data Handling Steps” Option has to be activated in “Method -> Instruments and Smart Steps”

<figure><img src="../../.gitbook/assets/image (46) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

The complete method should look like the image presented below, following the first “Initialize” Step.

<figure><img src="../../.gitbook/assets/image (47) (1) (1) (1) (1) (1) (1).png" alt="" width="552"><figcaption></figcaption></figure>



### Method Analysis

A look on how the method is constructed.

1. First, all carriers are loaded using the “Load” Smart Step:
2. A user input is used in line 2 to get both the number of samples to process and the temperature of the TCC to set. Do not forget to enclose the text in quotation marks; otherwise the system will interpret it as a new variable.
3. Step 3 will set the temperature of the TCC.

<figure><img src="../../.gitbook/assets/image (48) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>



4. The carrier temperature is not set in absolute. It is held in the variable depending on the user’s input.
5. Please note that this step will continue when the temperature is reached. This means that it will wait for 600 sec and then check if the temperature was reached. For detailed information, refer to the steps in the help file.
6. In step 4, the end position of the AllSamples sequence is set to the number the user has specified. Since there is a limit in the user’s input, the number cannot be set wrong.

<figure><img src="../../.gitbook/assets/image (49) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

7. The “Pipette Simple” Step will bring the liquid from the tubes into the plate. Depending on the number of samples, either only one plate or both plates are used.
8. In step 6 a “Report Mapping File” is generated. In this file, all the liquid transfers of selectable sequences are reported.&#x20;
9. Enter a sequence in the “Generate mapping file(s) of sequence” Field. The mapping file will contain all information about the liquid that was pipetted into the sequence. Using “Sequences of interest”, it is possible to select which source sequences shall be taken into account.
10. In the “Sequences of interest”, selecting sequences where the liquid comes from is specified. In this case, the samples are coming from the AllSample sequences. If there was a buffer or reagent sequence as well, insert those sequences too. This is to see where all liquid comes from.
11. The filename is created by a constant string, but it is more useful to use information contained in the database by place-holders. The default file name is built using the labware ID, the barcode and an auto-incrementing number.
12. The path where to store the mapping file(s) has to be specified. If left blank like in the example, the data will be stored to the logfiles directory.
13. If a customized path is entered, be sure the path exists before the mapping file has to be generated.\
    \


    <figure><img src="../../.gitbook/assets/image (50) (1) (1) (1) (1) (1).png" alt="" width="315"><figcaption></figcaption></figure>
14. The output file will be filtered to contain only the error free processed samples.
15. To do so, click the \[Customize…] Button.\




    <figure><img src="../../.gitbook/assets/image (51) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>



16. To filter and keep the errorless ones only, select the \[Without errors only] Radio Button.
17. In the Sorting field, specify the sorting direction to “Sort records by column”.
18. As seen below, it is possible to customize the columns. The standard and constant columns are displayed on the left side; either the CAT heater shaker or TELESHAKE. Renaming the column name on the right side can be done.\


    <figure><img src="../../.gitbook/assets/image (52) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>
19. The resulting file is shown below. If customized column names are specified, all columns are marked with a “T” refers to the Target Sequence while all columns beginning with “S” refers to the Source Sequence.\
    \


    <figure><img src="../../.gitbook/assets/image (53) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>
