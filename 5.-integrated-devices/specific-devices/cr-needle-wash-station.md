# ‌CR Needle Wash Station‌

## Needle Washing Using the CR Needle Wash Station

In combination with a wash station, re-usable steel needles can be used for pipetting with the spreadable 1000μl-pipetting channels of the ML STAR, instead of using the disposable tips. The result of washing needles depends on the wash setting.

<table data-header-hidden><thead><tr><th width="145"></th><th></th></tr></thead><tbody><tr><td><img src="../../.gitbook/assets/image (10) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" data-size="original"></td><td><p>NOTE</p><p><em>If carry-over is not acceptable for the application, use new disposable tips for each aspiration step instead of washed steel needles.</em></p></td></tr></tbody></table>



The picture shows a completely hooked-up CR needle wash station:

<figure><img src="../../.gitbook/assets/image (55) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>



The wash cycle of the CR needle wash station works in parallel to the pipetting steps. Liquid level sensors in the containers recognize whether the wash solution is used up or if the waste bottle is full. During run time, a message box is displayed giving the opportunity to refill/empty the containers.

\


## Command Description

The following tables in this section give a brief overview of the available commands for the CR needle wash station.

<table data-header-hidden><thead><tr><th width="145"></th><th></th></tr></thead><tbody><tr><td><img src="../../.gitbook/assets/image (10) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" data-size="original"></td><td><p>NOTE</p><p><em>It is recommended to use the “SmartStep Needle Pickup”. If the “1000μl- Channel Tip Pick Up” Single Step is used, a “1000μl Channel Wait for Needle Wash” Step has to be programmed before the tip pick up step.</em></p><p><em>With the Easy Step ASPIRATE, the needle pick up is also possible.</em></p><p><em>With the Easy Step DISPENSE, needle eject and start washing is also possible.</em></p></td></tr></tbody></table>

{% tabs %}
{% tab title="Single Steps" %}


| Command                             | Icon                                                                                     | Action Performed                                                                 |
| ----------------------------------- | ---------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- |
| 1000μl Channel Tip Pick Up          | <img src="../../.gitbook/assets/image (56) (1) (1) (1).png" alt="" data-size="original"> | Picks up a CO-RE tip or needle.                                                  |
| 1000μl Channel Start Needle Wash    | <img src="../../.gitbook/assets/image (57) (1) (1) (1).png" alt="" data-size="original"> | Starts a needle wash module.                                                     |
| 1000μl Channel Wait For Needle Wash | <img src="../../.gitbook/assets/image (58) (1) (1) (1).png" alt="" data-size="original"> | Waits for the needle wash module to be ready.                                    |
| 1000μl Channel Tip Eject            | <img src="../../.gitbook/assets/image (59) (1) (1) (1).png" alt="" data-size="original"> | Discards the tip into the tip waste or the needle into the wash station or rack. |
{% endtab %}

{% tab title="Smart Steps" %}
The needle wash step is embedded in the “Needle Eject” Command.

| Command                       | Icon                                                                                     | Action Performed                          |
| ----------------------------- | ---------------------------------------------------------------------------------------- | ----------------------------------------- |
| 1000μl Needle Wash Settings   | <img src="../../.gitbook/assets/image (60) (1) (1) (1).png" alt="" data-size="original"> | Sets Wash Parameters.                     |
| 1000μl Channel Needle Pick Up | <img src="../../.gitbook/assets/image (61) (1) (1) (1).png" alt="" data-size="original"> | Picks up a needle.                        |
| 1000μl Channel Needle Eject   | <img src="../../.gitbook/assets/image (62) (1) (1) (1).png" alt="" data-size="original"> | Ejects the needle for (optional) washing. |
{% endtab %}
{% endtabs %}



## Programming the CR Needle Wash Station



Below is a simple example of a method showing how to program the CR Wash Station using the Smart Steps. This method will wash all three sets of needles in the wash station. This could be useful after the instrument was not used for a long time.

1.  First, activate the wash station in the System Configuration Editor. Please note that this entry will work globally for all methods. If the method does not use a wash station, it can also be switched off here.\
    \


    <figure><img src="../../.gitbook/assets/image (63) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>
2.  The method requires the following Deck Layout:\


    <figure><img src="../../.gitbook/assets/image (66) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

\


### Creating the Deck Layout

1.  Create a new method called DemoWashStation.med.\


    <figure><img src="../../.gitbook/assets/image (64) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>



2.  Switch to the “Labware” Tab and add the search string “Wash high” to the “Search Labware” Field. The system will filter out everything except the two possible wash stations. Select the “Car\_Wash\_1\_CR\_HighNeedle\_A00” Carrier for the wash station and drag it onto the deck. Refer to the image below.\


    <figure><img src="../../.gitbook/assets/image (65) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

### Creating the Sequences

Create one sequence over all three wash blocks and name it “AllHighNeedles”.

\


### Creating the Method

The resulting method should look like this:

<figure><img src="../../.gitbook/assets/image (68) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

1. Define the wash settings using the “Needle Wash Settings” Smart Step (line 2).
2. This table shows default values of the wash parameters for 1000µl, 300µl and 10µl-volume needles.

| Needle  | Rinse time | Soak time | Flow rate    | Draining time |
| ------- | ---------- | --------- | ------------ | ------------- |
| 10 µl   | 5 seconds  | 5 seconds | 16 ml/second | 10 seconds    |
| 300 µl  | 5 seconds  | 5 seconds | 15 ml/second | 10 seconds    |
| 1000 µl | 5 seconds  | 5 seconds | 11 ml/second | 10 seconds    |

3. Select the wash sequence that shall be used for washing needles. Set all wash parameters and Click \[OK].
4.  Create a loop of 3 iterations (or use the sequence “AllHighNeedles” as the limitation).\


    <figure><img src="../../.gitbook/assets/image (69) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>
5.  The next step would be to pick up the needles:\


    <figure><img src="../../.gitbook/assets/image (70) (1) (1).png" alt=""><figcaption></figcaption></figure>
6. Please note that the sequence can be selected from the drop down list or by clicking \[Ctrl]. It can be “Drag and Dropped” directly from the Deck Layout.
7.  The needle eject dialog box appears as shown:\


    <figure><img src="../../.gitbook/assets/image (71) (1) (1).png" alt=""><figcaption></figcaption></figure>
8. Make sure that the “Start wash” Checkbox is ticked. Activating this box will close the wash modules lid right after ejecting and start the washing with the specified parameters.



<table data-header-hidden><thead><tr><th width="145"></th><th></th></tr></thead><tbody><tr><td><img src="../../.gitbook/assets/image (10) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" data-size="original"></td><td><p>NOTE</p><p><em>It is recommended to use the “Needle Pickup” Smart Step. If the “1000μl Channel Tip Pick Up” Single Step is used, a “1000μl Channel Wait for Needle Wash” Step has to be programmed before the tip pick up step.</em></p><p><em>With the Easy Step ASPIRATE, the needle pick up is also possible.</em></p><p><em>With the Easy Step DISPENSE, needle eject and start washing is also possible.</em></p></td></tr></tbody></table>



The error settings are similar to those of the “Pipette” Smart Step.

\
