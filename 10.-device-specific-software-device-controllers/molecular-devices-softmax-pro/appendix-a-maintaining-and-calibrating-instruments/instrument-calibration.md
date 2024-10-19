# Instrument Calibration

Use the Calibration dialog to have the instrument step through all available wavelengths one-by-one to measure the signal that reaches the detector when there is no sample in the optical path.

The Operations tab contains a Calibration icon when the instrument supports the air calibration process.

**Note:** Air-calibration applies to absorbance reads. You do not need a plate or cuvette for instrument calibration. The cuvette chamber must be empty for a cuvette calibration.

![](<../../../.gitbook/assets/1 (23) (1).png>)

The software calculates air-calibration values and stores these values in the firmware. The instrument uses the stored air-calibration values when you use Speed Read and when the Calibrate icon is disabled in the Settings dialog. See Speed Read Settings on page 125 and Calibrate on page 141.

1. Select the Operations tab and click **Calibration** to display the Calibration dialog.
2. Select **Plate** to calibrate for plates and/or select **Cuvette** to calibrate for cuvettes.
3. Click **Calibrate Now**.
4. When the calibration indicator shows that the calibration is complete, click **Close**.

### Calibrating SpectraMax L Instruments

For the SpectraMax L instrument, do the following for calibration.

Calibrate the instrument once a year for maximum performance. Select the Operations tab and click Calibration to display the Calibration dialog. There are two calibration methods:

![](<../../../.gitbook/assets/2 (25).png>) Select **Internal Light Emitting Diodes** to calibrate using the instrument’s onboard LEDs.

This method does not require sample preparation.

![](<../../../.gitbook/assets/3 (27).png>) Select **Custom Multi-PMT Normalization Microplate** when the instrument has multiple PMTs and you want to use the light spectrum from your own assays to calibrate the instrument, rather than the light spectrum from the factory configured LEDs.

### Calibrate with Internal Light Emitting Diodes

To calibrate the internal light emitting diodes:

1. Remove any plate from the plate drawer.
2. Select the Operations tab and click **Calibration** to display the Calibration dialog.
3. Select the **Internal Light Emitting Diodes** Calibration Method option.
4. Click **OK**. Calibration is done automatically.

### Custom Multi-PMT Normalization Microplate

Create your own custom calibrations if you prefer to calibrate using the light spectrum from your assays rather than the light spectrum from the factory configured LEDs. Custom calibrations are used from the Settings dialog in the Sensitivity category. See SpectraMax L Protocols on page 326.

There are two different PMT Calibration Factor options:

![](<../../../.gitbook/assets/4 (24).png>) Select **Auto Calculation** to use your own assay materials for calibration, but you want the software to automatically calculate a PMT calibration factor.

![](<../../../.gitbook/assets/5 (25).png>) Select **Manual Set** to use your own assay materials for calibration, and you want to manually calculate the PMT calibration factor based on the signal obtained from each PMT.

### Auto Calculation

Use this option to use your own assay materials for calibration and have the software automatically calculate a PMT calibration factor.

1. Remove any plate from the plate drawer.
2. Select the Operations tab and click **Calibration** to display the Calibration dialog.
3. Select the **Custom Multi-PMT Normalization Microplate** Calibration Method option.
4. Click the **Custom Calibration #** drop-down and select the custom calibration to define. You can define two different custom calibrations.
5. Select the **Auto-Calculation** PMT Calibration Factor option.
6. In the **Dark Adapt Delay** field, enter the number of seconds to enable the sample to adapt to the dark interior of the plate drawer before the calibration starts. This allows the plate autophosphorescence to subside.
7. Click **OK**.
8. A message displays to tell you to insert a 96-well plate into the instrument with material of greater than 100k RLU in wells B2, G2, B11, and G11. After you insert the plate, click **OK**.

### Manual Set

Use this option to use your own assay materials for calibration and manually calculate the PMT calibration factor based on the signal obtained from each PMT. You can read all or part of a plate that contains your assay material (should be greater than 100k RLU) to determine these values and then determine a factor, or multiplier, for each PMT that equalizes the RLU values for each PMT.

1. Select the Operations tab and click **Calibration** to display the Calibration dialog.
2. Select the **Custom Multi-PMT Normalization Microplate** Calibration Method option.
3. Click the **Custom Calibration #** drop-down and select the custom calibration to define. You can define two different custom calibrations.
4. Select the **Manual Set** PMT Calibration Factor option.
5. Enter the values for each available PMT from your calculations. Available fields are dependent the instrument configuration.
6. Click **OK**.
