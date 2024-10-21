# Making Sequences

## Library Functions In Practice

### Part One: Instrument Step, Bind Return, Find # Blocks

<figure><img src="../../.gitbook/assets/image (57).png" alt=""><figcaption></figcaption></figure>

### Part 2: Processing Loop to Extract Information

<figure><img src="../../.gitbook/assets/image (58).png" alt=""><figcaption></figcaption></figure>

\*\*The AND condition using Step Data wouldn’t be needed to build a sequence from samples that had an error





## Making Sequences - Results - Capturing Run Time Information

###

### Example Return: Aspirate Single Step with errors&#x20;

* Using the example Step Returns from earlier examples, in the sequence processing loop just described, what would the resulting sequence be?

<figure><img src="../../.gitbook/assets/image (69).png" alt=""><figcaption></figcaption></figure>



### Example Return: Aspirate Single Step with limited channels – All Sequence Pos.&#x20;

* Using the example Step Returns from earlier examples, in the sequence processing loop just described, what would the resulting sequence be?

<figure><img src="../../.gitbook/assets/image (43).png" alt=""><figcaption></figcaption></figure>

### Example Return: Aspirate Single Step with limited channels – Channel Pattern

* How does this example change if the channel reference mode is changed from all sequence positions to Channel Pattern mode?

<figure><img src="../../.gitbook/assets/image (44).png" alt=""><figcaption></figcaption></figure>

This example shows why checking for only Labware ID or Labware Position (Position ID) can lead to incorrect results. We used Step Data for this reason!
