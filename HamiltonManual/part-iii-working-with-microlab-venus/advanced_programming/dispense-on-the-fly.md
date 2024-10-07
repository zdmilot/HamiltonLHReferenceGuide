# Dispense on the Fly

_VENUS Software offers a dispense on the fly (Single Step). This step does not stop the x- movement while pipetting which allows a very fast dispensing of liquid, e.g. to fill a plate with reagent._

\


![image](../../.gitbook/manual-images/assets/Image\_612.png)

_ATTENTION_

_This feature is available for 1000µl-pipetting channels and for 5ml-pipetting channels._

\


_Refer to the dialog box shown below while reading this section. The following parameters of the dialog box must be filled._

_Sequence_

_The sequence positions where to dispense the previously aspirated liquid._

_Sequence Counting_

_Select “Automatic” to update the current position of the sequence or choose “Manually” to not adjust the current position of the sequence._

_Volume_

_The volume that shall be dispensed per well. Note: The volume per pipetting channel is constant._

_Dispense on the Fly Mode_

_Complete plate will sort the sequence accordingly._

_Sequence order uses a sorted sequence (must fit to the selected pipetting channel pattern)._

_Labware Surface Distance_

_The position above the labware surface where the liquid is dispensed (travelling height)._

_X-Speed During Dispense_

_This value specifies the x-move speed. This value is dependent on the volume to be dispensed, the flow rate in the liquid class and the distance between the wells._

_Start X-Offset_

_The dispense normally starts in the center of the well. For larger volumes, shift the start point to the left to make sure the full volume is dispensed into the well._

![image](../../.gitbook/manual-images/assets/Image\_613.jpg)

_The display below shows distances to be specified._

\


![image](../../.gitbook/manual-images/assets/Image\_614.gif)

\


_In the Advanced section, the following parameters can be changed. Please refer to the image below whil reading this section._

_Liquid Class_

_It is possible to use a different liquid class than in the aspirations step_

_X-Acceleration Distance Before First Shoot_

_The distance at which speed for pipetting should be reached (see graphic above)._

_Dispense Direction_

_Choose “Serpentine” (for quick dispense) or “From left only”_

_Exclude Labware Positions_

_This option allows to not dispense to specified positions._

![image](../../.gitbook/manual-images/assets/Image\_615.jpg)

\


_Example: A1 / B1 must be left empty since it is a blank position on the reader plate._

_Add a separate dispense step after dispense on the fly, using the dispense mode ‘Drain tip in jet mode’ to dispense the rest of the volume out of the tip._

\


![Originalbild anzeigen](../../.gitbook/manual-images/assets/Image\_616.gif)

_NOTE_

_Make sure that the liquid class in the aspiration is set to DispenseJet Part Volume, otherwise the “Dispense on the Fly” Step will show an error._

_Run some tests on the instrument to properly adjust the x-speed during dispense. Set the value to “0” to let VENUS calculate the x-speed._

_The x-speed during dispense depends on the volume, the liquid class parameters and the labware geometry._

\


![image](../../.gitbook/manual-images/assets/Image\_617.gif)

_A table guide to find the correct settings. Liquid: Water_

_Tip Size: High volume 1000ul, no filter_

_Liquid Class:High\_Volume\_Water\_DispenseJet\_Part Shots per pipetting channel: 12 (full plate)_

![Originalbild anzeigen](../../.gitbook/manual-images/assets/Image\_618.gif)

_NOTE_

_Different tip sizes, liquid classes and shoot numbers may require different settings._
