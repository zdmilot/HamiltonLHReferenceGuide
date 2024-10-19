# Luminescence Read Mode

In luminescence read mode, no excitation is necessary as the measured species emit light naturally. For this reason, the lamp does not flash, so no background excitation interference occurs.

For the Luminescence (LUM) read mode, the instrument provides measurements in Relative Light Units (RLUs).

Luminescence is the emission of light by processes that derive energy from essentially non- thermal changes, the motion of subatomic particles, or the excitation of an atomic system by radiation. Luminescence detection relies on the production of light from a chemical reaction in a sample.

To help eliminate background luminescence from a plate that has been exposed to light, you should dark adapt the plate by placing the sample-loaded plate inside the instrument for several minutes before you start the read.

For some monochromator-based instruments, the default setting for luminescence is the “zero order” position where the grating monochromator acts as a mirror that reflects all light to the PMT detector.

The instrument bypasses the emission monochromator for luminescence reads that detect all wavelengths.

You can choose the wavelength where peak emission is expected to occur. Also, multiple wavelength choices let species with multiple components be differentiated and measured easily.

Concentrations or qualitative results are derived from raw data with a standard curve or by comparison with reference controls.

### Applications of Luminescence

Chemiluminescent or bioluminescent reactions can be induced to measure the quantity of a particular compound in a sample. Examples of luminescent assays include the following:

![](<../../../.gitbook/assets/0 (14) (1).png>) Reporter gene assays (the measurement of luciferase gene expression)

![](<../../../.gitbook/assets/1 (16) (1).png>) Quantitation of adenosine triphosphate (ATP) as an indication of cell counts with cell- proliferation, cytotoxicity, and biomass assays

![](<../../../.gitbook/assets/2 (18).png>) Enzyme measurements with luminescent substrates, such as immunoassays

For information about setting up a luminescence mode protocol, see Creating Luminescence Mode Protocols on page 168.

### Luminescence Instruments and Detection Cartridges

The following instruments have luminescence read mode capability: ![](<../../../.gitbook/assets/3 (19).png>) SpectraMax iD5 Multi-Mode Microplate Reader on page 320

![](<../../../.gitbook/assets/4 (17).png>) SpectraMax iD3 Multi-Mode Microplate Reader, see page 317

![](<../../../.gitbook/assets/5 (18).png>) SpectraMax i3x and SpectraMax i3 Multi-Mode Detection Platforms, see page 323 (supports user-installable detection cartridges to expand read capability)

![](<../../../.gitbook/assets/6 (18).png>) SpectraMax L Luminescence Microplate Reader on page 324

![](<../../../.gitbook/assets/7 (18).png>) SpectraMax Paradigm Multi-Mode Microplate Reader, see page 327 (requires detection cartridges)

![](<../../../.gitbook/assets/8 (17).png>) SpectraMax M5 and SpectraMax M5e Multi-Mode Microplate Readers, see page 330 ![](<../../../.gitbook/assets/9 (13).png>) SpectraMax M4 Multi-Mode Microplate Reader, see page 331

![](<../../../.gitbook/assets/10 (11).png>) SpectraMax M3 Multi-Mode Microplate Reader, see page 332

![](<../../../.gitbook/assets/11 (13).png>) SpectraMax M2 and SpectraMax M2e Multi-Mode Microplate Readers, see page 333 ![](<../../../.gitbook/assets/12 (12).png>) Gemini XPS Microplate Reader, see page 334

![](<../../../.gitbook/assets/13 (11).png>) Gemini EM Microplate Reader, see page 334

![](<../../../.gitbook/assets/14 (11).png>) FlexStation 3 Multi-Mode Microplate Reader, see page 335 ![](<../../../.gitbook/assets/15 (9).png>) FilterMax F5 Multi-Mode Microplate Reader, see page 335 ![](<../../../.gitbook/assets/16 (7).png>) FilterMax F3 Multi-Mode Microplate Reader, see page 338

The following detection cartridges have luminescence read mode capability: ![](<../../../.gitbook/assets/17 (7).png>) Tunable Wavelength (TUNE) Detection Cartridge, see page 345

![](<../../../.gitbook/assets/18 (9).png>) Multi-Mode (MULTI) Detection Cartridge, see page 346

![](<../../../.gitbook/assets/19 (8).png>) Glow Luminescence (LUM) Detection Cartridges, see page 348

![](<../../../.gitbook/assets/20 (8).png>) Dual Color Luminescence (LUM) (BRET2) Detection Cartridge, see page 349



**Note:** For the SpectraMax i3x, you can use the detection cartridges for top reads only.

### Luminescence Reads with Injectors

Injectors deliver a specified volume of a reagent to the wells of a plate. They are generally used when delivery of the reagent initiates a reaction that occurs rapidly and results in a luminescent or fluorescent signal that must be detected quickly.

The SpectraMax i3x with the Injector Cartridge installed can be set up to inject and read well by well to reduce signal loss.

Common inject-and-read assays include luciferase reporter assays.

The Injector Cartridge is DLReady™ certified by Promega for the Dual-Luciferase Reporter (DLR™) assay system.

DLReady, DLR, and the DLReady logo are trademarks of Promega Corporation.

### Analyzing Luminescence Data

The conversion rate of photons to counts is individual for each reader. Therefore, raw data from the same plate can seem significantly different from one instrument to the next. Also, the data format used by other manufacturers might not be counts per second and can be different by several orders of magnitude. It is important to know that the number of counts and the size of figures is not a benchmark of sensitivity.

Concentrations or qualitative results are derived from raw data with a standard curve or by comparison with reference controls. The raw data can then be expressed in equivalent concentration of a reference label. The raw data is normalized to counts per second by dividing the number of counts by the read time per well.

### Background Correction

The light detected in a luminescent measurement generally has two components: specific light from the luminescent reaction and an approximately constant level of background light caused by various factors, including the plate material and impurities in the reagents. The background can be effectively measured using blank replicates. Blanks should include the luminescent substrate (chemical energy source) but not the luminescence agent (generally an enzymatic group which makes the substrate glow).

A blank well contains everything used with the sample wells except the label and sample- specific compounds. Do not use an empty well for a blank.

The blank sample reveals the offset underlying each data sample. This offset does not carry information on the label and is generally subtracted before data reduction is done.

For optimal results, you should run replicates for all blanks, controls, and samples. In this case, the blank value that will be subtracted is the average value of all blanks.

To help eliminate background luminescence from a plate that has been exposed to light, you should dark adapt the plate by placing the sample-loaded plate inside the instrument for several minutes before you start the read.

### Sample Volumes and Concentration of Reactants

The concentration of the luminescent agent impacts the quantity of light output in a luminescent reaction. Light is emitted as a result of a reaction between two or more compounds. Therefore, the quantity of light output is proportional to the quantity of the limiting reagent in the sample.

For example, in an ATP/luciferin-luciferase system, when total volume is held constant and ATP is the limiting reagent, the blanked light output is proportional to the concentration of ATP in the sample. Even if the reaction begins with a high concentration of ATP, as it gets used up it can become rate-limiting. In this case, the non-linearity is an effect of the assay and not caused by the microplate reader.

**Note:** Very bright samples can exceed the linear dynamic range of the instrument. If so, the read can be done with an attenuation filter.



### Data Optimization

Measurement noise is dependent on the read time per sample (time per plate or time per well). The detection limit improves when the read time is increased. Therefore, it is important to specify the read time when you compare measurements.

All low-light-level detection devices have some measurement noise in common. To average out the measurement noise, optimization of the time per well involves accumulating as many counts as possible. Within some range, you can reduce noise (CVs, detection limit) by increasing the read time per well, as far as is acceptable from throughput and sample stability considerations.

Z´ is the standard statistical parameter in the high-throughput screening community for measuring the quality of a screening assay independent of test compounds. It is used as a measure of the signal separation between the positive controls and the negative controls in an assay.

The value of Z´ can be determined using the following formula:

3(SDc+ ) + 3(SDc– )

Z´ = 1 – | Mean

c+

– Meanc– |

where **SD** is the standard deviation, **c+** is the positive control, and **c–** is the negative control.

A Z´value greater than or equal to 0.4 is the generally acceptable minimum for an assay. You can use higher values when results are more critical.

Z´ is not linear and can be made unrealistically small by outliers that skew the standard deviations in either population. To improve the Z´value, you can increase the quantity of label in the sample, if acceptable for the assay, or increase the read time per well.
