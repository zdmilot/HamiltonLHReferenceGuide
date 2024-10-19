# Absorbance Read Mode

The instrument uses the Absorbance (ABS) read mode to measure the Optical Density (OD) of the sample solutions.

Absorbance is the quantity of light absorbed by a solution. To measure absorbance accurately, it is necessary to eliminate light scatter. If there is no turbidity, then absorbance = optical density.

A = log10(I0 /I) = –log10(I/I0)

where _I0_ is intensity of the incident light before it enters the sample divided by the light after it passes through the sample, and _A_ is the measured absorbance.

The temperature-independent PathCheck® Pathlength Measurement Technology normalizes your absorbance values to a 1 cm path length based on the near-infrared absorbance of water.

The instrument allows you to choose whether to display absorbance data as Optical Density (OD) or %Transmittance (%T) in the Reduction dialog.

#### Optical Density

Optical density (OD) is the quantity of light passing through a sample to a detector relative to the total quantity of light available. Optical Density includes absorbance of the sample plus light scatter from turbidity and background. You can compensate for background using blanks.

A blank well contains everything used with the sample wells except the chromophore and sample-specific compounds. Do not use an empty well for a blank.

Some applications are designed for turbid samples, such as algae or other micro-organisms in suspension. The reported OD values for turbid samples are likely to be different when read by different instruments.

For optimal results, you should run replicates for all blanks, controls, and samples. In this case, the blank value that will be subtracted is the average value of all blanks.

#### % Transmittance

%Transmittance is the ratio of transmitted light to the incident light for absorbance reads.

T = I/I0

%T = 100T

where _I_ is the intensity of light after it passes through the sample and _I0_ is incident light before it enters the sample.

Optical Density and %Transmittance are related by the following formulas:

%T = 10

2–OD

OD = 2 – log10(%T)

The factor of two comes from the fact that %T is expressed as a percent of the transmitted light and log10(100) = 2.

When in %Transmittance analysis mode, the instrument converts the raw OD values reported by the instrument to %Transmittance using the above formula. All subsequent calculations are done on the converted numbers.

### Applications of Absorbance

Absorbance-based detection is commonly used to evaluate changes in color or turbidity, permitting widespread use including ELISAs, protein quantitation, endotoxin assays, and cytotoxicity assays. With absorbance readers that are capable of measuring in the ultraviolet (UV) range, the concentration of nucleic acids (DNA and RNA) can be found using their molar extinction coefficients.

For micro-volume measurements, you can use SpectraDrop 24-well Micro-Volume Microplates and SpectraDrop 64-well Micro-Volume Microplates.

For information about setting up an Absorbance mode protocol, see Creating Absorbance Mode Protocols on page 159.

### Absorbance Instruments

The following instruments have absorbance read mode capability: ![](<../../../.gitbook/assets/0 (12) (1).png>) SpectraMax iD5 Multi-Mode Microplate Reader on page 320

![](<../../../.gitbook/assets/1 (14) (1).png>) SpectraMax iD3 Multi-Mode Microplate Reader, see page 317

![](<../../../.gitbook/assets/2 (16).png>) SpectraMax i3x and SpectraMax i3 Multi-Mode Detection Platforms, see page 323 ![](<../../../.gitbook/assets/3 (17).png>) SpectraMax Paradigm Multi-Mode Microplate Reader, see page 327 (requires the

Absorbance Detection Cartridge, see page 344.

![](<../../../.gitbook/assets/4 (15) (1).png>) VersaMax Microplate Reader, see page 329

![](<../../../.gitbook/assets/5 (16).png>) SpectraMax ABS and SpectraMax ABS Plus Microplate Readers on page 329 ![](<../../../.gitbook/assets/6 (16).png>) SpectraMax Plus 384 Absorbance Microplate Reader, see page 330

![](<../../../.gitbook/assets/7 (16).png>) SpectraMax M5 and SpectraMax M5e Multi-Mode Microplate Readers, see page 330 ![](<../../../.gitbook/assets/8 (15).png>) SpectraMax M4 Multi-Mode Microplate Reader, see page 331

![](<../../../.gitbook/assets/9 (11).png>) SpectraMax M3 Multi-Mode Microplate Reader, see page 332

![](<../../../.gitbook/assets/10 (9).png>) SpectraMax M2 and SpectraMax M2e Multi-Mode Microplate Readers, see page 333 ![](<../../../.gitbook/assets/11 (11).png>) SpectraMax 340PC 384 Absorbance Microplate Reader, see page 333

![](<../../../.gitbook/assets/12 (10).png>) SpectraMax 190 Absorbance Microplate Reader, see page 333 ![](<../../../.gitbook/assets/13 (9).png>) FlexStation 3 Multi-Mode Microplate Reader, see page 335

![](<../../../.gitbook/assets/14 (9).png>) FilterMax F5 Multi-Mode Microplate Reader, see page 335 ![](<../../../.gitbook/assets/15 (7).png>) FilterMax F3 Multi-Mode Microplate Reader, see page 338 ![](<../../../.gitbook/assets/16 (5).png>) VMax Kinetic Microplate Reader, see page 339

![](<../../../.gitbook/assets/17 (5).png>) EMax Endpoint Microplate Reader, see page 340 ![](<../../../.gitbook/assets/18 (7).png>) EMax Plus Microplate Reader, see page 340

### PathCheck Pathlength Measurement Technology

To use PathCheck technology, select the PathCheck check box in the PathCheck Settings category in the Settings dialog for absorbance endpoint reads.

The temperature-independent PathCheck® Pathlength Measurement Technology normalizes your absorbance values to a 1 cm path length based on the near-infrared absorbance of water.

The Beer–Lambert law states that absorbance is proportional to the distance that light travels through the sample:

A = cL

where _A_ is the absorbance, is the molar absorptivity of the sample, _c_ is the concentration of the sample, and _L_ is the pathlength. The longer the pathlength, the higher the absorbance.

Microplate readers use a vertical light path so the distance of the light through the sample depends on the volume. This variable pathlength makes it difficult to do extinction-based assays and makes it confusing to compare results between microplate readers and spectrophotometers.

The standard pathlength of a 1 cm cuvette is the conventional basis to quantify the unique absorptivity properties of compounds in solution. Quantitative analysis can be done on the basis of extinction coefficients, without standard curves (for example, NADH-based enzyme assays). When you use a cuvette, the pathlength is known and is independent of sample volume, so absorbance is directly proportional to concentration when there is no background interference.

In a plate, pathlength is dependent on the liquid volume, so absorbance is proportional to both the concentration and the pathlength of the sample. Standard curves are often used to determine analyte concentrations in vertical-beam photometry of unknowns, yet errors can still occur from pipetting the samples and standards. The PathCheck technology determines the pathlength of aqueous samples in the plate and normalizes the absorbance in each well to a pathlength of 1 cm. This way of correcting the microwell absorbance values is accurate to within ±4% of the values obtained directly in a 1 cm cuvette.

![](<../../../.gitbook/assets/19 (6).png>)

Horizontal light path

Vertical light path

![](<../../../.gitbook/assets/20 (6).png>)

Cuvette Microplate wells

PathCheck technology normalizes the data acquired from an Absorbance read mode Endpoint read type to a 1 cm pathlength, correcting the OD for each well to the value expected if the sample were read in a 1 cm cuvette. The instrument uses the factory installed Water Constant to obtain the 1 cm values. For the SpectraMax ABS Plus you can read a cuvette that contains deionized water or buffer to use the Cuvette Reference correction method (typically not necessary when you use aqueous solutions with minimal alcohol, salt, or organic solvent content).

### Water Constant

The PathCheck technology is based on the absorbance of water in the near infrared spectral region (between 900 nm and 1000 nm). If the sample is completely aqueous, has no turbidity and has a low salt concentration (less than 0.5 M), the Water Constant correction method is sufficient. The Water Constant is determined for each instrument during manufacture and is stored in the instrument.

### Cuvette Reference

The Cuvette Reference correction method is supported by the SpectraMax M2, M2e, M3, M4, M5, M5e, SpectraMax ABS Plus, and SpectraMax Plus 384. This method is not applicable if the solvent contains a substance that absorbs in the 900 nm to 1000 nm range. See the Interfering Substances topic.

**Note:** The Cuvette Reference correction method that the software uses with the PathCheck Pathlength Measurement Technology is different from the reference read of a cuvette that occurs when you click the Ref button in the Cuvette Set section tool bar.



Use the Cuvette Reference correction method if the sample contains an organic solvent such as ethanol or methanol. When you add a non-interfering solvent to the aqueous sample, the water absorbance decreases proportionally to the percentage of organic solvent present. For example, 5% ethanol decreases the water absorbance by 5% and results in a 5% underestimation of the pathlength. To minimize the error, put the same water/solvent mixture in a cuvette and use the Cuvette Reference.

Place a standard 1 cm cuvette that contains the aqueous/solvent mixture you use for the plate samples into the cuvette port. The cuvette must be in place when you read the plate. When you click Read, the instrument first makes the 900 nm and 1000 nm measurements in the cuvette and then makes the designated measurements in the plate. The software temporarily stores the cuvette values and uses the cuvette values in the PathCheck calculations for the plate samples.

The Cuvette Reference that the software uses with the PathCheck Pathlength Measurement Technology is different from the reference read of a cuvette that occurs when you click the Ref button in the Cuvette Set section tool bar. The software uses the Cuvette Reference data for PathCheck calculations does not produce data that displays in a Cuvette Set section. The software uses the Cuvette Reference data for the PathCheck calculations in plates, not cuvettes. However, you can use the accessors in the Formula Editor dialog to obtain these values. See the !PathCheckLm1000 and !PathCheckLm900 accessor in the _SoftMax Pro Data Acquisition and Analysis Software Formula Reference Guide_.

**Note:** After you read a plate with PathCheck technology turned on, the software stores PathCheck information permanently in the document. You can apply or not apply PathCheck technology to the absorbance values. If you do select to use PathCheck technology for the plate read, you cannot apply the PathCheck Pathlength Measurement Technology feature after the read.



### Eliminating Pathlength Independent Component

Raw OD measurements of plate samples include both pathlength-dependent components (sample and solvent) and a pathlength-independent component (OD of plate material). The pathlength-independent component must be eliminated from the calculation to get valid results that have been normalized by the PathCheck technology. You can do this using a plate blank or using a plate background constant.

#### Use a Plate Blank

You can use this method if all samples in the plate are the same volume and the read does not depend on the PathCheck technology to correct for variability in volumes.

1. Designate a minimum of one well (preferably several) as Plate Blank.
2. Pipette buffer (for example, your sample matrix) into those wells and read along with the samples. Do not use an empty well for a blank.

The instrument automatically subtracts the average of the blank wells from each of the samples. The OD of the plate material is subtracted as part of the blank.

1. Select the Use Plate Blank check box in the Data Reduction dialog.

#### Use a Plate Background OD

If your sample volumes are not identical or if you choose not to use a Plate Blank, then you must use a Plate Background OD. Omitting a Plate Background OD results in artificially high values after being normalized by the PathCheck technology.

To determine the Plate Background OD:

1. Fill a clean plate with water.
2. Read at the wavelengths you will use for the samples.

The average OD value is the Plate Background OD. If you intend to read your samples at more than one wavelength, there should be a corresponding number of Plate Background OD values for each wavelength.

**Note:** It is important that you put water in the wells and do not read a dry plate for the Plate Background OD. A dry plate has a slightly higher OD value than a water filled plate because of differences in refractive indices. Use of a dry plate results in PathCheck technology normalized values that are lower than 1 cm cuvette values.



### Interfering Substances

Material that absorbs in the 900 nm to 1000 nm spectral region could interfere with PathCheck technology measurements. Fortunately, there are few materials that do interfere at the concentrations generally used.

Turbidity is the most common interference. If you can detect turbidity in your sample, you should not use the PathCheck technology. Turbidity elevates the 900 nm measurement more than the 1000 nm measurement and causes an erroneously low estimate of pathlength. Use of the Cuvette Reference does not reliably correct for turbidity.

Samples that are highly colored in the upper-visible spectrum might have absorbance that extends into the near-infrared (NIR) spectrum and can interfere with the PathCheck technology. Examples include Lowry assays, molybdate-based assays, and samples that contain hemoglobins or porphyrins. In general, if the sample is distinctly red or purple, you should check for interference before you use the PathCheck technology.

To determine possible color interference:

&#x20;Measure the OD at 900 nm and 1000 nm (both measured with air reference).  Subtract the 900 nm value from the 1000 nm value.

Do the same for pure water.

If the delta OD for the sample differs significantly from the delta OD for water, then you should not use the PathCheck technology.

Organic solvents could interfere with the PathCheck technology if they have absorbance in the region of the NIR water peak. Solvents such as ethanol and methanol do not absorb in the NIR region, so they do not interfere, except for causing a decrease in the water absorbance to the extent of their presence in the solution. If the solvent absorbs between 900 nm and 1000 nm, the interference would be similar to the interference of highly colored samples. If you add an organic solvent other than ethanol or methanol, you should run a Spectrum scan between 900 nm and 1000 nm to determine if the solvent would interfere with the PathCheck technology.
