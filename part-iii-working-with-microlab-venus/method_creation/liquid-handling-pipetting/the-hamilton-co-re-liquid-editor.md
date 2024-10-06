# The Hamilton CO-RE Liquid Editor‌

### _The Hamilton CO-RE Liquid Editor‌_

\


1.  #### _‌Concept of Liquid Classes‌_

    \


    _Liquid classes manage the background parameters for pipetting._

    _Definition_

    _A liquid class is a set of parameters determining the aspiration and dispensing behavior of the pipette appropriate for a given liquid, tip type, and dispense mode. For all aspiration and dispense steps a valid liquid class must be selected._

    _Predefined liquid classes_

    _Several predefined liquid classes are supplied along with the VENUS Software for the following liquids: water, DMSO, glycerin, acetonitrile, ethanol, plasma and serum. The standard liquid classes cover a wide range of applications, and there will probably be no need to make any changes of the parameter settings to adapt the liquid class to a specific application._

    _Custom liquid classes_

    _For special applications, a liquid class can be custom-defined. This custom liquid class can be used just like the predefined classes._

    _Defining liquid classes independent from a method serves to simplify the steps in the method and allows the complete set of parameters to be defined once for all pipetting tasks._

    _The liquid editor is used to display the parameters of the liquid classes and to create custom liquid classes._

    \

2.  #### _‌Editing Liquid Details‌_

    \


    1.  _To start the Liquid Editor, select "ML STAR Series Liquid Editor" from the “Tools” Menu of the Method Editor._

        \


        ![image](../../../.gitbook/assets/Image\_1382.jpg)

        _or_
    2.  _Double-click the program icon found on the desktop_

        \


        ![image](../../../.gitbook/assets/Image\_1383.jpg)

        _or_
    3.  _Open a pipetting step and use the info sign to show the liquid details._

        \


        ![image](../../../.gitbook/assets/Image\_1384.jpg)

        \

    4.  _From there, open the liquid editor:_

        \


        ![image](../../../.gitbook/assets/Image\_1385.jpg)
    5.  _The liquid editor main window opens with a list of liquid classes as presented below._

        \


        ![image](../../../.gitbook/assets/Image\_1386.jpg)

        \

    6.  _Double-click on a liquid class. This will activate the “Edit Liquid Class” Dialog._

        \


        ![image](../../../.gitbook/assets/Image\_1387.jpg)

        _Liquid Details_

        _The “Liquid Details” Tab has two sections. In the image on the previous page, the following attributes of the liquid class are shown:_

        * _Liquid device_
        * _Liquid (name)_
        * _Tip (or needle) type_
        *   _Dispense mode._

            _The image below shows the parameters of a liquid class:_

            \


            ![PM\_361\_liquid\_parameters](../../../.gitbook/assets/Image\_1388.gif)

            \


            _Liquid Parameters_

            _The liquid parameters section shows the appropriate instrument parameters for aspirating and dispensing._

            _Here is what the various parameters mean:_
        * _“Flow Rate” and “Mix Flow Rate” are volume flows of liquid in µl/s; they correspond to plunger speeds for aspirating, dispensing and mixing._
        * _“Air Transport Volume”: air for transport is aspirated at the end of the aspirate and/or dispense step and automatically dispensed again as an extra volume in the first part of the dispense step._
        * _“Blowout Volume”: blow-out air is taken up first during aspiration. If dispensing will later be done using the “Empty tip” Dispense Mode, the entire volume including blow-out air is dispensed in the dispense step._
        * _“Swap Speed” is the speed at which the dispensing head (single pipetting channel, CO-RE 96 Probe Head or CO-RE 384 Probe Head) is drawn up out of the liquid._
        * _“Settling Time” is the time the dispensing head has to wait in the liquid after aspiration/dispense until it begins to withdraw._
        * _“Over-Aspirate Volume” is a kind of pre-wetting volume: on aspirating e.g. 20µl of liquid, first more than 20µl is aspirated (20µl + Over-asp. vol.), so as to pre-wet the tip. Then this volume is dispensed again immediately (still in the aspirate step)._
        * _“Clot Retract Height”: a parameter for recognizing clots which determines how high the dispensing head is allowed to travel up out of the liquid if there is a residual cLLD signal after aspiration. It is measured in mm from the height of the liquid surface upwards. If this distance is exceeded, an error message is generated._
        * _“Stop Flow Rate”: dispensing speed of the plunger (expressed as a stream of liquid volume in µl/s), at which the dispense step terminates abruptly. If the “Dispense flow rate“ is equal to the “Stop flow rate“, the dispense breaks off abruptly after dispensing the volume without slowing down beforehand. If the “Stop flow rate“ is set to its minimum permitted value, the plunger movement becomes gradually slower during the dispense until it stops._
        * _“Stop Back Volume”: volume which is aspirated again immediately after dispensing “Jet Part Volume” Mode. This volume is aspirated automatically as quickly as possible in order to have a cut-off of the liquid flow._
        * _“Pressure LLD Sensitivity”: Default value for the pressure LLD sensitivity to be used in aspiration steps. Determined by the liquid._
        * _“Max Height Difference”: Default tolerated maximum height difference in mm between pressure and capacitive LLD if both are activated during aspiration._

    \


    _Range Button_

    1. _Click on the \[Range] Button (see image on the previous page) to see the limitations of the parameters depending on the pipetting tool._
    2.  _Activate the "Correction Curve" Tab as shown below._

        \


        ![image](../../../.gitbook/assets/Image\_1389.jpg)
    3. _A correction curve shows a target volume and a corrected volume._

    _Target Volume_

    _The “Target volume“ is the volume to be dispensed (the one entered in the pipetting steps)._

    _Corrected Volume_

    _The “Corrected volume“ is the volume that actually needs to be moved by the plunger for this purpose. In aspiration or dispense steps, the “Target volume“ which will actually be dispensed into the vessel must be entered. Corrected volumes for a desired target volume are usually determined gravimetrically._

    _Correspondingly, a corrected volume of 107.2µl for a target volume of 100µl does not mean that 107.2µl of liquid will be dispensed. When the tip is emptied, 100µl are dispensed. The correction is mainly due to the properties of the air column above the liquid._

    _The high flexibility of the liquid classes allows pipetting any liquid with high accuracy. Custom liquid classes are also available upon request from Hamilton’s Application Engineering Group for the customer specified applications._

    \


    _Liquid Notes_

    \


    ![image](../../../.gitbook/assets/Image\_1390.gif)

    _Under this tab, information can be stored concerning the way the custom-made liquid class is determined. Information about the accuracy reached with this liquid class can also be stored here._

    \


    ![Originalbild anzeigen](../../../.gitbook/assets/Image\_1391.jpg)

    _NOTE_

    _The predefined liquid classes that come along with the instrument cannot be changed by the user but they can be copied, saved under a different name and then edited._
3.  #### _‌Defining a Custom Liquid Class‌_

    \


    _To define a custom liquid class, for instance, for a new liquid:_

    1.  _Select a predefined liquid class in the liquid editor main window_

        \


        ![image](../../../.gitbook/assets/Image\_1392.jpg)

        \

    2.  _From the Liquid Class Menu, click “Create”._

        \


        ![image](../../../.gitbook/assets/Image\_1393.jpg)

        \

    3. _Enter the name of the new custom liquid class and click \[OK]._
    4. _Back in the liquid editor main window, select the new liquid class and click \[Open]._
    5. _Changes can be made, now that all the parameter input fields in the liquid details window are already enabled._
4.  #### _‌Importing and Exporting Liquid Classes‌_

    \


    _Liquid classes are stored in a database file. Opening the liquid editor loads liquids defined in the standard liquid database file (...\Hamilton\Config\ML\_STARLiquids.mdb). If other liquids are needed from another liquid configuration file, they can be imported._

    \


    _To Import a Liquid:_

    1.  _Click “File  Import Liquid Classes...” in the liquid editor start window:_

        \


        ![image](../../../.gitbook/assets/Image\_1394.jpg)

        \

    2.  _After doing so, the “Import Liquid(s)” Window will be prompted._

        \


        ![image](../../../.gitbook/assets/Image\_1395.jpg)
    3.  _Click the \[Open file...] Button to open the desired liquid database (in .mdb format)._

        \


        ![image](../../../.gitbook/assets/Image\_1396.jpg)

        \

    4. _In the left window, all liquids of the database to be imported are listed._
    5. _Click on the list to select the required liquids._
    6.  _Click on \[>>] to select single liquid classes or use the \[Add all] Button._

        \


        ![image](../../../.gitbook/assets/Image\_1397.jpg)

        \

    7. _The selected liquid classes appear in the right window._
    8. _To import all the liquids selected in the right window, click \[OK]._
    9. _In addition, a similar dialog is available for exporting liquid classes to the configuration files. This dialog is accessed by clicking on “File  Export Liquid Classes...”._
