# Total Air Displacement Monitoring (TADM)

## **General information**

This chapter should be read thoroughly before applying the _Total Aspiration and Dispense Monitoring (TADM)_ feature. It contains important information about the use of TADM and this document.

All features described in this document are valid for TADM only. Refer to the corresponding manuals for programming and operating instruments controlled by the MICROLAB STAR Line Software.

The TADM feature 5.1 supports all pipetting channels such as the (old) 300μl channel, the 1000μl channel, the 5ml channel and the 96 CO-RE head TADM. The 384 CO-RE head does not have individual pressure sensors on each channel and does therefore not support TADM.

TADM (Total Aspiration and Dispense Monitoring) is a tool to increase the safety and the robustness of pipetting processes. A pressure sensor inside each individual pipetting channel constantly records the pressure in the system during aspiration and dispensing.

<figure><img src="../../.gitbook/assets/image (1).png" alt="" width="375"><figcaption><p><strong>Fig. 1: Air displacement system with pressure sensor for TADM</strong></p></figcaption></figure>

The software generates a pressure / time curve (See Fig. 2) that is different for each liquid (class) and each volume pipetted. The values obtained by the pressure sensor during a pipetting step (aspiration or dispensing) can be compared to user-defined values, which means real-time monitoring of the pipetting process.

Generally, TADM is best operated for volumes between 10μl and 1000μl on 1000μl channels (50μl - 5000μl on 5ml channels) when pipetting serum, plasma, or other water-based liquids. However, depending on the specific requirements of an application, other volumes and liquids may be used as well.

<figure><img src="../../.gitbook/assets/image (2).png" alt="" width="375"><figcaption><p><strong>Fig. 2: Pressure signal over time</strong></p></figcaption></figure>

Total Air Displacement Monitoring (TADM) monitors aspiration and dispense of a liquid in real time. The pressure sensor in the channel is used during both aspiration and dispense steps to detect errors, like clots, foam, and lack of liquid. Upper and lower tolerance bands can be established and monitored for exception.

TADM can be used in two different modes:

* **Recording mode:** The pressure inside the pipetting channel is recorded and stored.&#x20;
* **Monitoring mode:** The recorded pressure is compared to a user defined tolerance band in real time. If the measured value leaves the tolerance band, the plunger movement stops immediately and the software-dependent error handling is executed. In Monitoring mode, the recorded pressure curves will be stopped after last defined TADM tolerance band point.

## When to Use

TADM should be used if both aspiration and dispense monitoring is required. TADM is optimized for unused disposable tips during:

* Single aspirations and dispenses for volumes above 10 μL.&#x20;
* Multiple dispenses for individual aliquot volumes above 10 μL.
* Transfers of various liquid types. TADM is not limited to the use of aqueous solutions only.

It is possible to use TADM with used disposable tips and washable steel needles, but success with these tip types depends on the consistency of their generated pressure curves. Residual liquid from used tips and residual wash fluid from steel needles could cause some irregularity in the pressure curves, making it a challenge to set meaningful guardbands.&#x20;

TADM is especially useful for regulated environments and development purposes since a recording of every transfer step is made. The recording of the pressure profile allows the automated liquid handler’s operator to review and compare the pressure profiles of liquid transfers during and after a method run. The recordings can be helpful in troubleshooting if the profile is not stable or some transfers show atypical behavior.



## When Not to Use

* If the volume to pipette is less than 10 μL, TADM may not be able to be used for monitoring as the pressure profiles for low volumes may not be consistent.&#x20;
* If you need to determine the pipetted volume, TADM cannot determine the volume.&#x20;
* If you need to determine how much volume is missing from a sample, TADM cannot determine this volume.&#x20;
* If you need to make a statement on trueness and precision, TADM cannot confirm the precision of the transfer.&#x20;
* If variable volumes are transferred in the method, it may not be practical to create tolerance bands for every possible volume. The volumes could still be recorded, but not monitored for exception.

In the scenarios listed above, TADM doesn’t offer a benefit or might not even be possible to implement. A method using TADM should be tested for maximum repeatability and robustness to ensure proper transfers before putting TADM into regular use.



## How to Read an Aspiration TADM Curve

During aspiration, TADM monitors the pressure in the channel and reports it in a curve. The curve can be used to detect anomalies in the aspiration. Use the figure to read the different aspects of the TADM curve.

<figure><img src="../../.gitbook/assets/image (24) (1) (1) (1) (1).png" alt="" width="375"><figcaption></figcaption></figure>

## How to Read an Dispense TADM Curve

During dispensing, TADM monitors the pressure in the channel and reports it in a curve. The curve can be used to detect anomalies in the dispense. Use the figure to read the different aspects of the TADM curve.

<figure><img src="../../.gitbook/assets/image (25) (1) (1) (1) (1).png" alt="" width="375"><figcaption></figcaption></figure>

## Use TADM Guardbands

When collecting TADM curves, look for consistency in the pressure profiles for each volume transferred. If the profile for any individual transfer differs from the others, it indicates that a poor liquid transfer may have occurred. Once enough information is collected, you can set guardbands to actively monitor for any exception during runtime.&#x20;

In the example image below, the green lines are guardbands put in place to monitor aspirations. Any aspiration that results in a line within the guardbands executed as expected. An error occurs when aspiration crosses outside of the guardbands. User or automated error recovery steps could be enabled to address the error.

<figure><img src="../../.gitbook/assets/image (26) (1) (1) (1) (1).png" alt="" width="375"><figcaption></figcaption></figure>
