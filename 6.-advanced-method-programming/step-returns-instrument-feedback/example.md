# Example

## Example Return: iSWAP/IPG Single Step Get Plate&#x20;

* Return Value #3: Get Plate Data With Recovery Details
* Block Structure: This return has no step data

<figure><img src="../../.gitbook/assets/image (67).png" alt=""><figcaption></figcaption></figure>

## Example Return: Load Single Step&#x20;

* Return Value #4: Barecodes With Recovery Details&#x20;
  * Requires Autoload and successful Carrier ID
* Block Structure with carriage returns added for ease of view

<figure><img src="../../.gitbook/assets/image (1) (1).png" alt=""><figcaption></figcaption></figure>

## Example Return: Aspirate Single Step

* Return Value #3: Channel Sequence With Recovery Details
* Block Structure with carriage returns added for ease of view

<figure><img src="../../.gitbook/assets/image (2) (1).png" alt=""><figcaption></figcaption></figure>

## Example Return: Aspirate Single Step with errors

* Block Structure with carriage returns added for ease of view
* What Happened to Tubes 16, 19, 21, 22?
  * Error Flag: 1 = Step had at least one error
  * Main Error: 4 = Clot Error/Blood clot detected\*\*
  * Slave Error: 82 = TADM measurement out of lower limit curve (consistent with a Clot event)\*\*
  * Recovery Button: 5 = Exclude
*   The EXCLUDE option alters the channel pattern.

    This can cause unanticipated sample placement – see Basic materials for All Sequence Positions vs Channel Pattern references.

    \*\*This process is described in greater detail later in this presentation!

<figure><img src="../../.gitbook/assets/image (4) (1).png" alt=""><figcaption></figcaption></figure>

## Example Return: Pipetting Single Step with Modified Channel Usage

Channel pattern of “11000011” using All Sequence Positions mode

<figure><img src="../../.gitbook/assets/image (13) (1).png" alt=""><figcaption></figcaption></figure>

### Why is there missing data?&#x20;

There are still eight blocks of data, one per channel. The omitted (“0”) channels still have error and recovery responses, however, they did not pipette or access a position.

Labware Position is sequential because under all sequence positions, only active channels will interact with a sequence



## Example Return: Pipetting Single Step with Modified Channel Usage

Channel pattern of “11000011” using Channel Pattern mode

<figure><img src="../../.gitbook/assets/image (14) (1).png" alt=""><figcaption></figcaption></figure>

### Why is there missing data?&#x20;

Now the omitted channels have labware information!

When using channel pattern mode, all channels interact with sequence positions. However, only active channels actually process in the step. This is clear because inactive channels are missing Step Data (volume) information.



## Example Return: Pipetting Single Step Using “Small” sequences

Channel pattern of “11111111” using All Sequence Positions mode

Sequence used only has four positions available

<figure><img src="../../.gitbook/assets/image (15) (1).png" alt=""><figcaption></figcaption></figure>

### Why is there missing data?&#x20;

Channels are omitted not because of a channel pattern, but because there are no more positions in the sequence to process.

Similar to the earlier example using all sequence positions, but channels will always be consecutive (Channels 1-N)
