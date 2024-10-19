# Wash Station 96/384‌

The Wash Station 96/384 is an optional device for washing 96/384 disposable tips in parallel. The tips are washed both outside and inside at the same time: on the outside in the wash chambers of the wash station and on the inside by aspiration/dispense cycles using the CO-RE 96 Probe Head / TADM or the CO-RE 384 Probe Head. The result of washing the tips depends on the wash setting.

<table data-header-hidden><thead><tr><th width="145"></th><th></th></tr></thead><tbody><tr><td><img src="../../.gitbook/assets/image (10) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" data-size="original"></td><td><p>NOTE</p><p><em>If carry-over is not acceptable for the application, use new disposable tips for each aspiration step.</em></p></td></tr></tbody></table>



Sample transfers can be done using new disposable tips, while reagents, buffers, etc. can be distributed with washed tips.

The picture below shows a complete, hooked-up wash station 96/384:\


<figure><img src="../../.gitbook/assets/image (95) (1).png" alt="" width="375"><figcaption></figcaption></figure>

Liquid level sensors inside the washer unit prevent flooding of the system. The washer unit recognizes if there is not enough liquid to fill the wash chamber.

<table data-header-hidden><thead><tr><th width="145"></th><th></th></tr></thead><tbody><tr><td><img src="../../.gitbook/assets/image (10) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" data-size="original"></td><td><p>NOTE</p><p><em>Always empty the waste container when refilling the wash solution container. When re-using washed tips, pipetting precision may increase by a factor of 3.</em></p></td></tr></tbody></table>



## Command Description

The table below gives a brief overview of the available commands for the wash station 96/384. Another possibility to wash the tips is given by the basic step commands “CO-RE 96 Head Dispense” / “CO-RE 384 Head Dispense”. In the basic dispense step, the wash function can be enabled via the “Wash tips after dispense” Parameter. The wash parameter can be set through the \[Customize…] Button.

\


| Command                     | Icon                                                                             |               |
| --------------------------- | -------------------------------------------------------------------------------- | ------------- |
| CO-RE 96 Head Wash          | <img src="../../.gitbook/assets/image (96) (1).png" alt="" data-size="original"> | Wash tips.    |
| CO-RE 96 Head Empty Washer  | <img src="../../.gitbook/assets/image (97) (1).png" alt="" data-size="original"> | Empty washer. |
| CO-RE 384 Head Wash         | <img src="../../.gitbook/assets/image (98) (1).png" alt="" data-size="original"> | Wash tips.    |
| CO-RE 384 Head Empty Washer | <img src="../../.gitbook/assets/image (99) (1).png" alt="" data-size="original"> | Empty washer. |



<table data-header-hidden><thead><tr><th width="125"></th><th></th></tr></thead><tbody><tr><td><img src="../../.gitbook/assets/image (9) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" data-size="original"></td><td><p>ATTENTION</p><p>The CO-RE 384 Probe Head performs a blow out after the wash steps. The software automatically uses the tip picking up position (tip rack). Therefore do not reload the tip rack of the pick-up position if performing any wash steps.</p></td></tr></tbody></table>



## Programming the Wash Station 96/384

The following is a simple example on how to program the wash station 96/384 using the Single Steps.

Activate the CO-RE 384 Probe Head and the Pump Station 2 in the Configuration Editor:

<figure><img src="../../.gitbook/assets/image (100) (1).png" alt=""><figcaption></figcaption></figure>

### Creating the Deck Layout

The method requires the following Deck Layout:

<figure><img src="../../.gitbook/assets/image (101) (1).png" alt=""><figcaption></figcaption></figure>

Use the “Search Labware” Field to add the following labware to the deck:

* “CORE384DualWashStation\_HU\_A00”
* “Core 384 Slide Waste”
* “TIP384\_CAR\_1920\_50ul\_A00”



### Creating the Sequences

In this example, the default sequences are being used.



### Creating the Method

The resulting method should look like the image below:

<figure><img src="../../.gitbook/assets/image (103) (1).png" alt=""><figcaption></figcaption></figure>

The step in line 1 initializes the instrument.

In step 2, the tips are picked up from the tip carrier (sequence counting = “Manually”).

<figure><img src="../../.gitbook/assets/image (104) (1).png" alt=""><figcaption></figcaption></figure>

1.  Use the “CO-RE 384 Head Wash” Wash Step without modifying the default values. These values guarantee and are the basis for good wash results.\


    <figure><img src="../../.gitbook/assets/image (105) (1).png" alt=""><figcaption></figcaption></figure>
2.  Eject the tips. Use “Eject on tip pick up position” to eject the tips back into the tip carrier.\


    <figure><img src="../../.gitbook/assets/image (106) (1).png" alt="" width="317"><figcaption></figcaption></figure>

<table data-header-hidden><thead><tr><th width="145"></th><th></th></tr></thead><tbody><tr><td><img src="../../.gitbook/assets/image (10) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" data-size="original"></td><td><p>NOTE</p><p><em>Always empty the waste container when refilling the wash solution container. When re-using washed tips, pipetting precision may increase by a factor of 3.</em></p></td></tr></tbody></table>

\
