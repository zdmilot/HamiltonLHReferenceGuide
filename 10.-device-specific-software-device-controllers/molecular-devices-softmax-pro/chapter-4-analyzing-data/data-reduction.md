# Data Reduction

Use the Data Reduction dialog to define how the software is to reduce data. The reduction process is based on formulas that reduce the raw data to show a single number for each well or cuvette. Further analysis of this reduced number is done in Group sections and Graph sections.

When the software reduces the raw information the instrument collects, calculations are done hierarchically. Only the data reduction calculations that apply to the data based on the instrument, read mode, read type, and settings are done. See Calculation Hierarchy on page 192.

Click ![](<../../../.gitbook/assets/0 (20).jpeg>) in the section toolbar, in the Reduction Settings area, or on the Home tab to display the Data Reduction dialog.

![](<../../../.gitbook/assets/1 (16).jpeg>)

The Data Reduction dialog displays only the reduction options that are available for the instrument you use, the options you select in the Settings dialog, and the options you define in the template.

The software does the applicable calculations in the Plate section or Cuvette Set section in the order that displays in the Data Reduction dialog. If you do not select an option in the Settings dialog, an option is not available for the instrument you use, or an option is not defined in the template, the software continues with the next applicable calculation.

### Raw Data Steps

The software uses the following steps to calculate the raw data displays:

**Apply PathCheck** (Absorbance Endpoint only)

PathCheck Pathlength Measurement Technology normalization calculations apply to the data only when you use PathCheck in the PathCheck category for an Absorbance Endpoint read. When you use PathCheck, you can disable this calculation in the Data Reduction dialog by clearing the **Apply PathCheck** check box. See PathCheck Pathlength Measurement Technology on page 280.

![](<../../../.gitbook/assets/2 (11).jpeg>)

**Apply Plate Background OD** (Absorbance Endpoint only)

The Plate Background OD is the OD of the plate material. It is independent of liquid volume in the well. Subtraction of the Plate Background constant applies to the data only when you use PathCheck in the PathCheck category for an Absorbance Endpoint read. To define the constant, enter a value in the field. When you use PathCheck, you can disable this calculation in the Data Reduction dialog by clearing the **Apply Plate Background OD** check box.

#### Use Plate Blank

The Use Plate Blank calculation is available when you specify a plate blank in the Template Editor for the plate. To allow subtraction of the plate blank value, select the **Use Plate Blank** check box. See Template Editor on page 87.

#### Smoothing

Use smoothing to reduce noise in Kinetic reads for the FlexStation 3 data. This setting takes the moving average of the raw data and displays the plot using the averaged values.

The default is no smoothing, or a setting of 1 “averaged” point.

![](<../../../.gitbook/assets/3 (26).png>) A setting of 3 provides the least amount of smoothing, where the software adds the value of the center point to the values of the points on either side. The software then divides the sum of these points by three and substitutes the resulting value for the center point.

![](<../../../.gitbook/assets/4 (23).png>) A setting of 9 averages the center point with the four points on each side.

When you read multiple wavelengths, the software does smoothing before doing wavelength combination calculations such as ratios or multiplication. For example, if you read at two wavelengths and choose to take a ratio of those wavelengths, the software performs smoothing on each individual wavelength and the wavelength ratio is calculated using smoothed data.

#### Time Alignment

For the FlexStation 3, the software logs each data value with its own read time and can align the time points by Wavelength or by Well to interpolate the data against a single time point.

![](<../../../.gitbook/assets/5 (24).png>) Select the **Time Alignment** check box and then click **Wavelength** to do wavelength combination calculations correctly. For example, you can take a ratio of two different wavelengths (Lm1/Lm2) in a single well that have been read at two different time points. The Wavelength option is available only when two or more wavelengths are present in the data.

With **Wavelength** selected, the software uses quadratic interpolation to calculate the interpolated values. This results in the loss of one point at each end of the plot. Before starting the calculation, the software determines the starting point by averaging the initial data points of the separate wavelengths. For example, if the first data points of the two wavelengths have time values of 0.3 and 0.5 seconds, the software averages these data points and uses 0.4 seconds as its initial point for interpolation.

![](<../../../.gitbook/assets/6 (24).png>) Select the **Time Alignment** check box and then click **Well** to normalize the kinetic read times of the wells in the column against the read time of the first well in the column.

Injection occurs at the same time in all the wells of a column, but each of the wells is read sequentially. So, each well is read at a different time point during the reaction from the injection. With Well selected, the data in the wells are interpolated against the time point of the read of the first well.

#### Group Blank Options

The Group Blank Options calculation is available when you specify a group blank in the Template Editor for the plate. The subtraction of the group blank value can be selected as a pre-reduction process or a post-reduction process.

![](<../../../.gitbook/assets/7 (24).png>) To use the group blank value subtraction calculation as a pre-reduction process, click

#### Before Reduction.

![](<../../../.gitbook/assets/8 (23).png>) To use the group blank value subtraction calculation as a post-reduction process, click **After Reduction**. When you select After Reduction in Group Blank Options, the last step in the Data Reduction dialog shows Group Blank Subtracted.

**Polarization** or **Anisotropy** (Fluorescence Polarization read mode only)

The Fluorescence Polarization read mode returns two sets of data: one for fluorescence intensity parallel (P) to the excitation plane, and the other for fluorescence intensity perpendicular (S) to the excitation plane. The software uses the S and P values to calculate the Polarization (mP) and Anisotropy (r) values. Click the data type to use as the raw data for the reduction.

#### G Factor

The G factor, or grating factor, is used in Fluorescence Polarization to correct polarization data for optical artifacts, converting relative mP data to theoretical mP data. Optical systems, particularly with reflective components, pass light of different polarization with different efficiency. G factor corrects for this instrument-based bias. To define the **G Factor**, enter a value in the field.

**Set first data point to zero** (Kinetic read type only)

Select this check box to offset the first data point to (0,) and shift all other data accordingly. If you clear this check box, some data points that do not fall within the reduction limits can disappear.

To see more data and still display absolute values, increase the reduction limits for **Min OD**, **Min RLU**, or **Min RFU** and the **Max OD**, **Max RLU**, or **Max RFU**.

**Raw Data Display Mode** (Absorbance read mode only)

For Absorbance reads, choose whether to display absorbance data as Optical Density or

%Transmittance.

![](<../../../.gitbook/assets/9 (18).png>) **Optical Density**: The quantity of light passing through a sample to a detector relative to the total quantity of light available. Optical Density includes absorbance of the sample plus light scatter from turbidity.

![](<../../../.gitbook/assets/10 (16).png>) **% Transmittance**: The ratio of transmitted light to the incident light (for the Absorbance read mode).

Click the data type to use as the raw data for the reduction.

**Note:** The software uses separate mathematical calculations to handle Optical Density (OD) and %Transmittance (%T) calculations for Pre-read plate blanking, PathCheck Pathlength Measurement Technology, and Reference, because OD calculations are done on a linear scale, while %T calculations are done on a logarithmic scale. However, the software does not do other calculations differently for OD and %T modes. Because of this, you should use %T only for raw OD, raw OD with Pre-read plate blank subtraction, or raw OD reads which are normalized by the PathCheck Pathlength Measurement Technology. Use caution when you use %T on reduced numbers or the reads that apply to other calculations since the software might not calculate data correctly.

![](<../../../.gitbook/assets/11 (17).png>)

### Data Reduction Steps

Data Reduction display includes one or more of the following calculations:

#### Baseline Options

Baseline options affect the way that the data is graphed for the FlexStation 3.

![](<../../../.gitbook/assets/12 (16).png>) **Absolute** displays the raw data without any change in the way it is graphed. The software uses raw data in subsequent reduction calculations.

![](<../../../.gitbook/assets/13 (15).png>) **Zero Baseline** offsets the graph slightly. For example, if you enter 5 for the number of points, then the software uses the average of the first 5 points as the baseline value, and all raw data is subtracted from this value.

Baseline subtraction applies only to the reduced data. The raw data plots do not change. To view the plot with baseline subtraction, select **Reduced Plot** in the Display dialog or select **Show Reduced** in the Zoom Well dialog.

If two or more wavelengths are present in a read, and you combine these wavelengths with the **Zero Baseline** selected, the zero baseline applies only after the wavelength combination.

![](<../../../.gitbook/assets/14 (15).png>) **% Baseline** makes data from the FlexStation 3 look similar to data from the FLIPR System. You can import data from the FLIPR System into the software, and this option modifies the plot and reduction calculations to make data from the FlexStation 3 comparable to data from the FLIPR System.

This method averages the first number of points you specify (the upper box), divides the raw data by this average value, and then multiplies by 100 (%). Enter a value from 0.001 to 99999 to use to multiply the % Baseline value.

This calculation is done only on the reduced data and only after any wavelength combinations are calculated.

To view the modified plot, select **Reduced Plot** in the Display dialog or select **Show Reduced** in the Zoom Well dialog.

#### Limits

Apply the specified reduction limits to the reduced data after this step. To specify the limits, enter values in the fields.

Limits define the data that displays and is included in data reduction. If you change a limit to show less data, you can change the limit to display the excluded data again.

The display of OD, RFU, or RLU values is relative to the first point measured for each well.

Negative Kinetic values decrease with time, and limits should be set accordingly (below 0) to view negative Kinetic data.

![](<../../../.gitbook/assets/15 (13).png>) **Min OD**, **Min RFU**, or **Min RLU** defines the limit for the minimum value to report. Values from the read that are under this limit do not display and are excluded from data reduction. The default is 0 OD or RFU/RLU. To display negative Kinetics, set the value below 0 (zero).

![](<../../../.gitbook/assets/16 (11).png>) **Max OD**, **Max RFU**, or **Max RLU** defines the limit for the maximum value to report.

Values from the read that are above this limit do not display and are excluded from data reduction.

![](<../../../.gitbook/assets/17 (11).png>) **Lag Time** for the Kinetic read type defines the period of time to be excluded from data reduction. It can be used to ignore the initial lag phase of reactions.

![](<../../../.gitbook/assets/18 (13).png>) **End Time** for the Kinetic read type specifies the time after which data points are excluded from data reduction. The default setting is the total assay time for the Kinetic read type.

![](<../../../.gitbook/assets/19 (12).png>) **Start** for the Spectrum read type specifies the limit in nm for the minimum wavelength setting to report. Values from the read that are under this limit do not appear in the reduced display and are excluded from data reduction.

![](<../../../.gitbook/assets/20 (12).png>) **End** for the Spectrum read type specifies the limit for the maximum wavelength setting to report. Values from reads that are above this limit do not appear in the reduced display and are excluded from data reduction.

#### Wavelength Options

Select an available wavelength formula from the list. To use a custom reduction, select **Custom** from the list and then, click  to display the Formula Editor dialog. See Data Reduction Formulas on page 199.

#### Kinetic Reduction

Select a Kinetic reduction mode from the list. To use a custom reduction, select **Custom** from the list and then, click  to display the Formula Editor dialog. See Data Reduction Formulas on page 199.

Set the number of Vmax Points as needed to ensure that the Vmax line segment passes though the most linear region of the reaction.

#### Spectrum Reduction

Select a Spectrum reduction mode from the list. To use a custom reduction, select **Custom** from the list and then, click  to display the Formula Editor dialog. See Data Reduction Formulas on page 199.

#### Well Scan Reduction

Select **Maximum**, **Minimum**, **Average**, or **Custom** from the list. **Average** provides the average value for all points in the Well Scan. To use a custom reduction, select **Custom** from the list and then, click  to display the Formula Editor dialog. See Data Reduction Formulas on page 199.

#### Group Blank Subtracted

When you select **After Reduction** under Group Blank Options, the last step in the Data Reduction dialog displays Group Blank Subtracted.

After you set all applicable data reduction options, click **OK**.

### Data Reduction Formulas

The software reduction process is based on formulas that reduce the raw data to show a single number for each well or cuvette. Further analysis of the reduced number is done in Group sections and Graph sections. See Group Sections on page 82 and Graphing Data on page 212.

For a full discussion of custom formulas, see the _SoftMax Pro Data Acquisition and Analysis Software Formula Reference Guide_.

### Custom Reduction Formulas

If the predefined Reduction formulas do not meet your needs, create custom Reduction formulas. Select **Custom** from the menus or dialogs to display a Formula button that provides access to the Formula Editor dialog.

The following tables list examples of formulas you can use to combine multiple wavelengths in the Formula Editor dialog.

#### Wavelength Reduction Formula Examples for Specific Wavelength Combinations

| **2 Wavelengths** | **3 Wavelengths**             | **4 to 6 Wavelengths**                                    |
| ----------------- | ----------------------------- | --------------------------------------------------------- |
| !Lm1 + !Lm2       | Lm1 + !Lm2 + !Lm3             | !Lm1 + !Lm2 + ... + !Lmn                                  |
| !Lm1 - !Lm2       | (!Lm1 – !Lm3) / (!Lm2 – !Lm3) | <p>(!Lm1 – !Lm6) /(!Lm2 –</p><p>!Lm5) / (!Lm3 – !Lm4)</p> |
| !Lm1 / !Lm2       | !Lm1 / !Lm3                   | !Lm1 / !Lmn                                               |
| !Lm1 \* !Lm2      | !Lm1 \* !Lm3                  | !Lm1 \* !Lmn                                              |
| Log10(!Lm1/!Lm2)  | Log10(!Lm1/!Lm3)              | Log10(!Lm1/!Lmn)                                          |
| !Pathlength       | !Pathlength                   | !Pathlength                                               |

**Wavelength Reduction Formula Examples for Wavelength Combinations**

| **Formula**                                                 | **Description**                                                                                                                                             |
| ----------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------- |
| !Lmx / constant                                             | For example, Lm1 / 1.44 for quantitating a polyclonal antibody by measuring the absorbance at A280 with PathCheck Pathlength Measurement Technology on.     |
| Average(!Lm1&!Lm2&!Lm3)                                     | Averages together the optical densities for multiple reads at the same wavelength (for example, if you read the well three times at 280 nm).                |
| Min(!Lm1&!Lm2&!Lm3)                                         | Reports the minimum OD/RFU/RLU recorded for multiple wavelength reads in each well.                                                                         |
| Max(!Lm1&!Lm2&!Lm3)                                         | Reports the maximum OD/RFU/RLU recorded for multiple wavelength reads in each well.                                                                         |
| If(!Lmz\<A,makeerr(118), (if (!Lmx>B, makeerr(117), !Lm1))) | Reports “low” for a well with an OD/RFU/RLU less than A, “high” for an OD/ RFU/RLU greater than B, and the OD/ RFU/RLU of a well that lies between A and B. |

You can use custom Reduction formulas that use mathematical operators or terms to obtain specific types of data. The following table provides examples of formulas for the Kinetic read type and the Spectrum read type.

#### Kinetic Reduction Formula Examples

| **Formula**                                                        | **Description**                                                 |
| ------------------------------------------------------------------ | --------------------------------------------------------------- |
| <p>Vmaxcorr(!combinedplot,</p><p>!Vmaxpoints,!readinterval)</p>    | Reports Vmax correlation coefficient for plots in all 96 wells. |
| <p>Vmax(Delta(!combinedplot),</p><p>!Vmaxpoints,!readinterval)</p> | Reports the Vmax Rate of the delta between each time point.     |

**Spectrum or Kinetic Reduction Formula Example**

| **Formula Description** |                                                                                                                                                                                                                                                                                                                                        |
| ----------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Nthitem (!Lm1,X)        | <p>Reports the optical density at item X in the list of reads. For example, if you have a Kinetic run with 20 time points and X is 10, it reports the OD/RFU/RLU of the 10th time point.</p><p>Similarly, if you have a Spectrum scan with 20 measurements and X is 10, it reports the OD/RFU/RLU of the 10th wavelength measured.</p> |

Enclose the accessor names for custom Reduction formulas for imaging data in square brackets to prevent conflicts with other formula elements.

#### Imaging Reduction Formula Example

| **Formula Description**                                |                                                                                             |
| ------------------------------------------------------ | ------------------------------------------------------------------------------------------- |
| <p>![TypeAObjectCount] -</p><p>![TypeBObjectCount]</p> | Reports the difference between the number of Type A and Type B cells detected in the image. |

Click **OK**. The formula displays and becomes the default selection for the Custom option.

### Kinetic Data Reduction Options

The software applies Kinetic reductions to the value at each time point after the wavelength combination formula is applied.

### Vmax

Vmax is the maximum slope of the Kinetic display of mOD/min or RFU/RLU per second. The software calculates Vmax by measuring the slopes of a number of straight lines, where Vmax Points determines the number of contiguous points over which each straight line is defined.

An alternative method to analyze non-linear Kinetic reactions is to report the elapsed time until the maximum reaction rate is reached, rather than to report the maximum rate itself. When you use this in conjunction with Vmax Points, Time to Vmax is the time to the midpoint of the line defined by Vmax Points and used to calculate Vmax.

Vmax Rate is reported as signal/min (milli-OD, RFU, or RLU units per minute) for the Kinetic read type. It is calculated using a linear curve fit, y = Ax + B. A creeping iteration is done using Vmax Points and the slope of the steepest line segment is reported as Vmax Rate. It can also be reported as units per second (the default for Fluorescence and Luminescence modes).

**Vmax (milli-units per min)** and **Vmax (units per sec)** reductions are available for all instruments that support the Kinetic read type. The default Kinetic absorbance reduction is **Vmax (milli-units per min)**.

**Time to Vmax** is useful for applications that include coagulation chemistry where the changing concentration of the reagents does not change Vmax, but rather changes the time at which the reaction reaches the maximum rate.

The software determines the number of available Vmax Points from the Timing settings. Enter a value in the **Vmax Points** field to define the maximum size of the line segment used to determine the slope of the line used to calculate the rate of the reaction. The default is the total number of points taken in the read.

The first slope is calculated for a line drawn that starts at the first read as defined by Lag Time and ends at a total number of reads equal to the Vmax Points setting. The second and subsequent slopes are calculated to start at the second time point and end at a total number of reads equal to the Vmax Points setting. The steepest positive or negative slope is reported as Vmax.

If the data plot displays fewer time points (data points) than Vmax Points, the software uses all the time points to determine the slope of the data.

### Onset Time

Onset Time reports the time required for a Kinetic reaction to reach a specified OD or RFU/RLU (onset OD/RFU/RLU).

This elapsed time data is useful for cascade reactions including clot formation (such as, endotoxin testing) and clot lysis applications where the change in reagent concentration does not have an effect on the maximum optical density change but changes the time required for the reaction to reach completion.

### Time at Minimum

Reports the time at the minimum OD, RFU/RLU, or %T that falls within the reduction limits.

### Time at Maximum

Reports the time at the maximum OD, RFU/RLU, or %T that falls within the reduction limits.

### Time at 1/2 Maximum

Reports the time at the half of the maximum OD, RFU/RLU, or %T that falls within the reduction limits.

To calculate this reduction, the software determines the Kinetic point (within the reduction limits) that has the maximum signal level (OD or %T) and divides it by 2 to get the 1/2 Maximum value. Then it finds the time value at the 1/2 Maximum.

### Area Under Curve

This reduction estimates the area under the curve as defined by the data plots within the reduction limits. The data plots are treated as a series of trapezoids with vertices at successive data points and at the X-axis coordinates of the data points. The areas defined by each of the trapezoids are then computed and summed.

### Slope

The slope reduction option determines the slope of the combined plot (for example, the slope of the line using linear regression after the wavelength combination reduction). This reduction uses all visible time points in the reduction window.

Slope is the same as Vmax Rate when Vmax Rate is set to the same number of points as the run but is different if you have modified Vmax Points.

To use a custom reduction, select **Custom** from the list and then, click  to display the Formula Editor dialog. See Data Reduction Formulas on page 199.

### Spectrum Data Reduction Options

The software applies the Spectrum Reduction formula to the list of numbers in each well (values at each wavelength) after the wavelength combination formula is applied. The default reduction for the Spectrum read type is Lambda at Maximum.

&#x20;**Maximum**: Reports the maximum absorbance (optical density) or percent transmittance (%T), RFU, or RLU within the reduction limits.

&#x20;**Minimum**: Reports the minimum absorbance (optical density) or percent transmittance (%T), RFU, or RLU within the reduction limits.

&#x20;**Lambda at Maximum**: Reports the wavelength at which maximum absorbance (optical density) or percent transmittance (%T), RFU, or RLU within the reduction limits.

&#x20;**Lambda at Minimum**: Reports the wavelength of minimum absorbance (optical density) or percent transmittance (%T), RFU, or RLU within the reduction limits.

&#x20;**Area Under Curve**: Estimates the area under the curve as defined by the data plots, within the reduction limits. The data plots are treated as a series of trapezoids with vertices at successive data points and at the X-axis coordinates of the data points. The software computes and sums the areas defined by each of the trapezoids.

To use a custom reduction, select **Custom** from the list and then, click  to display the Formula Editor dialog. See Data Reduction Formulas on page 199.

### Imaging Data Reduction Options

The Imaging Data list contains the measurement selections from the Image Analysis Settings in the Settings dialog. See Viewing and Selecting Measurement Statistics on page 134.

Separate data types are available for each measured wavelength and classification.

&#x20;**Object Count**: The total number of objects detected in the image. Not used for field analysis of confluent areas.

&#x20;**Field Count**: The total number of confluent areas detected in the image. Not used for discrete object analysis.

&#x20;**Object Percentage**: The percentage the objects detected in the image by classification.

Not used for field analysis of confluent areas.

&#x20;**Covered Area**: The combined area of all the objects or confluent areas detected in the image as a percentage of the entire image area.

**Object Area**: The average area of the objects detected in the image expressed in µm . Not used for field analysis of confluent areas.

2

**Field Area**: The average area of the confluent areas detected in the image expressed in µm . Not used for discrete object analysis.

2

**Object Roundness**: The average roundness of each object detected in the image. A shape factor of 1.00 is perfectly round, while a shape factor of 0.00 is not round at all. Not used for field analysis of confluent areas.

**Field Roundness**: The average roundness of each confluent area detected in the image. A shape factor of 1.00 is perfectly round, while a shape factor of 0.00 is not round at all. Not used for discrete object analysis.

**Object Average Intensity**: The average fluorescent signal intensity of the objects detected in the image. This measurement is not used for field analysis of confluent areas. Not used for transmitted light.

**Field Average Intensity**: The average fluorescent signal intensity of the confluent areas detected in the image. This measurement is not used for discrete object analysis and not used for transmitted light.

**Object Intensity**: The average total fluorescent signal intensity of the objects detected in the image. Not used for field analysis of confluent areas and not used for transmitted light.

**Field Intensity**: The average total fluorescent signal intensity of the confluent areas detected in the image. Not used for discrete object analysis and not used for transmitted light.\\

**Total Intensity**: The combined total fluorescent signal intensity of the objects or confluent areas detected in the image expressed in million intensity counts. Not used for transmitted light.

To use a custom reduction, select **Custom** from the list and then, click ![](<../../../.gitbook/assets/1 (3).jpeg>) to display theFormula Editor dialog. See Data Reduction Formulas on page 199.
