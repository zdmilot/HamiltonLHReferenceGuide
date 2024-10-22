# Case Study – Non homogenous (clotted) Samples

{% embed url="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FSJm30951AW7z9xuqm5sS%2Fuploads%2FhTdgtbl05Colhp74WsCc%2FMedia1.mp4?alt=media&token=1683df84-17ef-4985-aa3d-fc04a03c6408" %}



| The RED/LEFT sample has ben artificially clotted with gelling crystals. | The BLUE/RIGHT sample is water only. |
| ----------------------------------------------------------------------- | ------------------------------------ |

pLLD is being used for LLD (Clear Tip) – error handling has been enabled



## Capacitance –Based Clot Detection

Requirements:

* Liquid class with a clot retract height greater than 0mm (2-5mm typical)
* Clot Detection Monitoring turned on/off bracketing the aspirate step (HSLML\_STAR Library)
* Aspirate using conductive channels and cLLD
* Works by checking for a cLLD signal after withdrawing from the liquid – if a conductive path is present, a clot is confirmed

Benefits:

* independent from any system settings or atmospheric pressure

Risks:&#x20;

* Labware definition errors + insufficient retract could leave the tip still in the liquid, yielding false positives
* Clots smaller than the retract height could caus false negatives

<div>

<figure><img src="../../.gitbook/assets/image (96).png" alt=""><figcaption></figcaption></figure>

 

<figure><img src="../../.gitbook/assets/image (95).png" alt="" width="201"><figcaption></figcaption></figure>

</div>

## Monitored Air Displacement

Requirements

* Aspiration Monitoring turned on/off bracketing the aspirate step (HSLML\_STAR Library)
* Minimum aspirate volume of \~50uL
* Works by checking for the initial pressure in a channel prior to the aspirate, and the pressure at the end.  An excessive negative change indicates a clot is present.

Benefits

* independent from any system settings or liquid class, sensitivity (thresholds) can be adjusted

&#x20;![](<../../.gitbook/assets/image (98).png>)

Risks:

* Pressure Data is temporary, sensitive to liquid remaining in the tip when pipetting in cycles&#x20;

<div>

<figure><img src="../../.gitbook/assets/image (100).png" alt=""><figcaption></figcaption></figure>

 

<figure><img src="../../.gitbook/assets/image (99).png" alt=""><figcaption></figcaption></figure>

</div>

## &#x20;Total Aspiration and Dispense Monitoring (TADM)

Requirements

* TADM installed on the system, set to monitoring
* Liquid class in use with TADM enabled
* Example “good” data to build guard bands per volume in the LC
* Works by checking the current pressure during an Aspirate against the lower guard band.  If the pressure falls below the lower guardband, a clot is confirmed

Benefits

* Customizable to particular liquids, triggers when the clot is encountered, data visible at the end of the run

Risks

* Not conducive to variable volumes (guard bands are per volume)

&#x20;![](<../../.gitbook/assets/image (101).png>)



## Clot Error Responses

<div>

<figure><img src="../../.gitbook/assets/image (102).png" alt=""><figcaption></figcaption></figure>

 

<figure><img src="../../.gitbook/assets/image (103).png" alt=""><figcaption></figcaption></figure>

</div>

### TADM clarifies Error Responses

<div>

<figure><img src="../../.gitbook/assets/image (104).png" alt=""><figcaption></figcaption></figure>

 

<figure><img src="../../.gitbook/assets/image (105).png" alt=""><figcaption></figcaption></figure>

</div>

<table data-header-hidden><thead><tr><th width="260"></th><th></th></tr></thead><tbody><tr><td><img src="../../.gitbook/assets/image (106).png" alt="" data-size="original"></td><td><p>The Waste option will eject the tips, and whatever sample has been aspirated.</p><p></p><p>Subsequent dispense steps will also be affected, as no tips are present</p></td></tr><tr><td><p>The Exclude option will dispense back to source (like a repeat), but then drop the channels from the existing pattern!</p><p></p><p>As covered in Venus Basic, the All Sequence Positions default can interrupt the source:destination sequence correlation.</p><p></p><p>Changing the mode to Channel Pattern will maintain the correlation</p></td><td><img src="../../.gitbook/assets/image (107).png" alt="" data-size="original"></td></tr></tbody></table>

### Automated Error Handling

| <img src="../../.gitbook/assets/image (17) (1).png" alt="" data-size="original"> | <p>Also covered in Venus Basic, error handling behavior can be set such that no operator input is necessary.</p><p></p><p>Here, when a channel encounters a clot, the system waits 0 seconds for the operator to respond (visible options). It immediately excludes the channel.</p> |
| -------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |

### Dynamic Response to Excluded Samples

We can use Step Returns to analyze what happened in the run!

<figure><img src="../../.gitbook/assets/image (18) (1).png" alt=""><figcaption></figcaption></figure>

What do you want to know?

The Step Return Library, Array, and Sequence loops can tell us whatever we need to know!

|                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |                                                                                  |
| ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- |
| <p></p><p>Document erroneous Samples on Aspirate</p><ul><li>Extract a sequence based on all Major Error codes</li><li><p><em>Manual Recovery</em></p><ul><li>Put this sequence into a SmartStep:Load/Unload</li><li>Operator will be given a GUI indicating exactly which samples were problematic</li></ul></li><li><p><em>Automated Recovery</em></p><ul><li><p>Run a different Aspirate – </p><ul><li>Wide Bore tip, or larger volume tip</li><li>Virtual Labware shift – new aspirate off-center</li></ul></li></ul></li></ul> | <img src="../../.gitbook/assets/image (19) (1).png" alt="" data-size="original"> |
|                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |                                                                                  |
| <p>Document Successful Dispenses </p><ul><li>Extract a sequence based on clear errors + Step Data </li><li>Use this sequence for down stream processing, like reagent addition</li><li>Make an array of transferred volumes (Step Data)</li><li>Use this array to “blank” entries out of any matched arrays</li><li>OR, if using a shorter sequence, do a reverse-check and remove array positions for missing sequence positions</li></ul><p> </p>                                                                                | <img src="../../.gitbook/assets/image (20) (1).png" alt="" data-size="original"> |



<div>

<figure><img src="../../.gitbook/assets/image (21) (1).png" alt=""><figcaption></figcaption></figure>

 

<figure><img src="../../.gitbook/assets/image (22) (1).png" alt=""><figcaption></figcaption></figure>

</div>

&#x20;
