# AlphaScreen Read Mode

ALPHA stands for Amplified Luminescent Proximity Homogeneous Assay. AlphaScreen® is a bead-based chemistry used to study molecular interactions between moieties A and B, for example. When a biological interaction between A and B moves beads (coated with A and B, respectively) together, a cascade of chemical reactions produce a greatly amplified signal.

The cascade finally resulting in signal is triggered by laser excitation (680 nm), making a photosensitizer on the A-beads convert oxygen to an excited (singlet) state. The energized oxygen diffuses away from the A-bead. When reaching the B-bead in close proximity, it reacts with a thioxene derivative on the B-bead generating chemiluminescence at 370 nm. Energy transfer to a fluorescent dye on the same bead shifts the emission wavelength into the

520 nm to 620 nm range. The limited lifetime of singlet oxygen in solvent (\~4 microseconds) lets diffusion reach up to only around 200 nm distance. Thus, only B-beads in the proximity of A-beads yield signal, which indicates binding between moieties A and B.

An AlphaScreen measurement includes a light pulse, by turning on the laser diode for a specified time, turning off the laser diode, followed by the measurement of the AlphaScreen signal, as specified in the measurement protocol timing parameters.

**Note:** AlphaScreen beads are light sensitive. Beads are best handled under subdued (<100 lux) or green filtered (Roscolux filters #389 from Rosco, or equivalent) light conditions. Do incubation steps in the dark.

![](<../../../.gitbook/assets/0 (7) (1).png>)

The raw data can be normalized to counts per second.

### Applications of AlphaScreen

AlphaScreen reagent and assays are used for drug discovery purposes. Examples of AlphaScreen assays include:

![](<../../../.gitbook/assets/1 (8) (1).png>) G-protein coupled receptor (GPCR) assay kits, for cAMP quantification or IP3 quantification.

![](<../../../.gitbook/assets/2 (10) (1).png>) Tyrosine Kinase assays.

![](<../../../.gitbook/assets/3 (11) (1).png>) Cytokine detection kits, such as TNF-alpha detection (immunoassay). AlphaScreen read mode can also capture the Europium emission line of AlphaLISA®.

For information about setting up a fluorescence polarization mode protocol, see Creating Fluorescence Polarization Mode Protocols on page 172.

### AlphaScreen Instruments and Detection Cartridges

The SpectraMaxi3x supports user-installable detection cartridges to expand its read capabilities. Each detection cartridge contains the light source, optics, and electrical components needed to do specific read modes.

The following instruments have AlphaScreen read mode capability:

![](<../../../.gitbook/assets/4 (9) (1).png>) SpectraMax i3x and SpectraMax i3 Multi-Mode Detection Platforms, see page 323

To do AlphaScreen reads, the SpectraMax i3x requires AlphaScreen Detection Cartridges , see page 346.

![](<../../../.gitbook/assets/5 (11) (1).png>) SpectraMax Paradigm Multi-Mode Microplate Reader, see page 327

To do AlphaScreen reads, the SpectraMax Paradigm Multi-Mode Microplate Reader requires AlphaScreen Detection Cartridges , see page 346.

![](<../../../.gitbook/assets/6 (11) (1).png>)

**Note:** For the SpectraMax i3x, you can use the detection cartridges for top reads only.

For more information, go to [www.perkinelmer.com](http://www.perkinelmer.com/).

ALPHASCREEN and ALPHALISA are registered trademarks of PerkinElmer, Inc.

### Analyzing AlphaScreen Data

The conversion rate of photons to counts and relative fluorescence units (RFU) is individual for each reader. Therefore, raw data from the same plate can seem to be different from one instrument to the next. Also, the data format used by instrument manufacturers might be counts normalized per second or not normalized counts, and therefore the raw data can be different by several orders of magnitude. It is important to know that the number of counts and the size of figures are not indicators of sensitivity.

The raw data can be normalized to counts per second by selecting the Normalization option in the Settings dialog. See Acquisition Settings on page 109.

### Background Correction

Although background is significantly lower than with fluorescence intensity measurements, you should use blanks or assay controls for background correction. The background can be effectively measured using blank replicates. When you read a sample with small signal, an interference can occur from the afterglow of a very strong emitting adjacent sample that was measured just before. Such cross talk can occur through the wall of a white 384-well plate. To prevent such interference, you can select the Interlaced Read option in the Settings dialog.

This option reads only every other well in a checkerboard pattern, and then reads the plate again to read the previously omitted wells.

A blank well contains everything used with the sample wells except the label and sample- specific compounds. Do not use an empty well for a blank.

For optimal results, you should run replicates for all blanks, controls, and samples. In this case, the blank value that will be subtracted is the average value of all blanks.

### Data Qualification and Validation

Z´ is the standard statistical parameter in the high-throughput screening community for measuring the quality of a screening assay independent of test compounds. It is used as a measure of the signal separation between the positive controls and the negative controls in an assay.

The value of Z´ can be determined using the following formula:

3(SDc+ ) + 3(SDc– )

Z´ = 1 – | Mean – Mean |

c+

c–

where **SD** is the standard deviation, **c+** is the positive control, and **c–** is the negative control.

A Z´value greater than or equal to 0.4 is the generally acceptable minimum for an assay. You can use higher values when results are more critical.

Z´ is not linear and can be made unrealistically small by outliers that skew the standard deviations in either population. To improve the Z´value, you can increase the quantity of label in the sample, if acceptable for the assay, or increase the read time per well.

**CAUTION!** The assay plate and the instrument should be kept at room temperature, since temperature variations cause fluctuations in signal.

![](<../../../.gitbook/assets/7 (11).png>)![](<../../../.gitbook/assets/8 (10).png>)
