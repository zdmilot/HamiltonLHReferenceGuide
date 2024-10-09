# Sequence Definitions

### Sequence Definitions for Transport Steps

The iSWAP works on the basis of sequences (see Section 15.1.7 iSWAP Movement). Plates are moved from one position to another, each defined by its own sequence. The labware definition remains fixed on the deck, but the plates change sequences. To make this possible, definition of target and source plate positions must be of the same labware type.

After processing of a sequence, the current position will be set to the next labware ID. If the same plate should be transported several times, select sequence counting '(0) Manually' or set the current position back to the previous position.

<table data-header-hidden><thead><tr><th width="145"></th><th></th></tr></thead><tbody><tr><td><img src="../../../.gitbook/assets/image (10) (1) (1) (1) (1) (1) (1) (1).png" alt="" data-size="original"></td><td><p>NOTE</p><p>Sequence positions for transport steps are always differentiated by the labware ID. The current position of the transport sequence is to set the next labware ID in the sequence.</p></td></tr></tbody></table>

<div>

<figure><img src="../../../.gitbook/assets/image (93) (1).png" alt=""><figcaption></figcaption></figure>

 

<figure><img src="../../../.gitbook/assets/image (94) (1).png" alt=""><figcaption></figcaption></figure>

</div>

In the example above, after the transport of plate Source\_1, the current position will be set to plate Source\_2 (line 5); and after transport of plate Soure\_2 to plate Source\_3 (line 9).&#x20;

It is recommended to define separate sequences for transport and pipetting, because the behavior of transport and pipetting is different.&#x20;

<table data-header-hidden><thead><tr><th width="145"></th><th></th></tr></thead><tbody><tr><td><img src="../../../.gitbook/assets/image (10) (1) (1) (1) (1) (1) (1) (1).png" alt="" data-size="original"></td><td><p>NOTE</p><p>The orientation of the plate depends on plate positioning on the deck and not on sequences. The orientation can be changed under the “Labware” Tab by the function ”Adjust Labware Position” – “Rotation”)</p></td></tr></tbody></table>

