# Creating Imaging Mode Protocols

To create an Imaging mode protocol:

1. Start the software. See Starting the Software on page 7.
2. Select the SpectraMax i3x instrument. See Selecting an Instrument on page 58.
3. In the Navigation Tree, select a Plate section or Cuvette Set section.
4. Click ![](<../../../.gitbook/assets/7 (3).jpeg>) in the section toolbar, the Settings Information area, or on the Home tab to display the Settings dialog.
5. Select ![](<../../../.gitbook/assets/8 (2).jpeg>) **MiniMax** in the Optical Configuration list.
6. Select the **Imaging** read mode.

If you have previously acquired images and want to make changes to the analysis settings for those images, select the **Re-analysis** read mode.

3\. Define the Imaging read settings or the Re-analysis settings.

For more information about the Imaging read settings or Re-analysis settings, see the SoftMax Pro Software application help.

1. After you define the instrument settings, click **OK** to close the Settings dialog.
2. Create a template, if applicable. See Template Editor on page 87.
3. Set Data Reduction parameters, if applicable. See Data Reduction on page 193.
4. Set Display options, if applicable. See Data Display Options on page 204.
5. Save the settings to a protocol. See Saving Protocols and Data Documents on page 22.

### Imaging Mode Protocol Overview

Imaging read mode does whole-cell imaging assays.

Whole-cell imaging assays are cell-based, or object-based, rather than the single-point measurements found in other types of plate reads. These types of assays can yield more biologically meaningful results that can discriminate the fluorescence related to objects, such as cells or beads, from the bulk solution within a plate well.

The measurement is primarily fluorescent with quantification of cell size, shape, area, and intensity. Label-free quantification is also supported through brightfield, transmitted light imaging. The camera resolution in the SpectraMax MiniMax 300 Imaging Cytometer is sufficient to determine the approximate shape of small 8 micron objects, such as blood cells.

For more information, see Imaging Read Mode on page 312.

**Optimizing the Computer for Image Acquisition**

Acquiring images requires a large portion of computer memory and resources. When the software has limited access to computer memory and resources, image acquisition can take a long time. In some cases, images of some of the wells can be lost. Turn off all other programs to minimize the demands on computer memory and resources.

Before you start an image acquisition, save the protocol to a .txt file format, in a location with enough capacity for the image files. For best results, save Imaging mode files on the secondary hard drive inside the computer. If you use Auto Save to save multiple Imaging mode documents, the software saves each new document without the folders required to save images and analysis results.

**Note:** Use of an external hard drive can slow the data acquisition and is not recommended. Use of a USB flash drive or saving to a network location is not supported.

![](<../../../.gitbook/assets/9 (2) (1) (1).png>)

When you create a document for an Imaging mode experiment or a Western Blot experiment, the software creates a folder with the same name as the document. Each image file can be larger than 2 megabytes. The software can generate 300 megabytes of image data when you acquire the image of a single site in each well of a 96-well plate. A 384-well plate can generate 1 gigabyte of image data. When you acquire images of multiple sites, you increase the data storage requirement.

### Zooming Image in a Well

An image of the selected well displays in the Image Acquisition, Image Selection, and Region of Interest categories in the Settings dialog.

To view a larger version of the image area:

![](<../../../.gitbook/assets/0 (3) (1) (1).png>) Double-click the image to display the Zoom Well dialog.

In the Zoom Well dialog, the image area displays the acquired image from the selected well. To zoom the image in and out:

![](<../../../.gitbook/assets/1 (4) (1) (1).png>) Right-click the image and select **Zoom In** or **Zoom Out**, ![](<../../../.gitbook/assets/2 (3) (1) (1).png>) Hold the **CTRL** key and press **+** or **-**.

![](<../../../.gitbook/assets/3 (7) (1) (1).png>) Use the mouse wheel to zoom in or out. To move the image in the image area:

![](<../../../.gitbook/assets/4 (7) (1) (1).png>)Use the scroll bars or click the image and drag it into position.
