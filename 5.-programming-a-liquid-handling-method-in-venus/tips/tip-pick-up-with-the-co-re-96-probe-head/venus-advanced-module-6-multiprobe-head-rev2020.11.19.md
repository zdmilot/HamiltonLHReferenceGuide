# Venus Advanced Module 6 Multiprobe Head REV2020.11.19

## MultiProbe Head (MPH) Review

### MPH96:

* 8x12 format
* cLLD sensors on A1/B2 + G11/H12
* Channel Pattern available (columns)
* Offset by rows, columns (full)

_(Other offsets available with sequence movement)_

![](<../../../.gitbook/assets/0 (28).jpeg>)

### MPH384

* “384” or “384 STP” _Shifted Tip Pickup_
* STP: _Shifted Tip Pickup_
* cLLD sensors on A5 / P24

![](<../../../.gitbook/assets/1 (29).png>)

## Reducing Options

### Physical Limitations

Offset pickup requires the tip shoulder to be the local highest coordinate Tip Support (Adapter) Rack

* Fits Framed Tip Rack (FTR) slot
* Available for MPH 384STP or 96

![](<../../../.gitbook/assets/2 (28).png>)![](<../../../.gitbook/assets/3 (30).png>)![](<../../../.gitbook/assets/4 (28).png>)![](<../../../.gitbook/assets/5 (9).jpeg>)

Nested Tip Rack

* An isolated tier (X, Y, or both)

![](<../../../.gitbook/assets/6 (9).jpeg>)![](<../../../.gitbook/assets/7 (28).png>)

### Channel Usage

Consider Method and Physical Limitations

![](<../../../.gitbook/assets/8 (25).png>) ![](<../../../.gitbook/assets/9 (20).png>) ![](<../../../.gitbook/assets/10 (18).png>)

* Channel selection must be continuous and touch a corner
* Tip access is reverse from the channel selected\
  _i.e. Channel 1(A1) = Tip #96 (H12)_
* If cLLD is being used, ensure
  * A cLLD probed channel is in the selection
  * The sample with the cLLD probe is a representative volume

### Channel Pattern Rules

* Are “Strings”
* Count from position 1 to N (96 or 384), column- wise from A1
* Run in “Reduced Pattern Mode”, row or column
* Pattern affects sample counting, sample tracking, and trace files
* For MPH 96, only referenced at tip pickup

![](<../../../.gitbook/assets/11 (19).png>) ![](<../../../.gitbook/assets/12 (18).png>)

![](<../../../.gitbook/assets/13 (17).png>)

## Sequence Considerations

### Sequence Orders - Columns

![](<../../../.gitbook/assets/14 (17).png>) ![](<../../../.gitbook/assets/15 (10).jpeg>)

Tips: Reducing by Columns 12->1

* Default Columns sequence use (A1:H1->A12:H12)

Tips: Reducing by Columns 1->12

* Reversed Columns sequence use (A12:H12->A1:H1)

Source / Destination

* Default Columns sequences

### Sequence Orders - Rows

![](<../../../.gitbook/assets/16 (13).png>) ![](<../../../.gitbook/assets/17 (7).jpeg>)

Tips: Reducing by Rows A->H

* Reverse by row H1:H12->A1:A12

Tips: Reducing by Columns HàA

* Only sorted by Row A1:A12->H1:H12

Source / Destination

* Must be sorted by ROW, usually A->H

### Changing Plate Formats: MPH384->96

![](<../../../.gitbook/assets/18 (15).png>)

![](<../../../.gitbook/assets/19 (14).png>)![](<../../../.gitbook/assets/20 (14).png>)

Rocket Tips!

* 300uL volume
* Use quadrupole head probes to make one tip

Reduced Tip Racks

* Regular 384 well tips racked every other row/column (96 tips/rack)

Either type is specified in the 384 Pickup step

### Changing Plate Formats: MPH96->384

<figure><img src="../../../.gitbook/assets/image (882).png" alt=""><figcaption></figcaption></figure>

The Head 96 Stamp Tool accounts for 9mm MPH96 channel raster

* Can sort existing sequences using the advanced tab
* Can use stamp tool to create new sequences in any fill order (A1/A2/B1/B2)
* No special labware considerations



### Sequence Mismatches - Changing Plate Formats: MPH96->24 (4:1)

Need overlapping labware to provide 96 sequence positions to the 24w plate

<figure><img src="../../../.gitbook/assets/image (883).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (884).png" alt=""><figcaption></figcaption></figure>

* Can provide 4:1, 2:1, or 1:1 tips/well
* Watch 24well raster – must be 18mm for best fit
* Test fit by teaching with 96mph and desired tip pattern
* Volume Remaining calculation and liquid following will be unreliable
* Will be “missed” by sample tracking of 24well plate
* MPH96 steps interact with the “fake” 96 labware, all previous sequence conditions apply

<figure><img src="../../../.gitbook/assets/image (885).png" alt=""><figcaption></figcaption></figure>

Need overlapping (Snapped) labware to provide 96 sequence positions to the 24w plate

* Allows up to 4ml dispense per well
* Round wells + watch dispense height – tips may fit but not channel barrel
* Square/flat bottom wells _may_ allow travel to well bottom
* 2:1 would use alternate tips by row or column
* Useful for washing plates (BVS or MPE2)

_Channel selection used only to show PHYSICAL tip locations – all 96 positions would be used_

Need overlapping (Adjusted) labware to provide 96 sequence positions to the 24 well plate

* Adjust 96w plate location such that both A1 coordinates (24w and 96w) are equivalent
* Allows Aspirate or dispense at bottom reliably (Volume present and following speed calculations may be incorrect)
* Channel pattern must be CONTINOUS – alternating tips controlled with physical tip arrangement

## Helpful Tools in the MPH 96 Library

### STAR MPH96 Tools - TIP\_OFFSET\_

<figure><img src="../../../.gitbook/assets/image (886).png" alt=""><figcaption></figcaption></figure>



* CleanUpTips\_Rows/Columns
  * Moves a partial support rack to an empty (USED) rack
* PickUpTips\_Rows/Columns
  * If support rack is empty, loads from a full Seq
  * Picks up **full** columns or rows **without** needing sequence adjustments

Limitations: doesn’t support sending tips back to a support – internal tip counter uses local database (sample tracking), doesn’t see outside sequence counting

<figure><img src="../../../.gitbook/assets/image (887).png" alt=""><figcaption></figcaption></figure>

Paramaters for **TIP\_OFFSET\_PickUpTips\_Rows/Columns**

1. The instrument (MLSTAR)
2. Tip seq. where support can be loaded from (typically system managed)
3. The sequence of the tip support – can use any sequence sorting
4. Columns (1-12) or Rows (1-8) that should be picked up. _Full strips only._
5. A name for the tip counter – typically keep consistent for column or row access
6. Boolean (true/false) that represents Left/Right or Top (back)/Bottom (front) MPH usage.



### STAR MPH96 Tools - GetLiquidLevelHeight

<figure><img src="../../../.gitbook/assets/image (888).png" alt=""><figcaption></figcaption></figure>

* Links Step Returns from tip pickups and an Asp/Disp with cLLD to return the Z- height of last LLD

### STAR MPH96 Tools - GetTipPresence

* Live only – returns true/false if tips are present

### STAR MPH96 Tools - PickUpNextMPH96Tips

* For a given tip sequence, will pickup within the sequence a full rack
* Useful for tips/channels accessing the same sequence of tips!

### Sometimes the best tool is the one you make for yourself! Generating an MPH 96 Channel Pattern:

1. Start with an empty string
2. MAJOR loop: Run 12 times – creating columns
3. MINOR loop: Run 8 times – writing values by rows
4. Decide if a “1” should be written or not (“0”)\*\*!

\*\*Note:

* Assignment with Calculation can build a string a fragment at a time
* Channel Patterns always go by Column – the tip pickup has a dropdown for row or column usage

## Example 1

<figure><img src="../../../.gitbook/assets/image (889).png" alt=""><figcaption></figcaption></figure>

1. How many active channels are present on the MPH96? **24**
2. Should the pattern mode use ROW or COLUMN? **ROW**
3. What should the tip pickup sequence look like? **By Row, Front to Back H1->H12 : A1->A12**

## Example 2

<figure><img src="../../../.gitbook/assets/image (890).png" alt=""><figcaption></figcaption></figure>

1. How many active channels are present on the MPH96? **56**
2. Should the pattern mode use ROW or COLUMN? **COLUMN**
3. What should the tip pickup sequence look like? **Default COLUMN, A1->H12**

## Example 3

<figure><img src="../../../.gitbook/assets/image (891).png" alt=""><figcaption></figcaption></figure>

1. How many active channels are present on the MPH96? **3 – This is an “AND” condition**
2. Should the pattern mode use ROW or COLUMN? **ROW**
3. What should the tip pickup sequence look like? **By Row, Front to Back H1**à**H12 : A1**à**A12**

_!! If the row of tips is FULL (12), all 12 will still be picked up, but sample tracking and the trace file will only “see” those interacting with the channel pattern!_
