# Tips

## _1000µl-Pipetting Channels versus 5ml-Pipetting Channels‌_

_Working with the 5ml-pipetting channel on the ML STAR is almost the same as working with 1000 µl-pipetting channels. The same CO-RE technology (in a different size) is used to pick up tips and tools, cLLD and pLLD can be performed and the same pipetting features (TADM, MAD, ADC) as on the 1000µl-pipetting channels are available on the 5ml-pipetting channels._

_However, although the familiar appearance of the Single Steps and Easy Steps for the 5ml- pipetting channel are kept the same, there are some differences to keep in mind when working with the 5ml-pipetting channel._

_Pipetting: 5ml-Pipetting Channel Pattern_

_Due to its large capacity, the 5ml-pipetting channel needs more space on the y-rail. Therefore, the closest distance from one tip end to the neighbor tip end is 18 mm (this is true if the pipetting channels are mounted on a double rail arm. On a single rail arm, the distance is 36 mm). This has an influence on the sequence, for example, on plates._

_Using the stamp tool for the 5ml-pipetting channel, a sequence on a plate will look like this:_

\


![image](../../.gitbook/manual-images/assets/Image\_623.png)

\


_This means that four 5ml-pipetting channels can work in parallel on a landscape plate._

\


_Pipetting: Well / Tube Diameter_

_Depending of the immersion depth, the 5ml-pipetting channel may collide with well or tube walls. See image guide below for useable diameters and heights to avoid hardware crashes._

\


![ep](../../.gitbook/manual-images/assets/Image\_624.jpg) ![image](../../.gitbook/manual-images/assets/Image\_625.png)





## _Tip Handling Details‌_

\


_This section discusses essential tip handling topics. Although the process of tip handling is stable and safe, some precautions must be considered when handling with special labware._

_VENUS Software offers a tip recognition feature based on the different tip geometries. It is available for both disposables and needles and it is activated during installation by a Service Engineer. This feature increases the ML STAR instrument´s security, especially when different tip types (e.g. low- and standard volume tips) are used. In addition, all tip racks have color-coded labels and are bar-coded to be identified by the Autoload option (if installed)._

_For distinguishing disposable CO-RE tips, 50µl and CO-RE tips and 300µl, a special library is needed. Please consult a local Hamilton Representative._

\


![Originalbild anzeigen](../../.gitbook/manual-images/assets/Image\_626.jpg)

_NOTE_

_All new or special tip types require additional settings (such as configuration file entries, liquid classes etc.) in the VENUS Software. Please consult a local Hamilton Representative for the implementation data of non-standard tips._

\


1.  #### _‌Tip Recognition with Different Tip Types on the Same Deck Layout‌_

    \


    _The tips used in a pipetting procedure must match with the suitable pipetting channel or pipetting head in order to prevent damage to the device. Proper precautions have to be taken when loading tips in order to prevent confusing with the tips or loading wrong tip types._

    _Whenever possible, use loading with Autoload and make sure that only tip carriers with the suffix …BC… (e.g. TIP\_CAR\_480BC\_ST\_A00) are used. In case of a wrong tip rack, the system, while loading will prompt an error which looks like the image shown below._

    \


    ![image](../../.gitbook/manual-images/assets/Image\_627.jpg)

    _When using another tip carrier (e.g. the 50 µl tip carrier) switch to the Deck Layout and change the properties MlStarCarBCOrientation to 1 and the MlStarCarNoReadBarcode to 0._

    \


    ![image](../../.gitbook/manual-images/assets/Image\_628.jpg) ![image](../../.gitbook/manual-images/assets/Image\_629.jpg)

    \


    _When loading manually, pay extra attention to the tip types which are similar in design and cannot be distinguished by the tip recognition feature. When CO-RE tips, 1-50µl and CO-RE tips, 10-300µl are used on the same Deck Layout, a special library is needed. Please consult a local Hamilton Representative. In addition, check the label of the tip rack. The volume of the tips can be found on the top left corner of the barcode label:_

    \


    ![image](../../.gitbook/manual-images/assets/Image\_630.png)

    \


    _When loading manually and there is no library available for distinguishing the different tip types used, visual inspection of the barcode label is the only option. This is the case for Slim Tips, 10- 300µl used in combination with CO-RE Tips, 10-1000µl._

    \


    ![Originalbild anzeigen](../../.gitbook/manual-images/assets/Image\_631.jpg)

    _NOTE_

    _Slim tips and 1000µl tips have the same head sizes therefore it can only be checked through the barcode reader._
2.  #### _‌Rocket Tips‌_

    \


    _It is possible to use Rocket Tips to pipette larger volumes than 50 µl using the CO-RE 384 Head. Rocket Tips combine a 300 µl tip body with a 4-channel head adapter._

    \


    ![Rocket\_Tip](../../.gitbook/manual-images/assets/Image\_632.png) ![TipRack\_RocketTips](../../.gitbook/manual-images/assets/Image\_633.jpg)

    \


    _To use the advantages of the Rocket Tips, the following settings have to be considered:_

    * _Use the tip mode: (1) 96 Tips / Rocket Tips in all the steps _ [_See_ ](tips.md#bookmark294)[_NOTE_](tips.md#bookmark294)
    * _Set the tip type to 300 µl Rocket Tip (96) for 384_
    *   _Use a Rocket Tip Liquid Class_

        \


        ![image](../../.gitbook/manual-images/assets/Image\_634.jpg)

        \


        _To pick up only single row(s), column(s) or a quarter:_

        \

    * _Use the reduced pattern mode: (1) Tips / Rocket tips in all the steps _ [_See_ ](tips.md#bookmark294)[_NOTE_](tips.md#bookmark294)
    * _Click the “Customize” Tab and select “Channel settings”_
    *   _Select all, one channel, quarter, row(s) or column(s), depending on the pattern that shall be used._

        _‌The picture below shows the head (not the plate) and which tips will be picked up._

        \


        ![image](../../.gitbook/manual-images/assets/Image\_635.png)

        \


        _The following is an example on how the head will be located over the plate if the plate sequence is sorted accordingly._

        \


        ![image](../../.gitbook/manual-images/assets/Image\_636.jpg)

        \


        [_For more details on the different pattern, see_ ](tips.md#bookmark193)_Section 8.2 Stamp Tool._

        \


        ![Originalbild anzeigen](../../.gitbook/manual-images/assets/Image\_637.gif)

        _‌NOTE_

        _Rocket tips can only be used on the 50 µl CO-RE 384 Probe Head. The reduced pattern mode has to be set in all pipetting steps._

        * _When using Single steps: in the Tip Pickup, Aspirate, Dispense and Tip Eject_
        * _When using Easy Steps: in the Easy Aspirate and Easy Dispense_
3.  #### _‌Tip Pick-up with the CO-RE 96 Probe Head‌_

    \


    ![image](../../.gitbook/manual-images/assets/Image\_638.png)

    ![image](../../.gitbook/manual-images/assets/Image\_639.png)

    _The multiprobe heads need more space to pick up tips than the single pipetting channels. Therefore, it is important to use an appropriate Deck Layout. This will avoid collisions at run time._

    \


    | <p>Example:</p><p>Picking up tips with the CO-RE 96 Probe Head out of e.g. the Nestable Tip Rack (NTR) will not work in the lower positions, if a high plate carrier, a wash station etc. is placed directly beside the tip carrier.</p> |
    | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
    | <p><br></p><p>Solution:</p><p>Leave a space of one track to the left and to the right of the tip carrier  See white lines.</p><p>The multiprobe heads are now able to pick up tips without collision with other carriers.</p>           |

    \


    ![Originalbild anzeigen](../../.gitbook/manual-images/assets/Image\_640.gif)

    _NOTE_

    _The same precautions have to be taken with all tip racks for the CO-RE 96 Probe Head / CO-RE 384 Probe Head and the single pipetting channels._
4.  #### _‌Nestable Tip Rack (NTR)‌_

    \


    _The Nestable Tip Rack (NTR) is designed to stack disposable tip racks which increase the amount of disposable tips by factor 4 per SBS position compared to one layer tip locations. NTRs come with 5 stacks of 4 layers each and have to be placed onto NTR Carriers of the ML STAR instrument._

    \


    ![ntr2](../../.gitbook/manual-images/assets/Image\_641.jpg) ![ntr1](../../.gitbook/manual-images/assets/Image\_642.jpg)

    \


    _Tip pick up directly from loaded NTR Carriers is basically possible. This eliminates the need for intermediate tip pickup positions since pipetting tools such as single 1000ul pipetting channels as well as MultiProbeHeads (MPH 96 and MPH 384) can pick up tips from the NTR stack in most cases._

    _A transport system (e.g. iSwap, CO-RE Gripper) is required to remove and dispose empty NTR frames away from NTR Stacks to allow access with the Pipetting Tools to the next lower layer with filled NTRs._

    _Forcing Pipetting Tools to go down to lower or to the lowest layer of the NTR stack may have limitations due to the required space between the Pipetting Tool and the neighbouring Carriers as well as its corresponding labware (also to other stacks, neighbour NTR’s, etc.). In these cases, an intermediate Tip pick up position becomes necessary. This intermediate tip pickup position is designed and available as an NTR MFX Module (MultiFlexModule, MULTIFLEX NTR 96 MODULE, and MULTIFLEX NTR 384 MODULE)._

    _The transport system as mentioned above must then be used to move NTRs to these intermediate Tip Pickup positions which enable constant tip pickup conditions in terms of the same X, Y and Z coordinates of a single NTR. Once the Tips out of the NTR frame of the intermediate tip pickup position are used up, the frame needs to be replaced by a new filled NTR._

    _When single-, row- or column wise Tip pickup is required with MultiProbeHeads, an additional tip pickup position equipped with a Tip adapter becomes necessary. The tip adapter may be positioned onto a Tip Rack Carrier as well as on a MFX Tip Module (MULTIFLEX TIP MODULE)._

    \


    _The recommended workflow would be:_

    1. _Transportation of one NTR from a loaded NTR Carrier to the intermediate Tip pickup position_
    2. _Tip pickup with MPH out of the intermediate Tip pickup position_
    3. _Tip eject into the Tip adapter_
    4. _As desired; single-, row- or column wise (shifted) Tip pickup out of the Tip adapter_
    5. _Ready for pipetting_

    ![Originalbild anzeigen](../../.gitbook/manual-images/assets/Image\_643.gif)

    _NOTE_

    _An empty NTR can be transported to the waste either by the iSWAP or the CO- RE gripper. Note that the use of the CO-RE gripper for transports to the waste needs a special library to grip the rack shifted. Otherwise it is not possible to move the rack to the default waste position on a ML STAR and ML STARlet._

    \


    [_Working with the CO-RE 96 Probe Head and Nestable Tip Racks will need some precautions (see also_ ](tips.md#bookmark295)_Section 11.6.3 Tip Pick-up with CO-RE 96 Probe Head)._

    _There is danger of collision when the CO-RE 96 Probe Head is picking up tips from lower positions if the neighboring positions are completely filled:_

    \


    ![image](../../.gitbook/manual-images/assets/Image\_644.png)

    \


    ![image](../../.gitbook/manual-images/assets/Image\_645.png)

    ![image](../../.gitbook/manual-images/assets/Image\_646.png)

    ![image](../../.gitbook/manual-images/assets/Image\_647.png)

    ![image](../../.gitbook/manual-images/assets/Image\_648.png)

    _In this case, either work from top to bottom over all stacks or transport the Nestable Tip Rack to a collision free position and pick up the tips there._

    \


    <table data-header-hidden><thead><tr><th></th><th></th><th></th><th></th><th width="205"></th><th></th><th></th><th></th><th></th><th></th></tr></thead><tbody><tr><td>Pos 1 / Rack 4</td><td></td><td>Pos 2 / Rack 4</td><td></td><td>Pos 3 / Rack 4</td><td></td><td>Pos 4 / Rack 4</td><td></td><td><p><img src="../../.gitbook/manual-images/assets/Image_649.png" alt="image"></p><p>Pos 5 / Rack 4</p></td><td><br></td></tr><tr><td>Pos 1 / Rack 3</td><td></td><td>Pos 2 / Rack 3</td><td></td><td>Pos 3 / Rack 3</td><td></td><td>Pos 4 / Rack 3</td><td></td><td><p><img src="../../.gitbook/manual-images/assets/Image_650.png" alt="image"></p><p>Pos 5 / Rack 3</p></td><td><br></td></tr><tr><td>Pos 1 / Rack 2</td><td></td><td>Pos 2 / Rack 2</td><td></td><td>Pos 3 / Rack 2</td><td></td><td>Pos 4 / Rack 2</td><td></td><td><p><img src="../../.gitbook/manual-images/assets/Image_651.png" alt="image"></p><p>Pos 5 / Rack 2</p></td><td><br></td></tr><tr><td>Pos 1 / Rack 1</td><td></td><td>Pos 2 / Rack 1</td><td></td><td>Pos 3 / Rack 1</td><td></td><td>Pos 4 / Rack 1</td><td></td><td><p><img src="../../.gitbook/manual-images/assets/Image_652.png" alt="image"></p><p>Pos 5 / Rack 1</p></td><td><br></td></tr></tbody></table>
