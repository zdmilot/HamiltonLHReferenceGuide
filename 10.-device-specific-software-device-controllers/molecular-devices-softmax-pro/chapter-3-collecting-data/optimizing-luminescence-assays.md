# Optimizing Luminescence Assays

Luminescence can be read from the top or the bottom of a plate. You should use solid white plates or white plates with clear bottoms for luminescence reads.

For standard luminescence a separate light path without monochromators carries the emitted light to a dedicated PMT. The optimal emission wavelength is between 360 nm and 630 nm. In the Settings dialog the emission says **All**.

For wavelength-selectable luminescence, the instrument uses the emission monochromator to differentiate the wavelengths being emitted from the well. You can define multiple emission wavelengths.

To read only one luminescent event in the well, you can get the best sensitivity using the standard luminescence measurement, without a wavelength selected.

Luminescence read times are not designated by multiple reads per well, but rather by the total integration time you enter (between 1 ms and 1500 ms). Typical luminescence assays require between 500 ms and 1000 ms integration.

If wells are incubated for a long period of time, you should mix the plate before the read. This can be done using the Shake setting.

If it seems that the signal is always higher in the first wells read (for example, column A), you should dark adapt the plate to reduce the auto-luminescence of the white plastic. To help eliminate background luminescence from a plate that has been exposed to light, you should dark adapt the plate by placing the sample-loaded plate inside the instrument for severalminutes before you start the read.

### Creating Time-Resolved Fluorescence Mode Protocols

To create a Time-Resolved Fluorescence Mode protocol:

1. Start the software. See Starting the Software on page 7.
2. Select an instrument. See Selecting an Instrument on page 58.
3. In the Navigation Tree, select a Plate section or Cuvette Set section.
4. Click ![](<../../../.gitbook/assets/0 (8) (1).jpeg>) in the section toolbar, the Settings Information area, or on the Home tab to display the Settings dialog.
5. For the SpectraMax Paradigm and SpectraMax i3x, select a TRF-capable detection cartridge.
6. Click ![](<../../../.gitbook/assets/1 (8).jpeg>) **TRF** to select the **Time-Resolved Fluorescence** read mode.
7. Click a Read Type.
8. Define the settings.

For more information about the settings, see the SoftMax Pro Application Help.

1. After you define the instrument settings, click **OK** to close the Settings dialog.
2. Create a template, if applicable. See Template Editor on page 87.
3. Set Data Reduction parameters, if applicable. See Data Reduction on page 193.
4. Set Display options, if applicable. See Data Display Options on page 204.
5. Save the settings to a protocol. See Saving Protocols and Data Documents on page 22.

### Time-Resolved Fluorescence Mode Overview

In Time-Resolved Fluorescence (TRF) read mode, the instrument detects the extremely long emission half-lives of rare earth elements called lanthanides.

Time-Resolved Fluorescence is a measurement technique that depends on three characteristics that lead to better discrimination between the specific signal, proportional to the quantity of label, and the unspecific fluorescence resulting from background and compound interference:

![](<../../../.gitbook/assets/2 (4) (1) (1).png>) Pulsed excitation light sources

![](<../../../.gitbook/assets/3 (8) (1) (1).png>) Time-gated electronics faster than the fluorescence lifetime ![](<../../../.gitbook/assets/4 (9) (1) (1).png>) Labels with prolonged fluorescence lifetime

The time-gating electronics introduce a delay between the cutoff of each light pulse and the start of signal collection. During the delay, the unspecific fluorescence (caused by test compounds, assay reagents, and the plate) vanishes, while only a small portion of the specific fluorescence from the label is sacrificed. Enough of the specific signal remains during the decay period, with the added benefit of reduced background.

The use of long-lived fluorophores combined with time-resolved detection (a delay between excitation and emission detection) minimizes interference from fluorescence excitation light. Assays with these long-lifetime fluorophores have the advantage of very low background fluorescence. TRF detection is widely used in high throughput screening applications such as kinase assays.

In normal Fluorescence Intensity mode, the reads are taken while the lamp is on. The most common limitation to sensitivity in normal fluorescence is excitation energy or background fluorescence that cannot be eliminated from the emission signal. Since the lamp is the source of excitation energy, turning it off provides the best means of eliminating background excitation. The elimination of background excitation is the critical difference between fluorescence intensity measurements and TRF measurements.

### Optimizing Time-Resolved Fluorescence Assays

For the Time-Resolved Fluorescence read mode, the instrument flashes the excitation lamp, then, after the lamp is off, collects the delayed emission for a period of time before the lamp flashes again. Long-lifetime rare-earth lanthanide dyes are generally used to provide a long- lived fluorescent signal that persists after the lamp turns off. Background fluorescence fades, while lanthanide chelates and cryptates have fluorescent lifetimes between 100 µs and 2 ms.

Time-Resolved Fluorescence assays can be read from the top or bottom of a plate. You should use solid white plates for top reads, and white plates with clear bottoms for bottom reads.

To optimize data collection for a particular assay, you define when to start and end data acquisition. The minimum is 50 µs after the lamp turns off and the maximum is 1450 µs, in 50 µs or 200 µs steps.

If the assay you use has low signal or gives results with high %CV, use 100 reads per well. If you require a faster read speed, experiment with fewer flashes per well until you achieve acceptable precision and speed.

The important settings to get the best results in Time-Resolved Fluorescence assays are integration delay and integration time:

To define TRF settings:

1. Click the **Integration Delay** drop-down and select the amount of time to elapse between the flash of the lamp (excitation) and the beginning of data acquisition from the well (emission).
2. Click the **Integration Time** drop-down and select the amount of time for the instrument to read the well.

The integration delay and integration time are usually specified in the package insert of commercially available Time-Resolved Fluorescence reagent kits. If you do not use a kit, start with a delay of 50 µs and try different delays up to 400 µs with a fixed integration time of

400 µs. After you choose the optimal delay, based on the highest ratio of a well that contains a fluorophore divided by wells that contain only buffer, optimize the integration time, which is generally between 400 µs and 1000 µs.

Some examples of TRF assays are:

![](<../../../.gitbook/assets/0 (6) (1) (1).png>) IMAP® TR-FRET

![](<../../../.gitbook/assets/1 (6) (1) (1).png>) Cisbio HTRF

![](<../../../.gitbook/assets/2 (6) (1) (1).png>) LanthaScreen TR-FRET ![](<../../../.gitbook/assets/3 (9) (1) (1).png>) LANCE TR-FRET

![](<../../../.gitbook/assets/4 (10) (1) (1).png>)DELFIA TRF
