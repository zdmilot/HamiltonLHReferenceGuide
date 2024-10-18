# Time-Resolved Fluorescence Read Mode

Time-Resolved Fluorescence is a measurement technique that depends on three characteristics that lead to better discrimination between the specific signal, proportional to the quantity of label, and the unspecific fluorescence resulting from background and compound interference:

![](<../../../.gitbook/assets/0 (17).png>) Pulsed excitation light sources

![](<../../../.gitbook/assets/1 (19).png>) Time-gated electronics faster than the fluorescence lifetime ![](<../../../.gitbook/assets/2 (20).png>) Labels with prolonged fluorescence lifetime

The time-gating electronics introduce a delay between the cutoff of each light pulse and the start of signal collection. During the delay, the unspecific fluorescence (caused by test compounds, assay reagents, and the plate) vanishes, while only a small portion of the specific fluorescence from the label is sacrificed. Enough of the specific signal remains during the decay period, with the added benefit of reduced background.

In Time-Resolved Fluorescence read mode, the instrument detects the extremely long emission half-lives of rare earth elements called lanthanides, such as europium (lifetime of about 700 µs), samarium (lifetime of about 70 µs), or terbium (lifetime of about 1000 µs).

### Applications of Time-Resolved Fluorescence

Time-Resolved Fluorescence is widely used in high throughput screening applications such as kinase assays, and is useful in some fluorescence immunoassays, such as DELFIA (dissociation-enhanced enzyme linked fluorescence immunoassay). TRF is also useful in some assay variants of TR-FRET (Time-Resolved Fluorescence Resonance Energy Transfer) in which the FRET acceptor label acts as a quencher only and does not emit fluorescence. The proximity between donor label and acceptor (quencher) is then quantified by the intensity decrease of the donor label.

DELFIA requires washing steps as in an ELISA, but the TR-FRET assay involving quenching is a homogeneous plate assay technique and requires only mixing and measuring—no wash steps are required. It can also be miniaturized, which makes it useful for high-throughput screening applications.

The Cisbio Bioassays HTRF® (Homogeneous Time-Resolved Fluorescence) technology is a proprietary Time-Resolved Fluorescence technology that overcomes many of the drawbacks of standard Fluorescence Resonance Energy Transfer (FRET) techniques, such as the requirements to correct for autofluorescence and the fluorescent contributions of unbound fluorophores. See HTRF Read Mode on page 300.

For information about setting up a Time-Resolved Fluorescence mode protocol, see Creating Time-Resolved Fluorescence Mode Protocols on page 169.

### Time-Resolved Fluorescence Instruments and Detection Cartridges

The following instruments have time-resolved fluorescence read mode capability:

![](<../../../.gitbook/assets/3 (21).png>) SpectraMax iD5 Multi-Mode Microplate Reader on page 320 (supports the Enhanced TRF module for enhanced capability)

![](<../../../.gitbook/assets/4 (18).png>) SpectraMax i3x and SpectraMax i3 Multi-Mode Detection Platforms, see page 323 (requires detection cartridges)

![](<../../../.gitbook/assets/5 (19).png>) SpectraMax Paradigm Multi-Mode Microplate Reader, see page 327 (requires detection cartridges)

![](<../../../.gitbook/assets/6 (19).png>) SpectraMax M5 and SpectraMax M5e Multi-Mode Microplate Readers, see page 330 ![](<../../../.gitbook/assets/7 (19).png>) SpectraMax M4 Multi-Mode Microplate Reader, see page 331

![](<../../../.gitbook/assets/8 (18).png>) SpectraMax M2 and SpectraMax M2e Multi-Mode Microplate Readers, see page 333 ![](<../../../.gitbook/assets/9 (14).png>) Gemini XPS Microplate Reader, see page 334

![](<../../../.gitbook/assets/10 (12).png>) Gemini EM Microplate Reader, see page 334

![](<../../../.gitbook/assets/11 (14).png>) FlexStation 3 Multi-Mode Microplate Reader, see page 335 ![](<../../../.gitbook/assets/12 (13).png>) FilterMax F5 Multi-Mode Microplate Reader, see page 335

The following detection cartridges have time-resolved fluorescence read mode capability: ![](<../../../.gitbook/assets/13 (12).png>) Tunable Wavelength (TUNE) Detection Cartridge, see page 345

![](<../../../.gitbook/assets/14 (12).png>) Multi-Mode (MULTI) Detection Cartridge, see page 346 ![](<../../../.gitbook/assets/15 (10).png>) Cisbio HTRF Detection Cartridge on page 346

![](<../../../.gitbook/assets/16 (8).png>) Time Resolved Fluorescence (TRF-EUSA) Detection Cartridge, see page 347

![](<../../../.gitbook/assets/17 (8).png>)

**Note:** For the SpectraMax i3x, you can use the detection cartridges for top reads only.

### Analyzing Time-Resolved Fluorescence Data

A time-resolved fluorescence (TRF) measurement includes a number of pulses. Each pulse consists of turning the light source on, then off (Excitation Time), pausing for a specified length of time (Measurement Delay), and measuring the fluorescence intensity of the sample for a specified length of time (Integration Time). The pulses are repeated several times, as specified in the protocol parameters.

### Blank Correction

Although background is significantly lower than with fluorescence intensity measurements, you should use blanks or assay controls.

A blank well contains everything used with the sample wells except the label and sample- specific compounds. Do not use an empty well for a blank.

The blank sample reveals the offset underlying each data sample. This offset does not carry information on the label and is generally subtracted before data reduction is done.

For optimal results, you should run replicates for all blanks, controls, and samples. In this case, the blank value that will be subtracted is the average value of all blanks.

### Data Normalization

TRF raw data changes in magnitude when the timing parameters are changed. However, TRF data are normalized for a number of 1000 pulses. This means that the sample raw data does not change when only the number of pulses is changed.

### Data Optimization

There are two timing parameters which can be optimized to adjust the performance of the measurement: time per well and integration time per cycle.

Measurement noise is dependent on the read time per sample (time per plate or time per well). The detection limit improves when the read time is increased. Therefore, it is important to specify the read time when you compare measurements. For TRF, the read time per well increases with the selected number of pulses. The time between pulses and the intensity of each pulse, however, can be different on various systems.

All low-light-level detection devices have some measurement noise in common. To average out the measurement noise, optimization of the time per well involves accumulating as many counts as possible. Within some range, you can reduce noise (CVs, detection limit) by increasing the read time per well, as far as is acceptable from throughput and sample stability considerations.

To further optimize measurement results, optimize the timing parameters. Use the following table and figure as guidelines for the selection of timing parameters.

**Time-Resolved Fluorescence Timing Parameters Example**

| **Parameter**                      | **Value** | **Comment**                                                                                                                                                                                       |
| ---------------------------------- | --------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Pulse length                       | 0.100 ms  | <p>The period for excitation of the sample, shown as t1 in the following figure.</p><p>This is the suggested value for the TUNE, MULTI, and TRF detection cartridges.</p>                         |
| Measurement delay                  | 0.010 ms  | <p>The delay to ensure the excitation pulse is no longer detectable, shown as t2 in the following figure.</p><p>This is the suggested value for the TUNE, MULTI and TRF detection cartridges.</p> |
| Integration time per cycle (pulse) | 0.890 ms  | <p>The period for accumulating the signal, shown as t3 in the following figure.</p><p>This is the suggested value for the TUNE and MULTI detection cartridges.</p>                                |
| Integration time per cycle (pulse) | 1.890 ms  | <p>The period for accumulating the signal, shown as t3 in the following figure.</p><p>This is the suggested value for the TRF detection cartridge.</p>                                            |
| Total cycle time                   |           | The total cycle time is shown as t4 in the following figure.                                                                                                                                      |

t 4

t 1

t

2

t 3

**Timing Parameters For Time-Resolved Fluorescence**

When neglecting the time delay t2 compared to the integration time window t3, the accumulated signal _A_ can be approximated with the following equation:

A / Amax = (1 - exp(-M)) x 100%

In the equation above, _M_ is the size of the time window (or integration time) divided by the exponential decay time constant (or the fluorescence lifetime of the label).

M = (integration time) / (fluorescence lifetime)

For example, using Europium, which has a fluorescence lifetime of 700 µs, and the suggested integration time per cycle of 1.890 ms (or 1890 µs), M = 1890 / 700 = 2.7. Inserting this value of _M_ into the first equation yields A / Amax = 93%.

To optimize the integration time per cycle (pulse), the integration time should be set such that the value of _M_ produces the desired signal. For example, to get more than 86% signal, select an integration time such that M is greater than 2.0. Using the previous Europium example and solving for the integration time, the integration time can be set to _M_ (2.0) times the fluorescence lifetime (700 µs), or 1400 µs (1.4 ms).

**Achievable Accumulated Signal Percentage Compared to M**

|              |      |      |      |      |      |      |      |      |
| ------------ | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- |
| M            | 0.25 | 0.50 | 0.75 | 1.00 | 1.25 | 1.50 | 2.00 | 3.00 |
| A / Amax\[%] | 22   | 39   | 53   | 63   | 71   | 78   | 86   | 95   |

M can be technically limited by the time between pulses. Further gain in signal above some value of M can be negligible to improve results.

When you do a dual-label Europium-Samarium measurement, there are more timing parameters. There is some residual cross-talk of the Samarium signal captured in the Europium emission channel. Samarium has a much shorter fluorescence lifetime. To reduce the cross-talk of Samarium in the Europium channel, Europium is measured in a time window shifted away from the time window for Samarium. This lets the Europium be quantified without cross contamination from the Samarium. The known Europium concentration can be used to remove the Europium cross-contamination in the Samarium channel.

**TRF Suggested Timing Parameters: Dual Label Europium-Samarium**

| **Parameter**                     | **Value** | **Comment**                                                                                                                                |
| --------------------------------- | --------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| Pulse length                      | 0.100 ms  | <p>The time interval for flash monitoring</p><p>This is the suggested value for the TRF detection cartridge.</p>                           |
| Measurement delay (first window)  | 0.010 ms  | <p>The delay to ensure the excitation pulse is no longer detectable</p><p>This is the suggested value for the TRF detection cartridge.</p> |
| Integration time (first window)   | 0.100 ms  | The period for accumulating the Samarium signal This is the suggested value for the TRF detection cartridge.                               |
| Measurement delay (second window) | 0.140 ms  | <p>The read out of the Samarium signal</p><p>This is the suggested value for the TRF detection cartridge.</p>                              |
| Integration time (second window)  | 0.750 ms  | The period for accumulating the Europium signal This is the suggested value for the TRF detection cartridge.                               |
