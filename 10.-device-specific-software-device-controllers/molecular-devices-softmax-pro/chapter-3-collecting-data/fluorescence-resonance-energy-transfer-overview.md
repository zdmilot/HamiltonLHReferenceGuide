# Fluorescence Resonance Energy Transfer Overview

Fluorescence resonance energy transfer (FRET) is a distance-dependent interaction between the electronic excited states of two dye molecules in which excitation is transferred from a donor molecule to an acceptor molecule _without emission of a photon_.

FRET relies on the distance-dependent transfer of energy from a donor molecule to an acceptor molecule. Due to its sensitivity to distance, FRET has been used to investigate molecular interactions. FRET is the radiationless transmission of energy from a donor molecule to an acceptor molecule. The donor molecule is the dye or chromophore that initially absorbs the energy and the acceptor is the chromophore to which the energy is subsequently transferred. This resonance interaction occurs over greater than interatomic distances, without conversion to thermal energy, and without a molecular collision. The transfer of energy leads to a reduction in the fluorescence intensity and excited state lifetime of the donor, and an increase in the emission intensity of the acceptor. A pair of molecules that interact in such a manner that FRET occurs is often referred to as a donor/acceptor pair.

While there are many factors that influence FRET, the primary conditions that need to be met for FRET to occur are relatively few:

![](<../../../.gitbook/assets/0 (5) (1) (1) (1).png>) The donor and acceptor molecules must be in close proximity to each other.

![](<../../../.gitbook/assets/1 (5) (1) (1) (1).png>) The absorption or excitation spectrum of the acceptor must overlap the fluorescence emission spectrum of the donor.

The degree to which they overlap is referred to as the spectral overlap integral (J).

![](<../../../.gitbook/assets/2 (5) (1) (1) (1).png>)The donor and acceptor transition must be approximately parallel.

### Creating Fluorescence Polarization Mode Protocols

To create a Fluorescence Polarization Mode protocol:

1. Start the software. See Starting the Software on page 7.
2. Select an instrument. See Selecting an Instrument on page 58.
3. In the Navigation Tree, select a Plate section or Cuvette Set section.
4. Click ![](<../../../.gitbook/assets/3 (2) (1) (1).jpeg>) in the section toolbar, the Settings Information area, or on the Home tab to display the Settings dialog.
5. For the SpectraMax Paradigm and SpectraMax i3x, select a Fluorescence Polarization (FP) Detection Cartridge.
6. Select the ![](<../../../.gitbook/assets/4 (1) (1) (1).jpeg>) **FP** read mode.
7. Select a Read Type.
8. Define the settings.

For more information about the settings, see the SoftMax Pro Application Help.

1. After you define the instrument settings, click **OK** to close the Settings dialog.
2. Create a template, if applicable. See Template Editor on page 87.
3. Set Data Reduction parameters, if applicable. See Data Reduction on page 193.
4. Set Display options, if applicable. See Data Display Options on page 204.
5. Save the settings to a protocol. See Saving Protocols and Data Documents on page 22.

### Fluorescence Polarization Mode Protocol Overview

Fluorescence Polarization detection is based on Fluorescence Intensity, with the important difference that it uses plane-polarized light, rather than non-polarized light. Microplate readers measure the Fluorescence Polarization of the sample by detecting light emitted both parallel and perpendicular to the plane of excitation.

By using a fluorescent dye to label a small molecule, the binding of a small molecule to an interaction partner of equal or greater size can be monitored through its speed of rotation.

The Fluorescence Polarization read mode returns two sets of data: one for fluorescence intensity parallel (P) to the excitation plane, and the other for fluorescence intensity perpendicular (S) to the excitation plane. The software uses the S and P values to calculate the Polarization (mP) and Anisotropy (r) values.

Although the raw S and P values are the true actual values returned from the instrument, the calculated Polarization (mP) and Anisotropy (r) values are treated as the raw data. These become the basis for further reduction calculations.

You can choose to display these data types in the Plate section. When raw (S\&P) is displayed, the mP value is by default used for all reduction calculations. When exporting, the raw values that display are exported, whether mP, r, or Raw (S\&P).

Polarization (mP) is calculated as follows:

mP = 1000 \*

(parallel - (G \* perpendicular)) (parallel + (G \* perpendicular))

Anisotropy (r) is calculated as follows:

r = (parallel - (G \* perpendicular)) (parallel + (2G \* perpendicular))

**Optimizing Fluorescence Polarization Assays**

Fluorescence Polarization for the SpectraMax i3x Multi-Mode Detection Platform, the SpectraMax Paradigm Multi-Mode Microplate Reader, the SpectraMax M5 and M5e Multi- Mode Microplate Readers, the FlexStation 3 Multi-Mode Microplate Reader, and the FilterMax F3 and FilterMax F5 Multi-Mode Microplate Readers can be read from the top of a plate. The plastic from which a plate is formed has an effect on the light polarization, precluding bottom reads and reads of a covered plate from the top.

You should use solid black plates for reads. If the assay components seem to bind to the plate, as evidenced by poor mP dynamic range (small difference between bound and unbound tracer), you should use plates treated to minimize binding, or polypropylene plates, and add a very small quantity of detergent to the assay buffer.

Background wells, which contain all assay components minus the fluorophore, should be run alongside samples. If the signal in the background wells is more than 1/10 the signal in the wells that contain fluorophore, then background wells should be run on each assay plate. The average raw signal from the background's parallel and perpendicular reads should be subtracted from the raw parallel and perpendicular reads of each sample well before the mP calculation is done.

For best precision in assays that uses a low quantity of fluorophore (for example, <5 nm fluorescein), set the PMT sensitivity to High and the number of reads to 100. If a faster read speed is required, experiment with fewer flashes per well until acceptable precision andspeed are achieved. Fewer flashes result in a higher speed, but with less precision.
