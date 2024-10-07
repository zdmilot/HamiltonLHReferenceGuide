# Temperature Controlled Carrier (TCC)

_The temperature controlled carrier (TCC) is a device for heating and cooling of microplates. It has four positions for microplates which are all of the same temperature. The TCC can heat microplates up to 60°C or cool them down to 22°C below ambient temperature._

_A maximum of two TCCs can be placed on one ML STAR and controlled by the VENUS Software. Activate the Temperature Controlled Carrier in the System Configuration Editor (ML STAR Tab)._

\


![image](../.gitbook/manual-images/assets/Image\_1679.gif)

\


_The method is also using the sample tracker to store the pipetting data to a file. It can be activated in the System Configuration Editor (System Tab) as well._

\


![image](../.gitbook/manual-images/assets/Image\_1680.gif)

\


1.  ### _‌Command Description‌_

    \


    _The table below gives a brief overview of the available commands for the TCC._

    \


    | ML\_STAR                |                                                                                                    |                                     |
    | ----------------------- | -------------------------------------------------------------------------------------------------- | ----------------------------------- |
    | Preparation             |                                                                                                    |                                     |
    | Command                 | Icon                                                                                               | Action Performed                    |
    | Set Carrier Temperature | <p><br></p><p><img src="../.gitbook/manual-images/assets/Image_1681.jpg" alt="NewIMAGES/setcarrierTemp.bmp"></p> | Sets the temperature of a TCC.      |
    | Get Carrier Temperature | <p><br></p><p><img src="../.gitbook/manual-images/assets/Image_1682.jpg" alt="NewIMAGES/getcarrierTemp.bmp"></p> | Retrieves the temperature of a TCC. |

    _Typical times (at 40% rel. humidity) to heat and cool a Microplate are (Tambient ≈ 20°C):_

    \


    | Tambient to 60°C:  | 20 min |
    | ------------------ | ------ |
    | 60 °C to Tambient: | 20 min |
    | Tambient to 4°C:   | 15 min |
    | 4°C to 60°C:       | 25 min |

    \

2.  ### _‌Programming the TCC / Sample Tracking‌_

    \


    _The following example makes use of the TCC and shows the additional functionality of the ML STAR user software. It can be found under the name “Example”._

    \


    _Creating the Deck Layout_

    _Create the Deck Layout holding the following:_

    * _Tip carrier (TIP\_CAR\_480\_ST\_A00)._
    * _6 tube carriers (SMP\_CAR\_32\_12x75\_A00) for 32 sample tubes each._
    * _Temperature-controlled carrier (Car\_TCC\_1)._
    * _Two standard Nunc plates (Nun\_96\_Fl\_L) on the TCC._

    \


    ![image](../.gitbook/manual-images/assets/Image\_1683.jpg)

    \

3.  ### _‌Creating the Sequences‌_

    \


    _Under the “Sequences” Tab, select the “Channels” Stamp Tool and create the following:_

    * _A sequence over all six tube carriers named “AllSamples”._
    * _A sequence over the two plates named ‘Target’._

    _Creating the Method_

    _In order to use the “Generate Mapping File” Step, which will create an output file with source / target / volume information, the “Data Handling Steps” Option has to be activated in “Method  Instruments and Smart Steps”_

    \


    ![image](../.gitbook/manual-images/assets/Image\_1684.gif)

    \


    _The complete method should look like the image presented below, following the first “Initialize” Step._

    \


    ![image](../.gitbook/manual-images/assets/Image\_1685.jpg)

    \


    _Method Analysis_

    _A look on how the method is constructed._

    1. _First, all carriers are loaded using the “Load” Smart Step:_
    2. _A user input is used in line 2 to get both the number of samples to process and the temperature of the TCC to set. Do not forget to enclose the text in quotation marks; otherwise the system will interpret it as a new variable._
    3.  _Step 3 will set the temperature of the TCC._

        \


        ![image](../.gitbook/manual-images/assets/Image\_1686.jpg)

        \

    4. _The carrier temperature is not set in absolute. It is held in the variable depending on the user’s input._
    5. _Please note that this step will continue when the temperature is reached. This means that it will wait for 600 sec and then check if the temperature was reached. For detailed information, refer to the steps in the help file._
    6.  _In step 4, the end position of the AllSamples sequence is set to the number the user has specified. Since there is a limit in the user’s input, the number cannot be set wrong._

        \


        ![image](../.gitbook/manual-images/assets/Image\_1687.jpg)

        \

    7. _The “Pipette Simple” Step will bring the liquid from the tubes into the plate. Depending on the number of samples, either only one plate or both plates are used._
    8. _In step 6 a “Report Mapping File_[_” is generated. In this file, all the liquid transfers of selectable sequences are reported. Refer to_ ](temperature-controlled-carrier-tcc.md#bookmark302)[_Section  11.9.2  Generating  a  Mapping_  ](temperature-controlled-carrier-tcc.md#bookmark302)_File for more information._
    9. _Enter a sequence in the “Generate mapping file(s) of sequence” Field. The mapping file will contain all information about the liquid that was pipetted into the sequence. Using “Sequences of interest”, it is possible to select which source sequences shall be taken into account._
    10. _In the “Sequences of interest”, selecting sequences where the liquid comes from is specified. In this case, the samples are coming from the AllSample sequences. If there was a buffer or reagent sequence as well, insert those sequences too. This is to see where all liquid comes from._
    11. _The filename is created by a constant string, but it is more useful to use information contained in the database by place-holders. The default file name is built using the labware ID, the barcode and an auto-incrementing number._
    12. _The path where to store the mapping file(s) has to be specified. If left blank like in the example, the data will be stored to the logfiles directory._
    13. _If a customized path is entered, be sure the path exists before the mapping file has to be generated._

        \


        ![image](../.gitbook/manual-images/assets/Image\_1688.jpg)

        \

    14. _The output file will be filtered to contain only the error free processed samples._
    15. _To do so, click the \[Customize…] Button._

        \


        ![image](../.gitbook/manual-images/assets/Image\_1689.gif)

        \

    16. _To filter and keep the errorless ones only, select the \[Without errors only] Radio Button._
    17. _In the Sorting field, specify the sorting direction to “Sort records by column”._
    18. _As seen below, it is possible to customize the columns. The standard and constant columns are displayed on the left side; either the CAT heater shaker or TELESHAKE. Renaming the column name on the right side can be done._

        \


        ![image](../.gitbook/manual-images/assets/Image\_1690.jpg)

        \

    19. _The resulting file is shown below. If customized column names are specified, all columns are marked with a “T” refers to the Target Sequence while all columns beginning with “S” refers to the Source Sequence.‌_

    ![image](../.gitbook/manual-images/assets/Image\_1691.gif)
