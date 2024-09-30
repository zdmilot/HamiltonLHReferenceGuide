# Pipette - Simple (1-1)

## Overview

The 'Pipette - Simple (1-1)' Smart Step is used to copy all elements of the aspirate sequence to the dispense sequence exactly once.

<figure><img src="../../../.gitbook/assets/image (411).png" alt=""><figcaption></figcaption></figure>

It aspirates the requested pipette volume with each channel and then dispenses it. Then, the next elements on the aspirate and dispense sequence are used until all elements of the controlling sequence are finished.

**Notes:**

* If the volume which has to be pipetted exceeds the capacity of the used tip, the pipette cycle for one element is repeated until the whole volume is moved properly. That means that the requested volume is not limited by the tip size.
* On a IVD System, the execution of each aspirate - dispense cycle can not be interrupted by pressing the pause button.

## Page 1: Sequences

This is the first step to define a Pipette - Simple (1-1).

<figure><img src="../../../.gitbook/assets/image (412).png" alt=""><figcaption></figcaption></figure>

On this page the instrument and the aspirate / dispense sequence has to be defined.

* Select the instrument on which the pipette shall be executed
* Aspirate / Dispense sequence

Add the aspirate / dispense sequence(s) from which the pipette shall aspirate / to which the pipette shall dispense.

If one sequence is specified, the step behaves same as in earlier version (version 4.4 and earlier).

If more than one sequence is specified, sequence merging is done to create the pipetting sequence. The merging operation does:

1. Concatenate the sequence positions.&#x20;
2. Sort sequence positions for a 1000ul channel head.
3. Remove duplicate sequence positions, so that the sequence contains distinct positions.

The 'Bind Merged Sequence' assigns the pipetting sequence (merged sequence) to a sequence variable.&#x20;

## Page 2: Volumes

On this page of the Pipette - Simple (1-1) the requested volumes has to be defined.

<figure><img src="../../../.gitbook/assets/image (413).png" alt=""><figcaption></figcaption></figure>

Volume to move from the aspirate to the dispense sequence, and if some rest volume shall be aspirated:

* Additional rest volume to aspirate.
* Redispense place for the rest volume.
* Redispense height from container bottom for the redispense of the rest volume.

## Page 3: Tip/Needle Handling

On this page of the Pipette - Simple (1-1) the tip/needle handling has to be defined.

&#x20;

<figure><img src="../../../.gitbook/assets/image (414).png" alt=""><figcaption></figcaption></figure>

* Select the requested tip/needle type to filter the tips/needles choice list.
* Select the tip or wash sequence from which the tips/needles shall be picked up.
* Select the event when the tips/needles shall be replaced:
  * After each dispense.
  * After the volume is transferred\
    (Option not available for a Pipette - Simple (1-1) because it is identical to After each sample is processed)
  * After each sample is proceeded.\
    Note: If the complete requested volume fits to the tip/needle size this option is identical to tip replacement After each dispense.
*
  * Use one set for the full pipette.
  * Never, use the tips/needles picked up before this pipette.
* If you like to write the tip counter enter a tip counter name (not available if you work with needles).
* Check the offered additional feature:

¨ Operator may reduce the tip sequence by a reload (not available if you work with needles).

**Note:**

By a step Pipette, tips are always ejected into the default waste specified by the selected instrument.

&#x20;

## Page 4: Liquid Handling

On this page of the Pipette - Simple (1-1) the liquid handling has to be defined.

<figure><img src="../../../.gitbook/assets/image (415).png" alt=""><figcaption></figcaption></figure>

**Liquid class**

* Select the liquid (liquid class) which shall be used for the aspirate and dispense.

**Aspirate parameters:**

* Check the offered additional feature:
  * Aspirate the complete requested volume without error, even if not enough volume is available.

**Dispense parameters:**

* Select the dispense mode:
  * Jet
  * Surface



## Page 5: Sequence Handling

On this page of the Pipette - Simple (1-1) the sequence handling has to be defined.

<figure><img src="../../../.gitbook/assets/image (417).png" alt=""><figcaption></figcaption></figure>

**Controlling sequence**

* Select the controlling sequence which determines the total number of pipetted elements.

**Aspirate**

* Select the desired reload setting for the aspirate sequence.
* Reducible by user

**Dispense**

* Select the desired reload setting for the dispense sequence.
* Reducible by user

&#x20;

Note:

The automatic reloading cannot be used for the controlling sequence if Pipette Over Array is used.
