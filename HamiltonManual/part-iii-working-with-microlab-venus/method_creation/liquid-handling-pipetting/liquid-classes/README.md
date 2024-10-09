# Liquid Classes

## _Concept of Liquid Classes‌_

_Liquid classes manage the background parameters for pipetting. A liquid class is a set of parameters determining the aspiration and dispensing behavior of the pipette appropriate for a given liquid, tip type, and dispense mode. For all aspiration and dispense steps a valid liquid class must be selected._

### Predefined liquid classes

_Several predefined liquid classes are supplied along with the VENUS Software for the following liquids: water, DMSO, glycerin, acetonitrile, ethanol, plasma and serum. The standard liquid classes cover a wide range of applications, and there will probably be no need to make any changes of the parameter settings to adapt the liquid class to a specific application._

### Custom liquid classes

_For special applications, a liquid class can be custom-defined. This custom liquid class can be used just like the predefined classes. Defining liquid classes independent from a method serves to simplify the steps in the method and allows the complete set of parameters to be defined once for all pipetting tasks. The liquid editor is used to display the parameters of the liquid classes and to create custom liquid classes._

***



Pipetting: In general, pipetting by the principle of air displacement (as with handheld pipettes) is sensitive to the following:

* Manner of pipetting (i.e. surface or jet, empty tip or part volume)
* Tip or needle type (geometry, tip orifice)
* Environmental effects (temperature, pressure, humidity)
* Liquid type (viscosity, evaporation)

The pipetting mode (e.g., surface or jet mode) and the liquid class determine the behavior of the instrument. Pipetting mode and liquid class represent two independent sets of information, both of which have to be specified.

<table data-header-hidden><thead><tr><th width="145"></th><th></th></tr></thead><tbody><tr><td><img src="../../../../../.gitbook/assets/image (10) (1) (1) (1) (1) (1) (1).png" alt="" data-size="original"></td><td><p>NOTE</p><p>Always use the same liquid class for one aspiration and dispense cycle. Otherwise uncalculated residual volumes may be left within the tip, or other errors regarding plunger position / movements may occur.</p></td></tr></tbody></table>

\


The liquid class stores all relevant background parameters, such as flow rates and volume corrections for one pipetting cycle, (i.e. for one aspiration and the subsequent dispense(s)). Depending on the pipetting mode chosen, only a subset of the parameters of the liquid class is active. According to the different dependencies listed above, liquid classes have attributes related to their intended use: tip type, liquid name, and dispense mode.

Different liquid classes are provided with the VENUS Software. They are optimized for different liquids, tip types, and important pipetting processes, such as aspiration followed by dispensing either to a surface or in a jet. Hamilton has optimized the standard liquid classes with great care to assure the best pipetting accuracy. To change Hamilton standard liquid classes, store the class under a different name first. For special applications, the programmer can define a liquid class to achieve the highest accuracy with the compounds and volumes of interest. The liquid classes can be adapted to the user-specific requirements.\


***



## _Liquid Details_

_The “Liquid Details” Tab, has the following editable attributes of the liquid class:_\


<details>

<summary>Liquid device</summary>



</details>

<details>

<summary>Liquid (name)</summary>



</details>

<details>

<summary>Tip (or needle) type</summary>



</details>

<details>

<summary>Dispense Mode</summary>



</details>

<details>

<summary>Liquid Parameters</summary>



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

</details>





### _‌Editing Liquid Details‌_

{% tabs %}
{% tab title="Step 1" %}
_To start the Liquid Editor, select "ML STAR Series Liquid Editor" from the “Tools” Menu of the Method Editor._

![image](../../../../../.gitbook/assets/Image\_1382.jpg)

_or Double-click the program icon found on the desktop_

![image](../../../../../.gitbook/assets/Image\_1383.jpg)

_or Open a pipetting step and use the info sign to show the liquid details._

![image](../../../../../.gitbook/assets/Image\_1384.jpg)


{% endtab %}

{% tab title="Step 2" %}
From there, open the liquid editor:

![image](../../../../../.gitbook/assets/Image\_1385.jpg)
{% endtab %}

{% tab title="Step 3" %}
_The liquid editor main window opens with a list of liquid classes as presented below._

![image](../../../../../.gitbook/assets/Image\_1386.jpg)
{% endtab %}

{% tab title="Step 4" %}
_Double-click on a liquid class. This will activate the “Edit Liquid Class” Dialog._

![image](../../../../../.gitbook/assets/Image\_1387.jpg)


{% endtab %}
{% endtabs %}





Correction Curve\



_Range Button_

1. _Click on the \[Range] Button (see image on the previous page) to see the limitations of the parameters depending on the pipetting tool._
2.  _Activate the "Correction Curve" Tab as shown below._

    \


    ![image](../../../../../.gitbook/assets/Image\_1389.jpg)
3. _A correction curve shows a target volume and a corrected volume._

_Target Volume_

_The “Target volume“ is the volume to be dispensed (the one entered in the pipetting steps)._

_Corrected Volume_

_The “Corrected volume“ is the volume that actually needs to be moved by the plunger for this purpose. In aspiration or dispense steps, the “Target volume“ which will actually be dispensed into the vessel must be entered. Corrected volumes for a desired target volume are usually determined gravimetrically._

_Correspondingly, a corrected volume of 107.2µl for a target volume of 100µl does not mean that 107.2µl of liquid will be dispensed. When the tip is emptied, 100µl are dispensed. The correction is mainly due to the properties of the air column above the liquid._

_The high flexibility of the liquid classes allows pipetting any liquid with high accuracy. Custom liquid classes are also available upon request from Hamilton’s Application Engineering Group for the customer specified applications._

\


Liquid Notes\



![image](../../../../../.gitbook/assets/Image\_1390.gif)

_Under this tab, information can be stored concerning the way the custom-made liquid class is determined. Information about the accuracy reached with this liquid class can also be stored here._

\


![Originalbild anzeigen](../../../../../.gitbook/assets/Image\_1391.jpg)

_NOTE_

_The predefined liquid classes that come along with the instrument cannot be changed by the user but they can be copied, saved under a different name and then edited._

## _‌_
