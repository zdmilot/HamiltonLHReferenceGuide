# Pipetting Steps

{% tabs %}
{% tab title="ML_STAR Smart Steps" %}
<table><thead><tr><th width="295">Command</th><th>Icon</th><th>Action Performed</th></tr></thead><tbody><tr><td>1000μl Channel Tip Pick up</td><td><p><br></p><p><img src="../../../.gitbook/manual-images/assets/Image_1398.jpg" alt="image"></p></td><td>Pick up disposable tips from tip rack.</td></tr><tr><td>1000μl Channel Needle Pick up</td><td><p><br></p><p><img src="../../../.gitbook/manual-images/assets/Image_1399.jpg" alt="NewIMAGES/btnneedlepickup.jpg"></p></td><td>Pick up needles from wash station (or racks).</td></tr><tr><td>1000μl Channel Pipette Simple (1-1)</td><td><p><br></p><p><img src="../../../.gitbook/manual-images/assets/Image_1400.jpg" alt="NewIMAGES/btnpipetteSimple.jpg"></p></td><td>Simple pipetting for simple aspiration/dispense cycle.</td></tr><tr><td>1000μl Channel Pipette Replica (1-n)</td><td><p><br></p><p><img src="../../../.gitbook/manual-images/assets/Image_1401.jpg" alt="NewIMAGES/btnpipettereplica.jpg"></p></td><td>Pipetting for cycles of aspirations/dispenses where the liquid from one source is dispensed into multiple target containers (no aliquoting).</td></tr><tr><td>1000μl Channel Pipette Pooling (n-1)</td><td><p><br></p><p><img src="../../../.gitbook/manual-images/assets/Image_1402.jpg" alt="NewIMAGES/btnpipettepooling.jpg"></p></td><td>Pipetting for cycles of multiple aspirations/dispenses where liquid from multiple source containers is dispensed into one target container.</td></tr><tr><td>1000μl Channel Pipette Aliquot</td><td><p><br></p><p><img src="../../../.gitbook/manual-images/assets/Image_1403.jpg" alt="NewIMAGES/btnpipettealiquot.jpg"></p></td><td>Pipetting for cycles with one aspiration followed by multiple dispenses.</td></tr><tr><td>1000μl Channel Tip Eject</td><td><p><br></p><p><img src="../../../.gitbook/manual-images/assets/Image_1404.jpg" alt="NewIMAGES/btnejecttips.bmp"></p></td><td>Eject disposable tips into tip waste.</td></tr><tr><td>1000μl Channel Needle Eject</td><td><p><br></p><p><img src="../../../.gitbook/manual-images/assets/Image_1405.jpg" alt="NewIMAGES/btnneedleseject.bmp"></p></td><td>Release needles in racks or wash station (and start wash).</td></tr></tbody></table>
{% endtab %}

{% tab title="Easy Steps‌" %}
_There are two Easy Steps for the pipetting channels, the CO-RE 96 Probe Head and the CO-RE 384 Probe Head:_

* _Aspirate (including the pickup of disposable tips/needles)._
* _Dispense (including the disposable tips/needles wash and eject)._

_The Easy Steps are installed by default. These commands can be found in the “ML\_STAR” Toolbox Group._



| Command                 | Icon                                                                                                     | Action Performed                                   |
| ----------------------- | -------------------------------------------------------------------------------------------------------- | -------------------------------------------------- |
| 1000μl Channel Aspirate | <p><br></p><p><img src="../../../.gitbook/manual-images/assets/Image_1406.jpg" alt="image"></p>                        | Aspirate liquid with the 1000μl-pipetting channels |
| 5ml Channel Aspirate    | <p><br></p><p><img src="../../../.gitbook/manual-images/assets/Image_1407.jpg" alt="image"></p>                        | Aspirate liquid with the 5ml-pipetting channels    |
| CO-RE 96 Head Aspirate  | <p><br></p><p><img src="../../../.gitbook/manual-images/assets/Image_1408.jpg" alt="NewIMAGES/core96aspirate.bmp"></p> | Aspirate liquid with the CO-RE 96 Probe Head       |
| CO-RE 384 Head Aspirate | <p></p><p><img src="../../../.gitbook/manual-images/assets/Image_1409.gif" alt="image"></p>                            | Aspirate liquid with the CO-RE 384 Probe Head      |
| 1000μl Channel Dispense | <p></p><p><img src="../../../.gitbook/manual-images/assets/Image_1410.jpg" alt="image"></p>                            | Dispense with the 1000μl-pipetting channels        |
| 5ml Channel Dispense    | <p></p><p><img src="../../../.gitbook/manual-images/assets/Image_1411.jpg" alt="image"></p>                            | Dispense with the 5ml-pipetting channels           |
| CO-RE 96 Head Dispense  | <p><br></p><p><img src="../../../.gitbook/manual-images/assets/Image_1412.jpg" alt="Disp96"></p>                       | Dispense liquid with the CO-RE 96 Probe Head       |
| CO-RE 384 Head Dispense | <p></p><p><img src="../../../.gitbook/manual-images/assets/Image_1413.gif" alt="image"></p>                            | Dispense liquid with the CO-RE 384 Probe Head      |

_The default settings of the aspirate steps correspond to an ordinary aspiration “Simple Aspiration” mode. If any other aspiration mode (Consecutive, All), mix step, LLD setting, etc. is required, clicking the \[Customize…] Button can modify the command._

\


![image](../../../.gitbook/manual-images/assets/Image\_1414.gif)

_The \[Error settings…] Dialog allows an error handling approach to be specified._
{% endtab %}

{% tab title="Single Steps‌" %}
{% tabs %}
{% tab title="1000μl Channel" %}
| Command                              | Icon                                                                              | Action Performed                                                                                             |
| ------------------------------------ | --------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------ |
| 1000μl Channel Aspirate              | <p><br></p><p><img src="../../../.gitbook/manual-images/assets/Image_1416.gif" alt="image"></p> | Aspirate liquid from a container                                                                             |
| 1000μl Channel Dispense              | <p><br></p><p><img src="../../../.gitbook/manual-images/assets/Image_1417.gif" alt="image"></p> | Dispense liquid into a container                                                                             |
| 1000µl Channel Dispense on the Fly   | <p><br></p><p><img src="../../../.gitbook/manual-images/assets/Image_1418.jpg" alt="image"></p> | Pipettes liquid without stopping in x over a full plate or sequence. Very fast for e.g. reagent distribution |
| 1000μl Channel Tip Eject             | <p><br></p><p><img src="../../../.gitbook/manual-images/assets/Image_1419.gif" alt="image"></p> | Discards the tip into the tip waste or the needle into the wash station or rack                              |
| 1000μl Channel Get Last Liquid Level | <p><br></p><p><img src="../../../.gitbook/manual-images/assets/Image_1420.jpg" alt="image"></p> | Gets the z-position of the last Liquid Level Detection                                                       |
{% endtab %}

{% tab title="5mL Channel" %}
| Command                           | Icon                                                                              | Action Performed                                                                                             |
| --------------------------------- | --------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------ |
| 5ml Channel Tip Pick Up           | <p><br></p><p><img src="../../../.gitbook/manual-images/assets/Image_1421.gif" alt="image"></p> | Picks up a CO-RE tip or needle                                                                               |
| 5ml Channel Aspirate              | <p><br></p><p><img src="../../../.gitbook/manual-images/assets/Image_1422.gif" alt="image"></p> | Aspirates liquid from a container                                                                            |
| 5ml Channel Dispense              | <p><br></p><p><img src="../../../.gitbook/manual-images/assets/Image_1423.gif" alt="image"></p> | Dispenses liquid into a container                                                                            |
| 5ml Channel Dispense on the Fly   | <p><br></p><p><img src="../../../.gitbook/manual-images/assets/Image_1424.jpg" alt="image"></p> | Pipettes liquid without stopping in x over a full plate or sequence. Very fast for e.g. reagent distribution |
| 5ml Channel Tip Eject             | <p><br></p><p><img src="../../../.gitbook/manual-images/assets/Image_1425.gif" alt="image"></p> | Discards the tip into the tip waste or the needle into the wash station or rack                              |
| 5ml Channel Get Last Liquid Level | <p><br></p><p><img src="../../../.gitbook/manual-images/assets/Image_1426.jpg" alt="image"></p> | Gets the z position of the last Liquid Level Detection                                                       |
{% endtab %}

{% tab title="CO-RE 96" %}
| Command                   | Icon                                                                                                         | Action Performed                  |
| ------------------------- | ------------------------------------------------------------------------------------------------------------ | --------------------------------- |
| CO-RE 96 Head Tip Pick Up | <p><br></p><p><img src="../../../.gitbook/manual-images/assets/Image_1427.jpg" alt="NewIMAGES/core96tipPickUp.bmp"></p>    | Pick up CO-RE tips                |
| CO-RE 96 Head Aspirate    | <p><br></p><p><img src="../../../.gitbook/manual-images/assets/Image_1428.jpg" alt="image"></p>                            | Aspirates liquid from a container |
| CO-RE 96 Head Dispense    | <p><br></p><p><img src="../../../.gitbook/manual-images/assets/Image_1429.jpg" alt="NewIMAGES/CORE96headDispense.bmp"></p> | Dispenses liquid into a container |
| CO-RE 96 Head Tip Eject   | <p><br></p><p><img src="../../../.gitbook/manual-images/assets/Image_1430.jpg" alt="NewIMAGES/core96headtipEject.bmp"></p> | Discards the tips                 |
{% endtab %}

{% tab title="CO-RE 384" %}
| Command                    | Icon                                                                              | Action Performed                   |
| -------------------------- | --------------------------------------------------------------------------------- | ---------------------------------- |
| CO-RE 384 Head Tip Pick Up | <p><br></p><p><img src="../../../.gitbook/manual-images/assets/Image_1431.gif" alt="image"></p> | Pick up CO-RE tips.                |
| CO-RE 384 Head Aspirate    | <p><br></p><p><img src="../../../.gitbook/manual-images/assets/Image_1432.gif" alt="image"></p> | Aspirates liquid from a container. |
| CO-RE 384 Head Dispense    | <p><br></p><p><img src="../../../.gitbook/manual-images/assets/Image_1433.gif" alt="image"></p> | Dispenses liquid into a container. |
| CO-RE 384 Head Tip Eject   | <p><br></p><p><img src="../../../.gitbook/manual-images/assets/Image_1434.gif" alt="image"></p> | Discards the tips.                 |


{% endtab %}
{% endtabs %}

_If highest flexibility of the system is required, use the Single Step commands. When using these commands, even most complex liquid handlings can be programmed._
{% endtab %}
{% endtabs %}









_In this section, the general features of the "Pipette" Smart Step are explained by means of the “Simple Pipetting” Smart Step (the other variants of the “Pipette” Command have similar wizards)._&#x20;

1.  _Drag one of the "Pipette" Smart Steps into the method window. The corresponding step of the "Pipette" Smart Step Wizard opens:_

    ![image](../../../.gitbook/manual-images/assets/Image\_1455.jpg)

    \

2. _Use the drop down list to identify the instrument on which pipetting must be performed, as well as the aspirate and dispense sequences._
3.  _Note that the sequences can also be indicated using arrays:_

    \


    ![image](../../../.gitbook/manual-images/assets/Image\_1456.jpg)
4.  _Click the \[Next >] Button. The next page of the pipetting wizard will be activated._

    \


    ![image](../../../.gitbook/manual-images/assets/Image\_1457.jpg)

    \

5.  _Note that in this dialog the volume can also be specified using an array as shown below._

    \


    ![image](../../../.gitbook/manual-images/assets/Image\_1458.jpg)
6. _Define: the volume(s) for the pipetting process, a possible rest volume and its re-dispense target._
7. _If a volume for “Simple“, “Replica” or “Pooling” is specified and exceeds the volume of the tip, multiple transfers with equally divided volumes will be performed automatically._

_Rest Volume_

_A residual volume “Rest volume” in the dialogs may be used for all pipetting modes too. This is handled at the end of a pipetting step after the (last) dispensing step. In the aliquot mode the additional handled residual volume is called “Post-aliquot” in contrast to the “Pre-aliquot”, which is handled before the aspirating step. The pre-aliquot is dispensed back into the aspiration sequence._

_With the “Rest volume”, the choice is to discard it back into the aspiration sequence, or to dispense it into the waste container. In the previous example, a re-dispense height counted from the bottom of the container has to be given._

1.  _Click the \[Next >] Button. The following pipetting wizard dialog will be displayed._

    \


    ![image](../../../.gitbook/manual-images/assets/Image\_1459.jpg)

    \

2. _Select the appropriate tip/needle handling which is the same for all dispense modes:_
3. _First, select the tip sequence - where the tips are to be picked up from (here, an array can also be selected). The tip type is automatically retrieved from the sequence. If the tip sequence is used up, it will be automatically reloaded. As an additional feature, the tip sequence can be reduced during a reload._
4. _Tip/needle handling can be specified, too (some items may not be selected, depending on the pipetting mode):_
   *   _Replace tips “After each dispense“ (if multiple dispenses are needed to transfer e.g. 900_

       _µl with a standard tip of 300 µl),_
   * _Only for replicas (and pooling) the option “After transferred volume“ becomes active. This allows the use of fresh tips even for multiple aspirations and multiple dispense cycles being performed with the same sample._
   * _“After each sample“ (multiple dispenses of the same sample are done with the same tip),_
   * _With “One tip set“, or_
   * _Without tip handling, “Never“. In this case, ML STAR will have to pick up tips prior to the pipette step and eject them after pipetting, using single steps._
5. _A tip counter can be specified, which enables the user to start with a set of tips, partly used in previous runs at the correct position. To read a tip counter, it can be specified within the Smart Step “Load” (see corresponding section). A tip counter is specified by a name (e.g., “cntTips“). Be reminded to enclose the name in quotation marks._
6. _Within the “Pipette” Smart Step, the current position of the tip sequence will continuously be stored under the name of the tip counter. Note that a tip counter has to be initialized if it is to be read by the “Load” Smart Step within the next run._
7.  _Click the \[Next >] Button. The next page of the pipetting wizard will be displayed._

    \


    ![image](../../../.gitbook/manual-images/assets/Image\_1460.jpg)
8. _Define the dispense mode and the liquid class._
9. _Define the aspiration and dispense (liquid handling) parameters used in the step._
10. _The “Aspirate the complete requested volume without an error“ Checkbox enables aspiration of the residual liquid from a container (specify a volume larger than the expected residual volume within the container) without an error, even if there is not enough liquid available._
    * _For dispense, select the “Surface“ or “Jet“Dispense Mode._
    *   _For aspiration and dispense, specify the LLD (Liquid Level Detection) settings by clicking the \[LLD] Button. Below is how the “Aspirate LLD” Screen should look like._

        \


        ![image](../../../.gitbook/manual-images/assets/Image\_1461.jpg)

        \

11. _Within the LLD dialog, capacitance, pressure, both LLD types or none may be selected._
    * _A sensitivity setting is necessary. Either use the predefined settings from the Labware or override these settings with Very high / High / Medium or Low._
    * _If no LLD is used in aspiration and jet dispensing cannot work with LLD, the height from the bottom has to be defined._
    * _If any LLD is used either for aspiration or dispense, a submerge depth has to be specified. For the parallel use of both LLD types, only selectable for aspiration, a maximum height difference has to be given within which both LLDs have to respond._
12. _Click \[OK], to close the “Aspirate LLD” Screen._
13. _In the “Pipetting Wizard” Screen, click the \[Advanced...] Button, to specify the options “Pre- rinsing” and “Liquid following”. Below is how the “Dispense” Screen looks like. Click \[OK], to close the “Dispense” Screen._

    \


    ![image](../../../.gitbook/manual-images/assets/Image\_1462.jpg)

    \

14. _Here in the “Channel Settings” Dialog, the user is allowed to specify a channel pattern manually, as well as the number of the channels which will be used to calibrate (1536-well) carriers._

    \


    ![image](../../../.gitbook/manual-images/assets/Image\_1463.jpg)
15. _Click the \[Next >] Button. The last page of the pipetting wizard will be displayed._

    \


    ![image](../../../.gitbook/manual-images/assets/Image\_1464.jpg)

    \

16. _Select the appropriate controlling sequence by activating the radio button. As long as both sequences are of the same length, this selection does not influence the pipetting (if no pipetting error occurs)._

\


_Sequence handling for Aliquot procedure_

_In the case of aliquoting, the dispense sequence is always the controlling sequence._

\


_Sequence Handling in Pipetting Mode “Simple”_

_Consider a situation where the aspiration sequence comprises 8 tubes, and the dispense sequence is a 96-well plate. What should be done now with the 88 remaining positions within the plate? If the aspiration sequence is controlling, the dispense sequence is reduced to the length of the aspiration sequence and the pipetting stops after dispensing into the first 8 positions of the plate sequence. If the dispense sequence is controlling, the aspiration sequence will be repeated until it reaches the length of the dispense sequence. This results in multiple transfers (12 for an 8- channel instrument) from the same 8 tubes to fill the complete plate. Then the (controlling) dispense sequence is finished and pipetting stops._

![Originalbild anzeigen](../../../.gitbook/manual-images/assets/Image\_1465.jpg)

_NOTE_

_The “Pipette” Smart Step always equalizes the length of aspiration and dispense sequences._

\


_The following table gives an overview of the different situations and examples._

\


| <p><br></p>                             | <p>Aspiration sequence is GREATER THAN</p><p>dispense sequence</p>                                                                                                                                              | <p>Aspiration sequence is SMALLER THAN</p><p>dispense sequence</p>                                                                                                                                                                                                                                               |
| --------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| <p><br></p><p>Aspiration Controls</p>   | <p><a href="pipetting-steps.md#bookmark435">The dispense sequence is REPEATED to the length of aspiration sequence (see </a><a href="pipetting-steps.md#bookmark435">Case </a>1)</p><p>Examples for use:</p>    | <p><a href="pipetting-steps.md#bookmark437">The dispense sequence is REDUCED to the length of the aspiration sequence (see </a><a href="pipetting-steps.md#bookmark437">Case </a>3)</p><p>Example for use:</p><p>- Transfer a variable number (&#x3C;96) of tubes into a 96-well plate (left partly filled).</p> |
| <p><br></p><p>Dispensation Controls</p> | <p><a href="pipetting-steps.md#bookmark436">The aspiration sequence is REDUCED to the length of the dispense sequence (see </a><a href="pipetting-steps.md#bookmark436">Case </a>2)</p><p>Examples for use:</p> | <p><a href="pipetting-steps.md#bookmark438">The aspiration sequence is REPEATED to the length of dispense sequence (see </a>Case 4)</p><p>Examples for use:</p>                                                                                                                                                  |

* _Copy 2 plates into 1 (after another)_
* _With reloading of the dispense sequence: Transfer available tubes to as many plates as needed._
* _Transfers from many tubes to a plate and stops when plate is filled._
* _With reloading of plate sequences: Automatically fill as many plates as needed with liquid from tubes._
* _Transfer reagent from a container (or, e.g., 8 tubes) to a complete plate._
* _Copy tubes repeatedly into plate._
* _With reload of aspiration sequence: Automatically reload tubes until plate is filled._

_‌Case 1: Aspiration sequence > dispense sequence, controlled by the aspiration sequence._

\


![reload](../../../.gitbook/manual-images/assets/Image\_1466.jpg)

\


_The target sequence is repeated to match the length of the source sequence._

_Another example for this case: All Tubes to Plate(s). This is a reloadable plate sequence used to load all tubes to as many plates as needed._

\


_‌Case 2: Aspiration sequence > dispense sequence. This case is controlled by the dispense sequence._

\


![image](../../../.gitbook/manual-images/assets/Image\_1467.jpg)

\


_The source sequence is cut to match the length of the target sequence, and stops when the plate is full (prepare plate for assay)._

_‌Case 3: Dispense sequence > aspiration sequence this case is controlled by the aspiration sequence_

\


![image](../../../.gitbook/manual-images/assets/Image\_1468.png)

\


_The target sequence is cut to match the length of the source sequence and stops when the tubes are processed (how many samples today?). If L(Sasp)>96, plate is filled again._

\


_‌Case 4: Dispense sequence > aspiration sequence. This case is controlled by the dispense sequence._

\


![image](../../../.gitbook/manual-images/assets/Image\_1469.jpg)

_The source sequence is repeated n-times to match the length of the target sequence and stops when the plate is full (distribute buffer, reagents...). Also used for aliquoting._

Sequence Handling in Pipetting Mode Pooling and Replica‌

_In these two cases, the aspiration sequence should be selected as controlling. It is possible to choose how to reload a sequence:_

* _If during pipetting a sequence is used up (no more tubes are left to aspirate from), the system asks for a new carrier of tubes to be loaded._
*   _If the “Operator may reduce the sequence by a reload“ Checkbox is ticked, the user has the option of reducing the newly loaded sequence at run time. This is especially helpful if the exact amount of sample tubes varies from run to run (or from tube carrier to tube carrier)._

    \


    _Advanced Buttons_

    _Sequence manipulations can be made (separately for aspiration and dispense sequences) by means of the dialogs invoked by the \[Advanced...] Buttons._
* _If the Smart Step is going to work with sequences that have been used within this method from the preceding steps, the sequence counters can be reset. This is done by using the two checkboxes for initial sequence manipulation._
*   _If other steps are following this Smart Step, the status of the sequence which is passed back can be defined by the \[Final sequence manipulation] Radio Button. Below is an example of the advanced dialog for “Aspirate” Sequence settings._

    \


    ![image](../../../.gitbook/manual-images/assets/Image\_1470.jpg)

    \


    _The “Error Settings” Dialog allows specifying an error handling approach. The choices are listed on the next page._

    \


    ![image](../../../.gitbook/manual-images/assets/Image\_1471.jpg)

    _In case of an error, the following choices are:_
* _Abort the method (only abort button on run time error dialog)_
* _Offer choices (in run time) whether to abort or cancel (continue with user-defined error handling if programmed, otherwise abort)_
* _Use the fixed default error recovery (recommended) pre-programmed for the Smart Step. In this case two choices can be made_
*   _“Copy pattern”, means that in case of an error on aspiration, the corresponding well of the dispense sequence will be left out (the pattern is kept). If “Copy pattern“ is not checked, the dispense sequence positions will all be pipetted, leaving a well not pipetted at the end of the sequence._

    \


    ![image](../../../.gitbook/manual-images/assets/Image\_1472.jpg)

    \

* _“Exclude error positions”, means exclude the erroneous positions from aspiration and dispensation sequences. If this option is enabled and an error occurs during an aspirate or dispense step, the erroneous position will be excluded from the sequence by removing the corresponding element from the aspirate or dispense sequence. The next time these sequences are used, the erroneous well will not be pipetted._
* _In addition, Walk-away mode can be enabled. If this checkbox is ticked, a timeout has to be specified after which the error dialog on run time will automatically close down and continue with the selected error handling: abort, cancel, or default error recovery._

\


![Originalbild anzeigen](../../../.gitbook/manual-images/assets/Image\_1473.jpg)

_NOTE_

_Exception: If the option “Default error recovery” is chosen and an error occurs for which the default is set to abort (e.g. a hardware error), the walk-away mode is left on and the dialog waits for user interaction._

1.  #### _‌Tip Pick Up and Tip Eject Smart Steps‌_

    \


    _These two Smart Steps allow picking up tips from a rack and then disposing them in the tip waste after use._

    _Below is the dialog for the “Tip Pick Up” Step._

    \


    ![image](../../../.gitbook/manual-images/assets/Image\_1474.jpg)

    \


    _The dialog is to specify a tip sequence. It is also possible to specify the tip counter. Below is the dialog for the “Tip Eject” Step._

    \


    ![image](../../../.gitbook/manual-images/assets/Image\_1475.jpg)

    \


    _For “Channel Settings” and “Error Settings_[_”, see the description of the previous Smart Steps found in_ ](pipetting-steps.md#bookmark68)_Section 3.4.2 ML STAR Smart Steps Settings._
