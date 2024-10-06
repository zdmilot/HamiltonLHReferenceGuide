# From Aspiration to Dispense

This section describes the processes involved in a simple pipetting step. These phases are:

* Movement to pick-up position
* Tip pick-up
* Movement to source position
* Aspiration
* Movement to target position
* Dispense
* Movement to drop-off position and
* Tip drop-off

Although they are also important, the movement phases are not described in details here.

\


1.  #### ‌Tip Pick-Up‌

    \


    The first task of the ML STAR is to pick up a disposable tip or a reusable steel needle.

    For disposable tips, special carriers (typically holding 5 tip racks of 96 tips each) are placed on the instrument deck.

    Steel needles can be picked up directly from the wash station or from a separate needle rack.

    The tip pick-up of the individual pipetting channels can happen simultaneously or one by one, as specified by the programmer.

    \

2.  #### ‌Aspiration‌

    \


    Blow out air

    The first step within an aspiration and dispense cycle is to aspirate a variable amount of “blow-out” air, which is used at the end of the (last) dispense, to blow all the liquid out of the tip. This is done with the tips still in the air.

    \


    Aspirate position

    The most important condition for a successful aspiration is to make sure that the tip dips into the liquid. Another important point is to prevent the tip from withdrawing from the liquid during the complete aspiration step.

    To make a good contact between the tip and the liquid, three positioning modes are available:

    * Moving the tip to a fixed height: For this, the exact height of the liquid surface has to be known in advance.
    * Using the capacitive Liquid Level Detection (cLLD): For conductive liquids, capacitive LLD should be used. Please make sure conductive (black) tips are used.
    * Using the pressure Liquid Level Detection (pLLD): For non-conductive liquids, or in case of an insufficient electrical coupling between container bottom and carrier, pressure LLD should be used.

    ![Originalbild anzeigen](../../../.gitbook/assets/Image\_1358.jpg)

    NOTE

    The capacitive Liquid Level Detection is available on the 1000μl- and 5ml- pipetting channels, the CO-RE 96, the CO-RE 96 TADM and the CO-RE 384 Probe Head. The pressure LLD is only available on the 1000μl-pipetting channels and 5ml-pipetting channels.

    \


    Fixed height

    [For the fixed height, a value must be chosen which ensures that the tip is permanently below the liquid level. The programmer must prevent aspiration of air instead of liquid. See ](from-aspiration-to-dispense.md#bookmark410)[Following ](from-aspiration-to-dispense.md#bookmark410)the[ ](from-aspiration-to-dispense.md#bookmark410)Liquid Level below.

    \


    Liquid Level Detection, LLD

    Vigorously and with more care, the liquid level of the vessel to be aspirated from can be detected. This can be provided by the Microlab STAR Liquid Level Detection (LLD) feature based on either capacitive (cLLD) or pressure (pLLD) signal detection.

    \


    Capacitive Liquid Level Detection, cLLD

    If conductive liquids are to be pipetted, Hamilton recommends using the advantage of the capacitive LLD. The sensitivity of the capacitive LLD that is to be used depends on the vessel size and the conductivity (or polarity) of the liquid that is to be detected. For a solution of 0.1% NaCl in distilled water, the required sensitivities are:

    \


    | <p>cLLD</p><p>setting</p> | Sensitivity level | Vessel                                               |
    | ------------------------- | ----------------- | ---------------------------------------------------- |
    | 1                         | Very High         | 384-well plates                                      |
    | 2                         | High              | 96-well round-bottom plates                          |
    | 3                         | Medium            | 96-well flat-bottom plates                           |
    | 4                         | Low               | Tubes, reagent reservoirs or any other large vessels |

    \


    The following table gives the minimum volume a single pipetting channel can detect in various containers for the capacitive Liquid Level Detection.

    \


    | Labware                           | Vmin \[µl] | Carrier            |
    | --------------------------------- | ---------- | ------------------ |
    | Tubes, 16 mm x 100 mm             | 200        | SMP\_CAR\_24       |
    | Tubes, 12 mm x 75 mm              | 150        | SMP\_CAR\_32       |
    | Eppendorf tubes 1.5 ml            | 50         | SMP\_CAR\_32\_EPIL |
    | Eppendorf tubes 0.5 ml            | 50         | SMP\_CAR\_32\_EPIS |
    | 96-well PCR plate                 | 50         | PLT\_CAR\_L5PCR    |
    | 96-well flat-bottom microplate    | 75         | PLT\_CAR\_L5MD     |
    | 384-well flat-bottom microplate   | 50         | PLT\_CAR\_L5MD     |
    | 96-deep well microplate (archive) | 150        | PLT\_CAR\_L5AC     |

    ![Originalbild anzeigen](../../../.gitbook/assets/Image\_1359.jpg)

    NOTE

    Using an ionic buffer in the assay in place of distilled water may help to overcome Liquid Level Detection problems.

    Use only original Hamilton labware carriers, disposables or needles. For a proper capacitive Liquid Level Detection, a sufficient conductive coupling of carrier and labware (tubes or microplates) is crucial.

    \


    Pressure Liquid Level Detection, pLLD

    When pipetting non-conductive liquids or in the case of an insufficient electrical coupling between the container bottom and the carrier, Hamilton recommends to use the advantage of pressure LLD.

    \


    ![Originalbild anzeigen](../../../.gitbook/assets/Image\_1360.jpg)

    NOTE

    Pressure LLD only works with new and empty tips. The suitable settings depend on the tip size and on the type of liquid.

    \


    Settings available for example, the 1000µl-pipetting channels:

    \


    | pLLD Setting | Sensitivity level | Tip      | Liquid                           |
    | ------------ | ----------------- | -------- | -------------------------------- |
    | 1            | Very High         | Standard | Low boiling point, low viscosity |
    | 2            | High              | High     | Low boiling point, low viscosity |
    | 3            | Medium            | Standard | Water or higher viscosity        |
    | 4            | Low               | High     | Water or higher viscosity        |

    In the case of aspiration from foaming liquids, capacitive Liquid Level Detection in particular may not detect the surface properly. As an alternative, try pressure LLD, or a combination of both. If a combination of both LLD types is used, the maximum height difference between the two independent LLDs can be used as a parameter.

    \


    Submerge Depth

    Once the liquid surface is detected, an additional immersion depth of 2mm (specified by default) is used to prevent the aspiration of air.

    \


    ‌Following the Liquid Level

    The tip follows the decreasing liquid level (specified by default) according to the aspirated volume. The distance covered while following the liquid level is computed from the known geometry of the liquid container.

    \


    Swap Speed

    In order to prevent droplets at the tip/needle orifice, the pipetting channel is moving at a slow speed out of the liquid.

    Transport Air

    After pulling out of the liquid and before moving to the target container, a variable amount of transport air is aspirated to prevent droplet formation.

    ![image](../../../.gitbook/assets/Image\_1361.png)

    At the end of an aspiration step the situation in the tip is as shown below.

    \


    Air of the system

    \


    Blow out air

    \


    Liquid Transport air

    \


    When using a fixed height aspiration (or dispense), the position of the transport air intake can be defined by the parameter “Retract distance for transport air”. Using this value makes sure that the tip’s end is out of liquid before aspirating the transport air.

    \


    ![image](../../../.gitbook/assets/Image\_1362.jpg)
3.  #### ‌Dispense‌

    \


    At the end of the aspiration step, transport air has been aspirated. The first step of the dispensing procedure is to search for the liquid surface or to move to a fixed height.

    Dispensing of the liquid may occur with three different modes:

    * Either onto/into a (liquid) surface
    * In a free jet
    *   Onto the side of the well

        \


        ![image](../../../.gitbook/assets/Image\_1363.png)

        \

    * In order to ensure that the specified accuracy is achieved, volumes below 20µl should always be dispensed onto or into a (liquid) surface. For dispensing at liquid surface, use cLLD to detect the position of the surface and then dispense while following the rising liquid level.
    * When the liquid level is known, dispensing from a fixed height while following the rising liquid level is also possible.
    * For volumes larger than 20µl, the liquid can be dispensed in a jet without touching the surface. To dispense in a jet, specify a position a few millimeters above the surface and dispense following the rising liquid level. For dispensing in a jet low volume, a varying amount of blow- out air is used to make sure that all liquid is dispensed from the tip.
    * If only a part of the liquid is dispensed with the jet mode, a stop back volume can be aspirated at the end of the dispense action. This will improve the droplet cut-off at the end of each dispense. In the last step of the dispense procedure, before any x- or y-movement occurs, a variable amount of transport air is aspirated to prevent droplet formation. The transport air is aspirated with the tip above the liquid surface.

    ![image](../../../.gitbook/assets/Image\_1364.png)

    1

    2

    3

    4

    The “Surface Part Volume” Dispensing Mode works as follows:

    \


    \


    1. When the target well is reached, the pipetting channel starts searching for the liquid surface (cLLD).
    2. At an immersion depth of 2 mm (default setting), transport air and liquid (part volume) are dispensed.
    3. The pipetting channel moves with swap speed to a distance of 5mm (default retract distance) above liquid level.
    4. Aspiration of the transport air.

    ![image](../../../.gitbook/assets/Image\_1365.png)

    1

    2

    3

    4

    The “Jet Part Volume” Dispensing Mode works as follows:

    \


    1. When the target well is reached, the pipetting channel starts to move to the fixed height (dispensing height).
    2. At the dispensing height the transport air and liquid (part volume) are dispensed while the pipetting channel is moving up in z-direction (following the liquid level).
    3. The pipetting channel moves up.
    4. Aspiration of the transport air.

    ![image](../../../.gitbook/assets/Image\_1366.png)

    1

    2

    3

    4

    The “Jet Empty Tip” Dispensing Mode works as follows:

    \


    \


    1. When the empty target well is reached, the pipetting channel moves to a fixed height (e.g. 2 mm above the bottom of the well).
    2. Transport air and liquid are dispensed while the pipetting channel is moving up in z-direction (following the liquid level).
    3. The blow out volume is dispensed: empty tip.
    4. The pipetting channel moves up, and then the aspiration of transport air follows.

    ![image](../../../.gitbook/assets/Image\_1367.png)

    1

    2

    3

    4

    The “Surface Empty Tip” Dispensing Mode works as follows:

    \


    \


    1. When the target well is reached, the pipetting channel starts searching for the liquid surface (cLLD).
    2. At an immersion depth of 2 mm (default setting), transport air and liquid are dispensed while the pipetting channel is moving up in z-direction (following the liquid level).
    3. The complete liquid and blow out volume is dispensed: empty tip.
    4. The pipetting channel out of the liquid using swap speed, then the aspiration of transport air follows.

    \

4.  #### ‌Tip Eject‌

    \


    Ejecting the used tip into the waste container of the ML STAR is the final step. A used needle will be returned to the wash station, where the wash process can be started directly.

    \

5.  #### ‌Avoiding Contamination‌

    \


    If cross-contamination is a concern, consider the following approaches:

    * Use only Hamilton tips on the ML STAR.
    * Use new tips for every pipetting step, to avoid carry-over between different wells or containers.
    * Use filter tips in order to avoid contamination of the pipetting channel by jets, aerosols, etc.
    * Dispense any compounds at risk for cross-contamination onto a surface. Dispensing in a jet may produce aerosols and thus can cause cross-contamination.

    Dispense using a residual volume, i.e. do not completely empty the tip on dispense. This can be achieved e.g. by aspirating 11µl and dispensing only 10µl.
6.  #### ‌Touch Off‌

    \


    The “Touch off” Function is used if very small amounts of liquid shall be aspirated or dispensed into a manually placed labware or labware with great tolerances. The “Touch off” Function will move to a certain height over the well bottom and smoothly move downwards. As soon as the tip hits the bottom of the container, the motor current of the z-drive increases. This change will be detected and the z-move stops. From that position, the pipetting channels moves back up the specified distance “Dispense position above touch” and starts dispensing.

    \


    ![image](../../../.gitbook/assets/Image\_1368.jpg)

    \

7.  #### ‌Side Touch‌

    \


    For a small amount of liquid, there is the possibility of dispensing liquid to the side of the well with the “Side touch” Mode (available in the Single Steps / Easy Steps).

    \


    ![image](../../../.gitbook/assets/Image\_1369.jpg)

    \


    The “Side touch” Mode will move the tip to a specified height in the center of the container, and then moves right (always right). At this position, the dispensing of the liquid starts.

    The values for “Touch off height” and “Right” move have to be defined in the container data in the Labware Editor.

    \


    ![image](../../../.gitbook/assets/Image\_1370.jpg)
