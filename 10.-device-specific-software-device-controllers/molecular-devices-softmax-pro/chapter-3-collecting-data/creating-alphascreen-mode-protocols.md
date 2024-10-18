# Creating AlphaScreen Mode Protocols

To create an AlphaScreen Mode protocol:

1. Start the software. See Starting the Software on page 7.
2. Select the SpectraMax Paradigm or SpectraMax i3x instrument. See Selecting an Instrument on page 58.
3. In the Navigation Tree, select a Plate section.
4. Click ![](<../../../.gitbook/assets/0 (6) (1).jpeg>) in the section toolbar, the Settings Information area, or on the Home tab to display the Settings dialog.
5. Select an AlphaScreen Detection Cartridge.
6. Select the ![](<../../../.gitbook/assets/1 (5) (1).jpeg>) **Screen** read mode.
7. Select a Read Type.
8. Define the settings.

For more information about the settings, see the SoftMax Pro Application Help.

1. After you define the instrument settings, click **OK** to close the Settings dialog.
2. Create a template, if applicable. See Template Editor on page 87.
3. Set Data Reduction parameters, if applicable. See Data Reduction on page 193.
4. Set Display options, if applicable. See Data Display Options on page 204.
5. Save the settings to a protocol. See Saving Protocols and Data Documents on page 22.

### AlphaScreen Mode Protocol Overview

ALPHA stands for Amplified Luminescent Proximity Homogeneous Assay. AlphaScreen® is a bead-based chemistry used to study molecular interactions between moieties A and B, for example. When a biological interaction between A and B moves beads (coated with A and B, respectively) together, a cascade of chemical reactions produce a greatly amplified signal.

The cascade finally resulting in signal is triggered by laser excitation (680 nm), making a photosensitizer on the A-beads convert oxygen to an excited (singlet) state. The energized oxygen diffuses away from the A-bead. When reaching the B-bead in close proximity, it reacts with a thioxene derivative on the B-bead generating chemiluminescence at 370 nm. Energy transfer to a fluorescent dye on the same bead shifts the emission wavelength into the

520 nm to 620 nm range. The limited lifetime of singlet oxygen in solvent (\~4 microseconds) lets diffusion reach up to only around 200 nm distance. Thus, only B-beads in the proximity of A-beads yield signal, which indicates binding between moieties A and B.

An AlphaScreen measurement includes a light pulse, by turning on the laser diode for a specified time, turning off the laser diode, followed by the measurement of the AlphaScreen signal, as specified in the measurement protocol timing parameters.

**Note:** AlphaScreen beads are light sensitive. Beads are best handled under subdued (<100 lux) or green filtered (Roscolux filters #389 from Rosco, or equivalent) light conditions. Do incubation steps in the dark.

![](<../../../.gitbook/assets/0 (4) (1).png>)

For more information, see AlphaScreen Read Mode on page 306.
