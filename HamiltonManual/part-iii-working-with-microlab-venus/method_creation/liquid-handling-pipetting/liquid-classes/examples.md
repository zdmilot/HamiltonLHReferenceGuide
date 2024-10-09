# Examples‌

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



Table of Aliquots:

<table data-header-hidden><thead><tr><th width="444"></th><th></th></tr></thead><tbody><tr><td>Tip types are:</td><td>Std. = Standard Volume Tip (300µl) High=High Volume Tip (1000µl)</td></tr><tr><td>Pre-wet:</td><td>If “Yes”, 3-fold mixing on aspiration with aspiration volume necessary</td></tr><tr><td>V(main aliq.):</td><td>Volume of main aliquot</td></tr><tr><td>V(pre-aliq.):</td><td>Volume of pre-aliquot</td></tr><tr><td>V(post-aliq.):</td><td>Volume of post-aliquot</td></tr><tr><td>CV:</td><td>Precision (coefficient of variation, for definition see the Technical Specifications in the Microlab STAR Line Operator’s Manual)</td></tr><tr><td>R:</td><td>Trueness (for definition see Technical Specifications in the Microlab STAR Line Operator’s Manual). The R and CV values mentioned here are typical results for measurements</td></tr><tr><td>Class:</td><td>Liquid class used</td></tr><tr><td>A:</td><td>”StandardVolume_Water_AliquotJet“</td></tr><tr><td>B:</td><td>“StandardVolume_Serum_AliquotJet“</td></tr><tr><td>C:</td><td>“HighVolume_Water_AliquotJet“</td></tr><tr><td>D:</td><td>“HighVolume_Serum_AliquotJet“</td></tr></tbody></table>

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
