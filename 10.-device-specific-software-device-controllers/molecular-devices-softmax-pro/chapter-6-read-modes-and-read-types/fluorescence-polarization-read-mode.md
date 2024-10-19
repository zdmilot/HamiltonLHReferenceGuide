# Fluorescence Polarization Read Mode

The Fluorescence Polarization (FP) read mode measures the relative change of polarization of emitted fluorescence compared to excitation light.

Fluorescence Polarization detection is based on Fluorescence Intensity, with the important difference that it uses plane-polarized light, rather than non-polarized light. Microplate readers measure the Fluorescence Polarization of the sample by detecting light emitted both parallel and perpendicular to the plane of excitation.

By using a fluorescent dye to label a small molecule, the binding of a small molecule to an interaction partner of equal or greater size can be monitored through its speed of rotation.

When molecules are excited with polarized light, the change in the polarization of the emitted light depends on the size of the molecule to which the fluorophore is bound (the emitted light quickly depolarizes if the fluorescent molecule is unbound). Larger molecules yield a stronger polarization of the emitted light, while smaller molecules cause less polarization because of their rapid molecular movement. Fluorescence Polarization is used for molecular binding assays in high-throughput screening (HTS).

### Applications of Fluorescence Polarization

Fluorescence Polarization measurements provide information on molecular mobility and are generally used to quantify the success of a binding reaction between a smaller labeled ligand and a binding site at a much larger or immobilized molecule. Fluorescence Polarization can also be used to quantify the dissociation or cleavage of the labeled ligand from a binding site.

Fluorescence Polarization is a homogeneous plate assay technique and requires only mixing and measuring—no wash steps are required as in an ELISA. It can also be miniaturized, which makes it useful for high-throughput screening applications.

For information about how to set up a Fluorescence Polarization mode protocol, see Creating Fluorescence Polarization Mode Protocols on page 172.

### Fluorescence Polarization Instruments and Detection Cartridges

The following instruments have Fluorescence Polarization read mode capability: ![](<../../../.gitbook/assets/0 (9) (1) (1).png>) SpectraMax iD5 Multi-Mode Microplate Reader on page 320

![](<../../../.gitbook/assets/1 (10) (1) (1).png>) SpectraMax i3x and SpectraMax i3 Multi-Mode Detection Platforms, see page 323 ( i3x requires a Fluorescence Polarization (FP) Detection Cartridges, see page 349)

SpectraMax Paradigm Multi-Mode Microplate Reader, see page 327 ( requires a Fluorescence Polarization (FP) Detection Cartridges, see page 349)

SpectraMax M5 and SpectraMax M5e Multi-Mode Microplate Readers, see page 330 FlexStation 3 Multi-Mode Microplate Reader, see page 335

FilterMax F5 Multi-Mode Microplate Reader, see page 335

![](<../../../.gitbook/assets/2 (12) (1).png>)

**Note:** For the SpectraMax i3x, you can use the detection cartridges for top reads only.

### Analyzing Fluorescence Polarization Data

The Fluorescence Polarization read mode returns two sets of data: one for fluorescence intensity parallel (P) to the excitation plane, and the other for fluorescence intensity perpendicular (S) to the excitation plane. The software uses the S and P values to calculate the Polarization (mP) and Anisotropy (r) values.

Fluorescence Polarization assays in plates are generally designed with two control samples:

![](<../../../.gitbook/assets/3 (13) (1).png>) LOW control sample: minimal polarization value resulting from unbound labeled ligand only

![](<../../../.gitbook/assets/4 (11) (1).png>) HIGH control sample: maximum polarization value resulting from bound labeled ligand only

The Fluorescence Polarization data for a sample is evaluated based on its relative position between the low and high control values. Total intensity can also be determined from the raw data and is proportional to the quantity of label in a sample.

### Blank Correction

Many Fluorescence Polarization assays use small fluorescent label concentrations in the lower nm range. In this range, blank controls become significant when compared to samples.

A blank well contains everything used with the sample wells except the label and sample- specific compounds. Do not use an empty well for a blank.

Background wells, which contain all assay components minus the fluorophore, should be tested. If the signal in the background wells is more than 1/10 the signal in the wells that contain fluorophore, then background wells should be run on each assay plate. The average raw signal from the background's parallel and perpendicular reads must be subtracted from the raw parallel and perpendicular reads of each sample well before the mP calculation is done.

For optimal results, you should run replicates for all blanks, controls, and samples. In this case, the blank value that will be subtracted is the average value of all blanks.

### Data Reduction

Although the raw S and P values are the true actual values returned from the instrument, the calculated Polarization (mP) and Anisotropy (r) values are treated as the raw data and become the basis for further reduction calculations.

Polarization (mP) is calculated as follows:

mP = 1000 \*

(parallel - (G \* perpendicular)) (parallel + (G \* perpendicular))

Anisotropy (r) is calculated as follows:

r = (parallel - (G \* perpendicular)) (parallel + (2G \* perpendicular))

The G factor, or grating factor, is used in Fluorescence Polarization to correct polarization data for optical artifacts, converting relative mP data to theoretical mP data. Optical systems, particularly with reflective components, pass light of different polarization with different efficiency. G factor corrects for this instrument-based bias.

### Data Qualification and Validation

When you validate the data of a Fluorescence Polarization measurement and the assay, the two factors to look at are the precision value and the Z´ factor.

The FP precision value is a measure of replicate uniformity determined by the standard deviation of replicates at a label concentration of 1 nM. Since the precision of a measured signal also depends on the read time, the read time must also be specified. A longer read time leads to a lower (better) precision value.

Z´ is the standard statistical parameter in the high-throughput screening community for measuring the quality of a screening assay independent of test compounds. It is used as a measure of the signal separation between the positive controls and the negative controls in an assay.

The value of Z´ can be determined using the following formula:

3(SDc+ ) + 3(SDc– )

Z´ = 1 – | Mean – Mean |

c+

c–

where **SD** is the standard deviation, **c+** is the positive control, and **c–** is the negative control.

A Z´value greater than or equal to 0.4 is the generally acceptable minimum for an assay. You can use higher values when results are more critical.

Z´ is not linear and can be made unrealistically small by outliers that skew the standard deviations in either population. To improve the Z´value, you can increase the quantity of label in the sample, if acceptable for the assay, or increase the read time per well.

The assay window is dependent on the fluorophore lifetime and relative size of the receptor to the ligand. Precision values are better (lower) at higher signals, which normally come from higher label concentrations.

For a given assay window, Z´ is a downward sloping linear function. That is, as precision values get higher (worse), the Z´value gets lower (worse).

Precision is dependent upon assay characteristics (sample volume, label concentration) and read time. In many assays, the characteristics are defined and cannot be changed. In this case, the only way to improve precision is to increase the read time per well.
