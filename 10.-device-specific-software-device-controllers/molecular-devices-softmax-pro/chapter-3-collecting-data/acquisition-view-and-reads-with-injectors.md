# Acquisition View and Reads With Injectors

The Settings dialog for the SpectraMax i3, SpectraMax i3x, SpectraMax iD3, and SpectraMax iD5 provides two methods to configure a plate read.

The Acquisition view uses an acquisition plan with tools that allows you to define settings in a workflow design when you need to do multi-step plate reads.

![](<../../../.gitbook/assets/1 (7) (1) (1) (1) (1).png>)

**Note:** You must use the Acquisition view to define reads with injection.

To switch between the views:

![](<../../../.gitbook/assets/2 (7) (1) (1) (1) (1).png>) Click ![](<../../../.gitbook/assets/3 (3) (1) (1).jpeg>) in the lower-left corner in the Settings dialog.

**Note:** If you define a read with injection and then switch to the Standard view, your settings are not saved.

![](<../../../.gitbook/assets/4 (11) (1) (1).png>)

The following image shows a read for a 96-well Standard plate of an entire plate with an Acquisition Plan for a Luminescence Kinetic read with SmartInject technology. The Acquisition Plan starts with plate optimization and does 10 baseline reads before the injection step. It then delays one second after the injection ends before the Luminescence read starts. All the acquisition steps are in a Loop between the For Each Well node and the Next Well node.

![](<../../../.gitbook/assets/5 (2) (1).jpeg>)

### Plate Settings

Use the top area of the dialog to select the plate settings, read area, and read order. To define plate settings:

1. Click the **Plate Size** drop-down and select the number of wells in the plate.
2. Click the **Plate Name** drop-down and select a plate.
3. Click ![](<../../../.gitbook/assets/6 (2) (1).jpeg>) to display the Plate Editor dialog where you can edit or create a plate. See Plate Editor on page 117.
4. Select the **Plate has a Lid on Top** check box if the plate has a lid.

**CAUTION!** If the plate has a lid, you must verify that the plate height with a lid is set accurately in the Plate Editor dialog before you start a read.

![](<../../../.gitbook/assets/7 (4) (1) (1).png>)![](<../../../.gitbook/assets/8 (4) (1) (1).png>)

1. Click **Read Area**:

![](<../../../.gitbook/assets/9 (4) (1) (1).png>) Select the **Select All** check box to read all the wells in the plate.

![](<../../../.gitbook/assets/10 (2) (1) (1) (1).png>) To select a contiguous, rectangular region on the plate, use your mouse to drag the pointer and select the wells to read.

1. Select a **Read Order**:

![](<../../../.gitbook/assets/11 (2) (1) (1) (1).png>) Select **Row** to read the entire plate row-by-row.

![](<../../../.gitbook/assets/12 (4) (1).png>) Select **Column** to read the entire plate column-by-column.

![](<../../../.gitbook/assets/13 (4) (1).png>) To do a Well read order, add a For Each Well loop in the Acquisition view.

### Toolbox and Acquisition Plan

The lower area of the dialog provides a toolbox that contains the available steps and the Acquisition Plan that displays the time line of steps for the protocol.

![](<../../../.gitbook/assets/14 (3) (1) (1).png>) ![](<../../../.gitbook/assets/15 (3).jpeg>) **Shake** - Add a Shake step to have the instrument shake the plate in the chamber.

Click ![](<../../../.gitbook/assets/16 (3) (1) (1).png>) to display Shake settings where you define the shake duration and shake method. To shake the plate at the same time as an injection, add a SmartInject™ step not an Inject step or a Shake step.

![](<../../../.gitbook/assets/17 (4) (1) (1).png>) ![](<../../../.gitbook/assets/18 (2).jpeg>) **Plate Optimizer** - Add a Plate Optimizer node to have the software display the Pre- Read Optimization Options dialog before the plate is read. You can place this step only at the beginning of the Acquisition Plan. See Show Pre-Read Optimization Options on page 143.

![](<../../../.gitbook/assets/19 (2) (1) (1).png>) ![](<../../../.gitbook/assets/20 (1) (1) (1) (1).jpeg>) **Delay** - Add a Delay step after an Inject step or a SmartInject step to have the instrument wait after the injection before the read begins. Click  to display Delay settings where you define the number of seconds to wait between steps (from 0.001 seconds to 100 seconds). The Delay node compensates for the hardware delay. See below for details.

&#x20; **Inject** - Add an Inject step for a simple injection. Click  to display Inject settings. Select the injector to use and enter the number of microliters (μL) to dispense. You can dispense from 1 μL to the maximum allowable volume of the well, based on the plate type you select. Define the dispense volume based on the requirements of your assay and the net volume available in the well. To shake the plate after an injection, add a Shake step after the Inject step. To shake the plate during an injection, use a SmartInject step not an Inject step.

&#x20; **Smart Inject** - Add a SmartInject step to shake the plate during an injection. The plate continues to shake through the following delay step, if you add a Delay step and stops shaking before the instrument reads the well. Click  to display SmartInject settings. Select the injector to use and enter the number of microliters (μL) to dispense. You can dispense from 1 μL to the maximum allowable volume of the well, based on the plate type you select. Define the dispense volume based on the requirements of your assay and the net volume available in the well.

&#x20; **Baseline** - For the Kinetic read type, add a Baseline step before an Inject step or a SmartInject step to have the instrument take baseline reads. Click  and enter the number of baseline reads (from 1 to 999). You can then subtract the baseline data from the reads that follow the injection. You can use the Formula Editor dialog to automate baseline subtraction.

&#x20; **For Each Well** - Reads with injection are generally done well-by-well. Use the For Each Well loop to have the instrument run all the steps in the Acquisition Plan for each well individually. All the injections, delays, and reads you define are done on the first well before the steps are run again for the next well. The software adds a Next Well node to the end of the plan. Add the steps for the assay between the For Each Well node and the Next Well node.

### Creating Acquisition Plans

The steps in the Acquisition Plan occur in sequence from left to right between the Begin node and the End node. When a step has multiple settings, the settings display below the step in the time line.

To create an acquisition plan:

1. To start from scratch, click **Clear All** or click the **Load Predefined Acquisition Template**

drop-down and select a predefined Acquisition Plan.

1. In the Toolbox area on the left, either double-click or drag **Acquisitions**, **Actions**, and **Loops** to the Acquisition Plan. The software allows you to place each step in an appropriate place in the plan. Example: You can place the Plate Optimizer node only at the beginning of the plan.
2. When you add a step to the Acquisition Plan, a prompt appears:

&#x20;Some Acquisitions require you to select hardware for the optical configuration. This can be the monochromator or a detection cartridge for the SpectraMax i3x. See Supported Detection Cartridges on page 343.

&#x20;All Acquisitions require you to select a read type. See Endpoint Read Type on page 275, Kinetic Read Type on page 275, Spectrum Read Type on page 276, and Well Scan Read Type on page 276.

1. Add Actions and Loops.
2. Add an injector step or a SmartInject step.
3. Click a node to display .  Click  to delete the node.

&#x20;Click  to display settings for the node.

&#x20;Wavelength Settings on page 113

&#x20;PathCheck Technology Settings on page 120  PMT and Optics Settings on page 121

&#x20;Timing Settings on page 123

&#x20;Well Scan Settings on page 124  Shake Settings on page 124

&#x20;Speed Read Settings on page 125

&#x20;Normalization on page 144 (for SpectraMax i3x)  Interlaced Reading on page 144

1. After you define the settings for a step in the Acquisition Plan, click the Workspace outside of the settings.
2. After you define the instrument settings, click **OK** to close the Settings dialog.
3. Before you start a read, you should save the document. See Saving Protocols and Data Documents on page 22.

### SpectraMax i3x Injector Reads

To define injector reads for the SpectraMax i3x:

1. Install the Injector Cartridge into the cartridge drawer.
2. When you add a Luminescence read to the Acquisition Plan, select **INJECTOR** from the Select Hardware list to use the Injector Cartridge for the read. A Luminescence read with injection is taken from the top of the plate.
3. When you add a Fluorescence Intensity read to the Acquisition Plan, select **MONO** from the Select Hardware list to use the instrument's built-in monochromator for the read. A Fluorescence Intensity read with injection is taken from the bottom of the plate.

### Delay Details

### SpectraMax iD3 and SpectraMax iD5 Delay

The Delay step compensates for the hardware delay. If the delay you define is longer than the hardware delay, then the actual delay time is the delay time you define. However, if the delay you define is shorter than the hardware delay, then the actual delay time is the hardware delay time. For example, if you define a Luminescence read delay of 1 second, then the actual delay time between the end of the injection and the beginning of the read is

1 second. However, if you define a Luminescence read delay of 0.05 seconds, then the actual delay time between the end of the injection and the beginning of the read is 0.3 seconds due to the hardware delay.

&#x20;For Absorbance reads there is an 800 msec delay after injection for both injectors.

&#x20;For Luminescence top reads there is a 500 msec delay after injection for both injectors.

&#x20;For Fluorescence top and bottom reads there is a 500 msec delay when the injector 1 injection starts and a 500 msec delay after the injector 2 injection ends.

### SpectraMax i3x Delay

&#x20;For Luminescence reads, there is a delay of 0.3 seconds after the injection ends and before the read begins to allow time for the detector to move into position for the read.

&#x20;For Fluorescence intensity reads, there is no delay for injector number 1. The read starts at the same time as the injection unless you add a Delay step. For injector number 2, there is a delay of 0.3 seconds after the injection ends and before the read begins.
