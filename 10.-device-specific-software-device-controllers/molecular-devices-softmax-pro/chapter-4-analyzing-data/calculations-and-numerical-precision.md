# Calculations and Numerical Precision

The calculations done by the software on real numbers use 64-bit double-precision (15+ digits of precision) as defined by the _Institute of Electrical and Electronics Engineers standard for floating point arithmetic (IEEE 754)_. Computations always use the maximum available precision. Rounding occurs only as required for display formatting purposes, or in the evaluation of a formula in which the Round operator is used.

See “Technical Details of Numerical Calculations” in the application help.

Numbers from Plate sections, Cuvette Set sections, Group sections, and Summaries display, print, and export with as many digits after the decimal point as you specify. All numbers the software saves for the document are stored with full 64-bit double-precision.

The precision of the Plate section data display varies based on the space available to view the characters. When you increase the number of digits, the font size of the values in the Plate section decreases. If the value becomes too long, the numbers are cut off at the edge of the wells. When you export plate data, the values are not limited by space and can have more digits for each well. The values that display in a Plate section are only a representation of the data. In both the Plate section and in the exported data, the last digit that displays or exports is rounded based on the actual data value.

You can customize the data display to Numeric notation or Scientific notation format and specify the number of Significant Figures or Decimal Places. You can set these options separately for raw data and reduced data.

Although the software can display reads and the numbers derived from those reads with more than four decimal places, the resolution of the instrument ultimately determines the precision of the calculations. For more information see the instrument user guide.

**Note:** In SoftMax Pro Software versions older than version 6.0, the software used a text-conversion algorithm with a slight upward bias. This can result in a mismatch between the rounded values in the newer version and the older version. Example: When rounding the raw value 14.849999… to one decimal place, versions 6.0 and newer display 14.8, while older versions display 14.9. This does not affect the accuracy of the calculations, since rounding occurs only as required for display formatting purposes, or in the evaluation of a formula in which you use the Round operator.

![](<../../../.gitbook/assets/1 (5) (1) (1).png>)

Computations always use the maximum available precision.

### Calculation Hierarchy

When reducing the data the instrument collects, the software does calculations hierarchically. If you do not select an option in the hierarchy in the Settings dialog, an option is not available for the instrument you use, an option is not applicable to the type of read being done, or an option is not defined in the Template Editor dialog or the Reductions dialog, then the software continues with the next listed calculation in the hierarchy.

The following is the general hierarchy of reduction calculations:

1. Apply Well Masking
2. Subtract Plate Background constant
3. Apply PathCheck Technology normalization
4. Subtract Plate Blank
5. Apply Smoothing
6. Time Alignment (Interpolate Raw Data)
7. Subtract Group Blank (pre-reduction option)
8. Calculate mP or Anisotropy
9. Set first data point to zero
10. Convert OD to %T
11. Apply Reduction Limits
12. Apply Wavelength Combination
13. Apply Baseline Options
14. Apply Kinetic or Spectrum Reduction
15. Subtract Group Blank (post-reduction option) For more information on calculations, see:

![](<../../../.gitbook/assets/2 (5) (1) (1).png>) Kinetic Data Reduction Options on page 201

![](<../../../.gitbook/assets/3 (6) (1) (1).png>) Spectrum Data Reduction Options on page 202

![](<../../../.gitbook/assets/4 (4) (1) (1).png>) Absorbance Read Mode on page 278 Optical Density and %Transmittance calculations ![](<../../../.gitbook/assets/5 (6) (1).png>) PathCheck Pathlength Measurement Technology on page 280

Fluorescence Polarization Read Mode on page 303 ![](<../../../.gitbook/assets/6 (7) (1).png>) Curve Fit Functions on page 366

![](<../../../.gitbook/assets/7 (7) (1).png>)

![](<../../../.gitbook/assets/8 (7).png>) For information on statistical functions, see the _SoftMax Pro Data Acquisition and Analysis Software Formula Reference Guide_.
