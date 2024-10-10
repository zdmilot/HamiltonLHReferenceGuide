# Monitored Air Displacement (MAD)‌

The ML STAR is equipped with an aspiration monitoring feature. During the aspiration process, the pressure within the pipetting channel is measured in real time. Analyzing the shape of the p(t) curve, the system can distinguish the following situations:

* A correct aspiration takes place
* Air is aspirated into the tip (because, for example, the container has not been filled properly)
* A clot blocks the tip

<table data-header-hidden><thead><tr><th width="145"></th><th></th></tr></thead><tbody><tr><td><img src="../../../../../.gitbook/assets/image (10) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" data-size="original"></td><td><p>NOTE</p><p>MAD is available on the 1000μl-pipetting channels and the 5ml-pipetting channels.</p></td></tr></tbody></table>

The aspiration monitoring can be switched on and off for each individual aspiration step of a method using the steps from “HLSMl\_StarLib.hsl”. For pressure-based clot detection, a threshold can be given in arbitrary A/D (analog/digital) values (typically 100 A/D values). The range of A/D values of the pressure sensor is from around 800 (at ambient pressure) to <10 A/D values for 18 mbar below ambient pressure. For comparison, the hydrostatic pressure of 100µl of water in our standard tip is around 2 mbar.

The following diagram shows the principle of aspiration monitoring based on pressure.

<figure><img src="../../../../../.gitbook/assets/image (61) (1).png" alt="" width="321"><figcaption></figcaption></figure>

<table data-header-hidden><thead><tr><th width="145"></th><th></th></tr></thead><tbody><tr><td><img src="../../../../../.gitbook/assets/image (10) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" data-size="original"></td><td><p>NOTE</p><ul><li>Pressure-based monitoring works with unused as well as used disposable tips and needles.</li><li>If multiple Aspirate/Dispense cycles are executed within a loop, make sure that the (last) dispense step uses the Pipetting mode ‘Drain tip’.</li><li>The volume range for the MAD depends on the specific assay. The lower limit in many cases is an aspiration volume of 50µl.</li><li>Pressure-based monitoring has been optimized for liquid solutions only.</li></ul></td></tr></tbody></table>
