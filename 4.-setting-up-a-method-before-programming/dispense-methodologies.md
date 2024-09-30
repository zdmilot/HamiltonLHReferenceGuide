# Dispense Methodologies

## Best Practices for Pipetting Low Volumes Using 1,000 μL Channels

Low volume pipetting using the 1,000 μL channels is defined as any volume between 0.5 and 20 μL.

### Method Settings

* Use 50 μL tips
* Single dispense if possible&#x20;
* Use surface empty mode&#x20;
* Keep distance between tip and pipetting surface minimal without blocking the tip&#x20;
* Liquid following turned off&#x20;
* Use new tips for each transfer

### Liquid Class Parameters&#x20;

* May require an increase in settling time&#x20;
* Slow swap speeds&#x20;
* Increase blowout volume on aspiration, but minimize on dispense. Prevents capillary action by creating an overpressure

## Best Practices for Multi-Dispensing (Aliquot)

Multi-dispensing, also known as aliquotting, is the act of aspirating enough total volume to dispense more than once from the same tip. While multi-dispensing can save time and tips, it can take more effort to control for the trueness and precision for each liquid transfer. To decide if pipetting should be implemented as a multi-dispense, refer to the chart on the next page.

<figure><img src="../.gitbook/assets/image (425).png" alt="" width="375"><figcaption><p><em>IMPLEMENT AS A MULTI-DISPENSE VS SINGLE DISPENSE</em></p></figcaption></figure>

## Method Settings

* Only use 50 μL tips or higher.&#x20;
* The first and last aliquots are often inaccurate and should be discarded in order to maintain good precision overall amongst the transfers. Some liquids may require 2 pre-dispenses. See the image below for an example of a pre- and post-aliquot transfer that are discarded, ensuring that the transfer in between are within an acceptable range.

<figure><img src="../.gitbook/assets/image (426).png" alt="" width="375"><figcaption></figcaption></figure>

* Limit total number of aliquots per cycle.&#x20;
  * The limit can vary based on transfer volume and tip size, but in general, it is recommended to keep the number of transfers to a minimum for easier control and more consistent liquid handling.&#x20;
  * Recommend restricting the number of transfers for ease of method programming. For example, if pipetting to a 96-well format plate with an 8-channel automated liquid handler, limit the number of transfers steps to 6 (half the plate) or 12 (one whole plate).&#x20;
* Pre-wet the tip on first aspirate. This action can nullify the effects of the correction curve and allow for consistent transfers.&#x20;
* Use “minimize z-move step” function to prevent the pipettes from moving to a default traverse height in between transfers, increasing the speed of the transfers.&#x20;
* Set dispense height equal to the clearance height.&#x20;
* To maximize speed, use “dispense on the fly” function to prevent the pipettes from stopping during the x and z-movement in between transfers. This function can be challenging to optimize. See Section 5.1.10 About the Dispense on the Fly Feature for more information.

## Liquid Class Parameters

* Increase stop back flow rate to match dispense flow rate.&#x20;
* Use a small stop back volume (dry dispense only).&#x20;
* For the correction curve, it is important to note the total volume aspirated and then use a step down approach to determine the correction for each transfer.
  * For example, to transfer six aliquots of 50 μL using 300 μL tips, do not adjust for trueness at the 50 μL target volume like one would for a single transfer. Instead, adjust the target volume of 300 μL for the first transfer, 250 μL for the next, and so on. Refer to the table below.&#x20;
  * Use more correction curve points to increase the trueness of every individual liquid transfer. The overall precision amongst all transfers would then improve.

<div>

<figure><img src="../.gitbook/assets/image (427).png" alt="" width="375"><figcaption></figcaption></figure>

 

<figure><img src="../.gitbook/assets/image (428).png" alt="" width="375"><figcaption></figcaption></figure>

</div>

## Best Practices for Serial Dilution

A dilution is one of the more common liquid transfers performed and occurs when a sample liquid is added to another liquid, decreasing its concentration. A serial dilution repeats this process over multiple steps in order to test samples at a variety of concentrations and/or to arrive at very low final concentration.&#x20;

For example, 90 μL of buffer solution is added to all of the wells in a 96-well plate. 10 μL of sample is then added to column 1, mixed, and then 10 μL of that mixture is transferred to column 2, mixed, and so on. Each step dilutes the sample by a factor of 10.

<figure><img src="../.gitbook/assets/image (429).png" alt="" width="375"><figcaption></figcaption></figure>

## Method Settings

* Use a new tip for each transfer.&#x20;
* Dispense to surface if possible.&#x20;
* Mix very well before and/or after each transfer. Start with many mix cycles and decrease only to optimize for speed if performance allows.&#x20;
* Mix at a fixed position to optimize the dispense and mix heights.&#x20;
* If using LLD and liquid following, properly defined labware is critical to ensure proper following and mixing.&#x20;
* Mix volume should be less than 80% of total volume in the well. If the mix volume is larger than 80%, it increases the chance of aspirating air and creating bubbles.&#x20;
* Be mindful of retract distance for air transport if dispensing at fixed height. If the retract distance and the fixed height are set too low, then it is possible that the tip may not be removed from the liquid before it aspirates the air transport volume. This results in the possibility of extra liquid being aspirated instead of air.

## Liquid Class Parameters

* Depending upon dilution factors, different liquid classes for each step may be required.&#x20;
* Remove the over-aspirate volume parameter, because it could lead to excess carryover after subsequent dispense and mixing.
