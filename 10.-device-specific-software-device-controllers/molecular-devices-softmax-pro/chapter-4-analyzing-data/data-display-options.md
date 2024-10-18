# Data Display Options

Use the Display Options dialog to specify how to display data for Plate sections and Cuvette Set sections. The values that display in a Plate section are only a representation of the data. In the Plate section, the last digit that displays is rounded based on the actual data value.

The values are not limited by space and can have more digits for each well when you export plate data.

You can clone a plate to view both raw and reduced data or multiple reductions of the same data. See Plate Sections on page 76.

**Note:** If you change the display setting for one cuvette, you change the display settings for all the cuvettes in that Cuvette Set section.

![](<../../../.gitbook/assets/2 (4).png>)

![](<../../../.gitbook/assets/3 (5).png>)

To define display options:

1. ![](<../../../.gitbook/assets/4 (4).jpeg>)Click in the section toolbar or on the Home tab to display the Display Options dialog.
2. Select a **Specify How Data Is Displayed** option:

![](<../../../.gitbook/assets/5 (5).png>) Select **Raw Data** to display the default data type for the read type you select, See the Raw Data Settings section below.

![](<../../../.gitbook/assets/6 (6).png>) Select **Reduced Data** to display reduced data. See the Reduced Data Settings section below.

![](<../../../.gitbook/assets/7 (6).png>) For the Imaging read mode **Imaging Data** replaces the **Raw Data** option. See the Imaging Data Settings section below.

1. In the **Raw/Reduced Data Format** area, click the drop-down:

![](<../../../.gitbook/assets/8 (6).png>) Select **Default** to have the software determine the number of decimal places to display based on the space available. For example, for a plate with 96 wells or fewer, each well is limited to five digits, plus one character for the decimal point, if applicable. For a 384-well plate, each well is limited to four characters, including the decimal point. If the value requires greater precision than can fit in the available space, the format changes to scientific notation.

![](<../../../.gitbook/assets/9 (5).png>) Select **Numeric Notation** to display data in numeric format. Select to display either **Significant Figures** or **Decimal Places** and then enter the number of figures or places to display.

![](<../../../.gitbook/assets/10 (4).png>) Select **Scientific Notation** to display data in scientific notation format. Select to display either **Significant Figures** or **Decimal Places** and then enter the number of figures or places to display.

1. Click **OK**.

### Raw Data Settings

Select **Raw Data** to display the default data type for the read type you select.

![](<../../../.gitbook/assets/11 (5).png>) The Endpoint read type displays raw absorbance, fluorescence, or luminescence values. ![](<../../../.gitbook/assets/12 (4).png>) The Kinetic read type displays the change in raw OD/RFU/RLU values over time as a plot.

![](<../../../.gitbook/assets/13 (4).png>) The Spectrum read type displays raw OD/RFU/RLU values for the range of wavelengths as a plot.

![](<../../../.gitbook/assets/14 (4).png>) The Well Scan read type displays raw OD/RFU/RLU values as shades of blue to red. ![](<../../../.gitbook/assets/15 (3).png>) To display a reduced number, select the **With Reduced Number** check box.

### Reduced Data Settings

Select **Reduced Data** to display reduced data only. The software reports the reduced number in the Group section when you define a template. The reduced data display is based on the selections you make in the Data Reduction dialog. See Data Reduction on page 193.

![](<../../../.gitbook/assets/16 (3).png>) Click the **Options** drop-down:

![](<../../../.gitbook/assets/17 (2).png>) Select **Number** to view only the reduced number.

![](<../../../.gitbook/assets/18 (4).png>) Select **Plot** for the Kinetic read type to display a plot of the raw data. To also view the reduced number, select the **Reduced Number** check box.

![](<../../../.gitbook/assets/19 (4).png>) Select **Grayscale** to display the raw data in eight shades of gray, that range from light for values less than or equal to the low limit, to dark for values greater than or equal to the high limit. Enter the **High Limit** and the **Low Limit** for the grayscale map. To also view the reduced number, select the **Reduced Number** check box.

![](<../../../.gitbook/assets/20 (3).png>) Select **Color Map** to display the raw data in eight colors, that range from blue for values less than or equal to the low limit, to red for values greater than or equal to the high limit. To define the **High Limit** and the **Low Limit** for the color map, enter values in the fields. To also view the reduced number, select the **Reduced Number** check box.

### Imaging Data Settings

For the Imaging read mode **Imaging Data** replaces the **Raw Data** option.

&#x20;Click the **Data Type** drop-down. The options available are the measurement selections you set in the Image Analysis Settings category in the Settings dialog. Separate data types are available for each measured wavelength and classification, if applicable. See Viewing and Selecting Measurement Statistics on page 134.

&#x20;Select **Object Count** to display the total number of objects detected in the image.

Not used for field analysis of confluent areas.

&#x20;Select **Field Count** to display the total number of confluent areas detected in the image. Not used for discrete object analysis.

&#x20;Select **Object Percentage** to display the percentage the objects detected in the image by classification. Not used for field analysis of confluent areas.

&#x20;Select **Covered Area** to display the combined area of all the objects or confluent areas detected in the image as a percentage of the entire image area.

&#x20;Select **Object Area** to display the average area of the objects detected in the image expressed in µm . Not used for field analysis of confluent areas.

2

&#x20;Select **Field Area** to display the average area of the confluent areas detected in the image expressed in µm . Not used for discrete object analysis.

2

&#x20;Select **Object Roundness** to display the average roundness of each object detected in the image. A shape factor of 1.00 is perfectly round, while a shape factor of 0.00 is not round at all. Not used for field analysis of confluent areas.

&#x20;Select **Field Roundness** to display the average roundness of each confluent area detected in the image. A shape factor of 1.00 is perfectly round, while a shape factor of 0.00 is not round at all. Not used for discrete object analysis.

&#x20;Select **Object Average Intensity** to display the average fluorescent signal intensity of the objects detected in the image. This measurement is not used for field analysis of confluent areas. Not used for transmitted light.

&#x20;Select **Field Average Intensity** to display the average fluorescent signal intensity of the confluent areas detected in the image. This measurement is not used for discrete object analysis and not used for transmitted light.

&#x20;Select **Object Intensity** to display the average total fluorescent signal intensity of the objects detected in the image. Not used for field analysis of confluent areas and not used for transmitted light.

&#x20;Select **Field Intensity** to display the average total fluorescent signal intensity of the confluent areas detected in the image. Not used for discrete object analysis and not used for transmitted light.

&#x20;Select **Total Intensity** to display the combined total fluorescent signal intensity of the objects or confluent areas detected in the image expressed in million intensity counts. Not used for transmitted light.

&#x20;Optionally, select the **With Reduced Number** check box to include the reduced data number in the display.

### Viewing Membrane Images

After you scan a membrane for Western Blot data, the data displays in the software as an image. Use the image tools in the Plate section to zoom, crop, colorize, and adjust the intensity of the image. You can select a region of interest (ROI) and rescan the membrane at a higher resolution. See Viewing Western Blot Membrane Data on page 241.

Western Blot membrane data is saved as a TIFF image to allow you to use the image analysis tool of your choice for analysis. The SoftMax Pro Software includes a version of the ImageJ software from U.S. National Institute of Health (NIH). See Analyzing Western Blot Images on page 246.

To view the membrane image in the ImageJ software, click  in the section toolbar and then click **ImageJ Editor**.

To view the membrane image with another image-analysis tool, click  in the section toolbar and then click **External Image Editor**. This option is available if you have .tif files associated with a program other than the ImageJ software. The icon for this tool changes depending on the image-analysis tool you select. See Defining the Membrane Image-Analysis Tool on page 246.

**Note:** The image tools are available when you view a Plate section that contains membrane data.



### Viewing Imaging Data in Wells

You can view a combination of the raw image and the analysis data in up to four wells from a Plate section or the two wells from the Image Analysis Settings. See Plate Sections on page 76 or Image Analysis Settings on page 128.

The Zoom icon becomes active for a Plate section when the imaging data in a well is available for a zoomed display.

To display the SoftMax Pro MiniMax Well Viewer dialog from a Plate section, double-click the well that you want to zoom or click  in the section toolbar or the Home tab. In the Image Analysis Settings Measurement Selection, click **Show Details**.

To view more than one well in a Plate section, drag the cursor to select up to four wells before you access the Zoom Well dialog.

It can take some time before the SoftMax Pro MiniMax Well Viewer dialog displays. It can also display behind the SoftMax Pro Software window. To bring the well viewer to the front, click the **SoftMax Pro MiniMax Well Viewer** icon in the Windows task bar.

The SoftMax Pro MiniMax Well Viewer dialog displays a zoomed image of the well, a table of data, and chart of the data. To choose to display one or more of these areas, select or clear the **Show Images**, **Show Tables**, or **Show Charts** check boxes in the lower-left area.

The three areas in the dialog are interactive.

&#x20;Click the cells in the image to highlight the data in the table and the data in the chart.  Click the data in the table to highlight the cells in the image and the data in the chart.  Click the data in the chart to highlight the cells in the image and the data in the table.

To use an image of the SoftMax Pro MiniMax Well Viewer dialog in a Microsoft PowerPoint presentation, click **Send to PowerPoint**. A new document opens in PowerPoint with an image of the Zoom Well dialog in a slide.

### Image Area Options

The image area displays the acquired image from the well you select. To zoom the image in and out:

&#x20;Right-click the image and select **Zoom In** or **Zoom Out**,  Hold the **CTRL** key and press **+** or **-**.

&#x20;Use the mouse wheel to zoom in or out. To move the image in the image area:

&#x20;Use the scroll bars or click the image and drag it into position.

Click the buttons above the image to switch the view of the image between wavelengths, and to display or hide the found objects or confluent areas.

&#x20;When a button is filled in, the related wavelength, objects, or areas display in the image.

&#x20;When a button is outlined, the related wavelength, objects, or areas do not display in the image.

When you click a button above the images, it affects the display of all the images. Use the controls below the image to adjust the intensity of each wavelength.

To adjust the wavelength intensity:

1. Select the wavelength to adjust.
2. Drag the slider bar on the left to adjust the low level of intensity or click  to move the sliders to the outside edges. The intensity level displays above the bar.
3. Drag the slider bar on the right to adjust the high level of intensity or click  to move the sliders to the outside edges.
4. From the list on the right, select the color for the view.

To automatically scale the intensity of all the wavelengths in the image, click **Auto Scale All Wavelengths**.

### Table Area Options

In the table area, drag the separator lines to change the size the columns. Drag the scroll bars to view the data in the table.

To use the table data in Microsoft Excel, click **Send to Excel**. A new spreadsheet opens in Excel with the data from the table in the cells.

### Chart Area Options

To change the type of chart that displays in the chart area, click **Histogram** or **Scatter Plot**.  For a histogram, select a data type for the **X Axis Data**.

&#x20;For a scatter plot, select data types for the **X Axis Data** and the **Y Axis Data**.
