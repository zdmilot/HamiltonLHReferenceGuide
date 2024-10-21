# Viewing Western Blot Membrane Data

After you scan a membrane for Western Blot data, the data displays in the software as an image. Use the image tools in the Plate section to zoom, crop, colorize, and adjust the intensity of the image. You can select a region of interest (ROI) and rescan the membrane at a higher resolution.

![](<../../../.gitbook/assets/0 (3) (1) (1) (1).png>) Drag the slider on the side of the Plate section to zoom the image in or out. ![](<../../../.gitbook/assets/1 (3) (1) (1) (1).png>) Click ![](<../../../.gitbook/assets/2 (2) (1) (1) (1).png>) on the side of the Plate section to view the image at its actual size. ![](<../../../.gitbook/assets/3 (3) (1) (1).png>) Click ![](<../../../.gitbook/assets/4 (2) (1) (1).png>) on the side of the Plate section to fit the image to the Plate section.

![](<../../../.gitbook/assets/5 (3) (1) (1).png>) Click ![](<../../../.gitbook/assets/6 (4) (1).png>) on the side of the Plate section and then drag across the image to define the area to zoom to zoom in on a specific area of the image.

![](<../../../.gitbook/assets/7 (4) (1).png>) Click ![](<../../../.gitbook/assets/8 (4) (1).png>) on the side of the Plate section and then drag the image to move it to move the image within the Plate section.

![](<../../../.gitbook/assets/9 (3) (1).png>) Click ![](<../../../.gitbook/assets/10 (2) (1) (1).png>) on the side of the Plate section and then drag across the image to define the cropped area to crop the image.

![](<../../../.gitbook/assets/11 (3) (1).png>) Select a color option from the **LUT** list at the top of the Plate section to colorize the image from a look-up table.

![](<../../../.gitbook/assets/12 (3) (1).png>) In the **Subtract** field, enter the value to subtract from the image intensity to adjust the intensity of the image.

![](<../../../.gitbook/assets/13 (3) (1).png>) Select the **Log** check box to scale the image intensity.

![](<../../../.gitbook/assets/14 (3) (1).png>) Select the **Invert** check box to invert the colors of the image similar to a photographic negative.

![](<../../../.gitbook/assets/15 (2) (1).png>) Click ![](<../../../.gitbook/assets/16 (2) (1).png>) on the left side of the Plate section and then drag across the image to define the region of interest (ROI) to scan. Click ![](../../../.gitbook/assets/17.jpeg) to scan the region using the ROI Scan Resolution you define in the Settings dialog. The data from the ROI scan replaces the data from the original scan.

![](<../../../.gitbook/assets/18 (2) (1).png>) Click the following to adjust the resolution of the scanned image: ![](<../../../.gitbook/assets/19 (2) (1).png>) Click ![](<../../../.gitbook/assets/20 (1).jpeg>) to view the image at the scanned resolution.

&#x20;Click  to view the image at a fine resolution suitable for external analysis.  Click  to view the image at a very fine resolution suitable for publishing.

&#x20;Click  to restore the image and use the data from the last scan.

Use the Plate section to export the image for further analysis or to publish. These tools are on the right side of the top in the Plate section

&#x20;Click  and then **Excel Analysis** to open the raw image data in a Microsoft Excel template for analysis. See Using Excel to Analyze Western Blot Data on page 242.

&#x20;Click  and then **ImageJ Editor** to open the raw image in the ImageJ software. See Analyzing Western Blot Images on page 246.

Click  and then **External Image Editor** to open the raw image in a pre-defined image- analysis tool. This option is available when you have .tif files associated with a program other than ImageJ software.

**Note:** If you use the ImageJ software or an external image analysis tool to make and save changes to the original image file, the edited image displays in the Plate section and  appears at the top of the section to indicate that you cannot edit the image. Click  to restore the image and use the data from the last scan.



&#x20;Click , click **Export as Text**, and then select a name for the exported text file to export the raw image data to a text file.

&#x20;Click , click **Export as Image**, and then select a name and format for the image export file to export the edited image as it displays in the Plate section.

For information on how to locate the generated image, see Managing Documents on page16.

### Using Excel to Analyze Western Blot Data

You can export the Western Blot image data to a Microsoft Excel template to analyze the image data.

Click  and then click **Excel Analysis** to export the raw image data to an Excel template. An Excel file opens to display the data you export. The Excel file has three worksheets.

&#x20;The **Analysis** worksheet displays the data using automatic background subtraction. You can select the bands to measure and display a bar graph showing an analysis of the selected bands in the **Analysis** worksheet. See Measuring Select Bands on page 242.

&#x20;The **Segmentation** worksheet displays the segmented bands with background subtraction. The segmented bands are displayed on a white background. You can adjust the background noise level and the minimum and maximum band size in the **Segmentation** worksheet. See Defining Segmentation Criteria on page 244.

&#x20;The **Data** worksheet displays the TIFF image and a color rendering of the raw data. No further analysis is shown in the **Data** worksheet. If the automatic background subtraction in the **Analysis** worksheet is not sufficient for your data, you can manually define the background for subtraction in the **Data** worksheet. See Selecting the Background for Subtraction on page 245.

Save the Excel file to save the data and analysis for future reference.

### Measuring Select Bands

Use the Analysis tab at the bottom of the Excel window to select the bands to measure and displays a bar graph of the selected bands.

The Analysis worksheet uses automatic background subtraction for the data display.  Click **Measure All Bands** to measure all the bands that display.

&#x20;Click **Measure Selected Bands**, and then drag the cursor to draw a rectangle around the bands to measure. In the ScanLater - Measure Selected Bands dialog, click **Measure**.

&#x20;Click **Clear Measurements** to remove the measurement analysis from the worksheet. After you select the bands to measure, a bar graph displays with a table below it to show an analysis of the bands based on the analysis criteria. Labels on the blot show the locations of

the bands that you reference in the graph and the table.

You can adjust the background noise level and the minimum and maximum band size in the Segmentation worksheet. See Defining Segmentation Criteria on page 244.

If the automatic background subtraction is not sufficient for your data, you can define the background for subtraction in the Data worksheet. See Selecting the Background for Subtraction on page 245.

### Defining Segmentation Criteria <a href="#bookmark3" id="bookmark3"></a>

Use the Segmentation worksheet to adjust the background noise level and the minimum and maximum band size. You can also remove artifacts that you do not want to include in your measurements. The segmented bands display on a white background.

To adjust the segmentation of the bands, click **Segment Bands** to display the ScanLater - Segment Bands dialog. Select either a **Low** or **High** background noise level to subtract and define the minimum and a maximum band size for the segmentation. The band size is the total number of cells in the Excel worksheet that the band occupies. To view the result of your settings, click **Segment**.

To remove artifacts from the data display, drag the cursor in a rectangle around the artifact, right-click the rectangle, and select **Clear Contents**.

You can select the bands to measure and display a bar graph that displays an analysis of the bands you select in the Analysis worksheet. See Measuring Select Bands on page 242.

If the automatic background subtraction is not sufficient for your data, you can define the background for subtraction in the Data worksheet. See Selecting the Background for Subtraction on page 245.

### Selecting the Background for Subtraction <a href="#bookmark4" id="bookmark4"></a>

Use the Data worksheet to define the background for subtraction in the Data worksheet. The worksheet displays the TIFF image and a color rendering of the raw data with no further analysis.

To define the background for subtraction, drag the cursor in a rectangle around the area to use as the background to display the ScanLater - Select Background dialog. Click **OK**.

You can select the bands to measure and display a bar graph to display an analysis of the bands you select bands in the Analysis worksheet. See Measuring Select Bands on page 242.

You can adjust the background noise level and the minimum and maximum band size in the Segmentation worksheet. See Defining Segmentation Criteria on page 244.

### Analyzing Western Blot Images <a href="#bookmark5" id="bookmark5"></a>

Western Blot membrane data is saved as a TIFF image to allow you to use the image analysis tool of your choice for analysis. The SoftMax Pro Software includes a version of the ImageJ software from U.S. National Institute of Health (NIH).

To view the membrane image in the ImageJ software, click  in the section toolbar and then click **ImageJ Editor**.

To view the membrane image with another image-analysis tool, click  in the section toolbar and then click **External Image Editor**. This option is available if you have .tif files associated with a program other than the ImageJ software. The icon for this tool changes depending on the image-analysis tool you select. See Defining the Membrane Image-Analysis Tool on page 246.

**Note:** If you use the ImageJ software or an external image analysis tool to make and save changes to the original image file, the edited image displays in the Plate section and  appears at the top of the section to indicate that you cannot edit the image. Click  to restore the image and use the data from the last scan.



To retain the editing capabilities within the software and edit the image with an external editor, export the image or make a copy of the generated .tiff image to open in the editor. For information on how to locate the generated .tiff image, see Managing Documents onpage 16.

### Defining the Membrane Image-Analysis Tool

1. In Windows Explorer, right-click a file with a .tif extension.
2. Click **Open With > Choose Default Program** to display the Open With dialog.
3. Select the program to use for membrane image analysis.

&#x20;If the program displays in the **Recommended Programs** list, select it.

&#x20;If the program does not display in the **Recommended Programs** list, click **Browse**.

Locate and select the .exe file for the program to use, and then click **Open**.

The ImageJ software .exe file installed with the SoftMax Pro Software can be found in the ImageJ folder within the SoftMax Pro Software installation folder.

1. Select the **Always Use the Selected Program to Open This Kind of File** check box.
2. Click **OK**.

The next time you open a Western Blot document, the Image icon changes to match the program you select.
