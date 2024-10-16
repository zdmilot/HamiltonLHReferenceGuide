# Dispense on the Fly

VENUS Software offers a dispense on the fly (Single Step). This step does not stop the x- movement while pipetting which allows a very fast dispensing of liquid, e.g. to fill a plate with reagent.

<table data-header-hidden><thead><tr><th width="125"></th><th></th></tr></thead><tbody><tr><td><img src="../.gitbook/assets/image (9) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" data-size="original"></td><td><p>ATTENTION</p><p><em>This feature is available for 1000µl-pipetting channels and for 5ml-pipetting channels.</em>.</p></td></tr></tbody></table>



Refer to the dialog box shown below while reading this section. The following parameters of the dialog box must be filled.

## Sequence

The sequence positions where to dispense the previously aspirated liquid.

## Sequence Counting

Select “Automatic” to update the current position of the sequence or choose “Manually” to not adjust the current position of the sequence.

## Volume

The volume that shall be dispensed per well. Note: The volume per pipetting channel is constant.

## Dispense on the Fly Mode

_Complete plate_ will sort the sequence accordingly.

_Sequence order_ uses a sorted sequence (must fit to the selected pipetting channel pattern).

## Labware Surface Distance

The position above the labware surface where the liquid is dispensed (travelling height).

## X-Speed During Dispense

This value specifies the x-move speed. This value is dependent on the volume to be dispensed, the flow rate in the liquid class and the distance between the wells.

## Start X-Offset

The dispense normally starts in the center of the well. For larger volumes, shift the start point to the left to make sure the full volume is dispensed into the well.\


<figure><img src="../.gitbook/assets/image (56) (1).png" alt="" width="266"><figcaption></figcaption></figure>

The display below shows distances to be specified.

<figure><img src="../.gitbook/assets/image (57) (1).png" alt=""><figcaption></figcaption></figure>

In the Advanced section, the following parameters can be changed. Please refer to the image below whil reading this section.

## Liquid Class

It is possible to use a different liquid class than in the aspirations step

## X-Acceleration Distance Before First Shoot

The distance at which speed for pipetting should be reached (see graphic above).

## Dispense Direction

Choose “Serpentine” (for quick dispense) or “From left only”

## Exclude Labware Positions

This option allows to not dispense to specified positions.

<figure><img src="../.gitbook/assets/image (59) (1).png" alt=""><figcaption></figcaption></figure>

\


Example: A1 / B1 must be left empty since it is a blank position on the reader plate.

Add a separate dispense step after dispense on the fly, using the dispense mode ‘Drain tip in jet mode’ to dispense the rest of the volume out of the tip.

<table data-header-hidden><thead><tr><th width="125"></th><th></th></tr></thead><tbody><tr><td><img src="../.gitbook/assets/image (10) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" data-size="original"></td><td><p>NOTE</p><p><em>Make sure that the liquid class in the aspiration is set to DispenseJet Part Volume, otherwise the “Dispense on the Fly” Step will show an error.</em></p><p><em>Run some tests on the instrument to properly adjust the x-speed during dispense. Set the value to “0” to let VENUS calculate the x-speed.</em></p><p><em>The x-speed during dispense depends on the volume, the liquid class parameters and the labware geometry.</em>.</p></td></tr></tbody></table>

<table><thead><tr><th width="445"></th><th></th></tr></thead><tbody><tr><td><p>A table guide to find the correct settings. Liquid: Water</p><p>Tip Size: High volume 1000ul, no filter</p><p>Liquid Class:High_Volume_Water_DispenseJet_Part Shots per pipetting channel: 12 (full plate)</p></td><td><img src="../.gitbook/assets/image (60) (1).png" alt="" data-size="original"></td></tr></tbody></table>



<table data-header-hidden><thead><tr><th width="125"></th><th></th></tr></thead><tbody><tr><td><img src="../.gitbook/assets/image (10) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" data-size="original"></td><td><p>NOTE</p><p><em>Different tip sizes, liquid classes and shoot numbers may require different settings.</em></p></td></tr></tbody></table>



\
