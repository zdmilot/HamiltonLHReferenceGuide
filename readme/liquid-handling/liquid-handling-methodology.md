# Liquid Handling Methodology

<figure><img src="../../.gitbook/assets/image (6) (1) (1).png" alt=""><figcaption></figcaption></figure>



## Step 1: Understand Properties of a Liquid

Liquid Properties to Consider:\


<details>

<summary>Density</summary>

The volumetric mass density of a substance is its mass per unit volume. It gives an impression if a material is heavy or light. The density of a material varies with temperature and pressure.

The density of different liquids is shown below to visualize the range (in kg/m3)\


<img src="../../.gitbook/assets/image (7) (1) (1).png" alt="" data-size="original">![](<../../.gitbook/assets/image (8) (1) (1).png>)



</details>

<details>

<summary>Viscosity</summary>

* Describes the flow behavior of a liquid&#x20;
* The more viscous a liquid, the thicker and less fluid the liquid

![](<../../.gitbook/assets/image (3) (1) (1) (1).png>)

</details>

<details>

<summary>Adhesion + Cohesion + Capillary</summary>

* The state of the interface between two materials is defined by the adhesion&#x20;
* In contrast to adhesion, the cohesion is based on binding forces within the same substance.&#x20;
* Capillary action is due to the pressure of cohesion and adhesion which cause the liquid to work against gravity

![](<../../.gitbook/assets/image (28) (1) (1).png>)

</details>

<details>

<summary>Vapor Pressure</summary>

* The pressure exhibited by vapor present above a liquid surface is known as vapor pressure&#x20;
* The equilibrium vapor pressure is an indication of a liquid's evaporation rate&#x20;
* A substance with a high vapor pressure at normal temperatures is referred to as volatile.&#x20;
* An increase in temperature increases the number of molecules coming into the vapor phase, thus increasing the vapor pressure.

![](<../../.gitbook/assets/image (29) (1) (1).png>)

</details>

<details>

<summary>Environmental Influences</summary>

* Humidity - Influences vapor saturation (rate of evaporation)
* Pressure - Influences the vapor pressure curve (rate of evaporation)
* Radiation - Alters the properties of substances
* Temperature - Influences vapor saturation, pressure curve, and density
* Vibrations- Supports drop formation

</details>



## Step 2/Step 3: Selecting and verifying a Liquid Class

### Start with Pre-defined Liquid Classes

1. Water (aqueous solutions)
2. EtOH (volatile organic solvents)
3. DMSO (non-volatile organic solvents)
4. 80% Glycerine (viscous liquids)
5. Serum (blood products)

### Establish Method Settings

<details>

<summary>Liquid Level Detection (LLD)</summary>

Prevent aspiration of air, excessive carryover when used in conjunction with submerge depth and can return height of found liquid and determine estimated volume. The different liquid level detection modes are:

* cLLD – capacitive liquid level detection for conductive liquids\
  ![](blob:https://app.gitbook.com/4fc66e3d-7bc1-4a12-b54d-e8d2d3af9994)
* pLLD – pressure liquid level detection for all types of liquids\
  ![](blob:https://app.gitbook.com/f7d1d4ba-a01a-4a22-9ff4-a01488bcf935)

</details>

<details>

<summary>Fixed height</summary>

* If the volume is too low, LLD may not work reliably and fixed height must be used&#x20;
* Fixed height helps to minimize dead volume and improve speed
* Enable additional functions to further optimize the liquid transfer\
  ![](<../../.gitbook/assets/image (31) (1) (1).png>)
  * Touch off helps ensure consistent aspirate or dispense height from the bottom of the labware
  * Side touch helps ensure proper dispense of liquids that have residual droplets or foam

</details>

<details>

<summary>Anti-Droplet Control (ADC)</summary>

·      ![](blob:https://app.gitbook.com/c76cd4f6-8283-4feb-8ee2-34498121ca3c)

* Enables pipetting of volatile liquids without dripping
* After aspiration, pressure is monitored for any increase
* Plunger increments up in order to equalize pressure and prevent droplets
* Important Settings for ADC
  * Set air transport volume close to zero
  * Set stop back volume lower than 10μL
  * Set a low swap speed (2 mm/s)
* ADC can be triggered maximally 25 times. Improper settings result in an unstable internal pressure right after aspiration. This pressure alterations trigger ADC uncontrolled over 25 times leading to an error.

</details>

### Choosing the Liquid Class Despense Mode

<div>

<figure><img src="../../.gitbook/assets/image (36) (1).png" alt="" width="375"><figcaption></figcaption></figure>

 

<figure><img src="../../.gitbook/assets/image (47) (1).png" alt="" width="226"><figcaption></figcaption></figure>

</div>

* Aspiration and dispense steps have different modes
* The mode determines which liquid class parameters are active
* Liquid classes are defined per each dispense mode&#x20;
* Usually, one aspiration/dispense cycle uses only one liquid class

<details>

<summary>Aspiration Modes</summary>

* Aspiration (default) (0)\
  Blow-Out Air is aspirated while the tips are above Liquid Level and is then used post-dispense to dispense the remaining liquid from the tip. &#x20;
* Consecutive aspiration (1) \[Cannot be 1st Aspiration]\
  Allows for an additional aspiration to follow up a previous one by not aspirating Blow-Out Air again.
* Aspirate all (2)\
  Used when the aspiration volume is greater than calculated container volume.  The tip will follow the liquid level (if enabled) to the container bottom and remain there until requested volume is aspirated - MAD is deactivated so as to avoid Liquid Level detection errors. &#x20;

</details>

<details>

<summary>Dispense Modes</summary>

* Use Surface Empty Mode when:
  * Optimal performance is required
  * Pipetting low volumes
  * Mixing is required during the dispense step
* Use Jet Empty Mode when:
  * Pipetting higher volumes into empty containers
  * Re-using tips and cannot touch liquid already present
* Use Jet Part Mode when:
  * Multi-dispensing is required into empty containers or when the tips cannot touch liquid already present
* Use Surface Part Mode when:
  * Multi-dispensing is required into liquid filled containers and re-use of tips is acceptable

</details>

### Other Parameters

<table><thead><tr><th>Parameter</th><th data-type="checkbox">Aspirate Parameters</th><th data-type="checkbox">Dispense Parameters</th></tr></thead><tbody><tr><td>Flow Rate</td><td>true</td><td>true</td></tr><tr><td> Mix Flow Rate</td><td>true</td><td>true</td></tr><tr><td>Air Transport Volume </td><td>true</td><td>true</td></tr><tr><td>Blowout Volume </td><td>true</td><td>true</td></tr><tr><td>Swap Speed </td><td>true</td><td>true</td></tr><tr><td>Settling Time </td><td>true</td><td>true</td></tr><tr><td>Over-Aspirate Volume </td><td>true</td><td>false</td></tr><tr><td>Clot Retract Height</td><td>true</td><td>false</td></tr><tr><td>Stop Flow Rate</td><td>false</td><td>true</td></tr><tr><td>Stop Back Volume</td><td>false</td><td>true</td></tr></tbody></table>



<details>

<summary>Flow Rate and Mix Flow Rate</summary>

* Liquid flow rates in μL/s, correspond to plunger speed for aspiration, dispense, and mixing
*   Influenced by tip geometry, liquid viscosity, density, and vapor pressure

    <figure><img src="../../.gitbook/assets/image (10) (1) (1).png" alt="" width="18"><figcaption></figcaption></figure>

<!---->

* Aspiration
  * Slower for smaller tip diameters
  * Faster for more volatile liquids
  * Slower for more viscous liquids
* Dispense
  * Slower for smaller tip diameters
  * Slower for surface dispense
  * Faster for jet dispense
  * Faster for more volatile liquids
  * Slower for more viscous liquids

</details>

<details>

<summary>Air Transport Volume</summary>

* Volume of air in μL is aspirated at the end of the aspiration and dispense step and is automatically dispensed again as an extra volume at the beginning of the dispense step
*   Influenced by tip geometry and liquid vapor pressure\


    <figure><img src="../../.gitbook/assets/image (12) (1) (1).png" alt="" width="49"><figcaption></figcaption></figure>
* Helps prevent droplet formation
* Recommend the following:
  * Use larger volume for volatile liquids
  * Use smaller volume for smaller tips
  * Set air volume to be less than liquid volume
  * Do not use excessive volume as leaks could be created

</details>

<details>

<summary>Blowout Volume</summary>

* Volume of air in μL that is aspirated first during the aspiration step. If dispensing in empty tip mode, part or all of the air is dispensed.
*   Influenced by liquid viscosity and liquid vapour pressure\


    <figure><img src="../../.gitbook/assets/image (13) (1) (1).png" alt="" width="51"><figcaption></figcaption></figure>
* Set larger for more viscous liquids
* Aspiration
  * Set equal to or greater than the blowout volume set for the dispense
  * Set higher than that set for the dispense when pipetting volatile liquids&#x20;
* Dispense
  * May create bubbles/foam in liquid if used in surface mode
  * Could cause aerosols in jet mode

</details>

<details>

<summary>Swap Speed</summary>

*   Speed in mm/s at which the pipette head is moved out of the liquid after aspiration and dispense.\


    <figure><img src="../../.gitbook/assets/image (14) (1) (1).png" alt="" width="40"><figcaption></figcaption></figure>
* Influenced by liquid viscosity and liquid vapour pressure
* Set slower for more viscous fluids
* Set faster for more volatile fluids

</details>

<details>

<summary>Settling Time</summary>

### Settling Time

*   Time in seconds that the pipette head remains in the liquid after the aspiration and dispense step before moving out of the liquid\


    <figure><img src="../../.gitbook/assets/image (15) (1) (1).png" alt="" width="54"><figcaption></figcaption></figure>
* Influenced by tip geometry and liquid viscosity
* Set shorter for aqueous solutions
* Set very short for highly volatile solutions
* Set longer for viscous solutions
* Set longer for surface dispense into empty containers

</details>

<details>

<summary>Over-aspirate Volume</summary>

*   A pre-wetting volume in μL. After aspirating the required volume an additional volume is aspirated and dispensed again immediately.\


    <figure><img src="../../.gitbook/assets/image (16) (1) (1).png" alt="" width="64"><figcaption></figcaption></figure>
* Influenced by liquid viscosity and vapor pressure
* Can help minimize capillary effect
* Useful at low volumes
* Set lower than the aspirate volume
* Set higher for viscous or volatile liquids
* Set to zero for dilution steps

</details>

<details>

<summary>Clot Retract Height</summary>

*   A parameter for clot detection which determines how high the pipette head is allowed to move out of the liquid while there is still a liquid detection signal after aspiration.\


    <figure><img src="../../.gitbook/assets/image (17) (1) (1).png" alt="" width="45"><figcaption></figcaption></figure>
* It is measured from the liquid surface upwards. If this distance is exceeded, an error message is generated.
* Doesn’t affect liquid transfers
* Only used to help detect clots after aspiration

</details>

<details>

<summary>Stop Flow Rate</summary>

### Stop Flow Rate

* Dispense flow rate in μL/s in at which the dispense step terminates abruptly
*   Influenced by liquid viscosity\


    <figure><img src="../../.gitbook/assets/image (18) (1) (1).png" alt="" width="93"><figcaption></figcaption></figure>
* Set equal to or less than Dispense flow rate
* Set slower for surface dispense and smaller relative to the dispense flow rate
* Set faster for jet dispense and generally equal to dispense flow rate, especially when multi- dispensing

</details>

<details>

<summary>Stop Back Volume</summary>

*   Volume in μL which is aspirated again immediately after the dispense. This volume is aspirated as quickly as possible.\


    <figure><img src="../../.gitbook/assets/image (20) (1) (1).png" alt="" width="63"><figcaption></figcaption></figure>
* Influenced by liquid viscosity
* Helps prevent droplets after dispense in jet part volume mode (setting only valid for jet part volume mode)
  * Acts as an air transport volume in between transfers when using jet part volume mode
* Pay attention to dispense height if using this setting. If set too low, volume of dispensed liquid could be aspirated inadvertently.
* Set higher for more viscous liquids

</details>



### Active Parameters

The settings of the liquid class are only active if supported by the aspiration and dispense modes. The next two tables provide an overview of the combinations that are possible given the selected mode.

#### Enabled Liquid Class Settings per Aspirate Mode

<figure><img src="../../.gitbook/assets/image (21) (1) (1).png" alt=""><figcaption></figcaption></figure>

#### Enabled Liquid Class Settings per Dispense Mode 

<figure><img src="../../.gitbook/assets/image (22) (1) (1).png" alt=""><figcaption></figcaption></figure>

## Step 4: Optimizing Parameters/Method Settings

Adjustment of Correction Curve

<div>

<figure><img src="../../.gitbook/assets/image (25) (1) (1).png" alt=""><figcaption></figcaption></figure>

 

<figure><img src="../../.gitbook/assets/image (24) (1) (1).png" alt="" width="285"><figcaption></figcaption></figure>

</div>

* The liquid class correction curve affects the trueness
* Any target volume can have a corrected volume
* Including more points on the curve ensures truer volume transfers across a larger dynamic range
* Software interprets the correction curve by linear regression

<div>

<figure><img src="../../.gitbook/assets/image (26) (1) (1).png" alt=""><figcaption></figcaption></figure>

 

<figure><img src="../../.gitbook/assets/image (27) (1) (1).png" alt=""><figcaption></figcaption></figure>

</div>

