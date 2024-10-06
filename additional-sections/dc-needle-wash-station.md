# DC Needle Wash Station‌

*   _In combination with a wash station, re-usable steel needles can be used for pipetting with the spreadable pipetting channels of the ML STAR, instead of using the disposable tips. The result of washing the needles depends on the wash setting._

    \


    ![Originalbild anzeigen](../.gitbook/assets/Image\_1641.jpg)

    _NOTE_

    _It is recommended to use the “Needle Pickup” SmartStep. If the “1000μl Channel Tip Pick Up” Single Step is used, a “1000μl Channel Wait for Needle Wash” Step has to be programmed before the tip pick up step._

    _With the Easy Step ASPIRATE, the needle pick up is also possible._

    _With the Easy Step DISPENSE, needle eject and start washing is also possible._

    \


    _Sample transfers may be done using new disposable tips, while reagents, buffers, etc. may be distributed with needles._

    _The picture below shows a complete, hooked-up DC needle wash station:_

    \


    ![DC-Wash station](../.gitbook/assets/Image\_1642.jpg)

    _b)_

    _a)_

    1.  _DC Washer Unit_

        1. _Pump Unit P and Tubing_
        2. _Wash Solution Container_
        3. _Waste Container_

        \


        _c) d)_

        \


        _The DC needle wash station does not allow parallel washing and pipetting. Liquid level sensors inside the washer unit prevent flooding of the system. The washer unit recognizes if there is not enough liquid to fill the wash chamber._

        _The DC needle wash station consists of 32 positions for needles. Two different sets of needles can be used simultaneously. All types of needles (10 µl, 300 µl and 1000 µl) can be washed._

        \


        ![Originalbild anzeigen](../.gitbook/assets/Image\_1643.jpg)

        _NOTE_

        _There is no liquid level sensor in the waste container. Always empty the waste container in refilling the wash solution container._

        ![Originalbild anzeigen](../.gitbook/assets/Image\_1644.jpg)

        _NOTE_

        _The DC Needle Wash Station is no longer available._

        \


        1.  ### _‌Command Description‌_

            \


            _The commands for the DC needle wash station are functions of the library “HSLMlStarDcWashstationLib”._

            \


            <table data-header-hidden><thead><tr><th width="660"></th><th></th><th></th></tr></thead><tbody><tr><td>HSLMlStarDcWashstationLib:</td><td></td><td></td></tr><tr><td>Command</td><td>Icon</td><td>Action Performed</td></tr><tr><td>Wash Settings</td><td><p><br></p><p><img src="../.gitbook/assets/Image_1645.jpg" alt="DCSet"></p></td><td>Sets wash parameters.</td></tr><tr><td>Needle Wash</td><td><p><br></p><p><img src="../.gitbook/assets/Image_1646.jpg" alt="DCwash"></p></td><td>Starts the wash step.</td></tr><tr><td>Needle Wash2</td><td><p><br></p><p><img src="../.gitbook/assets/Image_1647.jpg" alt="DCwash"></p></td><td>Starts the wash step.</td></tr><tr><td>Empty Fill Wash Chamber</td><td><p><br></p><p><img src="../.gitbook/assets/Image_1648.jpg" alt="DCrefill"></p></td><td>Empties or refills the wash chamber.</td></tr></tbody></table>

            \

        2.  ### _‌Programming the DC Needle Wash Station‌_

            \


            _To create a method using needle washing with the DC needle wash station, follow these steps:_

            1.  _Create a new method called DC\_WashstationDemo._

                ![image](../.gitbook/assets/Image\_1649.png)

                _2_

                _1_

                _3_
            2.  _Add the template for the DC needle wash station: Car\_DC\_WashStation\_CR\_Needle\_A01 to the layout._

                _The following sequences belong to the template of the DC needle wash station:_

                \


                | Pos | Sequence Name                      | Use                                                            |
                | --- | ---------------------------------- | -------------------------------------------------------------- |
                | 1   | waste\_dc\_washstation\_0001       | Dispensing the rest volume before the needle wash (empty tip). |
                | 2   | waste\_dc\_washstation\_0002       | Dispensing the rest volume before the needle wash (empty tip). |
                | 3   | washchamber\_dc\_washstation\_0001 | Washing the needles.                                           |

                \

            3.  _Add the needle sequence (according to the used needles and the Node ID setting of the pump unit and washer unit) to the template of the DC needle wash station. The needle sequence corresponds to the position (for picking up/ releasing) of the needles._

                _E.g. DC 300μl needles rack (HU)_

                \


                ![image](../.gitbook/assets/Image\_1650.jpg) ![image](../.gitbook/assets/Image\_1651.gif)

                _HU, HW and HV are the node (ID-) names of the corresponding pump unit_

                \

            4. _Switch to the method and add the HSLMlStarDcWashstationLib library._
            5. _Program a similar method like for the CR-Washstation. Use the help file of the HSL Library._
            6. _Recommended wash settings and typical carry-over:_

            \


            | <p>300µl needle</p><p>(Asp./disp 100µl fluorescein solution 2g/100ml PBS; wash solution deionized water)</p> | Result |                    |              |
            | ------------------------------------------------------------------------------------------------------------ | ------ | ------------------ | ------------ |
            | Wash volume:                                                                                                 | 300µl  | Duration:          | 45 sec       |
            | Wash cycles:                                                                                                 | 2      | Water consumption: | 125 ml       |
            | Mix cycles:                                                                                                  | 3      | Carryover:         | > 4.0 x 10-5 |
            | Soak time:                                                                                                   | 0 sec  | <p><br></p>        | <p><br></p>  |
            | Immersion depth:                                                                                             | 5 mm   | <p><br></p>        | <p><br></p>  |
            | Wash volume:                                                                                                 | 300µl  | Duration:          | 70 sec       |
            | Wash cycles:                                                                                                 | 3      | Water consumption: | 250 ml       |
            | Mix cycles:                                                                                                  | 3      | Carryover:         | > 3.0 x 10-6 |
            | Soak time:                                                                                                   | 0 sec  | <p><br></p>        | <p><br></p>  |
            | Immersion depth:                                                                                             | 5 mm   | <p><br></p>        | <p><br></p>  |
* ##
