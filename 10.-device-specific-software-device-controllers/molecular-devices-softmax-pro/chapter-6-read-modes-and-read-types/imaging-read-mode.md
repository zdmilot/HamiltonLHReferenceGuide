# Imaging Read Mode

To use this read mode, you must have the SpectraMax MiniMax 300 Imaging Cytometer installed with the SpectraMax i3x.

Imaging read mode does whole-cell imaging assays.

Whole-cell imaging assays are cell-based, or object-based, rather than the single-point measurements found in other types of plate reads. These types of assays can yield more biologically meaningful results that can discriminate the fluorescence related to objects, such as cells or beads, from the bulk solution within a plate well.

The measurement is primarily fluorescent with quantification of cell size, shape, area, and intensity. Label-free quantification is also supported through brightfield, transmitted light imaging. The camera resolution in the SpectraMax MiniMax 300 Imaging Cytometer is sufficient to determine the approximate shape of small 8 micron objects, such as blood cells.

Other advantages of these assays include the direct interrogation of individual cells instead of whole well or cell lysates that permit controlling for cell numbers and heterogeneity in cell- based assays. Also, increased sensitivity by both detecting a few fluorescent cells per well, as well as detecting cells that are, on average, less fluorescent.

The SpectraMax MiniMax 300 Imaging Cytometer 300 can acquire image data using transmitted light and two fluorescent channels during the same plate read. Use the Settings dialog to select the channels for the acquisition. The StainFree™ Cell Detection Algorithm eliminates cell staining for cell counting and confluency measurements using proprietary transmitted light analysis technology.

You can obtain imaging data through visual inspection of the image or by using the analysis tools available in the SoftMax Pro Software.

### Applications of Whole-Cell Imaging

Whole-cell imaging assays measure a diverse set of cellular responses, such as fluorescent protein expression (phosphorylated and total), cell viability (cell toxicity), cell apoptosis, and cell cycle analysis.

Supported dyes include the following:

![](<../../../.gitbook/assets/0 (6).png>) EarlyTox™ Cell Integrity Kit

![](<../../../.gitbook/assets/1 (7).png>) Fluorescein isothiocyanate (FITC) ![](<../../../.gitbook/assets/2 (9).png>) Calcein AM

![](<../../../.gitbook/assets/3 (10).png>) Alexa Fluor 488 or Alexa Fluor 647 ![](<../../../.gitbook/assets/4 (8).png>) Cy5

![](<../../../.gitbook/assets/5 (10).png>) DRAQ5

For information about creating Imaging read mode protocols, see Creating Imaging Mode Protocols on page 177.

### Imaging Instruments and Detection Cartridges

The following instrument has Imaging read mode capability:

![](<../../../.gitbook/assets/6 (10).png>) SpectraMax i3x and SpectraMax i3 Multi-Mode Detection Platforms, see page 323 The SpectraMax® MiniMax™ 300 Imaging Cytometer adds imaging capability to the

SpectraMax i3x to visually inspect your sample and to run cell-based assays at cellular or

whole-cell resolution.

To do brightfield, transmitted-light imaging, install the SpectraMax Transmitted Light (TL) Detection Cartridge in the detection cartridge drawer. See Transmitted Light (TL) Detection Cartridge on page 351.

### Analyzing Imaging Data

You can obtain imaging data through visual inspection of the image or you can use the analysis tools in the SoftMax Pro Software.

In fluorescent imaging, the fluorescence in the sample is excited with light of a specified wavelength. The fluorophore emits at a longer wavelength that is captured in the image.

The software measures the intensity of the emitted fluorescence and estimates the intensity of the background in the image.

You can select one of the following image analysis types.

### Discrete Object Analysis

Discrete Object Analysis uses proprietary algorithms to analyze separate objects, or cells, based on multiple parameters including the signal intensity over the background and the size of the objects.

Click **Discrete Object Analysis** to display the Wavelength for Finding Objects list below the analysis types. Select the wavelength to use to identify the objects in the well images. You can use transmitted light or a fluorescent wavelength to find nuclei or easily separable objects in the image. The StainFree™ Cell Detection Algorithm eliminates cell staining for cell counting and confluency measurements using proprietary transmitted light analysis technology.

Select the **Image Analysis Settings** category to display the following:

![](<../../../.gitbook/assets/7 (10).png>) Click **Find Objects** to enter size and intensity values or to use proprietary algorithms with the drawing tools to graphically define the objects and the background areas for the analysis. See Finding Discrete Objects or Confluent Areas on page 129.

![](<../../../.gitbook/assets/8 (9).png>) Click **Classify Objects** to define separate measurements for different types of found objects, or cells. See Classifying Discrete Objects on page 133.

![](<../../../.gitbook/assets/9 (8).png>) Click **Select Measurements** to view the results of the analysis for the wells you select. See Viewing and Selecting Measurement Statistics on page 134.

### Field Analysis

Field Analysis uses proprietary algorithms to analyze confluent areas based on parameters including the signal intensity over the background and the size of the areas.

Click **Field Analysis** to display the Wavelength for Finding Confluent Areas list below the analysis types. Select the wavelength to use to identify the confluent areas in the well images. The StainFree™ Cell Detection Algorithm eliminates cell staining for cell counting and confluency measurements using proprietary transmitted light analysis technology.

The Image Analysis Settings category expands to display the following:

![](<../../../.gitbook/assets/10 (6).png>) Click **Find Confluent Areas** to use proprietary algorithms with the provided drawing tools to graphically define the confluent areas and the background areas for the analysis. See Finding Discrete Objects or Confluent Areas on page 129.

![](<../../../.gitbook/assets/11 (8).png>) Click **Select Measurements** to view the results of the analysis for the wells you select. See Viewing and Selecting Measurement Statistics on page 134.

The SoftMax Pro Software proprietary algorithms with the provided drawing tools help the software learn the patterns of the objects that you want to find. Depending on the complexity of the object patterns, this teaching process can take several iterations before you get the expected results. See Resolving Issues with Object Drawing and Finding on page 136.

### Analysis Measurement Parameters

Depending on the needs of your application, you can use one or more of the following analysis measurement parameters for the region of interest (ROI) in your experiment:

![](<../../../.gitbook/assets/12 (7).png>) **Object Count**: The total number of objects detected in the image. Not used for field analysis of confluent areas.

![](<../../../.gitbook/assets/13 (6).png>) **Field Count**: The total number of confluent areas detected in the image. Not used for discrete object analysis.

![](<../../../.gitbook/assets/14 (7).png>) **Object Percentage**: The percentage the objects detected in the image by classification.

Not used for field analysis of confluent areas.

![](<../../../.gitbook/assets/15 (6).png>) **Covered Area**: The combined area of all the objects or confluent areas detected in the image as a percentage of the entire image area.

**Object Area**: The average area of the objects detected in the image expressed in µm . Not used for field analysis of confluent areas.

2

**Field Area**: The average area of the confluent areas detected in the image expressed in µm . Not used for discrete object analysis.

2

**Object Roundness**: The average roundness of each object detected in the image. A shape factor of 1.00 is perfectly round, while a shape factor of 0.00 is not round at all. Not used for field analysis of confluent areas.

**Field Roundness**: The average roundness of each confluent area detected in the image. A shape factor of 1.00 is perfectly round, while a shape factor of 0.00 is not round at all. Not used for discrete object analysis.

**Object Average Intensity**: The average fluorescent signal intensity of the objects detected in the image. This measurement is not used for field analysis of confluent areas. Not used for transmitted light.

**Field Average Intensity**: The average fluorescent signal intensity of the confluent areas detected in the image. This measurement is not used for discrete object analysis and not used for transmitted light.

**Object Intensity**: The average total fluorescent signal intensity of the objects detected in the image. Not used for field analysis of confluent areas and not used for transmitted light.

**Field Intensity**: The average total fluorescent signal intensity of the confluent areas detected in the image. Not used for discrete object analysis and not used for transmitted light.

**Total Intensity**: The combined total fluorescent signal intensity of the objects or confluent areas detected in the image expressed in million intensity counts. Not used for transmitted light.
