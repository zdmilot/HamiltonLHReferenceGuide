# Speed Up cLLD Detection‌

Using the cLLD (capacitive Liquid Level Detection) can cause extended pipetting time when used on labware with high walls. The reason is that, the cLLD search starts at the LLD Search height which is defined in the labware, normally very close to the upper border.&#x20;

Having only small amounts of liquid in such labware, the pipetting channel starts almost at the upper border and travels a long way down to find liquid (see picture below with the “first pipette” label).&#x20;

<figure><img src="../../.gitbook/assets/image (184).png" alt=""><figcaption></figcaption></figure>

Using the “Speed up cLLD detection” Function, the following aspirate / dispense steps will use a calculated height from the previously detected level. This reduces the total time for pipetting due to the decreased search time.&#x20;

To enable Speed up cLLD detection apply the following settings.&#x20;

Set the Sample Tracking in the System Configuration Editor (system settings) to ON.&#x20;

_Set the Speed up cLLD Detection in the System Configuration Editor (instrument) to ON._

![image](../../.gitbook/assets/Image\_670.png)

\


_Make sure that the labware is higher than 40mm. The smaller labware will not benefit from this feature._

_Make sure to use the cLLD in the desired steps (aspiration and/or dispense)._

\


![Originalbild anzeigen](../../.gitbook/assets/Image\_671.gif)

_NOTE_

_The system will calculate the amount of liquid in the tube when using the instrument. That means, when pipetting into a tube with pipetting channels, CO- RE 96 Probe Head or other pipetting devices, the level will be adapted to the new height._

_If the tube is filled up manually, the level is NOT adapted. The cLLD search in the liquid may start already and prompt an “Unexpected liquid found” error message._
