# Acoustic Drop Ejection (ADE)

ADE method is an entirely contactless method of dispensing liquids. placing the source of acoustics (sound energy) near the surface helps eject a small droplet of samples into the plate. the frequency of the sound determines the sample volume.

{% embed url="https://www.diamond.ac.uk/default/Instruments/Mx/XFEL-Hub/Sample-delivery-methods/ADE.html#part1" %}

**Acoustic Droplet Ejection (ADE) via an immersed focus transducer**

**Principle:** a sine wave amplified by a RF power amplifier will be sent to the transducer which will focus and emit an acoustic wave allowing a droplet ejection. The droplet size depends of the transducer frequency, in general we are working with droplet size ranging from 1 nl to 2.5 nl.

![Figure from Olympus. The transducer can focus the acoustic energy at the meniscus of the liquid and eject a droplet.](https://www.diamond.ac.uk/default/dam/jcr:43cfd9c9-babe-4a2a-9b48-581fe069e69f/Unfocused\_Focused\_transducers.2020-02-21-14-12-08.jpg)



**Applications:** Allen Orville and collaborators used this technique for first time to eject droplet containing crystals at synchrotron (BNL) and XFEL (LCLS). In the intial setup, the droplet was exposed to X-ray while flying through space. Later, the droplets were dispensed onto a kapton belt to bring them to the X-ray interaction region ([Roessler at _al._, J Synchrotron Radiat. 2013](https://www.ncbi.nlm.nih.gov/pubmed/23955046); [Roessler et _al._, Structure 2016](https://www.ncbi.nlm.nih.gov/pubmed/26996959)). This delivery system is on demand, meaning that a droplet is ejected only when an X-ray pulse at XFEL is generated. It is efficient and greatly reduces sample consumption compared to jet technique such as GDVN.    &#x20;

The latest iteration of the of the ADE on tape has been published in 2017 ([Fuller _et al._, Nat Methods. 2017](https://www.ncbi.nlm.nih.gov/pubmed/28250468)).

![Figure from Fuller et al., Nat Methods. 2017.](https://www.diamond.ac.uk/default/dam/jcr:563280e9-e155-4b6c-99ab-152dd5cff589/ADE\_LCLS.2020-02-21-14-12-08.png)

&#x20;In the interaction region, the belt was run at a small angle with respect to the z-axis (vertical) in the xz-plane (zoomed in view of interaction point). Positioning the droplet in the X-ray focus is accomplished by moving the entire system in the horizontal plane, while the droplet z-position (vertical) on the tape at the intersection is adjusted by changing the deposition delay. The belt is cleaned and dried _in situ_, enabling continuous use for days.

The ADE on tape has been succesfully used at XFEL for a large variety of sample such as photosystem II, phytochrome, or anaerobic enzymes ([Fuller _et al._, Nat Methods. 2017](https://www.ncbi.nlm.nih.gov/pubmed/28250468); Y[oung _et al._, Nature. 2016](https://www.ncbi.nlm.nih.gov/pubmed/27871088); [Kern _et al._, Nature. 2018](https://www.ncbi.nlm.nih.gov/pubmed/30405241)).

**Development:** The tape drive is actually used through our collaboration with [Yano/Yachandra lab](https://www2.lbl.gov/vkyachan/index.html) at Lawrence Berkeley National Laboratory. We are working on a system to reduce the footprint of the device and adapt it to MX beamlines and XFEL's instruments.

**Commercial liquid dispenser PolyPico**

**Principle:** [Polypico](https://www.polypico.com/) is a liquid dispenser. The liquid is first transfered to a cartridge before being loaded on the dispenser head. The cartridge has an aperture that will define the size of the droplet. The droplet volume ejected is ranging from about 30 pl to more than 100 pl. The drops can be ejected at a frequency of 10 kHz.&#x20;

The XFEL Hub acquired in 2017 a [PicoSpotter](https://www.polypico.com/products/picospotter/) to test crystal and buffer ejection via the cartridge with different aperture sizes (30um to 150um).

![](https://www.diamond.ac.uk/default/dam/jcr:5033661d-5b15-4b98-a2e4-350d9bf96e14/commercial\_PolyPico.2020-02-21-14-12-07.jpg)

&#x20;Movie of a drop ejection horizontally using a fast camera (50,000fps) at Diamond:

{% embed url="https://youtu.be/HUNdrAx48sk" %}



**Development:**

Thanks to a deep collaboration with PolyPico, we have now an externally triggered dispensing setup. We are able to eject droplets at a frequency of up to 33 kHz. We are working closely with the [European XFEL](https://www.xfel.eu/) to test PolyPico as a sample delivery method for the second interaction region in atmosphere of [SPB/SFX](https://www.xfel.eu/facility/instruments/spb\_sfx/index\_eng.html).

It is also possible to mount the dispenser on VMXi beamline to expose with X-rays the droplet containing crystals.

![](https://www.diamond.ac.uk/default/dam/jcr:22e41d6f-b1ff-4a52-90a4-1e62323ae103/Overall\_PolyPico\_VMXi.2020-02-21-14-12-07.jpg)
