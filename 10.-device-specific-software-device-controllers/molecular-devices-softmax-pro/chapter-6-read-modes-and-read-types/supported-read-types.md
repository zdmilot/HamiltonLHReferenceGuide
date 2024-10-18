# Supported Read Types

For most read modes, you can use the Endpoint, Kinetic, Well Scan, and Spectrum read types. In addition, the FlexStation 3 supports the Flex read type that allow you to integrate fluid transfer with a Kinetic read.

### Endpoint Read Type

For the Endpoint read type, a read of each plate well is taken in the center of each well, at a single wavelength or at multiple wavelengths. Depending on the read mode, raw data values are reported as optical density (OD), %Transmittance (%T), relative fluorescence units (RFU), or relative luminescence units (RLU).

### Kinetic Read Type

For the Kinetic read type, the instrument collects data over time with reads taken in the center of each well at regular intervals. To get the shortest possible interval for multiple- wavelength Kinetic reads, choose wavelengths in ascending order.

The values calculated based on raw kinetic data include VMax, VMax per Sec, Time to VMax, Onset Time, and more. Kinetic reads can be single-wavelength or multiple-wavelength reads.

Kinetic analysis can collect data points in time intervals of seconds, minutes, hours, or days.

Kinetic analysis has many advantages when determining the relative activity of an enzyme in different types of plate assays, including ELISAs and the purification and characterization of enzymes and enzyme conjugates. Kinetic analysis can provide improved dynamic range, precision, and sensitivity relative to endpoint analysis.

Peak Pro™ Analysis functions provide advanced peak detection and characterization for applicable kinetic reads. See the _SoftMax Pro Data Acquisition and Analysis Software Formula Reference Guide_.

### Fast Kinetic Read Type

In a Fast Kinetic read the instrument performs repeated reads of one or more wells up to a 200 point maximum integration. All reads of a single well are made before the next well is read. You cannot Pre-read a plate with the Fast Kinetic read type. Each well can receive multiple injections and reads. You can specify multiple injections and multiple reads, for multiple times. You can set the integration time from 0.01 to 3600 seconds.

### Spectrum Read Type

Depending on the read mode you select, the Spectrum read type measures optical density (OD), %Transmittance (%T), relative fluorescence units (RFU), or relative luminescence units (RLU) across a spectrum of wavelengths.

### Well Scan Read Type

The Well Scan read type takes reads at more than one location within a well. The Well Scan read type takes multiple reads of a single well of a plate on an evenly spaced pattern inside of each well at single or multiple wavelengths.

Some applications involve the detection of cells in large area tissue culture plates. Use the Well Scan read type with such plates to permit maximum surface area detection in cell-based protocols. Since many cell lines tend to grow as clumps or in the corners of plate wells, you can choose from several patterns and define the number of points to scan in order achieve the best results for your application.

Depending on the read mode selected, the values are reported as optical density (OD),

%Transmittance (%T), relative fluorescence units (RFU), or relative luminescence units (RLU).

### Dual Read Type

In a Dual Read, each well receives two injections and two reads. The first injection is the P- injection with a subsequent read. The second injection is the M-injection with a subsequent read. You can set a delay time after each injection, from 0.1 to 3,600 seconds for the P- injection, and from 0 to 3,600 seconds for the M-injection.

### Flex Read Type

The fluidics module in the FlexStation 3 is designed to aspirate fluids from a compound source plate and dispense them into an assay plate. Fluid transfer is made possible with an 8- channel or 16-channel pipettor that is fully automated, including changing the tips from a tip rack.

In the Flex read type, one to eight or one to sixteen wells in one column of the assay plate are read repeatedly for a selected total experimental time. At a preselected point or points during that time sequence, the pipettor can transfer up to three reagents from the compound plate to the assay plate. The instrument continues to read at the preselected time intervals before and after each fluid transfer. After completion of a column read (or partial column) for a preselected time, the instrument can repeat this cycle with other columns. All data the software collects in one document is represented as a 96-well or 384- well plate.

For example, an experiment with a two-minute run time accommodates a 96-well plate in about 24 minutes.

Run time × Number of columns = Plate time 2 minutes × 12 columns = 24 minutes

### Membrane Read Type

The Membrane read type is used for a Time-Resolved Fluorescence read of a Western Blot membrane. The selected area is read, and a TIFF image is generated with the results of the read.

The Molecular Devices ScanLater™ Western Blot Assay Kit is a novel system for protein analysis that can be used with the SpectraMax Paradigm, SpectraMax i3x, and SpectraMax iD5. Membranes are incubated with Eu-chelate labeled secondary antibodies or streptavidin that bind specifically to the target protein-specific primary antibody. For more information, contact your Molecular Devices representative or search the knowledge base for ScanLater or Western Blot at [www.moleculardevices.com/service-support](http://www.moleculardevices.com/service-support).

If you use the SoftMax Pro Software - GxP edition, you must have the following permissions to complete a Western Blot membrane read:

![](<../../../.gitbook/assets/11 (10).png>) **Read Empty Plates/Cuvettes** to start a read.

![](<../../../.gitbook/assets/12 (9).png>) **Create/Save Data Documents** to save the data document before the read.

![](<../../../.gitbook/assets/13 (8).png>) **Overwrite Plate/Cuvette Data** to do a high-resolution ROI read. See SoftMax Pro Software - GxP Edition on page 247.
