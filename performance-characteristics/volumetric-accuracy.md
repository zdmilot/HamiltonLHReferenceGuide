# Volumetric Accuracy

Volumetric accuracy refers to the ability of a liquid handling device to deliver the intended volume of a liquid, with minimal deviation from the target volume. it is a key performance metric that assesses the overall reliability and consistency of the liquid handling system.

![graphic showing liquid vapor and the effect of pressure on pipetting](https://assets-robotics.hamiltoncompany.com/File-Uploads/\_thumbnail/ADP-01.jpg?v=1717441271)

### The Physics of Pipetting a Liquid

This page is part of the comprehensive Hamilton [Automated Liquid Handling Guide](https://www.hamiltoncompany.com/automated-liquid-handling/everything-you-need-to-know-about-liquid-handling).

When pipetting volatile liquids like isopropanol, acetone, ethanol, and chloroform, it is common to experience dripping of liquid from the pipette tip. Air Displacement Pipetting ([link](https://www.labmanager.com/how-it-works/2017/06/how-positive-displacement-pipettes-work)) requires a vacuum pressure in the tip above the liquid column to hold the liquid in the tip. When a vacuum is applied to volatile liquids they vaporize which increases the pressure in the pipette tip. The increased pressure pushes fluid out of the tip.

**Common techniques for avoiding drips and improving pipetting accuracy include:**

* Reverse Pipetting
* Pre-wetting the tip
* Anti-Droplet Control

### Reverse Pipetting Volatile Liquids

Typical pipetting involves aspirating an air gap and then aspirating the solution. The solution is then dispensed and the air gap is used to force (or blow out) the last droplets of liquid from the pipette tip. However, for volatile solutions this procedure can be reversed by overaspirating the liquid and then dispensing the precise volume with no blow out. This technique leaves some excess liquid in the pipette tip so the dispense volume is not impacted by minimal dripping during transfer. The negative aspect of reverse pipetting is that the liquid can still drip onto the work surface.

### Pre-wet the Tip to Improve Pipetting Accuracy with Volatile Liquids

Prewetting the pipette tip involves aspirating and dispensing the liquid several times prior to attempting to transfer a precise volume. Prewetting saturates the air inside the pipette tip with vapors from the solution. Then when the sample is aspirated, the dripping is minimized because no additional vapors are forming so the pressure above the liquid column stays constant. One consideration with pre-wetting is that it does increase the time that it takes to complete each liquid transfer.

### Anti-Droplet Control for Automated Transfers of Volatile Liquids

Pipette channels equipped with [Anti-Droplet Control (ADC)](https://www.hamiltoncompany.com/anti-droplet-control-adc) monitor the pressure in the pipette tip above the liquid column. After aspiration, ADC maintains a constant pressure by retracting the plunger as the pressure builds in the pipette tip. This prevents the formation of a droplet and ensures accurate pipetting with volatile liquids.
