# Instrument Settings

Use the Settings dialog to configure the settings for the instrument to use to read each Plate section and Cuvette Set section. Settings include the read mode, the read type, wavelengths, plate type, wells to read, PathCheck technology, optics settings, shake parameters, timing for Kinetic runs, speed read, and more.

To access the Settings dialog:

1. In the Navigation Tree, select a Plate section or Cuvette Set section.
2. Click ![](<../../../.gitbook/assets/2 (4) (1) (1).jpeg>) in the section toolbar, the Settings Information area, or on the Home tab to display the Settings dialog.

#### Standard View

Use the Settings dialog, for all instruments, to select a read mode and a read type. The settings that determine how the instrument is to read the plate or cuvette are then grouped into categories along the left side of the dialog. This is known as the Standard view of the Settings dialog. See Acquisition Settings on page 109.

You must use the Standard view to define the settings for Imaging reads and ScanLater Western Blot reads.

**CAUTION!** If you define an Imaging read or a ScanLater Western Blot read in the Standard view and then switch to the Acquisition view, your settings are not saved.

![](<../../../.gitbook/assets/3 (5) (1) (1) (1).png>)![](<../../../.gitbook/assets/4 (5) (1) (1).png>)

#### Acquisition View

The Settings dialog for the SpectraMax i3, SpectraMax i3x, SpectraMax iD3, and SpectraMax iD5 provides an Acquisition view to configure plate reads.

The Acquisition view uses an acquisition plan with tools that allow you to define settings in a workflow design when you need to do multi-step plate reads. See Acquisition View and Reads With Injectors on page 154.

To switch between the Standard view and the Acquisition view:

![](<../../../.gitbook/assets/5 (4) (1) (1) (1).png>) Click ![](<../../../.gitbook/assets/6 (1) (1).jpeg>) in the lower-left corner in the Settings dialog.

**CAUTION!** You must use the Acquisition view to define reads with injection. If you define a read with injection and then switch to the Standard view, your settings are not saved.

![](<../../../.gitbook/assets/7 (3) (1) (1) (1).png>)![](<../../../.gitbook/assets/8 (3) (1) (1) (1).png>)

**Acquisition Settings**

Use the Settings dialog to configure the following parameters for a Plate section or Cuvette Set section: read type, read mode, wavelengths, plate type, wells to read, PathCheck technology, optics, shake, timing for Kinetic runs, speed read, and more.

![](<../../../.gitbook/assets/9 (1) (1) (1).jpeg>)

Each Plate section or Cuvette Set section in a document must use the same instrument but can have different parameters for the acquisition settings.

To define acquisition settings:

1. In the Navigation Tree, select a Plate section or Cuvette Set section.
2. Click ![](<../../../.gitbook/assets/10 (2) (1).jpeg>) in the section toolbar, in the Settings Information area, or on the Home tab to display the Settings dialog.
3. For the SpectraMax Paradigm, SpectraMax i3, and SpectraMax i3x, select the detection cartridge or optical configuration to use. This determines the available read modes. See Selecting a Detection Cartridge or Optical Configuration on page 111.
4. For all instruments, select a read mode. This determines the available read types. ![](<../../../.gitbook/assets/11 (1) (1) (1) (1) (1) (1).png>) Absorbance Read Mode on page 278

![](<../../../.gitbook/assets/12 (2) (1) (1) (1).png>) Fluorescence Intensity Read Mode on page 284

![](<../../../.gitbook/assets/13 (2) (1) (1) (1).png>) Luminescence Read Mode on page 289 (Luminescence Dual Wavelength is available for the SpectraMax L and SpectraMax iD5)

![](<../../../.gitbook/assets/14 (2) (1) (1).png>) Time-Resolved Fluorescence Read Mode on page 293 ![](<../../../.gitbook/assets/15 (1) (1) (1) (1) (1).png>) FRET Read Mode on page 298

![](<../../../.gitbook/assets/16 (1) (1) (1) (1) (1).png>) HTRF Read Mode on page 300

![](<../../../.gitbook/assets/17 (2) (1) (1).png>) Fluorescence Polarization Read Mode on page 303 ![](<../../../.gitbook/assets/18 (1) (1) (1) (1) (1).png>) AlphaScreen Read Mode on page 306

![](<../../../.gitbook/assets/19 (10).png>) ScanLater Western Blot TRF Read Mode on page 309 ![](<../../../.gitbook/assets/20 (1) (1) (1) (1) (1).png>) Imaging Read Mode on page 312

1. Select a read type. This determines which setting categories appear in the Category list.  Endpoint Read Type on page 275

&#x20;Kinetic Read Type on page 275

&#x20;Spectrum Read Type on page 276  Well Scan Read Type on page 276  Flex Read Type on page 277

&#x20;Membrane Read Type on page 277

1. Select each category in the list on the left to display the corresponding settings. The options that display depend on the instrument, read mode, and read type you select.

&#x20;Wavelength Settings on page 113  Plate Type Settings on page 115

&#x20;Read Area Settings on page 119

&#x20;PathCheck Technology Settings on page 120  TRF Settings on page 121

&#x20;PMT and Optics Settings on page 121  Timing Settings on page 123

&#x20;Well Scan Settings on page 124  Shake Settings on page 124

&#x20;Speed Read Settings on page 125  Well Area Settings on page 126

&#x20;Image Acquisition Settings on page 126  Image Analysis Settings on page 128

&#x20;Region of Interest Settings on page 140  More Settings on page 141

&#x20;Compound Transfer Settings on page 145  Compound Source Settings on page 148  Pipette Tips Layout Settings on page 149

&#x20;Compound and Tips Columns Settings on page 150  Triturate Settings on page 153

&#x20;Acquisition View and Reads With Injectors on page 154

1. After you define the instrument settings, click **OK** to close the Settings dialog.

**Note:** You should save the document before you start a read. For Imaging reads and Western Blot reads, you must save the document before you start the read.



### Selecting a Detection Cartridge or Optical Configuration <a href="#bookmark2" id="bookmark2"></a>

When the instrument uses detection cartridges or another optional optical configuration, the Settings dialog displays the available options above the read modes. Each detection cartridge contains the light source, optics, and electrical components needed to do specific read modes for some applications. See Supported Detection Cartridges on page 343.

&#x20;The SpectraMax Paradigm requires detection cartridges to do reads.

&#x20;The SpectraMax i3x supports user-installable detection cartridges to expand its read capabilities. Cartridges are for top reads only.

**Note:** When you select to work offline in Simulator mode, the Settings dialog displays all detection cartridges that the instrument supports.



When you connect the computer to an instrument, the Settings dialog displays the detection cartridges that you install in the instrument.

For the SpectraMax i3x:

&#x20;Select **Monochromator** to use the instrument monochromator.

&#x20;Select **MiniMax** for imaging reads that use the SpectraMax MiniMax 300 Imaging Cytometer. For transmitted light imaging, you need to install the Transmitted Light (TL) Detection Cartridge, but you do not need to select it in the Settings dialog.

After you select the detection cartridge or optical configuration, select the read mode and read type for the protocol.

### Temperature Control

Use the Temperature Control dialog to set the temperature in the plate chamber when you use an instrument that provides temperature control. The instrument monitors the temperature of the air inside the plate chamber and the software displays the air temperature of the chamber on the Home tab. The temperature display continuously updates with the current air temperature in the chamber.

For instruments with a cuvette chamber, the instrument control panel displays the temperature within the cuvette chamber. The plate chamber temperature can be different from what displays on the instrument control panel. The software plate chamber temperature display should be similar to the control panel temperature display after both chambers reach equilibrium. During warm-up, you might notice a discrepancy in temperatures, which is normal.

You can set the temperature 2°C or more above the current air temperature in the chamber. After you turn on the temperature control, the chamber can take from 10 to 30 minutes to reach the set temperature, depending on the difference between the start temperature and the set temperature.

**Note:** The instrument temperature sensors detect the temperature of the air inside the chamber, not the temperature of the samples in the plate. If you use the instrument to warm the samples, you should use a seal or lid on the plate to prevent evaporation of the sample. A seal or lid helps to maintain uniform temperature.



Letting the prepared sample equilibrate inside the plate chamber can take an hour or more. You can speed up equilibration by pre-warming the sample and the assay reagents before you place the plate in the chamber. Validate the data quality to determine whether the seal or lid can stay on the plate for the read.

To set the temperature in the plate chamber:

1. Select the **Home** tab and click  **Temperature** to display the Temperature Control dialog.
2. Select the **On** option.
3. In the **Plate Chamber Set Point** field, enter the temperature in degrees Celsius.
4. Click **OK**.
5. After you turn off the temperature control, open the plate drawer to help the platechamber cool to the ambient temperature.

### Wavelength Settings

Use the Wavelengths category in the Settings dialog to define wavelength settings. These settings are dependent on the instrument, read mode, and read type you select.

Some instruments allow you to choose to use all wavelengths for the read or to specify specific bandwidths. Select the spectral bandwidth of the wavelength. The instrument uses the bandwidth you select for all the wavelengths in a multiple wavelength read.

The user guide for each instrument describes the instrument's bandwidth range and how to optimize excitation and emission wavelengths for a protocol. See the instrument user guide.

#### Fluorescence Intensity Read Mode

To define wavelengths for the Fluorescence Intensity read mode:

1. Click the **Number of Wavelength Pairs** drop-down and select the number of wavelength pairs.
2. In the **Excitation** fields, enter the excitation wavelengths.
3. In the **Emission** fields, enter the emission wavelengths.

#### Endpoint, Kinetic, Well Scan, and Flex Read Types

To define wavelengths for the Endpoint, Kinetic, Well Scan, and Flex read types:

1. Click the **Number of Wavelengths** drop-down and select the number of wavelengths to read.
2. For each wavelength, enter or select the wavelength value for the read.

#### Spectrum Read Type

To define wavelengths for the Spectrum read type:

*
  1. In the **Start** field, enter the starting wavelength.
  2. In the **Stop** field, enter the ending wavelength.
  3. In the **Step** field, enter the value for how much the wavelength should increment between reads. The minimum step increment is 1 nm.

#### Cutoffs

The Gemini™ XPS, Gemini™ EM, and SpectraMax M series instruments support cutoff filters. The term cutoff refers to the longpass filters the instrument uses to block unwanted residual excitation light and minimize background interference.

The cutoff settings depend on the read mode (Fluorescence, Fluorescence Polarization, or Time Resolved Fluorescence) and the read type (Endpoint, Kinetic, Spectrum, or Well Scan). The Luminescence read mode does not use emission cutoff filters.

To define the cutoff filters:

&#x20;Select the **Auto Cutoff** check box to have the software choose the longpass emission filter based on the excitation wavelength you enter.

&#x20;Clear the **Auto Cutoff** check box, then click the drop-down and select the cutoff filter for each wavelength. For the Spectrum read type you must select a cutoff filter (or None).

When you clear the Auto Cutoff check box, to determine the manual setting for a cutoff filter, you need to know the value of the Stokes shift, which is the difference between the wavelengths of the excitation and emission maxima. If the Stokes shift is small, choose an excitation wavelength that is as far as possible from the emission maximum while still capable of exciting the fluorophore. This causes less of the excited light to overlap the emission spectrum which permits better selection and quantitation of the emitted light.

#### Imaging Read Mode

Select the wavelengths or channels to use. The software acquires images separately for each wavelength or channel and you can analyze each image separately.

The SpectraMax MiniMax 300 Imaging Cytometer captures images from the bottom of each plate well. You can illuminate the sample with white transmitted light from the top of the plate when you use the Transmitted Light (TL) Detection Cartridge, or you can use fluorescent excitation from the bottom of the plate. See Transmitted Light (TL) Detection Cartridge on page 351.

#### Path of Selected Light Sources

| **Item** | **Description**                                                         |
| -------- | ----------------------------------------------------------------------- |
| 1        | Transmitted Light (TL) Detection Cartridge                              |
| 2        | Path of white light from the Transmitted Light (TL) Detection Cartridge |
| 3        | Path of fluorescent excitation                                          |
| 4        | Light source for fluorescent excitation                                 |
| 5        | Camera lens                                                             |

For best results with transmitted-light reads, use a plate with no cover. You can use a clearcover, if required. For Fluorescent reads, you can use a plate with a solid cover.

### Plate Type Settings

Use the Plate Type category in the Settings dialog to select the type of plate to read. The software includes a plate library that contains plates of various sizes with standard dimensions. If you are uncertain which plate to use, select the Standard plate definition.

If you change the Plate Type setting, the software discards the well assignments for the template you assign to that Plate section. Group sections remain and you can select new wells to assign to the existing Group sections.

Your plate selection determines the display of the wells in the Plate section in the Workspace.

To define the plate setting:

1. Click the **Plate Format** drop-down and select the number of wells in the plate.
2. Select the **Is Lidded** check box if the plate has a lid.

**CAUTION!** If the plate has a lid, you must verify that the plate height with a lid is set accurately in the Plate Editor dialog before you start a read.



1. In the **Select Specific** list, select the plate to read.

For the SpectraMax Paradigm you can define the plate orientation to match the orientation of the plate in the drawer.

To define the plate orientation:

&#x20;Select **Landscape** to put the A1 location in the upper-left corner closest to the instrument.

&#x20;Select **Portrait** to put the A1 location in the upper-right corner closest to the instrument.

&#x20;Select **Opposite Landscape** to put the A1 location in the lower-right corner farthest from the instrument.

&#x20;Select **Opposite Portrait** to put the A1 location in the lower-left corner farthest from the instrument.

### Edit Plate

You can edit the dimensions of a plate or add a custom plate to the plate library.

**Note:** You can use the custom plate definitions you create or edit for Imaging reads when you select the Imaging read mode. Plate definitions you create, edit, or optimize for other read modes do not appear in the list of available plates for the Imaging read mode.



To edit the dimensions of a plate or to add a new plate to the library:

*
  1. Select a plate from the list.
  2. Click **Edit Plate** to display the Plate Editor dialog. See Plate Editor on page 117.
  3. For a new plate, in the **Plate Name** field, enter the name for the plate.
  4. Define the plate dimensions and click **Save**.
  5. You can select the plate and click **Remove** to remove it from the plate library.

**CAUTION!** The SpectraMax Paradigm, SpectraMax i3x, SpectraMax iD3, SpectraMax iD5, and FilterMax F5 have an automatic read height (Z-height) adjustment for Fluorescence read mode and Luminescence read mode. For top reads, the lens or the plate can be damaged if you do not properly set the plate height. If the plate has a lid, you must select the Is Lidded check box and verify that the plate height with a lid is set accurately in the Plate Editor dialog before you start a read.



### Import Plate Definitions

You can import plates for the SpectraMax i3, SpectraMax i3x, SpectraMax Paradigm, SpectraMax iD3, SpectraMax iD5, FilterMax F3, and FilterMax F5.

To import plate definitions:

1. Click **Import Plate** to display the Open dialog.
2. Navigate to and select the plate definition file: Plate File \*.plt format or Multimode File

\*.xml format.

1. Click **Open**.

### Plate Editor <a href="#bookmark5" id="bookmark5"></a>

Use the Plate Editor dialog to modify the definition of a plate or to add a plate definition to the plate library. The software saves plate definitions with a \*.plt file in a sub-folder of the Program Data folder. Custom plate definitions save to the computer. When you open a protocol that uses a custom plate definition that you save on a different computer, the software allows you to save the custom plate definition on the new computer.

**CAUTION!** To prevent damage to the instrument, set the plate height and read height accurately before you start a read.



To edit a plate definition:

1. In the Navigation Tree, select a Plate section.
2. Click  in the section toolbar, the Settings Information area, or on the Home tab to display the Settings dialog.
3. Select the **Plate Type** category.
4. Click the **Plate Format** drop-down and select the number of wells in the plate.
5. In the **Select Specific** list, select the plate to edit or copy.
6. Click **Edit Plate** to display the Plate Editor dialog. In the Acquisition view, click  to display the Plate Editor dialog.
7. To create a new plate, in the **Plate Name** field, enter the new plate name.
8. If you access the Plate Editor from the Acquisition view, you can click **Delete** to remove a custom plate definition. You cannot remove the plates installed with the software.
9. After you define the plate settings described in the table on the following page, click

#### Save.

**Note:** For the Left Edge to Left Well Center measurement in the table on the following page, the distance from the left edge of the plate to the center of well A1 must also include an offset for the angle of the optics. To determine the correct settings for these fields, measure the applicable areas of the plate in the lab.



**Plate Editor Settings (all measurements in millimeters)**

| **Field Name**                   | **Image**    | **Description**                                                                                                                                                                                                                                                                                                                                                            |
| -------------------------------- | ------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Left Edge to Left Well Center    | F3NLbE9MScag | Enter the distance from the left edge of the plate to the center of well A1.                                                                                                                                                                                                                                                                                               |
| Horizontal Center to Center      | Uoupldk4siIy | Enter the horizontal distance between well centers.                                                                                                                                                                                                                                                                                                                        |
| Top Edge to Top Left Well Center | kX4YfjwIJfOj | Enter the distance from the top edge of the plate to the center of well A1.                                                                                                                                                                                                                                                                                                |
| Vertical Center to Center        | phPMugo58Vfv | Enter the vertical distance between well centers.                                                                                                                                                                                                                                                                                                                          |
| Well Diameter and Well Shape     | jBFsu3W7Vt43 | Enter the diameter of a round well or the width of a square well. For the SpectraMax i3, SpectraMax i3x, SpectraMax Paradigm, SpectraMax iD3, SpectraMax iD5, FilterMax F3, and FilterMax F5, select the **Well Shape Square** check box for square wells.                                                                                                                 |
| Well Bottom Type / Thickness     | IYfKQh04ClZE | Select the **Clear Well Bottom** check box if the wells have a clear bottom, rather than opaque. For the SpectraMax i3x with the SpectraMax MiniMax 300 Imaging Cytometer, enter the thickness of the bottom of the well of the plate. This determines the initial focus distance for Imaging reads.                                                                       |
| <p>Well Volume</p><p>/ Depth</p> | ySRvG1gPGprf | For the SpectraMax i3, SpectraMax i3x, SpectraMax Paradigm, SpectraMax iD3, SpectraMax iD5, FilterMax F3, and FilterMax F5, enter the depth of the well. For the SpectraMax i3x with the SpectraMax Injector Cartridge, enter the working volume of the well for the plate in microliters. This determines the maximum allowable dispense volume for reads with injection. |
| Plate Height                     | aX3aT5Prde5g | For the SpectraMax i3, SpectraMax i3x, SpectraMax Paradigm, SpectraMax iD3, SpectraMax iD5, FilterMax F3, and FilterMax F5, enter the height of the plate in millimeters and also the height of the plate with a lid. This determines the read height for top reads.                                                                                                       |
| Plate Length                     | Xo2phP7cjjJr | For the SpectraMax i3, SpectraMax i3x, SpectraMax Paradigm, SpectraMax iD3, SpectraMax iD5, FilterMax F3, and FilterMax F5, enter the length of the plate.                                                                                                                                                                                                                 |

**Plate Editor Settings (all measurements in millimeters) (continued)**

| **Field Name** | **Image**    | **Description**                                                                                                                                           |
| -------------- | ------------ | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Plate Width    | GhOz9VbFHmj7 | For the SpectraMax i3, SpectraMax i3x, SpectraMax Paradigm, SpectraMax iD3, SpectraMax iD5, FilterMax F3, and FilterMax F5, enter the width of the plate. |

### Read Area Settings <a href="#bookmark6" id="bookmark6"></a>

Use the Read Area category in the Settings dialog to select the wells to read. Partial plate reads are available for all read types, although it is most useful for the Fast Kinetic read type or the Imaging read mode. Partial plate reads can significantly reduce the time required for the Kinetic read type or to acquire images because the instrument does not have to read the entire plate.

To select a contiguous, rectangular region on the plate:

&#x20;Drag the mouse pointer to select the wells to read.

Columns do not need to start with “1” but must be contiguous. To read all the wells in the plate:

&#x20;Select the **Select All** check box.

To select non-contiguous wells for the SpectraMax i3, SpectraMax iD3, SpectraMax iD5, and SpectraMax i3x:

1. Select the **More Settings** category.
2. Select the **Well** read order.
3. Select the **Read Area** category.
4. Press the **CTRL** key as you click each well.

If you select a partial plate read, only the wells to read are visible in the data display, to indicate that no data will be collected for the other wells. All wells display in the Template Editor dialog.

### Western Blot Membrane Read Area Settings

To scan a membrane, you must first place it in a Molecular Devices ScanLater™ membrane holder. See Loading the Membrane Holder on page 176.

A high resolution scan of the entire surface can take approximately 15 minutes. Define a smaller area for the scan to reduce the scan time. The Read Area category displays the approximate area to scan.

To select the area to scan from the Target Read Area list:

&#x20;Select **Mini Membrane** to scan an area 85 mm x 65 mm.

&#x20;Select **Whole Membrane Holder** to scan an area 109 mm x 77 mm.

&#x20;Select **ROI Selection** to scan an area based on the region of interest (ROI) you define and acquire in the Plate section.

If you do not define and acquire a region of interest in the Plate section, the ROISelection option is not available.

### PathCheck Technology Settings

Use the PathCheck category in the Settings dialog to use PathCheck Technology for Absorbance read mode Endpoint read type protocols. See PathCheck Pathlength Measurement Technology on page 280.

To define PathCheck settings:

&#x20;Select the **PathCheck** check box to use the PathCheck Technology Water Constant correction.

&#x20;Clear the **PathCheck** check box to not use the PathCheck Technology Water Constant correction.

The temperature-independent PathCheck® Pathlength Measurement Technology normalizes your absorbance values to a 1 cm path length based on the near-infrared absorbance of water.

The Beer–Lambert law states that absorbance is proportional to the distance that light travels through the sample:

A = cL

where _A_ is the absorbance, is the molar absorptivity of the sample, _c_ is the concentration of the sample, and _L_ is the pathlength. The longer the pathlength, the higher the absorbance.

Microplate readers use a vertical light path so the distance of the light through the sample depends on the volume. This variable pathlength makes it difficult to do extinction-based assays and makes it confusing to compare results between microplate readers and spectrophotometers.

The standard pathlength of a 1 cm cuvette is the conventional basis to quantify the unique absorptivity properties of compounds in solution. Quantitative analysis can be done on the basis of extinction coefficients, without standard curves (for example, NADH-based enzyme assays). When you use a cuvette, the pathlength is known and is independent of sample volume, so absorbance is directly proportional to concentration when there is nobackground interference.

### TRF Settings

Use the TRF Settings category in the Settings dialog to define the integration delay before data is collected and the integration time of the fluorescence signal. The Time-Resolved Fluorescence read mode measures fluorescence as a function of time after excitation. See Time-Resolved Fluorescence Read Mode on page 293.

To define TRF settings:

1. Click the **Integration Delay** drop-down and select the amount of time to elapse between the flash of the lamp (excitation) and the beginning of data acquisition from the well (emission).
2. Click the **Integration Time** drop-down and select the amount of time for the instrumentto read the well.

### PMT and Optics Settings

Use the PMT and Optics category in the Settings dialog to define sensitivity settings for the Photomultiplier Tubes and optics for all read modes except Absorbance.

Click the **PMT Gain** drop-down:

&#x20;Select **Automatic** to have the instrument automatically adjust the PMT voltage for varying concentrations of sample in the plate. Available for the Fluorescence read mode with the Endpoint, Spectrum, and Well Scan read types. The Luminescence and Time- Resolved Fluorescence read modes use the Automatic setting and the following options are not available.

&#x20;Select **High** for samples that have a lower concentration (dim samples).  Select **Medium** for samples that have medium concentration.

&#x20;Select **Low** for samples that have a higher concentration (bright samples).  Select **Manual** to enter a specific voltage.

The SpectraMax i3x uses two light sources. The Spectral Fusion™ Illumination uses the spectral range of a high power Xenon flash lamp intensified by LEDs in the visible range. The instrument uses automatic LED power adjustment with high PMT Gain when the excitation wavelength is between 430 nm and 680 nm for high sensitivity across multiple fluorophores. In multiple-wavelength reads, the PMT Gain is set to High and cannot be changed.

For some instruments, the PMT sensitivity is set to Automatic for the Luminescence and Time Resolved Fluorescence read modes. For these instruments, the PMT Gain category is not available for these read modes.

To set the resolution for the full scan and for a secondary scan of a region of interest for Western Blot membrane scans:

*
  1. Click the **Default Scan Resolution** and select the resolution to apply to the entire read area of the membrane you define in the Read Area category settings.
  2. Click the **ROI Scan Resolution** and select the resolution to apply to the region of interest (ROI) you define in the Plate section.

A High resolution scan provides the best results. A Low resolution scan provides the fastest read.

The general workflow to acquire Western Blot data is to scan the read area of the membrane you define with a low resolution and then scan the region of interest (ROI) you define at a high resolution.

For some instruments in certain read modes, you can enter the **Integration Time** or the number of **Flashes Per Read**.

#### On-the-Fly Detection

For the SpectraMax Paradigm and for the SpectraMax i3x with some detection cartridges you can select the On the Fly Detection options.

On-the-Fly Detection yields faster read times because the plate moves continuously as the instrument measures each well.

To disable On-the-Fly Detection and have the plate stop moving for each read:  Select **Off-Stop and Go**.

To use On-the-Fly Detection:

&#x20;Select **Performance** for a faster read time than not using On the Fly Detection, but not as fast as the Speed mode. Performance provides considerably better results than Speed for demanding assays.

&#x20;Select **Speed** for the fastest possible read time per plate. However, there is a tradeoff between the data quality and read speed because the instrument samples each well for shorter integration times.

To set the integration time for the SpectraMax Paradigm and FilterMax F5, and the SpectraMax i3x with some detection cartridges:

&#x20;In the **Integration Time** field, enter the number of milliseconds needed to validate the measurement time per well.

To have an instrument with bottom read capability read up through the bottom of the plate:  Select the **Read From Bottom** check box.

For the SpectraMax i3, i3x, iD3, iD5, Paradigm, and FilterMax F5, you can specify the read height.

**CAUTION!** To prevent damage to the instrument, set the plate height and read height accurately before you start a read.



To set the read height:

&#x20;In the **Read Height** field, enter the distance in millimeters between the objective lens and the plate.

#### Read Height Optimization

Use the Read Height Optimization feature to find the optimized read height before the read.

1. Select the **More Settings** category.
2. Select the **Show Pre-Read Optimization Options** check box.

Read Height is available for the SpectraMax i3x and FilterMax F5 for top read only.

### Timing Settings

Use the Timing category in the Settings dialog to define the total run time and the time interval between reads for the Kinetic read type and Flex read type.

Each instrument has a unique minimum allowable read interval that depends on factors that include the number of wavelengths, the number of wells to read, and the distance the instrument filter wheel must move. The maximum read interval also varies by instrument, for example, the SpectraMax M2 has a maximum read interval of 2 hours and 45 minutes, and the SpectraMax Paradigm has a maximum read interval of 18 hours and 12 minutes. If you enter an invalid read interval, a message indicates the minimum or maximum allowable value for the read interval.

**Tip:** In some cases, choosing wavelengths in ascending order can yield the shortest possible interval.



The software calculates the minimum interval, maximum interval, and number of reads based on the values you enter in the Total Run Time field and the Interval field. The minimum permitted interval values display below the Interval field.

To define Timing settings when you select the Row and Column read order in the More Settings category:

1. In the **Total Run Time** field, enter the total run time.
2. In the **Interval** field, enter the time to wait between reads.

To define Timing settings when you select the Well read order in the More Settings category:

1. In the **Well Run Time** field, enter the well run time.
2. In the **Interval** field, enter the time to wait between reads. You can define the Interval down to the millisecond.

**Note:** Well read order is not available for the Time-Resolved Fluorescence read mode on the SpectraMax iD5.



Single Point Read sets the Total Run Time and the Interval to the same value and is useful when you run a multitask kinetic read with alternating read modes within a cycle. See Defining and Running Workflows on page 102.

To read only one time point:

Click **Single Point Read**.

### Well Scan Settings

Use the Well Scan Settings category in the Settings dialog to define the pattern and density for the reads within each well.

The Well Scan read type takes reads at more than one location within a well. The Well Scan read type takes multiple reads of a single well of a plate on an evenly spaced pattern inside of each well at single or multiple wavelengths.

Some applications involve the detection of cells in large area tissue culture plates. Use the Well Scan read type with such plates to permit maximum surface area detection in cell-based protocols. Since many cell lines tend to grow as clumps or in the corners of plate wells, you can choose from several patterns and define the number of points to scan in order achieve the best results for your application.

The image in the Well Scan settings displays the shape of the well based on the definition of the plate you select. The fill pattern is either round or square to match the well shape. The number of available points depends on the well size of the plate you select.

Density determines the number of points to read in the line patterns and the maximum number of horizontal and vertical points to include in the cross or fill pattern.

To define Well Scan settings:

*
  1. Select a **Pattern**. Up to four scan patterns are available, depending on the instrument.
*
  1. Click the **Density** drop-down and select the density.

### Shake Settings

Use the Shake category in the Settings dialog to set options to shake the plate in the chamber. Shake options are dependent on the instrument and the read type you select.

To define shake settings:

&#x20;Select the **Before First Read** check box to shake the plate for the duration you enter into the text field before the first wavelength read.

&#x20;Clear the **Before First Read** check box to not shake the plate.

For the Kinetic read type, you can shake the plate before the first read as described above and you can shake the plate between reads. For single wavelength reads, this shakes the plate before each read at that wavelength. For multiple wavelength reads, this shakes the plate before each read at the first wavelength only.

To define shake settings for the Kinetic read type:

&#x20;Select the **Between Reads** check box to shake the plate for the duration you enter into the text fields between reads.

&#x20;Clear the **Between Reads** check box to not shake the plate between reads.

**Note:** The Before First Read and Between Reads options are available in the Standard View. To shake the plate from the Acquisition view, place a Shake node in the time line where you want the shake to occur.



For the SpectraMax i3, SpectraMax i3x SpectraMax Paradigm, FilterMax F3, and FilterMax F5, define the following shake settings:

1. Select the **Before First Read** check box.
2. In the text field, enter the length of time to shake the plate in seconds.
3. Click the **Shake Intensity** drop-down and select **Low**, **Medium**, or **High**. The actual shake speed is based on the plate format.
4. Click the **Shake Mode** drop-down and select **Linear** or **Orbital**.

For the SpectraMax iD3 and SpectraMax iD5, define the following shake settings:

1. Select the **Before First Read** check box.
2. In the text field, enter the length of time to shake the plate in seconds.
3. Click the **Shake Intensity** drop-down and select **Low**, **Medium**, or **High**. The actual shake speed is based on the plate format.
4. Click the **Shake Mode** drop-down and select **Orbital**, **Linear**, or **Double Orbital**.

### Speed Read Settings

Use the Speed Read category in the Settings dialog to read the plate faster for the Absorbance read mode by decreasing the number of lamp flashes. The Speed Read option is useful for the Spectrum read type and can greatly reduce the protocol run time.

For instruments that support software calibration, Speed Read turns off calibration and uses the air calibration values stored in the instrument firmware. As a result, Speed Read might not provide as accurate an absorbance measurement at each wavelength of a scan as with the normal read.

To define Speed Read settings:

&#x20;Select the **Speed Read** check box to use the speed read.  Clear the **Speed Read** check box to not use speed read.

### Well Area Settings <a href="#bookmark14" id="bookmark14"></a>

Use the Well Area Settings category in the Settings dialog to acquire images at more than one location, or site, within a well to form a single seamless tiled image for the Imaging read mode. If you select to acquire images of more than one site in the well, the software tiles the images together into a single image for analysis. Image acquisition time increases with each site you select. For faster image acquisition, select fewer sites.

To define Well Area settings, select the number of sites to acquire:

### Image Acquisition Settings <a href="#bookmark15" id="bookmark15"></a>

Use the Image Acquisition Settings category in the Settings dialog to define the exposure time and focus adjustment for two sample wells. The instrument uses these settings for every well in the plate during acquisition. You can set the exposure and focus adjustment separately for each wavelength or channel.

The instrument acquires one site in each well. If you select to acquire more than one site, the instrument acquires the first site.

To acquire the image for maximum intensity:

For some multi-channel experiments, the brightest and darkest images for one channel can be different than the brightest and darkest images for another channel. In this case, try to locate the wells that give you the best results between the different channels.

To view the image for a specific wavelength:

&#x20;Click the tab above the image for that wavelength. To view an image with all the wavelengths:

&#x20;Click **Composite**.

To zoom the image in and out:

&#x20;Right-click the image and select **Zoom In** or **Zoom Out**,  Hold the **CTRL** key and press **+** or **-**.

&#x20;Use the mouse wheel to zoom in or out. To move the image in the image area:

&#x20;Use the scroll bars or click the image and drag it into position. To view a larger version of the image area:

&#x20;Double-click the image to display the Zoom Well dialog. See Zooming Image in a Well on page 179.

### Set Exposure Time and Focus Adjustment

You can adjust the exposure and focus separately for each wavelength or channel. To view the image for a specific wavelength:

&#x20;Click the tab above the image for that wavelength. To view an image with all the wavelengths:

&#x20;Click **Composite**.

Set the exposure and focus adjustment in the row you designate for the specific channel.

#### Exposure

Use Auto Exposure to have the software determine the perceived best intensity for the Max Intensity or Min Intensity image, whichever is brightest. To view what effect the new exposure value has on the images, acquire the maximum intensity and minimum intensity images again.

To have the software determine the best exposure:

&#x20;Click **Auto Expose**.

Increase the exposure time to increase the intensity of the image or decrease the exposure time to decrease the intensity of the image. After each adjustment, acquire the images again to view what effect the change has on the intensity.

To manually adjust the intensity of the images,

&#x20;In the **Exposure** field, enter the number of milliseconds to hold the camera shutter open.

#### Focus

The system optics use a laser automatic focus system and software algorithms to find the initial focus distance for the cells in the plate wells. Increase the Focus Adjustment value to move the objective lens closer to the sample. Decrease the Focus Adjustment value to move the objective lens farther away from the sample. The instrument uses this setting for every well in the plate during acquisition.

For transmitted light images, make sure that enough contrast exists between the objects and the background. Less contrast exists as you make the focus sharper. For best results when you use a preset drawing analysis, make sure that the objects are brighter than the background.

To adjust the focus:

&#x20;In the **Focus Adjustment** field, enter the number of microns to move the objective lens closer to or farther away from the sample.

After each adjustment, acquire the images again to view what effect the change has on thefocus.

### Image Analysis Settings

Use the Image Analysis Settings category in the Settings dialog to define how to analyze images for the Imaging read mode.

To acquire images without analysis:

&#x20;Click **No Analysis**.

### Discrete Object Analysis

Discrete Object Analysis uses proprietary algorithms to analyze separate objects, or cells, based on multiple parameters including the signal intensity over the background and the size of the objects. You can use transmitted light or a fluorescent wavelength to find nuclei or easily separable objects in the image. The StainFree™ Cell Detection Algorithm eliminates cell staining for cell counting and confluency measurements using proprietary transmitted light analysis technology.

To define discrete object analysis settings:

1. Click **Discrete Object Analysis** to display the Wavelength for Finding Objects list.
2. Select the wavelength to use to identify the objects in the well images.
3. Select the **Image Analysis Settings** category.
4. Click **Find Objects** and enter size and intensity values or use proprietary algorithms with the drawing tools to graphically define the objects and the background areas for the analysis. See Finding Discrete Objects or Confluent Areas on page 129.
5. Click **Classify Objects** and define separate measurements for different types of found objects, or cells. See Classifying Discrete Objects on page 133.
6. Click **Select Measurements** and view the results of the analysis for the wells you select. See Viewing and Selecting Measurement Statistics on page 134.

### Field Analysis

Field Analysis uses proprietary algorithms to analyze confluent areas based on parameters including the signal intensity over the background and the size of the areas.

To define field analysis settings:

1. Click **Field Analysis** to display the Wavelength for Finding Confluent Areas list.
2. Select the wavelength to use to identify the confluent areas in the well images. The StainFree™ Cell Detection Algorithm eliminates cell staining for cell counting and confluency measurements using proprietary transmitted light analysis technology.
3. Click **Find Confluent Areas** and use proprietary algorithms with the provided drawing tools to graphically define the confluent areas and the background areas for the analysis. See Finding Discrete Objects or Confluent Areas on page 129.
4. Click **Select Measurements** and view the results of the analysis for the wells you select. See Viewing and Selecting Measurement Statistics on page 134.

The SoftMax Pro Software proprietary algorithms with the drawing tools in the Find Objects and Find Confluent Areas settings help the software learn the patterns of the objects you want to find. Depending on the complexity of the object patterns, this teaching process cantake several iterations. See Resolving Issues with Object Drawing and Finding on page 136.

### Finding Discrete Objects or Confluent Areas

The Find Objects or Find Confluent Areas settings display the minimum and maximum images from the Image Acquisition Settings.

&#x20;Click  to view the page in full screen.

&#x20;Click  to restore the page to its original size.

In full screen view, select the tabs at the top of the page to switch between the different analysis settings.

Use the buttons above the image to switch the view of the image between wavelengths and to show or hide found objects (or confluent areas) and drawings. When a button is filled, the related wavelength, objects (or confluent areas), and drawings display in the image. When a button is outlined, the related wavelength, objects (or confluent areas), and drawings do not display in the image. When you click a button above one of the images, it affects the display of both images.

Use the controls below the image to adjust the intensity of each wavelength.

To adjust the wavelength intensity:

*
  1. Select the wavelength to adjust.

For fluorescent acquisition and discrete object analysis, select a Finding Method:

&#x20;Select **Set Size and Intensity** to define the intensity threshold above the background intensity to apply separately to each object in the image that meets the defined size range. This analysis helps to detect objects in areas of the image where the intensity is uneven.

&#x20;Select **Draw on Images** to use the drawing tools to help the software learn the patterns of the objects you want to find.

### Set Size and Intensity

The Set Size and Intensity settings are available for fluorescent acquisition and discrete object analysis.

To define set size and intensity settings:

1. Click .
2. Click four or more representative objects on the images that you want to detect as cells.
3. In the **Min Width** field, enter the minimum width of the object to find, in microns.
4. In the **Max Width** field, enter the maximum width of the object to find, in microns.
5. In the **Intensity Above Background** field, enter the intensity threshold above the background intensity at which to detect the dimmest object. For example, if the background intensity is 1000 and the intensity of the dimmest object is 1200, enter 200.
6. Click **Apply**.

#### Grow

Use the Grow setting to define the number of pixels to increase the diameter of the found objects in one wavelength, so they can be measured at the new size in another wavelength of the acquisition. For example, if you use a stain for nuclei, you can find the object in the first wavelength and then increase the diameter to find the protein of interest in another fluorescence wavelength. The innovative "grow without touching" algorithm increases the size of the measured areas without letting the areas touch or overlap their edges.

### Draw on Images

Use the drawing tools to help the software learn the patterns of the objects or confluent areas you want to find. Depending on the complexity of the object or area patterns this teaching process can take some time. Each preset drawing analysis works with specific cell types. Select the preset analysis that works best with your images.

To use a preset drawing analysis:

1. In the **Settings** list, select a preset drawing.
2. Click **Apply** to find objects or confluent areas that use the preset.
3. After you acquire data, select **Stored Setting** in the Settings list to use the previously defined analysis settings.
4. To start from scratch, select **Create New Setting** in the Settings list.

To select the objects for fluorescent acquisition and discrete object analysis:

**Note:** This method is not available for transmitted light acquisition or for confluent area analysis.



1. Click .
2. Click a line width.
3. Click four or more representative objects on the images. To define the objects or confluent areas:
   1. Click the object or area pen .
   2. Select a line width.
   3. For discrete object analysis, draw inside the object up to the edge, but do not include the edge. When the object is filled in with yellow, the drawing is outlined in green. For best results, fill in four or more representative objects.
   4. For field analysis, draw across confluent areas, avoiding background. For best results, draw across four or more representative areas.

To define the background:

*
  *
    1. Click the background pen .
    2. Select a line width.
    3. Draw on the image to define artifacts and background areas in blue.



**Tip:** For best results, define four or more representative background areas.

To correct a drawing of an object or area:

&#x20;Click **Undo** to undo the most recent action.  Click **Redo** to restore the most recent action.

&#x20;Click **Start Over** to clear the drawings from the image.

To erase parts of drawings:

1. Click  **Erase**.
2. Select a line width.
3. Drag the eraser across the drawings to remove.
4. After you define the objects and areas, click **Apply** to find the objects or confluent areas in the image.
5. Continue to draw and to apply until you get satisfactory results. See Resolving Issues with Object Drawing and Finding on page 136.

You can then classify objects or view the measurement statistics.

### Classifying Discrete Objects

The Classify Objects settings display the minimum and maximum images from the Image Acquisition settings display along with the found objects from the Find Objects settings. The Classify Objects settings are not available for field analysis of confluent areas.



**Note:** Before you can classify objects, you must first find objects in the Find Objects

settings. See Finding Discrete Objects or Confluent Areas on page 129.

Use the bottom of the page to classify the found objects in the images into two separate classifications.

To classify the found objects:

&#x20;Select **Use Existing Classification** to use the previously defined classification settings when in Re-Analysis mode.

&#x20;Select **Skip Classification** to not use classification in the analysis.

&#x20;Select **Create New Classification** to replace the Type A and Type B titles with your own titles for the classifications. See below.

#### Create New Classification

When you select Create New Classification, you can replace the Type A and Type B titles with your own titles for the classifications. Titles must use only letters, numbers, and spaces, and can be up to 16 characters long, including spaces. They must start and end with a letter. The titles must be unique and you cannot use "Exclude" as a title, since this is a reserved word.

To create a new classification:

### Viewing and Selecting Measurement Statistics

The Measurement Selections settings table displays the analysis results for the minimum intensity and maximum intensity images.

The possible included measurements are as follows:

&#x20;**Object Count**: The total number of objects detected in the image. Not used for field analysis of confluent areas.

&#x20;**Field Count**: The total number of confluent areas detected in the image. Not used for discrete object analysis.

&#x20;**Object Percentage**: The percentage the objects detected in the image by classification.

Not used for field analysis of confluent areas.

&#x20;**Covered Area**: The combined area of all the objects or confluent areas detected in the image as a percentage of the entire image area.

**Object Area**: The average area of the objects detected in the image expressed in µm . Not used for field analysis of confluent areas.

2

&#x20;**Field Area**: The average area of the confluent areas detected in the image expressed in µm . Not used for discrete object analysis.

2

&#x20;**Object Roundness**: The average roundness of each object detected in the image. A shape factor of 1.00 is perfectly round, while a shape factor of 0.00 is not round at all. Not used for field analysis of confluent areas.

&#x20;**Field Roundness**: The average roundness of each confluent area detected in the image. A shape factor of 1.00 is perfectly round, while a shape factor of 0.00 is not round at all. Not used for discrete object analysis.

&#x20;**Object Average Intensity**: The average fluorescent signal intensity of the objects detected in the image. This measurement is not used for field analysis of confluent areas. Not used for transmitted light.

&#x20;**Field Average Intensity**: The average fluorescent signal intensity of the confluent areas detected in the image. This measurement is not used for discrete object analysis and not used for transmitted light.

&#x20;**Object Intensity**: The average total fluorescent signal intensity of the objects detected in the image. Not used for field analysis of confluent areas and not used for transmitted light.

&#x20;**Field Intensity**: The average total fluorescent signal intensity of the confluent areas detected in the image. Not used for discrete object analysis and not used for transmitted light.

&#x20;**Total Intensity**: The combined total fluorescent signal intensity of the objects or confluent areas detected in the image expressed in million intensity counts. Not used for transmitted light.

To include the measurements in the analysis:

1. Click **Select Measurements** in the lower-right area of the page.  Click **Remove** to exclude a measurement.

&#x20;Click **Add** to include a measurement.

&#x20;Click **Remove All** to exclude all measurements.  Click **Add All** to include all measurements.

1. Click **Done** to add the selected measurements to the data reduction list that you use to view data in the Plate section or to add to a Group section for further analysis. See Plate Sections on page 76 or Group Sections on page 82.
2. Click **Show Details** to view the measurements in an interactive image, data table, and chart. See Viewing Imaging Data in Wells on page 207.
3. If no measurements display and you did not make changes to the analysis settings since the last measurement, click **Measure** to analyze the selected wells. This is useful if you change acquisition wells and want to analyze the new wells.

### Resolving Issues with Object Drawing and Finding <a href="#bookmark20" id="bookmark20"></a>

The SoftMax Pro Software proprietary algorithms provide drawing tools in the Find Objects or Find Confluent Areas settings to help the software learn the patterns of the objects that you want to find. Depending on the complexity of the object patterns, this teaching process can take several iterations.

The software uses a complex algorithm to learn the properties of the cells or confluent areas in the image. The algorithm examines each pixel and how it relates to its surrounding area. Cells change shape and size under different conditions such as confluency. Artifacts can look like cells or confuse the algorithm. Cells that are touching are more difficult to find than sparse cells in an image. Complex images can require more drawing examples to create a good training set.

Some common issues with finding cells and confluent areas are as follows:

&#x20;Under splitting finds multiple cells or confluent areas that can also include background.

&#x20;Over splitting finds portions of cells or confluent areas and can include several found objects within a single cell or confluent area.

&#x20;Artifacts can be found and counted as cells or confluent areas.

&#x20;Ghosting finds background areas next to cells or confluent areas.

Each preset drawing analysis is designed to work with specific cell types. Select the preset analysis that works best with your images.

To resolve issues:

*
  1. In the **Settings** list, select a preset drawing analysis.
  2. Click **Apply** to find objects or confluent areas using the preset.

For transmitted light images, make sure that enough contrast exists between the objects and the background. The sharper the focus, the less contrast exists. To increase the contrast between the objects and the background, move the lens closer to or farther away from the plate.

Adjust the focus in the Image Acquisition Settings. Increase the Focus Adjustment value to move the objective lens closer to the sample. Decrease the Focus Adjustment value to move the objective lens farther away from the sample. In general, move the lens closer to make the objects darker than the background, move the lens farther away to make the objects brighter than the background.

**Note:** For best results when you use a preset drawing analysis, make sure that the objects are brighter than the background.



To create an iterative training set for complex images:

1. Carefully draw four or more cells or confluent areas that best represent your target population. Draw inside the cell or confluent area up to the edge, but do not include the edge.
2. Define the artifacts and background areas in the image.
3. Apply the drawing and then try to fix the problems.
4. Continue to adjust the drawings. After you fix some problems, the results can look worse as the algorithm emphasizes the fixes. Continue to adjust to create a complete training set.
5. After the result looks reasonable, scroll and look around the image for other issues.
6. Stop when you are satisfied or you get diminishing returns. As the training data set grows, more drawings will have less impact. At some point changes will be of little benefit.

If, at the end of the process, it is still not right, start again and repeat all the steps. Sometimes there is something that had an unexpected influence on the algorithm and starting over can produce a better result.

### Resolve Under Splitting Issues <a href="#bookmark21" id="bookmark21"></a>

Under splitting finds multiple cells or confluent areas that can also include background.

Under splitting can be caused by drawing outside of the edge of the cells or confluent areas. The lines between the cells or confluent areas are interpreted as being part of the cell or confluent area structure.

To resolve under splitting issues:

&#x20;Draw inside the cell or confluent area up to the edge, but do not include the edge. You can also use the background pen to draw on the lines between the cells or confluent areas.

### Resolve Over Splitting Issues <a href="#bookmark22" id="bookmark22"></a>

Over splitting finds portions of cells or confluent areas and can include several found objects within a single cell or confluent area.

Over splitting can be caused by drawing too small within the cells or confluent areas. Sometimes over splitting can happen after you use the background pen to remove an artifact.

To resolve over splitting issues:

&#x20;Draw inside the cell or confluent area up to the edge, but do not include the edge.

If over splitting is the result of artifact removal:

&#x20;Erase the blue from the artifact defined by the background pen.

### Resolve Artifact Issues <a href="#bookmark23" id="bookmark23"></a>

Artifacts can be found and counted as cells or confluent areas.

Artifact issues can be caused by debris or other artifacts in the image where the edges and surrounding pixels confuse the software.

To resolve artifact issues:

&#x20;Use the background pen to define artifacts as background and not cells or confluent areas.

### Resolve Ghosting Issues <a href="#bookmark24" id="bookmark24"></a>

Ghosting finds background areas next to cells or confluent areas.

Ghosting can be caused by the edges of cells or confluent areas and the surrounding pixels that confuse the software.

To resolve ghosting issues:

&#x20;Use the background pen to draw over the area of the ghost. Draw this area right to the edge of the cell or confluent area.

&#x20;If necessary, use the object pen to draw on the cell or confluent area so that the drawing goes out to the edge of the cell or confluent area.

### Region of Interest Settings <a href="#bookmark25" id="bookmark25"></a>

You can define a region of interest for the images in all wells to analyze for your application. The software uses only the region of interest you select for analysis. This is useful if cells tend to congregate in the same region of the wells.

To select the well to use to define the region of interest:

1. Click  to the right of the **Well** field above the image area. The well fills with red and is used to determine the region of interest.
2. Select the well to use and click **Acquire All Sites**. To view the image for a specific wavelength:

&#x20;Click the tab above the image for that wavelength. To view an image with all the wavelengths:

&#x20;Click **Composite**.

To zoom the image in and out:

&#x20;Right-click the image and select **Zoom In** or **Zoom Out**,  Hold the **CTRL** key and press **+** or **-**.

&#x20;Use the mouse wheel to zoom in or out. To move the image in the image area:

&#x20;Use the scroll bars or click the image and drag it into position. To define a region of interest:

1. Select the **Enable Region Selection** check box to display a rectangle on the image.
2. Click **Resize** and then drag the corners of the rectangle to redefine the size of the region.
3. To start over, click **Draw** and then drag a new rectangle on the image to define the region.

To use the entire image for the analysis:

&#x20;Clear the **Enable Region Selection** check box.

### More Settings <a href="#bookmark26" id="bookmark26"></a>

The More Settings category in the Settings dialog provides more settings options. The options vary depending on the instrument you select, read mode, and read type.

### Calibrate

The More Settings category in the Settings dialog provides a Calibrate option for some instruments.

For the Absorbance read mode, the instrument makes an air-calibration measurement at each wavelength before the read. If you turn calibration off, the software uses the air- calibration values stored in the instrument firmware or the values from the previous calibration.

For Fluorescence and Luminescence read modes, the instrument makes a reference read at each wavelength before the read. If you turn calibration off, the software uses the default values stored in the instrument firmware or the values from the previous calibration.

For the Kinetic read type, the instrument makes the calibration measurement between reads during a run, unless the read interval is too short to allow calibration.

To define calibration settings:

&#x20;Select the **Calibrate** check box to have the instrument run calibration for the wavelengths you specify before each read.

&#x20;Clear the **Calibration** check box to have the instrument begin reads or complete reads more quickly. You should calibrate at your assay wavelengths for at least one plate before you turn off calibration.

New calibrations overwrite the calibration setting stored in firmware for the current data acquisition read, and for any subsequent reads you do with the Calibration check box clear. When you power the instrument off and then back on, calibrations reset to those stored in the firmware.

To update the air-calibration values stored in the firmware for the Absorbance read mode:

1. Select the **Operations** tab.
2. Click **Calibration**.
3. See Instrument Calibration on page 352.

### Carriage Speed

The More Settings category in the Settings dialog provides a Carriage Speed option for some instruments. You can slow down the carriage speed for samples (such as, fragile clots) that rapid carriage movement can disrupt.

Click the **Carriage Speed** drop-down:

&#x20;Select **Normal** to use the normal carriage speed.  Select **Slow** to use a slower carriage speed.

### Read Order

The More Settings category in the Settings dialog provides a Read Order option that varies depending on the instrument, read mode, and read type.

For multi-wavelength reads, click the **Read Order** drop-down:

&#x20;Select **Column** to have the instrument read the entire plate (or chosen number of strips) at the first wavelength. The instrument then goes back and reads the plate at the second and subsequent wavelengths.

&#x20;Select **Wavelength** to have the instrument read all wavelengths for the first column of wells in the plate first and then read all wavelengths for the second column, third column, and so on.

For single wavelength reads, click the **Read Order** drop-down:

&#x20;Select **Row** to read the entire plate row-by-row.

&#x20;Select **Column** to read the entire plate column-by-column.

&#x20;Select **Well** to read each well individually with all wavelengths and intervals you define for the read before the software reads the next well. This is useful for spectral scans, area scans, and specialized, fast-kinetic applications.

### Settling Time

The More Settings category in the Settings dialog provides a Settling Time option for some instruments.

Settling Time is the delay between the motion of the instrument and the start of the read. This delay allows time for the meniscus motion to cease, which potentially improves precision, especially in the low density, high volume plates with fewer than 96 wells.

To define settling time settings:

&#x20;Select the **Settling Time** check box to add a delay between the read of each column. In the **Duration** field, enter the delay time between 100 and 1000 milliseconds. There is no delay between each well in a column.

&#x20;Clear the **Settling Time** check box to not have a delay.

### Show Pre-Read Optimization Options

The More Settings category in the Settings dialog provides a Show Pre-Read Optimization Options check box for some instruments. From the Acquisition view, you can add Plate Optimization to the beginning of the time line. Plate dimensions can vary slightly between production lots, which can have a potential effect on measurement accuracy.

To define pre-read optimization settings:

&#x20;Select the **Show Pre-Read Optimization Options** check box to display the Pre-Read Optimization Options dialog before the instrument reads the plate. Use this dialog to optimize the plate dimensions after you click Read and before the instrument reads the plate. See Pre-Read Optimization Options on page 184.

&#x20;Clear the **Show Pre-Read Optimization Options** check box to use the plate dimensions saved in the plate library.

Use the Pre-Read Optimization Options dialog to optimize labware dimensions by determining the centers of the four corner wells on the plate. The software adds a new plate definition to the plate library with dimensions from each plate you optimize. If you change the plate orientations for measurements, you must do labware optimization for each plate orientation separately.

Some instruments feature an objective lens that you can adjust. Use the Pre-Read Optimization Options dialog to move the lens up and down to optimize the read height for the Luminescence, Fluorescence Intensity, Fluorescence Polarization, and Time-Resolved Fluorescence read modes. Read height is the distance between the top (for top reads) or bottom (for bottom read) surface of the plate to read and the surface of the objective lens. You optimize the read height to match the focus of the optics with the sample volume. This maximizes the raw signal, which yields the highest precision and maximum sensitivity. For the FilterMax F5, this is available for top reads only.

### Attenuation

The More Settings category in the Settings dialog provides an Attenuation option for some instruments. Attenuation filters reduce the intensity of very bright samples that can exceed the linear dynamic range of the detection system.

To define Attenuation settings:

&#x20;Select the **Attenuation** check box to use attenuation filters for very bright samples.  Clear the **Attenuation** check box to not use attenuation filters.

### Normalization

The More Settings category in the Settings dialog provides a Normalization option for instruments that support the AlphaScreen read mode. The conversion rate of photons to counts is individual for each detector. Raw data from the same plate can seem to be different from one instrument to the next. The data format each instrument manufacturer uses can be counts normalized-per-second or not-normalized counts, therefore raw data can be different by several orders of magnitude.

**Note:** The number of counts and the size of figures is in no way an indication of sensitivity.



To define normalization settings:

&#x20;Select the **Normalization** check box to normalize raw data to counts per second.

&#x20;Clear the **Normalization** check box to not normalize raw data to counts per second.

### Interlaced Reading

The More Settings category in the Settings dialog provides an Interlaced Reading option for the SpectraMax i3x and SpectraMax Paradigm when you install the AlphaScreen Detection Cartridge and do an Endpoint read type.

When you read a sample with a small signal, an interference can occur from the afterglow of a very strong emitting adjacent sample that the instrument just measured. Such cross talk can occur through the wall of a white 384-well plate. Use Interlaced Reading to have the instrument read every other well in a checkerboard pattern, and then do another plate run to read the omitted wells.

Although background is significantly lower with the AlphaScreen read mode than with the Fluorescence Intensity read mode measurements, you should use blank or assay controls for background correction. Use blank replicates to effectively measure the background. For improved results, you should use replicates for all blanks, controls, and samples.

To define interlaced reading settings:

&#x20;Select the **Interlaced Reading** check box to prevent interference.  Clear the **Interlaced Reading** check box to not use the feature.

### Compound Transfer Settings <a href="#bookmark27" id="bookmark27"></a>

The Compound Transfer category in the Settings dialog displays for the FlexStation 3.

You must configure all compound transfer settings correctly. When you select to do compound transfers, four additional categories appear in the Settings dialog. Use these settings to define precise fluid transfers for the protocol and help prevent flooding of the assay plate. Keep in mind the actual maximum volume the wells allow as you define the settings. The maximum cumulative volume depends on the assay plate type you select.

For the Endpoint and Kinetic read types, the transfers are done to all the wells you select before the first read.

For the Flex read type, the transfers are done for a column while that column is read. All transfers and reads are done for that column before the instrument moves to the next column.

To set the number of compound transfers in each column during a read: Click the **No. of Compound Transfers** drop-down.

&#x20;Select **0** to not do compound transfers for the read. No other options display and no other settings are required.

&#x20;Select **1** to do one compound transfer.  displays with additional settings.

&#x20;Select **2** to do two compound transfers.  displays with additional settings.

&#x20;Select **3** to do three compound transfers.  displays with additional settings.

#### Initial Volume

The software assigns the initial volume to all wells and uses this value to compute the total volume in each well after all fluids dispense. As you define the volume for each transfer in the Compound & Tips Column category, the software uses the Initial Volume value to warn you of the potential for overflow of fluid from the wells. See Compound and Tips Columns Settings on page 150.

In the **Initial Volume** field, enter a value that equals the largest initial volume in the wells of the assay plate before the compound transfers. If there is no fluid volume in the assay plate before the compound transfers, enter **0**.

&#x20;For a 96-well plate, this value can be 0 µL to 269 µL. Typical values are about 10 µL to 200 µL.

&#x20;For a 384-well plate, this value can be 0 µL to 120 µL. Typical values are about 5 µL to 80 µL.

### Transfer Settings

You define the following settings for each compound transfer.

1. Select the compound transfer to define.

**Note:** The compound transfer you select displays with a light blue background and this is the only indication for which transfer you are defining.



1. In the **Pipette Height** field, enter a value between 1 µL to 300 µL for a 96-well plate or 1 µL to 130 µL for a 384-well plate. This setting determines the volume of fluid in microliters, measured from the bottom of the assay plate well, above which the tip of the pipette is to remain during the dispense portion of the transfer event. Use this setting to place the tip of the pipette below the surface of the liquid at the end of the transfer to minimize the possibility that undispensed drops remain on the tips.

**Note:** As you configure subsequent transfers, calculate the amount of fluid added and set the pipette height accordingly. Example: If the initial volume is 15 μL and the first transfer dispenses 20 μL, set the pipette height for the first transfer to



25 μL. If the second transfer dispenses 15 μL, set the pipette height for the second transfer to 45 μL.

1. In the **Volume** field, enter the volume of liquid to dispense to each well of the assay plate that you select to receive the transfer.

&#x20;For a 96-well plate, the range is 1 µL to 200 µL.  For a 384-well plate, the range is 1 µL to 30 µL.

**Note:** Keep in mind the maximum total volume each well can hold as you accumulate volumes with multiple transfers.



1. In the **Rate** field, enter a value of 1 to 8. This setting determines the rate at which the instrument dispenses fluid into the well of the assay plate.

&#x20;In a 96-well plate, a setting of 1 is equal to 16 µL per second and each subsequent number increases in increments of \~16 µL per second, so that a setting of 2 is equal to 31 µL per second.

&#x20;In a 384-well plate, a setting of 1 is equal to 4 µL per second and each subsequent number increases in increments of 4 µL per second, so that a setting of 2 is equal to 8 µL per second.

A setting of 1 or 2 can help minimize cell damage or dislodgment. For non-contact dispensing, use a rate of 8 to make sure that all liquid dispenses from the pipette tip.

1. In the **Time Point** field, enter the point in time after the read starts when the fluid is to begin being dispensed. This value must be equal to or greater than the value the instrument displays for the **Minimum Time** up to 9999 seconds. This time point becomes the baseline time. This is not the time interval between transfers. For the Endpoint and Kinetic read types, Time Point is the time at which the first dispense occurs. The Endpoint or Kinetic read begins after all transfers are made.

**Note:** The Time Point value cannot be less than the Minimum Time the software identifies for each transfer.



1. The **Minimum Time** field displays the minimum time required before a pipetting event can occur. This minimum time value is cumulative, not an interval between pipetting events. The value is the minimum number of seconds of elapsed time from the beginning of the read. It considers the mechanical speed of the pipette head and the time needed to load and unload tips, aspirate and dispense fluids, triturate fluids, and shake the plate.

The minimum time for the second pipetting event depends on when the first pipetting event occurs. The calculation for the second event starts at the end of the first event and adds the total time necessary to load pipette tips, aspirate new fluids from the compound plate, and dispense them into the assay plate.

### Leave Tips On Between Columns

For the Flex read type, the pipettor returns the tips to the tip rack after all the transfers for a column are complete and then installs tips from the tip rack before the first transfer for the next column.

&#x20;Select the **Leave Tips On Between Columns** check box to use tips from the same position in the tip rack for the first and last transfers in each column. This can reduce the cycle time between columns.

&#x20;Clear the **Leave Tips On Between Columns** check box to have the instrument install tips from the tip rack before the first transfer for the next column.

You define tip assignments in the **Compound & Tips Columns** category. See Compound and Tips Columns Settings on page 150.

### Avoiding Problems

Time point calculations are based on the number of wells you select in the Read Area category and the Pipette Tips & Columns category settings you define for the transfer. If your Time Point entry is not long enough to be compatible with the volumes and transfer speed you define, a message instructs you to increase the Time Point entry.

If you enter transfer volumes that add up to more than the maximum that can fit in the assay plate, an overflow message indicates that you have exceeded the volume limit of the assay plate.

**Note:** The Minimum Time Value that displays below the Time Point field is different for each transfer you define.



### Compound Source Settings <a href="#bookmark28" id="bookmark28"></a>

Use the Compound Source category in the Settings dialog to select the plate type for the compound plate. The instrument aspirates (withdraws) fluids from the compound plate and then dispenses (injects) the fluids into the assay plate during the run.

The plate type you select in the Compound Source category must match the type and well configuration of the actual compound plate to use and it must be compatible with the number of wells in the plate type you select for the assay plate in the Plate Type category. See Plate Type Settings on page 115.

The instrument sets the pipette height for the compound plate. The well bottom height is different for different types of plates. Select the plate type correctly to prevent jamming the pipette tips into the bottom of the well.

&#x20;For 96-well plates, the instrument aspirates using a pipette height of 20 µL above the bottom of the well.

&#x20;For 384-well plates, the instrument aspirates using a pipette height of 10 µL above the bottom of the well.

You define the pipette height for the assay plate in the Compound Transfer category. See Compound Transfer Settings on page 145.

**CAUTION!** Selection of an incorrect compound plate type can result in the pipette tips jamming into the wells and damaging the plate, the tips, and the instrument.



### Pipette Tips Layout Settings <a href="#bookmark29" id="bookmark29"></a>

Use the Pipette Tips Layout category in the Settings dialog to define which pipette tips to use. If you use a partial rack of tips, use this category to have the software instruct the instrument to pull tips from the location of the tips you insert in the tip drawer.

When you select a 96-well assay plate in the Plate Type category, the Plate Tips Layout category displays a column of 12 tips. See Plate Type Settings on page 115.

When you select a 384-well assay plate in the Plate Type category, the Plate Tips Layout category displays a column of 24 tips.

To use all the tips in the rack:

&#x20;Select the **Select All** check box.

The tips selection must be contiguous. To select a contiguous set of tips:  Drag the mouse to select the tips to use.

If you change the assay plate type in the Plate Type category to a plate with a different number of wells (for example, from 96-wells to 384-wells), the Pipette Tips Layout category defaults to the selection of the full rack of tips.

**CAUTION!** You should use a full rack of tips each time you do a fluid transfer. If you configure a pipetting function from a tip that is not present, your samples do not receive the intended compound. There is potential of damage to the plate, the tips, and the instrument.



### Compound and Tips Columns Settings <a href="#bookmark30" id="bookmark30"></a>

Use the Compound & Tips Columns category in the Settings dialog to define the tips and compounds to use for each transfer.

These settings are dependent on the selection you make in the Plate Type category for the assay plate and the number of transfers you define in the Compound Transfer category. See Plate Type Settings on page 115 and Compound Transfer Settings on page 145.

&#x20;For a 96-well assay plate, 12 columns display.

&#x20;For 384-well assay plate, use the scroll bar to view the additional columns. Each transfer appears as a color coded row.

The black row at the bottom represents the initial volume in the wells based on your Initial Volume entry in the Compound Transfer category.

Your Read Area category setting also affects these settings. See Read Area Settings on page 119.

#### Display for a read area that includes columns 3 - 8 on a 96-well assay plate

The left axis displays the dispensed compound volume as a percentage of the total well volume on the assay plate.

Each assay plate column has two indicators for each transfer:

&#x20;\#T = Tips: Displays the column in the tip rack drawer from which the instrument will pull the tip for the transfer. You define available tips in the Pipette Tips Layout category. See Pipette Tips Layout Settings on page 149.

&#x20;\#C = Compound: Displays the column in the compound plate from which the instrument will aspirate the fluid to transfer to the assay plate for each pipetting event.

&#x20;Hover the mouse over a cell to display details including the transfer volume.

**Tip:** To leave the tips on between columns for the Flex read type, select the Leave Tips On between Columns check box in the Compound Transfer category.



### Auto Populate

Use the Auto Populate feature to have the software assign the fluid to aspirate from the compound plate starting with the first available column. The instrument then dispenses the aspirated fluid to the first available column in the assay plate based on your Read Area category settings.

The software makes the assignments based on the following conditions:  All columns you select in the Read Area category are to receive fluid.

&#x20;The fluids transfer from left to right. The read-transfer-read sequence in each column is initiated only after the read-transfer-read event from the previous column completes (the total read time for that column).

&#x20;The fluid transfer targets are cumulative from transfer to transfer. That is, the targets for the second transfer start with the next available clean tip and untargeted compound column rather than reusing tips and compound columns targeted by the preceding fluid

transfer.

&#x20;Each fluid transfer uses a new tip.

Example: Suppose you define the following settings for three fluid transfers:  Read Area category: Columns 1 through 4

&#x20;Compound Source category: 12-column compound plate, such as a 96-well plate  Pipette Tips Layout category: Full rack of tips

The software instructs the instrument to selects tips from columns 1 - 4 in the tip rack drawer, to aspirate compound from columns 1 - 4 in the compound plate drawer, and to dispense the compound into the wells in columns 1 - 4 on the assay plate in the read chamber drawer. The second transfer uses the next four columns (5 through 8), and the third transfer uses the remaining four unused columns (9 through 12).

**Note:** The software does not assign targets beyond the limitations of the available tips and compound source columns. After all available tips and compound source columns have been assigned, the software stops assigning targets.



To have the software automatically assign the tips and columns:  Click **Auto Populate**.

### Manually Populate

For more complex assays, you can manually define the tips to use and the columns from which to aspirate compound.

**Image example displays:**

**Read Area: columns 3 - 8 on a 96-well assay plate Compound Transfers: 2**

**Selecting a tip with Pipette Tips Layout: columns 3 - 8 No fluid transfer for compound 2 into column 3**

You can manually assign tips and source columns for each and every transfer.

To assign each transfer a set of tips from the tip rack and a column from the source plate:

1. Click **T** in a column to display a drop-down list of the pipette tip columns you made available in the Pipette Tips Layout category. Select the column from which to have the instrument pull the tip from the instrument tip drawer.
2. Click **C** in a column to display a drop-down list of the number of columns in the compound plate from which the instrument can aspirate the compound. Select the column on the source plate from which to aspirate the compound.
3. If the assay requires that no fluid is to transfer to the assay plate for a column during one or more transfer operations, click **X** at the top of the drop-down list.  displays for the columns to skip.
4. To allow a transfer for a skipped column, click , then assign the tip and source columns for the transfer.

**Tip:** To leave the tips on between columns for the Flex read type, select the Leave Tips On between Columns check box in the Compound Transfer category.



### Triturate Settings <a href="#bookmark31" id="bookmark31"></a>

Use the Triturate category in the Settings dialog to define how to mix the contents of the wells in a plate by using the pipettor to alternately aspirate fluid from a well and then dispense it back into the well.

Trituration is recommended when you need to resuspend the compound in the source plate before it is added, when you transfer low volumes of fluid to the assay plate, or when you transfer fluid before or during an absorbance read to make sure that the well contents are properly mixed.

To define triturate settings:

1. &#x20;\- Select the compound transfer to define and repeat the following steps for each applicable transfer.
2. Select the **Compound Source** check box to do trituration in the compound plate.
3. Select the **Assay Plate** check box to do trituration in the assay plate.



**Note:** Select both check boxes to do trituration in both plates.

1. In the **Volume** field, enter the volume of fluid in microliters to withdraw from the well.
2. In the **Cycles** field, enter the number of times to aspirate and dispense the fluid in the well.
3. For the Assay Plate, enter a value for the **Height** at which the trituration occurs. The height setting must consider the trituration volume you enter and the total volume in the well to have the tips remain below the liquid surface and not aspirate air.

**Note:** If you enter a Time Point that is incompatible with the Triturate settings, a message appears. You modify the Time Point in the Compound Transfer category. See Compound Transfer Settings on page 145.

![](<../../../.gitbook/assets/0 (7) (1) (1) (1).png>)
