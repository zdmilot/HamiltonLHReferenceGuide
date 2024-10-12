# Wash Station 96‌

The Wash station 96 is an optional device for washing 96 disposable tips in parallel. The tips are washed both outside and inside at the same time: on the outside in the wash chamber of the wash station 96 and on the inside by aspiration/dispense cycles with the CO-RE 96 Probe Head. The result of washing the tips depends on the wash setting.

<table data-header-hidden><thead><tr><th width="145"></th><th></th></tr></thead><tbody><tr><td><img src="../../.gitbook/assets/image (10) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" data-size="original"></td><td><p>NOTE</p><p><em>If carry-over is not acceptable for the application, use new disposable tips for each aspiration step.</em></p><p><em>The wash station 96 is no longer available. It was replaced by the wash station 96/384.</em></p></td></tr></tbody></table>

Sample transfers may be done using new disposable tips, while reagents, buffers, etc. may be distributed with washed tips.

The picture below shows a complete, fully connected wash station 96:\


<figure><img src="../../.gitbook/assets/image (83) (1).png" alt="" width="375"><figcaption></figcaption></figure>

Liquid level sensors inside the washer unit prevent flooding of the system. On the other hand, the washer unit recognizes if there is not enough liquid to fill the wash chamber.

<table data-header-hidden><thead><tr><th width="145"></th><th></th></tr></thead><tbody><tr><td><img src="../../.gitbook/assets/image (10) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" data-size="original"></td><td><p>NOTE</p><p><em>There is no liquid level sensor in the waste container. In case of refilling the wash solution container, always empty the waste container.</em></p><p><em>When re-using washed tips, pipetting precision may decrease by a factor of 3.</em></p></td></tr></tbody></table>



## Command Description

The table below gives a brief overview of the available commands for the wash station 96. Another possibility to wash the tips is given by the “CO-RE 96 Head Dispense” Basic Step Command. In the Basic dispense step, the wash function via the “Wash tips after dispense” Parameter can be enabled. The wash parameter can be set through the \[Customize…] Button.

| Command                    | Icon                                                                             | Action Performed                      |
| -------------------------- | -------------------------------------------------------------------------------- | ------------------------------------- |
| CO-RE 96 Head Wash         | <img src="../../.gitbook/assets/image (84) (1).png" alt="" data-size="original"> | Wash tips using the default settings. |
| CO-RE 96 Head Empty Washer | <img src="../../.gitbook/assets/image (85) (1).png" alt="" data-size="original"> | Empty washer.                         |



## Programming the Wash Station 96

The following is a simple example on how to program the wash station 96 using Single Steps.

Please note that the CO-RE 96 Probe Head and one of the Pump Stations in the System have to be activated in the Configuration Editor.\


<figure><img src="../../.gitbook/assets/image (86) (1).png" alt=""><figcaption></figcaption></figure>

### Creating the Deck Layout

The method requires the following Deck Layout:

<figure><img src="../../.gitbook/assets/image (87) (1).png" alt=""><figcaption></figcaption></figure>

Add a wash station, slide waste and a standard tip carrier to the deck. Use the “Search Labware” Field to add the following labware:

* “CORE\_HU\_96WashStation\_A00”
* “Core\_96SlideWaste” from "ML STAR Wastes"
* “TIP\_CAR\_480\_ST\_A00”



### Creating the Method

The resulting method should look like the image shown below.

<figure><img src="../../.gitbook/assets/image (91) (1).png" alt=""><figcaption></figcaption></figure>

1. Pick up tips from the tip carrier. Set “Manually” for sequence counting to eject the tips to the pickup position (Step 2).
2. In line 3, use the “CO-RE 96 Head Wash” Wash Step without modifying the default values. These values guarantee and are the basis for good wash results.
3.  Eject the tips. Use “Eject on tip pick up position” to eject the tips back into the tip carrier.\
    \


    <figure><img src="../../.gitbook/assets/image (92) (1).png" alt=""><figcaption></figcaption></figure>

<table data-header-hidden><thead><tr><th width="145"></th><th></th></tr></thead><tbody><tr><td><img src="../../.gitbook/assets/image (10) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" data-size="original"></td><td><p>NOTE</p><p><em>The method can be accelerated when programming the last “Refill wash chamber” Command parallel to the succeeding method steps.</em></p></td></tr></tbody></table>

### Creating a Modified Method

The method above can be modified to speed up the wash step. The last refilling command for the wash chamber has to be programmed in parallel to the tip eject step. The resulting modified method should look like the image shown below.

<figure><img src="../../.gitbook/assets/image (93) (1).png" alt="" width="375"><figcaption></figcaption></figure>

Use the “Begin Parallel” and “End Parallel” Steps to do this.

In the CO-RE 96 Head empty washer step, set the washer parameters to “(2) On – chamber one only” to have the maximum speed up.

<figure><img src="../../.gitbook/assets/image (94) (1).png" alt=""><figcaption></figcaption></figure>
