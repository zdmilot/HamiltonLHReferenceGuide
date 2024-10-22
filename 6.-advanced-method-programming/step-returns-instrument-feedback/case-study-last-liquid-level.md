# Case Study – Last Liquid Level

## What was the Liquid level?

* 100ul/5ml Channels Get Last Liquid Level accesses volume information (using LLD) from the individual channels
* Called after an aspirate or dispense step – the steps are not linked by return values!
* It has no parameters, and has it’s own return values – in block format!

<figure><img src="../../.gitbook/assets/image (59).png" alt=""><figcaption></figcaption></figure>

## Get Last Liquid Level

* Labware and Labware Position are not populated – use the return value of the Aspirate/Dispense step to determine positional information
* Step Data is the Z-value (mm, float) where it encountered a liquid level – reference to system origin
* Isn’t that just GetStepData?  It’s similar - GetStepData returns a STRING which isn’t as useful for numeric comparisons

&#x20;&#x20;

<figure><img src="../../.gitbook/assets/image (60).png" alt=""><figcaption></figcaption></figure>

## Calculating a Volume

* DevComputeContainerVolume2 can turn a liquid level into a volume
* Height comes from the liquid level return (previous), labware and position ID could come from the Pippette Step Return – or compared to a fixed, representative position
* deckCoordinates changes the reference point for height, use 0 for the container reference
* Use connectedContainers =0 for all but troughs
* Requires sample tracking to be ON

<figure><img src="../../.gitbook/assets/image (61).png" alt=""><figcaption></figcaption></figure>

&#x20;
