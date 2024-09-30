# Volume Verification

## Verification Procedure

This technical note describes the verification procedure at Hamilton Robotics. It has been applied in the design phase of the Microlab STAR Line to validate the pipetting performance.

### Validation

* **Trueness:** Validated by a precision balance (5 digits).
* **Precision:** Validated by photometric analyses during the design phase using a plate photometer and strictly controlled environmental conditions.
* The specifications in Table 1 are those validated under the conditions described in this technical note.

### Final QC

Each individual STAR system undergoes final testing in our production environment using a balance. The measurements are taken under broader environmental conditions and correspond with the specifications in Table 1. The final testing data can be found in the Declaration of Quality (DoQ), which is part of the documentation delivered with each instrument.

### Field Verification

The specifications of the volume field verification (FV2) allow the use of a transportable balance under a broader variety of environmental conditions, typically those found in laboratories around the globe.

### Protocol

Testing of the Microlab STAR Line is done gravimetrically using a high precision balance. The precision of the balance used is less than 1/6 of the specified pipetting precision (for one channel). The trueness and precision specifications for the STAR Line refer to an instrument with 8 x 1000µl pipetting channels. The gravimetric method uses 10 single pipettings per channel at the specified volume. For each pipetting (aspiration/dispensation), a new CO-RE disposable tip is used.

* Volumes > 20µl: Dispensed in jet dispense mode.
* Volumes ≤ 20µl: Dispensed in surface mode.

### Pipetting Specifications of Disposable Tips for the STAR Line

<table><thead><tr><th width="143">Disposable Tip Size</th><th width="138">Dispense</th><th>Volume</th><th>Trueness (IRI %)</th><th>Precision (CV %)</th></tr></thead><tbody><tr><td>10µl</td><td>Surface</td><td>0.5µl</td><td>10.0%</td><td>6.0%</td></tr><tr><td></td><td>Surface</td><td>1µl</td><td>5.0%</td><td>4.0%</td></tr><tr><td></td><td>Surface</td><td>5µl</td><td>2.5%</td><td>1.5%</td></tr><tr><td></td><td>Surface</td><td>10µl</td><td>1.5%</td><td>1.0%</td></tr><tr><td>50µl</td><td>Surface</td><td>0.5µl</td><td>10.0%</td><td>6.0%</td></tr><tr><td></td><td>Surface</td><td>1µl</td><td>5.0%</td><td>4.0%</td></tr><tr><td></td><td>Surface</td><td>5µl</td><td>2.5%</td><td>1.5%</td></tr><tr><td></td><td>Jet</td><td>50µl</td><td>2.0%</td><td>0.75%</td></tr><tr><td>300µl</td><td>Surface</td><td>10µl</td><td>5.0%</td><td>2.0%</td></tr><tr><td></td><td>Jet</td><td>50µl</td><td>2.0%</td><td>0.75%</td></tr><tr><td></td><td>Jet</td><td>200µl</td><td>1.0%</td><td>0.75%</td></tr><tr><td>1000µl</td><td>Surface</td><td>10µl</td><td>7.5%</td><td>3.5%</td></tr><tr><td></td><td>Jet</td><td>100µl</td><td>2.0%</td><td>0.75%</td></tr><tr><td></td><td>Jet</td><td>1000µl</td><td>1.0%</td><td>0.75%</td></tr></tbody></table>

***

##

### Volume Verification Design Phase

Careful preparation is essential to set up the verification procedure. The test equipment should be equilibrated with the temperature of the test environment and installed at least 12 hours before verification starts. The STAR Line instrument requires a warm-up period of at least 1 hour.

#### Required Instruments and Resources

* **Test temperature:** 20 ± 2°C
* **Relative humidity:** 50% ± 5%
* **Balance:** Mettler Toledo WXS
* **Windshield on the balance stage**
* **Measuring vessel on the balance stage**
* **Test fluid:** Hamilton verification solution
* **CO-RE tips:** 10µl, 50µl, 300µl, 1000µl

### Measurement Procedure

1. Pick up the disposable tips.
2. Aspirate red sodium salt solution at the corresponding test volume (using the cLLD function to detect the liquid surface).
3. Zero the balance.
4. Dispense the test volume (volumes > 20µl in jet mode, ≤ 20µl in surface mode).
5. Measure the weight of the liquid pipetted (stable balance value).
6. Eject the disposable tip to the tip waste.

Steps 1–6 are executed ≥ 10 times per volume and channel.

### Statistical Calculation

Statistical calculations are done using the corresponding liquid density at the test temperature.

#### Applied Statistics

* **n:** Number of measured values
* **xi:** Volume dispensed in pipetting cycle \[μl]
* **xt:** Nominal volume \[μl]
* **s:** Standard deviation \[μl]
* **x̄:** Mean \[μl]

### Acceptance Criteria

* Trueness (R) and precision (CV) values must be within the specifications, as shown in Table 1.
* Results may vary under different liquid or environmental conditions.
* Environmental conditions such as vibration, ventilation, foot traffic, dust, strong light, and fluctuating temperature and humidity can adversely affect pipetting results.
