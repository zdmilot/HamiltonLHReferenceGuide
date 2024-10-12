# DC Needle Wash Station‌

In combination with a wash station, re-usable steel needles can be used for pipetting with the spreadable pipetting channels of the ML STAR, instead of using the disposable tips. The result of washing the needles depends on the wash setting.

<table data-header-hidden><thead><tr><th width="145"></th><th></th></tr></thead><tbody><tr><td><img src="../../.gitbook/assets/image (10) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" data-size="original"></td><td><p>NOTE</p><p><em>It is recommended to use the “Needle Pickup” SmartStep. If the “1000μl Channel Tip Pick Up” Single Step is used, a “1000μl Channel Wait for Needle Wash” Step has to be programmed before the tip pick up step.</em></p><p><em>With the Easy Step ASPIRATE, the needle pick up is also possible.</em></p><p><em>With the Easy Step DISPENSE, needle eject and start washing is also possible.</em></p></td></tr></tbody></table>



Sample transfers may be done using new disposable tips, while reagents, buffers, etc. may be distributed with needles.

The picture below shows a complete, hooked-up DC needle wash station:

<figure><img src="../../.gitbook/assets/image (73) (1).png" alt=""><figcaption></figcaption></figure>

The DC needle wash station does not allow parallel washing and pipetting. Liquid level sensors inside the washer unit prevent flooding of the system. The washer unit recognizes if there is not enough liquid to fill the wash chamber.

The DC needle wash station consists of 32 positions for needles. Two different sets of needles can be used simultaneously. All types of needles (10 µl, 300 µl and 1000 µl) can be washed.

<table data-header-hidden><thead><tr><th width="145"></th><th></th></tr></thead><tbody><tr><td><img src="../../.gitbook/assets/image (10) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" data-size="original"></td><td><p>NOTE</p><p><em>There is no liquid level sensor in the waste container. Always empty the waste container in refilling the wash solution container.</em></p></td></tr><tr><td><img src="../../.gitbook/assets/image (10) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" data-size="original"></td><td><p>NOTE</p><p><em>The DC Needle Wash Station is no longer available.</em></p></td></tr></tbody></table>



## Command Description

The commands for the DC needle wash station are functions of the library “HSLMlStarDcWashstationLib”.

| Command                 | Icon                                                                             | Action Performed                     |
| ----------------------- | -------------------------------------------------------------------------------- | ------------------------------------ |
| Wash Settings           | <img src="../../.gitbook/assets/image (78) (1).png" alt="" data-size="original"> | Sets wash parameters.                |
| Needle Wash             | <img src="../../.gitbook/assets/image (75) (1).png" alt="" data-size="original"> | Starts the wash step.                |
| Needle Wash2            | <img src="../../.gitbook/assets/image (76) (1).png" alt="" data-size="original"> | Starts the wash step.                |
| Empty Fill Wash Chamber | <img src="../../.gitbook/assets/image (77) (1).png" alt="" data-size="original"> | Empties or refills the wash chamber. |



## Programming the DC Needle Wash Station

To create a method using needle washing with the DC needle wash station, follow these steps:

1. Create a new method called DC\_WashstationDemo.
2.  Add the template for the DC needle wash station: _Car\_DC\_WashStation\_CR\_Needle\_A01_ to the layout.

    <figure><img src="../../.gitbook/assets/image (80) (1).png" alt="" width="375"><figcaption></figcaption></figure>

    The following sequences belong to the template of the DC needle wash station:\


    <table><thead><tr><th width="67">Pos</th><th>Sequence Name</th><th>Use</th></tr></thead><tbody><tr><td>1</td><td>waste_dc_washstation_0001</td><td>Dispensing the rest volume before the needle wash (empty tip).</td></tr><tr><td>2</td><td>waste_dc_washstation_0002</td><td>Dispensing the rest volume before the needle wash (empty tip).</td></tr><tr><td>3</td><td>washchamber_dc_washstation_0001</td><td>Washing the needles.</td></tr></tbody></table>


3.  Add the needle sequence (according to the used needles and the Node ID setting of the pump unit and washer unit) to the template of the DC needle wash station. The needle sequence corresponds to the position (for picking up/ releasing) of the needles.\
    \
    E.g. _DC 300μl needles rack (HU)_\
    \


    <figure><img src="../../.gitbook/assets/image (81) (1).png" alt=""><figcaption><p><em>HU, HW and HV are the node (ID-) names of the corresponding pump unit</em> </p></figcaption></figure>



4. Switch to the method and add the HSLMlStarDcWashstationLib library.
5. Program a similar method like for the CR-Washstation. Use the help file of the HSL Library.
6. Recommended wash settings and typical carry-over:



| 300µl needle (Asp./disp 100µl fluorescein solution 2g/100ml PBS; wash solution deionized water)           | Result                                                                          |
| --------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- |
| <p>Wash volume: 300µl<br>Wash cycles: 2<br>Mix cycles: 3<br>Soak time: 0 sec<br>Immersion depth: 5 mm</p> | <p>Duration: 45 sec<br>Water consumption: 125 ml<br>Carryover: > 4.0 x 10-5</p> |
| <p>Wash volume: 300µl<br>Wash cycles: 3<br>Mix cycles: 3<br>Soak time: 0 sec<br>Immersion depth: 5 mm</p> | <p>Duration: 70 sec<br>Water consumption: 250 ml<br>Carryover: > 3.0 x 10-6</p> |

\
