# TR-FRET Read Mode

Time-resolved fluorescence is a measurement technique based on fluorescence resonance energy transfer (FRET) using the advantages of time-resolved fluorescence (TRF) read. TR- FRET read mode requires the installation of the Enhanced TRF module in the instrument and a computer running the SoftMax Pro Software.

TR-FRET uses a donor fluorophore with a long fluorescence lifetime, such as Europium. The acceptor fluorophore acts as if it also has a long fluorescence lifetime. This lets the time- gating principle of time-resolved fluorescence be applied to the acceptor emission to separate specific signal from background and signal caused by compound interference.

Time-gating electronics introduce a delay between the flashes and the start of signal collection. During the delay, the unspecific fluorescence caused by test compounds, assay reagents, and the plate vanishes while only a small portion of the specific fluorescence from the acceptor fluorophore is sacrificed. Enough of the specific signal remains, with the benefit of reduced background.

### Applications of TR-FRET

TR-FRET is used in competitive assays to quantify the binding between two labeled molecules, or the disintegration of a bound complex. Binding partners can have similar molecular weights as opposed to fluorescence polarization read modes. TR-FRET is an assay that requires only mixing and measuring—no wash steps are required. It can also be miniaturized, which makes it useful for high-throughput screening applications.

### HTRF Read Mode

Homogeneous time-resolved fluorescence (HTRF) is a measurement technique based on fluorescence resonance energy transfer (FRET) using the advantages of time-resolved fluorescence (TRF) read.

HTRF uses a donor fluorophore with a long fluorescence lifetime, such as Europium. The acceptor fluorophore acts as if it also has a long fluorescence lifetime. This lets the time- gating principle of time-resolved fluorescence be applied to the acceptor emission to separate specific signal from background and signal caused by compound interference.

Time-gating electronics introduce a delay between the flashes and the start of signal collection. During the delay, the unspecific fluorescence caused by test compounds, assay reagents, and the plate vanishes while only a small portion of the specific fluorescence from the acceptor fluorophore is sacrificed. Enough of the specific signal remains, with the benefit of reduced background.

### Applications of Homogeneous Time-Resolved Fluorescence

Homogeneous time-resolved fluorescence (HTRF) is used in competitive assays to quantify the binding between two labeled molecules, or the disintegration of a bound complex.

Binding partners can have similar molecular weights as opposed to fluorescence polarization read modes. HTRF is a homogeneous assay that requires only mixing and measuring—no wash steps are required. It can also be miniaturized, which makes it useful for high- throughput screening applications.

The fluorescence ratio related to the HTRF readout is a correction method developed by Cisbio, for which Cisbio has granted a license to Molecular Devices. Its application is strictly limited to the use of HTRF reagents and technology, excluding other TR-FRET technologies such as IMAP TR-FRET calculations of acceptor to donor ratios.

### HTRF Instruments and Detection Cartridges

The following instruments have HTRF read mode capability:

![](<../../../.gitbook/assets/0 (10).png>) SpectraMax iD5 Multi-Mode Microplate Reader on page 320 (requires the Enhanced TRF module)

![](<../../../.gitbook/assets/1 (11).png>) SpectraMax M5 and SpectraMax M5e Multi-Mode Microplate Readers on page 330 ![](<../../../.gitbook/assets/2 (13).png>) SpectraMax i3x and SpectraMax i3 Multi-Mode Detection Platforms, see page 323 (

requires the Cisbio HTRF Detection Cartridge, see page 346)

![](<../../../.gitbook/assets/3 (14).png>) SpectraMax Paradigm Multi-Mode Microplate Reader, see page 327 (requires the Cisbio HTRF Detection Cartridge, see page 346)

![](<../../../.gitbook/assets/4 (12).png>)

**Note:** For the SpectraMax i3x, you can use the detection cartridges for top reads only.

HTRF is a registered trademark of Cisbio Bioassays.

### Analyzing HTRF Data

A Homogeneous Time-Resolved Fluorescence (HTRF) measurement includes a number of flash intervals. Each flash interval consists of flashing the lamp, pausing for a specified length of time, and measuring the fluorescence intensity of the sample. These flash intervals are repeated several times, as specified in the protocol parameters.

#### Data Reduction

Data reduction for HTRF reads consists of two steps.

First, a ratio of the signal measured by the emission from the acceptor label at 665 nm to the signal measured by the emission of the donor label at 616 nm is calculated and multiplied by a factor of 10,000. This generates what is called the HTRF ratio.

In the second step, ratios are calculated that represent the relative change in the HTRF signal compared to that of the assay background, represented by assay controls potentially named negative or Standard 0. This relative response ratio is called the Delta F and is formatted as a percentage, although values greater than 100 can be generated.

#### Data Optimization

Measurement noise is dependent on the read time per sample (time per plate or time per well). The detection limit improves when the read time is increased. Therefore, it is important to specify the read time when you compare measurements. For TRF, the read time per well increases with the number of pulses you enter. The time between pulses can be different on various systems.

#### HTRF Timing Parameters Example

| **Parameter**                      | **Value** | **Comment**                                                       |
| ---------------------------------- | --------- | ----------------------------------------------------------------- |
| Number of pulses                   | 30        | The number of flashes per read.                                   |
| Measurement delay                  | 30 µs     | The delay to ensure the excitation pulse is no longer detectable. |
| Integration time per cycle (pulse) | 400 µs    | The period for accumulating the signal.                           |

Defining the number of flashes (pulses) cannot be used for comparative purposes because the flash and intensity rate varies from system to system.

There are two timing parameters which can be optimized to adjust the performance of the measurement: time per plate or time per well, and integration time per cycle.

All low-light-level detection devices have some measurement noise in common. To average out the measurement noise, optimization of the time per well involves accumulating as many counts as possible. Within some range, you can reduce noise (CVs, detection limit) by increasing the read time per well, as far as is acceptable from throughput and sample stability considerations.

As the number of flashes (read time per well) is increased, several aspects of the data improve:

![](<../../../.gitbook/assets/5 (13).png>) Delta F values show less variability (better CVs).

![](<../../../.gitbook/assets/6 (13).png>) Small Delta F values are better distinguished from noise. ![](<../../../.gitbook/assets/7 (13).png>) Noise of background is reduced.

The second timing parameter which can be optimized is the Integration time per cycle. Care must be taken in optimizing the integration time to consider noise. Delta F is higher at low integration times, but noise is also high at low integration times. The optimal integration time is where noise is minimized while maximizing Delta F.

In the following example, the optimal integration time (read time per cycle) is displayed to be in the 500 µs to 1000 µs range, as noise is minimized and Delta F is still relatively high. Going greater than 1000 µs shows a sharp decline in Delta F without apparent improvement in noise.

![](<../../../.gitbook/assets/8 (12).png>)

#### Relationship Between Integration Time, Noise, and Delta F

Z´ is the standard statistical parameter in the high-throughput screening community for measuring the quality of a screening assay independent of test compounds. It is used as a measure of the signal separation between the positive controls and the negative controls in an assay.

The value of Z´ can be determined using the following formula:

$$
Z' = 1 - \frac{3(\text{SD}_{c+}) + 3(\text{SD}_{c-})}{|\text{Mean}_{c+} - \text{Mean}_{c-}|}
$$

where **SD** is the standard deviation, **c+** is the positive control, and **c–** is the negative control.

A Z´value greater than or equal to 0.4 is the generally acceptable minimum for an assay. You can use higher values when results are more critical.

Z´ is not linear and can be made unrealistically small by outliers that skew the standard deviations in either population. To improve the Z´value, you can increase the quantity oflabel in the sample, if acceptable for the assay, or increase the read time per well.
