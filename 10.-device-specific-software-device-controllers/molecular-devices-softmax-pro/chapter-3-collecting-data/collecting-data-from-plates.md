# Collecting Data From Plates

You can start a read after you define the acquisition settings. It is not necessary to define groups and assign wells in the Template Editor dialog first. The values that the software receives from the instrument are raw values. The settings in the Template Editor have no effect on these raw values.

The SoftMax Pro Options dialog has an option to have the plate remain inside the instrument after the read completes. See Application Options on page 45.

Use auto read to read multiple Plate sections in the same experiment. See Using Auto Read on page 180.

To collect data from plates:

1. To open the plate drawer of the instrument, select the **Home** tab and click ![](<../../../.gitbook/assets/5 (6) (1) (1).png>)

**Open/Close**. See Home Tab on page 49.

The plate carrier on the EMax Plus moves in and out of the read chamber during the read, and then returns to the home position after the read ends. If the plate carrier does not return to the home position, select the Operations tab and click **Initialize**.

1. Insert the prepared plate matching well A1 with position A1 in the plate drawer. Make sure the plate is flat against the drawer bottom or against the adapter.
2. Click ![](<../../../.gitbook/assets/6 (6) (1) (1).png>) **Open/Close** to close the plate drawer.
3. Open a document that contains the acquisition settings for the plate read. As an alternative, create new acquisition settings by selecting the Plate section in the Navigation Tree and configuring the acquisition settings sing the Settings dialog. See Acquisition Settings on page 109.
4. You should save the document before you start a read. For Imaging reads and Western Blot reads, you must save the document before you start the read.
5. Click ![](<../../../.gitbook/assets/7 (4).jpeg>) **Read** below the Settings Information area or on the Home tab. The Read button changes to ![](<../../../.gitbook/assets/8 (1) (1) (1).jpeg>) **Stop** so you can terminate a read.
6. The instrument reads the Plate section you select.

![](<../../../.gitbook/assets/9 (3) (1) (1).png>) For the SpectraMax i3x, SpectraMax Paradigm, SpectraMax iD3, SpectraMax iD5, FilterMax F3, and FilterMax F5 and you select to do pre-read optimizations, the Pre- Read Optimization Options dialog displays. See Pre-Read Optimization Options on page 184.

![](<../../../.gitbook/assets/10 (1) (1) (1) (1) (1) (1).png>) For the SpectraMax i3x and SpectraMax Paradigm with a Tunable Wavelength (TUNE) Detection Cartridge and select to run spectral optimization, the Spectral Optimization Wizard runs before the plate is read. See Spectral Optimization on page 182.

1. After the read completes, the plate drawer opens so you can remove the plate. If temperature control is on, the drawer closes again after approximately 10 seconds.
2. After the read completes, save the document and do any additional data analysis.

### Using Auto Read

Use auto read to have the software automatically advances to the next Plate section after a read. The reads progress in the sequence that the Plate sections display within an experiment in the Navigation Tree. When you start a read for a Plate section that you configure to automatically advance with Auto Read, the software advances to the next Plate section in the experiment and then reads that plate. If you configure multiple Plate sections to automatically advance with Auto Read, the Auto Read feature reads all enabled Plate sections until it reads a non-enabled Plate section or the last Plate section in the experiment. The software does not read the Plate sections that appear above the Plate section you select in the Navigation Tree.

For example, if you have five Plate sections (Plate 1, Plate 2, Plate 3, Plate 4, and Plate 5) in an experiment, you can configure Plate 1, Plate 2, and Plate 3 to automatically advance with Auto Read. If you start a read for Plate 2, then the software reads Plate 2, Plate 3, and Plate 4 in sequence. Plate 1 is not read, since it comes before Plate 2. Plate 5 is not read since Plate 4 is not configured to automatically advance with Auto Read.

You can set an interval, or delay time, between plate reads.

The software can collect data from one or more plates, using the same or different instrument settings for different plates, and stores the data in a single document. You can read multiple plates with a single command in the software when you define separate plate reads and use Auto Read.

To enable Auto Read:

1. In the Navigation Tree, select the experiment that has the Plate sections that you want to automatically advance with Auto Read.
2. Select the Operations tab and click ![](<../../../.gitbook/assets/11 (2).jpeg>) **Auto Read**.

![](<../../../.gitbook/assets/12 (3) (1) (1).png>)

1. In the Auto Read dialog, select the Plate sections you want to automatically advance with Auto Read.
2. Optionally, enter the number of seconds to delay (the interval) between each Plate section read.
3. Click **OK**.

**Note:** If you have a Cuvette Set section that follows an enabled Plate section, Auto Read does not advance to or beyond the Cuvette Set section.

![](<../../../.gitbook/assets/13 (3) (1) (1).png>)

### Spectral Optimization <a href="#bookmark2" id="bookmark2"></a>

Spectral optimization in spectral assays improves accuracy while reducing data acquisition and computational burden. Spectral optimization can help to get the maximum signal-to- background ratio for most fluorophores or luminescence labels that are compatible with the wavelength ranges of the instrument or detection cartridge.

To do spectral optimization, there must be a minimum of 10 data points in the range for both the excitation and emission wavelengths. Make sure that the Wavelength Increment permits a minimum of 10 data points in each range.

The Start Emission Wavelength value must be a minimum of 20 nm greater than the Start Excitation Wavelength value. You should use an emission value that is a minimum of 40 nm greater than the excitation value.

Spectral optimization for fluorescence intensity reads is available for the SpectraMax iD3, SpectraMax iD5, and SpectraMax i3x using the built-in monochromator.

Spectral optimization for both Fluorescence Intensity and Luminescence reads is available for the SpectraMax Paradigm with the Tunable Wavelength (TUNE) Detection Cartridge.

To add spectral optimization to a protocol:

*
  1. In the Navigation Tree, select a Plate section.
  2. Click ![](<../../../.gitbook/assets/14 (1) (1).jpeg>) in the section toolbar, in the Settings Information area, or on the Home tab to display the Settings dialog.
  3. On the left, select the **Wavelengths** category.
  4. Select the **Unknown** option.
  5. Define all acquisition settings and click **OK** to close the Settings dialog.

### Spectral Optimization Wizard

To run spectral optimization:

1. In the Navigation Tree, select the Plate section.
2. Click ![](<../../../.gitbook/assets/15 (2).jpeg>) **Read** below the Settings Information area or on the Home tab to display the Spectral Optimization Wizard.
3. On the Read Settings page:
   1. Enter the wavelength ranges and other optimization parameters. You can enter only emission values for Luminescence reads.
   2. Click **Advanced Parameters** to display advanced parameters.
   3. In the **Reading Height** field, enter the reading height.
   4. In the **Integration Time** field, enter the integration time.
   5. For Time-Resolved Fluorescence reads, enter **Pulse Length**, **Number of Pulses**, and

**Measurement Delay**.

*
  1. Click **Next** to display the Blank Well page.

1. On the Blank Well page:
   1. Select the well that corresponds with a well that contains buffer or other liquid for background correction.
   2. Click **Next** to display the Sample Well page.
2. On the Sample Well page:
   1. Select the well that corresponds with a well that contains your sample.
   2. Click **Next** and wait while the indicator displays the progress.
3. On the Optimization Complete page:
   1. View the 3-dimensional heat map image. The software uses the formula (S – B) / B to generate, where S = signal and B = background.

![](<../../../.gitbook/assets/16 (2) (1) (1).png>)

**Note:** For a Luminescence protocol, this is a 2-dimensional graph.

*
  1. In the image, locate the cross hair that indicates the optimized peak wavelengths.

1. To change the wavelengths for the read, either: ![](<../../../.gitbook/assets/17 (3) (1) (1).png>) Drag the cross hair to a new location

![](<../../../.gitbook/assets/18 (2) (1) (1).png>) Enter values in the Excitation field and the Emission field. The Emission value must be a minimum of 20 nm greater than the Excitation value. Use an emission value that is a minimum of 40 nm greater than the excitation value. You can specify only emission values for Luminescence reads.

1. Select the **Use Log Scale** check box to use log scale for the display of the heat map image.
2. If you edit the Wavelength (Custom) values, click **Reset to Optimized Peak** to reset the values to the software defined optimized peak.
3. Right-click on the image:

![](<../../../.gitbook/assets/19 (1) (1) (1) (1) (1).png>) Select **Copy Raw Data** to copy the data in a tab-delimited format that you can paste into a spreadsheet or text editor (SpectraMax i3x only).

![](<../../../.gitbook/assets/20 (2) (1) (1).png>) Select **Copy Image** to copy the image into a bitmap file that you can paste into an image editing program.

&#x20;Select **Save Raw Data to Disk** to save the data into a text file in tab delimited format (SpectraMax i3x with the monochromator only).

&#x20;Select **Save Image to Disk** to save the image into a .bmp file.

1. Click **Restart Wizard** to redefine the settings and run the wizard again.
2. To save the wavelength values without reading the plate, click **Cancel** and then click **Yes**

in the message.

1. Click **Read** to save the protocol with the specified excitation and emission wavelengths and use these values to read the plate.

### Pre-Read Optimization Options <a href="#bookmark3" id="bookmark3"></a>

Use the Pre-Read Optimization Options dialog to run the Microplate Optimization wizard and the Read Height Optimization wizard before the instrument reads the plate.

Plate dimensions can vary slightly between production lots, which can have a potential effect on measurement accuracy. Use the software to optimize plate dimensions by determining the centers of the four corner wells on the plate. Each time you optimize a plate, the software adds a new plate definition with dimensions specific to that lot.

For the SpectraMax i3x, SpectraMax Paradigm, SpectraMax iD3, SpectraMax iD5, FilterMax F3, and FilterMax F5, in certain read modes, you can use pre-read optimization options. Use this function to do plate optimization and read height adjustment. The optimization settings are dependent on the instrument and the read mode.

To have the Pre-Read Optimization Options dialog display before a plate read:

1. In the Navigation Tree, select a Plate section.
2. Click  in the section toolbar, in the Settings Information area, or on the Home tab to display the Settings dialog.
3. On the left, select the **More Settings** category and then select the **Show Pre-Read Optimization Options** check box. From the Acquisition view, add a Plate Optimizer node to the beginning of the Acquisition Plan.
4. Define all acquisition settings and click **OK** to close the Settings dialog.

### Run Pre-Read Optimization Options

To run a protocol with pre-read optimization options:

1. In the Navigation Tree, select the Plate section.
2. Click  **Read** below the Settings Information area or on the Home tab to display the Pre-Read Optimization Options dialog.
3. Select the **Run Microplate Optimization...** check box to run the Microplate Optimization wizard before the plate read.
4. Select the **Run Read Height Adjustment...** check box to run the Read Height Optimization wizard before the plate read.
5. Select the **Plate is Lidded** check box if the plate has a lid.
6. Some instruments allow you to select the plate orientation:

**Note:** If you change the plate orientation for a read, you must do plate optimization for each plate orientation separately.



Landscape Portrait

Opposite Landscape Opposite Portrait

1. Click **Run Optimization** to run the optimization options.

&#x20;If you select the Run Microplate Optimization... check box, the Microplate Optimization wizard displays. See Microplate Optimization Wizard on page 185.

&#x20;If you select the Run Read Height Adjustment... check box, the Read height Optimization wizard displays. If you select both check boxes this wizard displays after you finish the Microplate Optimization wizard. See Read Height Optimization Wizard on page 186.

1. After the wizards run, the Pre-Read Optimization Options dialog displays. Click **Read Plate** to start the read.

### Microplate Optimization Wizard

Use the Microplate Optimization wizard to optimize the plate dimensions to determine the centers of the four corner wells on the plate. Each time you optimize a plate, the software adds a new plate definition with dimensions specific to that lot.

**Note:** If you use a plate type in different plate orientations for measurements, you must do plate optimization for each plate orientation separately.



To do plate optimization:

1. In the Pre-Read Optimization Options dialog, select the **Run Microplate Optimization Before Reading the Plate** check box. See Pre-Read Optimization Options on page 184.
2. Select the **Plate Is Lidded** check box if the plate has a lid.
3. Select a **Microplate** orientation option.
4. Click **Run Optimization** to display the Microplate Optimization wizard.
5. On the Insert the Microplate page:
   1. Click **Open the Microplate Drawer** to move the plate drawer outside the instrument.
   2. Fill the corner wells of the plate with identical samples. To ensure accuracy, samples must be applicable for the read mode. Sample concentration and volume must be identical in each well.
   3. Place the prepared plate on the plate drawer.
   4. Click **Close the Microplate Drawer** to load the plate into the instrument.
   5. Select the **Select the Microplate Orientation** option that matches the orientation of the plate in the plate drawer and is the same as the orientation you select in the Pre- Read Optimization Options dialog. The orientation displays on the right, with well A1 marked in red.
   6. Click **Next** to start the optimization.
6. On the Optimize page:

&#x20;Wait for the software to optimize the plate.

&#x20;If needed, click **Stop Optimization** to stop the plate optimization.

1. On the Select the Center of the Up... page:
   1. Drag the cross hair to the center of the upper left well.
   2. Click **Next**.
2. On the Select the Center of the Lo... page.
   1. Drag the cross hair to the center of the lower left well.
   2. Click **Next**.
3. On the Select the Center of the Up... page:
   1. Drag the cross hair to the center of the upper right well.
   2. Click **Next**.
4. On the Select the Center of the Lo... page:
   1. Drag the cross hair to the center of the lower right well.
   2. Click **Next**.
5. On the Verify Well Centers page:
   1. Verify that the x and y offset and distances between rows and columns are correct. If needed, click in each of the Microplate Dimensions fields and enter the dimension in millimeters.
   2. In the **Microplate Name** field, enter the name of the plate.
6. Click **Save** to add the plate definition to the plate library and to either return to the Pre- Read Optimization dialog or to start the Read Height Optimization wizard. See ReadHeight Optimization Wizard on page 186.

### Read Height Optimization Wizard

When the instrument features an objective lens, use the Read Height Optimization Wizard to adjust the settings to move the lens up and down to optimize the read height for the Luminescence, Fluorescence Intensity, Fluorescence Polarization, and Time-Resolved Fluorescence read modes. Read height is the distance between the top (for top reads) or bottom (for bottom read) surface of the plate to read and the surface of the objective lens.

Optimize read height to match the focus of the optics with the sample volume. This maximizes the raw signal, which yields the highest precision and maximum sensitivity.

The optimized read height is saved in the protocol and is used for all subsequent runs of the protocol until you perform a new optimization or you manually select a read height option.

Use a standard or sample position with a good signal or pipette liquid with a known maximum signal to a well on the plate used in the optimization. The concentration of the optimization sample should be a minimum of ten times greater than the detection limit. The sample volume should be the same as that of samples measured in the protocol. If you use a layout with standards, the software selects the standard well closest to the center of the plate. If you do not use a layout with standards, the software selects the first sample.

**Note:** When you optimize read height for a fluorescence protocol, make sure the optimization sample is the same fluorescent substance that the detection method is configured to detect.



To use the Read Height Optimization wizard:

1. In a plate of the same type for the read, place a single sample that has a known maximum signal and volume.
2. Place the plate into the instrument plate chamber.
3. In the Pre-Read Optimization Options dialog, select the **Run Read Height Adjustment...**

check box. See Pre-Read Optimization Options on page 184.

1. Select the **Plate Is Lidded** check box if the plate has a lid.
2. Select a **Microplate** orientation option.
3. Click **Run Optimization** to display the Read Height Optimization wizard.
4. On the Select Well page:
   1. Select the well in the plate image that contains the sample.
   2. Click **Next**.
5. On the Optimize page:

&#x20;Wait for the software to optimize. Optimization can take from several seconds to several minutes depending on the detection methods you use.

1. On the Optimization Complete page:
   1. To specify a different read height, enter a value in the **Custom Read Height** field, in millimeters.
   2. Click **Save** to save the read height in the protocol. The software uses this read height for all subsequent runs of the protocol until you perform a new optimization or you select a read height option.
2. The Pre-Read Optimization dialog displays. When you complete the optimization, click

**Read Plate** to start the plate read.
