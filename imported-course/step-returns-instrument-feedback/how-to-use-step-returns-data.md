# How to Use Step Returns Data?

## Step Return Library - Analyzing Block Data&#x20;

* The HSLMlStarStepReturnLib (Step Return Library) is designed to extract information from block data&#x20;
* Most functions parse the block data, and return a single string element
* For a single block return (like a transport), Get functions are straightforward – but where multiple blocks are present, things may change!

<figure><img src="../../.gitbook/assets/image (45).png" alt=""><figcaption></figcaption></figure>

Library Functions - Access Modes

Accessing a Block:&#x20;

* By POSITION simply counts block delimiters (left brackets, \[ ).
  * It is absolute!&#x20;
* By NUMBER will search the return string, until the number is found, and then use that block It is relative!&#x20;
  * Number and Position do not always match!

<figure><img src="../../.gitbook/assets/image (47).png" alt=""><figcaption></figcaption></figure>

This Load Command may have had a recovered error for Tube#1.\
Repeating the scan has placed Position ID 1 at the end of the list!

<figure><img src="../../.gitbook/assets/image (48).png" alt=""><figcaption></figcaption></figure>

## Library Functions - Get Error Code

<figure><img src="../../.gitbook/assets/image (49).png" alt="" width="180"><figcaption></figcaption></figure>

* Returns the Error Code of a step return&#x20;
* Use as an initial check – if equal to 0, the step processed as expected!

<figure><img src="../../.gitbook/assets/image (50).png" alt=""><figcaption></figcaption></figure>



## Library Functions - Get Error Code cont.

<figure><img src="../../.gitbook/assets/image (51).png" alt="" width="181"><figcaption></figcaption></figure>

* When an error occurs, it is often tied to a recovery - an actual button that the operator can select&#x20;
* Not all recoveries will show an error code!

| Recovery Button ID | Recovery Button Text | Description                                                            | Action State |
| ------------------ | -------------------- | ---------------------------------------------------------------------- | ------------ |
| 1                  | Abort                | Run is aborted.                                                        | Fatal        |
| 2                  | Cancel               | Run is canceled and a defined user error handler is started            | Warning      |
| 3                  | Initialize           | Instrument is reinitialized                                            | No Error     |
| 4                  | Repeat               | The command is repeated                                                | No Error     |
| 5                  | Exclude              | The channel or position is excluded until a new tip pick up is called. | Error        |
| 6                  | Waste                | The tip is ejected to the default waste                                | Error        |
| 7                  | Air                  | Rest of missing volume is filled up with air                           | Error        |
| 8                  | Bottom               | Repeats the aspiration on container bottom                             | Error        |
| 9                  | Continue             | Continue without any change                                            | Error        |
| 10                 | Barcode              | Barcose is assigned manually                                           | Warning      |
| 11                 | Next                 | Repeat the command on next sequence position                           | No Error     |
| 12                 | Available            | Aspirate & dispense the available volume.                              | Error        |
| _NA_               | _NA_                 | Refill                                                                 | No Error     |

\


Library Functions - Get Number of Positions\



<figure><img src="../../.gitbook/assets/image (52).png" alt="" width="177"><figcaption></figcaption></figure>

* Counts the number of data blocks in a step return&#x20;
* Use as a loop cycle control for subsequent steps!\


<figure><img src="../../.gitbook/assets/image (53).png" alt=""><figcaption></figcaption></figure>

t\_intReturnNumberPositions = 8, one per block delimiter
