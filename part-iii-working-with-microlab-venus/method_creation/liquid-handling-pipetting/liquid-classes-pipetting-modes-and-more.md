# Liquid Classes, Pipetting Modes and More

Pipetting

In general, pipetting by the principle of air displacement (as with handheld pipettes) is sensitive to the following:

* Manner of pipetting (i.e. surface or jet, empty tip or part volume)
* Tip or needle type (geometry, tip orifice)
* Environmental effects (temperature, pressure, humidity)
* Liquid type (viscosity, evaporation)

The pipetting mode (e.g., surface or jet mode) and the liquid class determine the behavior of the instrument. Pipetting mode and liquid class represent two independent sets of information, both of which have to be specified.

\


![Originalbild anzeigen](../../../.gitbook/assets/Image\_1371.jpg)

NOTE

Always use the same liquid class for one aspiration and dispense cycle. Otherwise uncalculated residual volumes may be left within the tip, or other errors regarding plunger position / movements may occur.

\


1.  #### ‌Aspiration‌

    \


    For aspiration, three modes are available:

    * “Aspiration”, for all standard cases.
    * “Consecutive Aspiration” for aspiration with a tip that has already aspirated liquid (e.g. if aspirating out of three different containers before the dispense step).
    * “Aspirate All” for aspiration of all the liquid in a container (specify a volume larger than what is expected to be in the container). In this case, aspiration monitoring is deactivated and the tip will follow the falling liquid level (if specified) to the bottom of the container, staying there for the rest of the aspiration.

    \

2.  #### ‌Dispense‌

    \


    For dispense, five modes are available:

    * “Surface Part Volume” for dispensing only a part of the liquid in the tip to a surface, leaving a residual volume in the tip,
    * “Surface Empty Tip” for dispensing all the liquid in the tip to a surface,
    * “Jet Part Volume” for dispensing only a part of the liquid in the tip in a jet, i.e. without touching a surface, leaving a residual volume in the tip,
    * “Jet Dispense Empty Tip” for dispensing all the liquid in the tip in a jet.
    * “Drain tip in Jet mode”

    The liquid class stores all relevant background parameters, such as flow rates and volume corrections for one pipetting cycle, (i.e. for one aspiration and the subsequent dispense(s)). Depending on the pipetting mode chosen, only a subset of the parameters of the liquid class is active. According to the different dependencies listed above, liquid classes have attributes related to their intended use: tip type, liquid name, and dispense mode.

    [Different liquid classes are provided with the VENUS Software. They are optimized for different liquids, tip types, and important pipetting processes, such as aspiration followed by dispensing either to a surface or in a jet. Hamilton has optimized the standard liquid classes with great care to assure the best pipetting accuracy. To change Hamilton standard liquid classes, store the class under a different name first. For special applications, the programmer can define a liquid class to achieve the highest accuracy with the compounds and volumes of interest. The liquid classes can be adapted to the user-specific requirements. For this purpose a liquid editor comes with the VENUS Software. It is described in ](liquid-classes-pipetting-modes-and-more.md#bookmark424)[Section 13.4 The Hamilton CO-RE Liquid Editor](liquid-classes-pipetting-modes-and-more.md#bookmark424)[.](liquid-classes-pipetting-modes-and-more.md#bookmark424)

    \

3.  #### ‌Liquid Handling Examples‌

    \


    Here are some examples of typically used combinations of liquid classes and pipetting modes:

    1.  Aspirate 50µl of a water-like liquid, dispense 50µl into an empty 96-well plate; use standard tips; change tips every cycle.

        \


        | Liquid Class:    | StandardVolume\_Water\_DispenseJet\_Empty                                                             |
        | ---------------- | ----------------------------------------------------------------------------------------------------- |
        | Aspiration Mode: | Aspiration                                                                                            |
        | Dispense Mode:   | Jet Dispense Empty Tip                                                                                |
        | Detection:       | Aspiration: LLD = pressure or capacitance or both, submerge to a depth of 2mm, following liquid level |
        | Dispense:        | Fixed height of 5mm, not following liquid level                                                       |

        \

    2.  Aspirate a water-like liquid, single dispense into a pre-filled 96-well plate; use low volume tips; change tips every cycle.

        \


        | Liquid Class:    | LowVolume\_Water\_DispenseSurface\_Empty                                                      |
        | ---------------- | --------------------------------------------------------------------------------------------- |
        | Aspiration Mode: | Aspiration                                                                                    |
        | Dispense Mode:   | Surface Dispense Empty Tip (in the liquid class selected here, the blow- out volume is 0)     |
        | Detection:       | Aspiration: LLD = pressure or capacitance or both, submerge depth 2mm, following liquid level |
        | Dispense:        | Capacitive LLD on, following liquid level                                                     |

        \

    3.  Aspirate ≥20µl of a water-like liquid, dispense the same amount into an empty 96-well plate; keep tips.

        \


        | Liquid Class:    | StandardVolume\_Water\_DispenseJet\_Empty                                                                                                  |
        | ---------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
        | Aspiration Mode: | Aspiration                                                                                                                                 |
        | Dispense Mode:   | Jet Dispense Empty Tip (Empty Tip only)                                                                                                    |
        | Detection:       | Aspiration: Capacitive LLD, submerge depth 2mm, following liquid level                                                                     |
        | Dispense:        | Fixed height of 5mm, not following liquid level                                                                                            |
        | Comment:         | On first aspiration, pre-wetting of the tip by 1-3 mixing cycles is necessary to equalize conditions for initial and subsequent dispenses. |
    4.  Aliquoting of liquid means aspirating a given volume at once and dispensing several partial volumes (aliquots) in a jet to different containers. In this frequently used pipetting procedure, the accuracy of the first and the last aliquot are often not within the specified range. Therefore, in order to dispense e.g. 10 aliquots of 20µl of a water-like liquid with the ML STAR, aspirate 240µl and dispense 20µl directly back into the container. This is followed by dispensing 10 aliquots of 20µl each. The last aliquot of 20µl is discarded to another container or ejected with the tip. In addition, after dispensing of every aliquot, a given amount of air is aspirated and dispensed with the next aliquot.

        \


        | Liquid Class:    | StandardVolumeWaterAliquotJet                                          |
        | ---------------- | ---------------------------------------------------------------------- |
        | Aspiration Mode: | Aspiration                                                             |
        | Dispense Mode:   | Jet Dispense part volume                                               |
        | Detection:       | Aspiration: capacitive LLD, submerge depth 2mm, following liquid level |
        | Dispense:        | Fixed height of 5mm, not following liquid level                        |

        \

    5. Table of Aliquots

    \


    | Tip types are: | Std. = Standard Volume Tip (300µl) High=High Volume Tip (1000µl)                                                                                                            |
    | -------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
    | Pre-wet:       | If “Yes”, 3-fold mixing on aspiration with aspiration volume necessary                                                                                                      |
    | V(main aliq.): | Volume of main aliquot                                                                                                                                                      |
    | V(pre-aliq.):  | Volume of pre-aliquot                                                                                                                                                       |
    | V(post-aliq.): | Volume of post-aliquot                                                                                                                                                      |
    | CV:            | Precision (coefficient of variation, for definition see the Technical Specifications in the Microlab STAR Line Operator’s Manual)                                           |
    | R:             | Trueness (for definition see Technical Specifications in the Microlab STAR Line Operator’s Manual). The R and CV values mentioned here are typical results for measurements |
    | Class:         | Liquid class used                                                                                                                                                           |
    | A:             | ”StandardVolume\_Water\_AliquotJet“                                                                                                                                         |
    | B:             | “StandardVolume\_Serum\_AliquotJet“                                                                                                                                         |
    | C:             | “HighVolume\_Water\_AliquotJet“                                                                                                                                             |
    | D:             | “HighVolume\_Serum\_AliquotJet“                                                                                                                                             |

    The dispense mode for all cases is “Jet Dispense, Part Volume“.

    The following table shows accuracy of aliquoting volumes in dependency upon various pipetting parameters. Sample values and results for pre- and post-aliquot volumes are listed. Please note that the examples for water\* and the following are not technical specifications:

    \


    | Channel type | Tip type | Liquid | Pre- wet | V \[µl] main aliq. | No. of aliq. | V \[µl] pre- aliq. | V \[µl] post- aliq. | CV \[%] | R \[%] | Class |
    | ------------ | -------- | ------ | -------- | ------------------ | ------------ | ------------------ | ------------------- | ------- | ------ | ----- |
    | 1000         | Std      | Water  | Yes      | 10                 | 12           | 20                 | >10                 | 3.9     | -3.8   | A     |
    | 1000         | Std      | Water  | Yes      | 20                 | 12           | 20                 | 20                  | 2.5     | -3.2   | A     |
    | 1000         | Std      | Water  | Yes      | 50                 | 4            | 50                 | 20                  | 2.0     | -1.5   | A     |
    | 1000         | High     | Water  | No       | 20                 | 12           | 20                 | 20                  | 5       | -1.6   | C     |
    | 1000         | High     | Water  | No       | 50                 | 12           | 50                 | 50                  | 2.5     | -1.2   | C     |
    | 1000         | High     | Water  | No       | 100                | 8            | 50                 | 100                 | 1.5     | -0.9   | C     |
    | 1000         | High     | Water  | No       | 200                | 4            | 50                 | 100                 | 1.5     | -1.5   | C     |

    _Other liquids data is available upon request. Please ask a Hamilton Representative for further information._

    \

4.  #### _‌Anti-Droplet Control (ADC)‌_

    \


    _The Anti-Droplet Control (ADC) function offers a way to prevent droplet formation at the tip of tips or needles while pipetting highly volatile liquids._

    _These liquids cause droplets because the high vapor pressure of the volatile solvents (e.g. acetone, ethanol, diethyl ether) results in a pressure increase in the tip. This pressure will push the liquid out of the tip (fig A and B)._

    _The working principle of ADC is to measure the pressure inside the pipetting channel (with the built-in pressure sensor) and compensate the increasing pressure by moving the piston upwards. The evaporated volume of the liquid will now be compensated._

    \


    ![image](../../../.gitbook/assets/Image\_1372.jpg)

    _Anti-droplet control (ADC)_

    ![image](../../../.gitbook/assets/Image\_1373.png)

    _ATTENTION_

    _The following statements will help in order to get best pipetting results using ADC:_

    _Use ADC only for pipetting steps where a change of pressure inside the tip is expected (e.g. if using a liquid with high vapor pressure)._

    _The air transport volume should be very small or zero. If necessary, create a new liquid class._

    _The swap speed should be slow. If necessary, create a new liquid class._

    _Keep in mind that the piston may not be in its initial position when tips are reused without ejecting. ADC might not be working after several steps._

    _ADC can be switched on using the appropriate steps from “HSLStarLib.hsl”. ADC works on both pipetting channel types, 1000μl and 5ml._

    \

5.  #### _‌Monitored Air Displacement (MAD)‌_

    \


    _The ML STAR is equipped with an aspiration monitoring feature. During the aspiration process, the pressure within the pipetting channel is measured in real time. Analyzing the shape of the p(t) curve, the system can distinguish the following situations:_

    * _A correct aspiration takes place_
    * _Air is aspirated into the tip (because, for example, the container has not been filled properly)_
    * _A clot blocks the tip_

    \


    ![Originalbild anzeigen](../../../.gitbook/assets/Image\_1374.jpg)

    _NOTE_

    _MAD is available on the 1000μl-pipetting channels and the 5ml-pipetting channels._

    \


    _The aspiration monitoring can be switched on and off for each individual aspiration step of a method using the steps from “HLSMl\_StarLib.hsl”. For pressure-based clot detection, a threshold can be given in arbitrary A/D (analog/digital) values (typically 100 A/D values). The range of A/D values of the pressure sensor is from around 800 (at ambient pressure) to <10 A/D values for 18 mbar below ambient pressure. For comparison, the hydrostatic pressure of 100µl of water in our standard tip is around 2 mbar._

    _The following diagram shows the principle of aspiration monitoring based on pressure._

    \


    ![Seite\_340\_Graphik](../../../.gitbook/assets/Image\_1375.jpg)

    _Aspiration monitoring based on pressure_

    \


    ![Originalbild anzeigen](../../../.gitbook/assets/Image\_1376.jpg)

    _NOTE_

    _Pressure-based monitoring works with unused as well as used disposable tips and needles._

    _If multiple Aspirate/Dispense cycles are executed within a loop, make sure that the (last) dispense step uses the Pipetting mode ‘Drain tip’._

    _The volume range for the MAD depends on the specific assay. The lower limit in many cases is an aspiration volume of 50µl._

    _Pressure-based monitoring has been optimized for liquid solutions only._
6.  #### _‌Capacitance-based Clot Detection‌_

    \


    _In addition to pressure-based clot detection, the ML STAR is equipped with capacitance-based clot detection. This detection approach works when the aspiration with capacitance Liquid Level Detection is switched on._

    \


    _Functionality_

    ![image](../../../.gitbook/assets/Image\_1377.png)

    _The system measures the conductive signal when the tip leaves the liquid after aspiration. Due to the air gap between tip and liquid, the capacitance signal will vanish once a given height is reached (the “Clot retract height”, which is specified within the liquid class). If a clot is present, it bridges the distance and the signal will remain, resulting in an error message. A typical clot retract height is 2-5 mm, as illustrated below. This clot detection is independent from pressure-based monitoring._

    \


    ![image](../../../.gitbook/assets/Image\_1378.png) _Clot retract height_

    \


    _The capacitance-based clot detection is only valid, if the liquid parameter “Clot retract height_[_” is set (>0). Refer to_ ](liquid-classes-pipetting-modes-and-more.md#bookmark424)_Section 13.4 The Hamilton CO-RE Liquid Editor._

    \


    ![Originalbild anzeigen](../../../.gitbook/assets/Image\_1379.jpg)

    _NOTE_

    _The capacitance-based clot detection is available on the 1000μl-pipetting channels and the 5ml-pipetting channels._
7.  #### _‌TADM – Total Aspiration and Dispensing Monitoring‌_

    \


    _TADM (Total Aspiration and Dispensing Monitoring) is a tool to increase the safety and the robustness of pipetting processes. However, it is not part of the standard software package._

    _The Principle of TADM_

    _The pressure inside each individual pipetting channel is constantly recorded during aspiration and dispensing. The values obtained by the pressure sensor during a pipetting step (aspiration or dispensing) can be compared to values defined by the user. This allows real-time monitoring of the pipetting process._

    \


    ![image](../../../.gitbook/assets/Image\_1380.gif)

    _The differences between error-free pipetting steps and erroneous ones are used to distinguish the results of the pipetting steps. Basically, there are two types of errors that can be detected:_

    * _Pressure above normal (overpressure)_
    * _Pressure below normal (underpressure)_

    _TADM verifies that a sample has been transferred with a traceable digital audit trail which is particularly beneficial for In Vitro Diagnostic (IVD) laboratories._

    _Peaks and fraying of TADM curves can be a sign that the liquid class and / or the pipetting process are not defined in a precise and robust way. With the help of TADM, the pipetting process can thus be optimized and made more robust._

    \


    ![Originalbild anzeigen](../../../.gitbook/assets/Image\_1381.jpg)

    _NOTE_

    _TADM is available on the 1000μl-pipetting channels, 5ml-pipetting channels and on the CO-RE 96 Probe Head TADM. The CO-RE 96 Probe Head TADM is now provided standard for the ML STAR with Multi Probe Head 96._

    _The TADM features are available only after purchase and installation of the TADM software package._

    _With VENUS M Software, the TADM test aspiration pressure curves are analysed to indicate pipetting performance._
