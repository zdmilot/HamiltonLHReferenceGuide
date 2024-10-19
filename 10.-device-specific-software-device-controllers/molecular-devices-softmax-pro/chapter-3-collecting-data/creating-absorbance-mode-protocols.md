# Creating Absorbance Mode Protocols

To create an Absorbance Mode protocol:

1. Start the software. See Starting the Software on page 7.
2. Select an instrument. See Selecting an Instrument on page 58.
3. Open a document.
4. In the Navigation Tree, select a Plate section or a Cuvette Set section.
5. Click ![](<../../../.gitbook/assets/0 (15).jpeg>) in the section toolbar, the Settings Information area, or on the Home tab to display the Settings dialog.
6. For the SpectraMax Paradigm, select the Absorbance Detection Cartridge. For the SpectraMax i3x, select **Monochromator**.
7. Select the ![](<../../../.gitbook/assets/1 (13).jpeg>) **ABS** read mode.
8. Select a Read Type.
9. Define the settings.

For more information about the settings, see the SoftMax Pro Application Help.

1. After you define the instrument settings, click **OK** to close the Settings dialog.
2. Create a template, if applicable. See Template Editor on page 87.
3. Set Data Reduction parameters, if applicable. See Data Reduction on page 193.
4. Set Display options, if applicable. See Data Display Options on page 204.
5. Save the settings to a protocol. See Saving Protocols and Data Documents on page 22.

### Absorbance Mode Protocol Overview

Absorbance is the quantity of light absorbed by a solution. To measure absorbance accurately, it is necessary to eliminate light scatter. If there is no turbidity, then absorbance = optical density.

A = log10(I0 /I) = –log10(I/I0)

where _I0_ is intensity of the incident light before it enters the sample divided by the light after it passes through the sample, and _A_ is the measured absorbance.

### Applications of Absorbance

Absorbance measurements are used to quantify the concentration of an absorbing species. It must be known at what wavelength a species absorbs light. For example, the concentration of nucleic acids can be quantified by measuring the absorbance at 260 nm.

### Optimizing Absorbance Assays

You can adjust the wavelength of the incident light in 1 nm increments. The software allows you to read up to six wavelengths per plate or cuvette for Endpoint and Kinetic read types and up to four wavelengths for Well Scan reads.

It is good scientific practice to designate wells in the plate to serve as plate blanks or group blanks in the Template Editor dialog from a Plate section. See Template Editor on page 87.

You can use the PathCheck Pathlength Measurement Technology feature to normalize the data to a 1 cm pathlength. See PathCheck Pathlength Measurement Technology on page 280.

![](<../../../.gitbook/assets/0 (8) (1) (1).png>)

**Note:** Assay optimization requires the use of a computer and SoftMax Pro Software.
