# Pipetting Steps

## Liquid Level Detection

Used to minimize amount of liquid on outside of tips

* Capacitive Liquid Level Detection  (cLLD)  used to detect    fluids that are polar or ionic (dielectric constant > 8) during either aspiration or dispense with either wet or dry tips
* Pressure Liquid Level Detection (pLLD) use to detect all types of fluids only during aspiration and _with dry tips_&#x20;
* Channels:  Independent LLD,  cLLD or pLLD or both \*\*
  * \*\* Use both to detect excessive foaming by setting a maximum height difference between cLLD and pLLD
* 96 Head: cLLD on A1, B2, G11, and H12 only\


**Minimum Detectible Volume** that is detectable depends on the container type, size, and geometry, as well as fluid type (**Dead Volume**)

<table><thead><tr><th width="330">Labware</th><th width="144">cLLD Vmin/μl</th><th>Carrier</th></tr></thead><tbody><tr><td>Tubes, 16 mm x 100 mm</td><td>200</td><td>SMP_CAR_24</td></tr><tr><td>Tubes, 12 mm x 75 mm</td><td>150</td><td>SMP_CAR_32</td></tr><tr><td>Eppendorf tubes 1.5 ml</td><td>50</td><td>SMP_CAR_32_EPIL</td></tr><tr><td>Eppendorf tubes 0.5 ml</td><td>50</td><td>SMP_CAR_32_EPIS</td></tr><tr><td>96-well PCR plate</td><td>50</td><td>PLT_CAR_L5PCR</td></tr><tr><td>96-well flat-bottom microplate</td><td>75</td><td>PLT_CAR_L5MD</td></tr><tr><td>384-well flat-bottom microplate</td><td>50</td><td>PLT_CAR_L5MD</td></tr><tr><td>96-deepwell microplate (archive)</td><td>150</td><td>PLT_CAR_L5AC</td></tr></tbody></table>

&#x20;

## Aspirate

Draws up fluid from a defined position into a tip or needle

{% tabs %}
{% tab title="Aspiration Modes" %}
| <ul><li><strong>Aspiration</strong> (default) (0) Blow-out air aspirated while the tips are still in the air and used at the end of the dispense to blow the liquid out of the tip</li><li><strong>Consecutive aspiration</strong> (1) Respects a previous aspiration - will not aspirate blowout air again (this is never the 1st aspiration)</li><li><strong>Aspirate all</strong> (2) Volume to be aspirated is larger than what is expected within the container - Tip will follow the falling liquid level (if specified) to the bottom of the container then stay there till requested volume is aspirated - MAD is deactivated so an error is not triggered when not enough liquid</li></ul> | <p></p><p><img src="../../.gitbook/assets/image (49) (1) (1).png" alt="" data-size="original"></p> |
| --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- |
{% endtab %}

{% tab title="Aspiration Positions" %}


<figure><img src="../../.gitbook/assets/image (63) (1) (1).png" alt=""><figcaption></figcaption></figure>

* **Fixed Height:** Liquid surface height known in advance
* **Capacitive LLD:** For conductive liquids
* **Pressure LLD:** For non-conductive liquids or Labware
* **Submerge Depth:** Pipetting depth (mm) below detected liquid surface
* **Max height difference \[mm]:** Active when both cLLD and pLLD are selected. If calculated difference during pipetting step is greater than this value then step returns an error. Used for foam thickness detection
{% endtab %}

{% tab title="Mixing" %}
Mixing is located under the Advanced button in the Aspirate and Dispense steps

| <img src="../../.gitbook/assets/image (69) (1) (1).png" alt="" data-size="original"> | <p></p><p><strong>Liquid following during aspirate and mix:</strong> Tips fall and rise with the liquid level<br><br>Pre-rinsing/Mix settings:</p><ul><li><strong>Cycles:</strong> Number of mixing cycles</li><li><strong>Mix position [mm]:</strong> Immersion depth from the set aspirate/dispense depth.</li><li><strong>Volume [µl]:</strong> Mixing volume (generally half of the volume in the container)</li></ul> |
| ------------------------------------------------------------------------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
{% endtab %}
{% endtabs %}

Aspirate parameters are directly related to the Dispense mode – and both are a function of the Liquid Class that is being selected

## Dispense

Dispenses fluid from the tip or needle (partial or complete volume) into a defined position &#x20;

{% tabs %}
{% tab title="Dispense Modes" %}
| <img src="../../.gitbook/assets/image (50) (1) (1).png" alt="" data-size="original"> | <p></p><ul><li><p>Jet dispense: tip stays above surface</p><div><figure><img src="../../.gitbook/assets/image (62) (1) (1).png" alt="" width="26"><figcaption></figcaption></figure></div></li></ul><ul><li>Jet empty tip: Tip emptied of all liquid using blow-out air</li><li>Jet part volume: Only part of volume within tip is dispensed<br><br></li></ul><ul><li><p>Surface dispense: tips go below the liquid surface, recommended for volumes &#x3C; 20 uL</p><div><figure><img src="../../.gitbook/assets/image (58) (1) (1).png" alt="" width="26"><figcaption></figcaption></figure></div></li><li>Surface empty tip: Tip emptied of all liquid</li><li>Surface part volume: Only part of volume within tip is dispensed</li></ul> |
| ------------------------------------------------------------------------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
{% endtab %}

{% tab title="Dispense Positions" %}


| <img src="../../.gitbook/assets/image (67) (1) (1).png" alt="" data-size="original"> | <p></p><ul><li>Fixed height from bottom: dispense position relative to the container bottom</li><li>Side touch: dispense at the container wall. Positioning of tip is defined within the Labware's container definition</li><li>Capacitive LLD: For conductive liquids</li><li>Submerge depth [mm]: immersion depth below the detected liquid level</li><li>Touch off: used to dispense volumes &#x3C; 5µl into dry wells – Note: Dispenses at the physical bottom or the Max Pipetting Depth as defined in the Labware definition</li><li>Dispense position above touch [mm]: distance the channels will move up after touching container bottom before dispensing</li></ul> |
| ------------------------------------------------------------------------------------ | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
{% endtab %}

{% tab title="Multi-Dispensing" %}
| <img src="../../.gitbook/assets/image (71) (1) (1).png" alt="" data-size="original"> | <ul><li>If <strong>normal</strong> is selected, the Z positions are set to the maximal traverse height.</li><li>If minimized is selected, the Z positions are set to the minimal traverse height of the Labware.<br></li></ul><p>Important: Make sure there isn’t any taller labware placed in between the dispense locations. Higher labware may lead to collisions with the used channels.</p> |
| ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
{% endtab %}
{% endtabs %}

## Channel Options



{% tabs %}
{% tab title="Individual volumes" %}
<table data-header-hidden><thead><tr><th width="194"></th><th></th></tr></thead><tbody><tr><td><img src="../../.gitbook/assets/image (72) (1) (1).png" alt="" data-size="original"></td><td>Defines individual pipetting volumes for each channel for the Aspirate step and the Dispense step</td></tr><tr><td><strong>Volume [µl] :</strong> Enter the individual volume or select a variable representing the volume<br><br><strong>Add / Change >></strong>: Press this button to add or change the volume of the selected channel to the value in the Volume [uL] field.</td><td><img src="../../.gitbook/assets/image (73) (1) (1).png" alt="" data-size="original"></td></tr></tbody></table>


{% endtab %}

{% tab title="Channel selection" %}


<figure><img src="../../.gitbook/assets/image (78) (1) (1).png" alt=""><figcaption></figcaption></figure>



| <img src="../../.gitbook/assets/image (74) (1) (1).png" alt="" data-size="original">                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     | Defines which channels will be in operation during the pipetting step.               |
| ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------ |
| <p><strong>Channel selection:</strong> All deselected channels will be excluded from this step<br></p><p><strong>Channel selection as variable:</strong></p><p>Channel variable: A string specifying the channels to be used (0=unused, 1=used) (e.g. “10101010” – only odd channels used)<br><br><img src="../../.gitbook/assets/image (76) (1) (1).png" alt="" data-size="original"><br><br><strong>Channel Use</strong><br><strong>(1) All sequence positions:</strong> remaining channels are used to process all sequence positions. </p><p><strong>(2) Channel pattern:</strong> sequence positions corresponding to deactivated channels are not processed but are “consumed”</p> | <img src="../../.gitbook/assets/image (75) (1) (1).png" alt="" data-size="original"> |



<figure><img src="../../.gitbook/assets/image (79) (1) (1).png" alt=""><figcaption></figcaption></figure>
{% endtab %}
{% endtabs %}
