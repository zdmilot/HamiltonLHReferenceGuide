# Wash Station 96‌

_The Wash station 96 is an optional device for washing 96 disposable tips in parallel. The tips are washed both outside and inside at the same time: on the outside in the wash chamber of the wash station 96 and on the inside by aspiration/dispense cycles with the CO-RE 96 Probe Head. The result of washing the tips depends on the wash setting._

\\

![Originalbild anzeigen](../.gitbook/manual-images/assets/Image\_1652.jpg)

_NOTE_

_If carry-over is not acceptable for the application, use new disposable tips for each aspiration step._

_The wash station 96 is no longer available. It was replaced by the wash station 96/384._

\\

_Sample transfers may be done using new disposable tips, while reagents, buffers, etc. may be distributed with washed tips._

_The picture below shows a complete, fully connected wash station 96:_

\\

![186380\_a](../.gitbook/manual-images/assets/Image\_1653.jpg)

_a)_

1. _Washer unit 96_
2. _b) Pump unit P and tubing_
3. _Waste container_
4. _Wash solution container_

\\

_c) d)_

_Liquid level sensors inside the washer unit prevent flooding of the system. On the other hand, the washer unit recognizes if there is not enough liquid to fill the wash chamber._

\\

![Originalbild anzeigen](../.gitbook/manual-images/assets/Image\_1654.jpg)

_NOTE_

_There is no liquid level sensor in the waste container. In case of refilling the wash solution container, always empty the waste container._

_When re-using washed tips, pipetting precision may decrease by a factor of 3._

1.  #### _‌Command Description‌_

    \\

    _The table below gives a brief overview of the available commands for the wash station 96. Another possibility to wash the tips is given by the “CO-RE 96 Head Dispense” Basic Step Command. In the Basic dispense step, the wash function via the “Wash tips after dispense” Parameter can be enabled. The wash parameter can be set through the \[Customize…] Button._

    \\

    | Liquid Handling            |                                                                                                                                              |                                       |
    | -------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------- |
    | CO-RE 96 Probe Head        |                                                                                                                                              |                                       |
    | Command                    | Icon                                                                                                                                         | Action Performed                      |
    | CO-RE 96 Head Wash         | <p><br></p><p><img src="../.gitbook/manual-images/assets/Image_1655.jpg" alt="NewIMAGES/core96headwash.bmp" data-size="original"></p>        | Wash tips using the default settings. |
    | CO-RE 96 Head Empty Washer | <p><br></p><p><img src="../.gitbook/manual-images/assets/Image_1656.jpg" alt="NewIMAGES/core96heademptyWasher.bmp" data-size="original"></p> | Empty washer.                         |

    \\
2.  #### _‌Programming the Wash Station 96‌_

    \\

    _The following is a simple example on how to program the wash station 96 using Single Steps._

    _Please note that the CO-RE 96 Probe Head and one of the Pump Stations in the System have to be activated in the Configuration Editor._

    \\

    ![image](../.gitbook/manual-images/assets/Image\_1657.jpg)

    \\

    _Creating the Deck Layout_

    _The method requires the following Deck Layout:_

    \\

    ![image](../.gitbook/manual-images/assets/Image\_1658.jpg)

    _Add a wash station, slide waste and a standard tip carrier to the deck. Use the “Search Labware” Field to add the following labware:_

    * _“CORE\_HU\_96WashStation\_A00”_
    * _“Core\_96SlideWaste” from "ML STAR Wastes"_
    * _“TIP\_CAR\_480\_ST\_A00”_

    \\

    _Creating the Method_

    _The resulting method should look like the image shown below._

    \\

    ![image](../.gitbook/manual-images/assets/Image\_1659.jpg)

    1. _Pick up tips from the tip carrier. Set “Manually” for sequence counting to eject the tips to the pickup position (Step 2)._
    2. _In line 3, use the “CO-RE 96 Head Wash” Wash Step without modifying the default values. These values guarantee and are the basis for good wash results._
    3. _Eject the tips. Use “Eject on tip pick up position” to eject the tips back into the tip carrier._

    \\

    ![image](../.gitbook/manual-images/assets/Image\_1660.jpg)

    \\

    ![Originalbild anzeigen](../.gitbook/manual-images/assets/Image\_1661.jpg)

    _NOTE_

    _The method can be accelerated when programming the last “Refill wash chamber” Command parallel to the succeeding method steps._

    _Creating a Modified Method_

    _The method above can be modified to speed up the wash step. The last refilling command for the wash chamber has to be programmed in parallel to the tip eject step. The resulting modified method should look like the image shown below._

    \\

    ![image](../.gitbook/manual-images/assets/Image\_1662.jpg)

    _Use the “Begin Parallel” and “End Parallel” Steps to do this._

    _In the CO-RE 96 Head empty washer step, set the washer parameters to “(2) On – chamber one only” to have the maximum speed up._
3.

    ![image](../.gitbook/manual-images/assets/Image\_1663.jpg)
