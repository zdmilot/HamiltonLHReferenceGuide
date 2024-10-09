# Unique Barcodes

The unique barcode check controls if a barcode has already been used on the system. To use this function, four settings must be made:

1. Activate sample tracking.
2. Specify the unique barcode check mode.
3. Specify the duration of the check period.
4. Set the unique barcode flag on the desired labware positions.

As soon as the unique barcode checking is set to “Track only” or “Check and Track”, all read barcodes will be written to the data base with a timestamp (when it was loaded).

Every load step will now refer to this database and check if the barcode has been loaded during the specified check duration.



## Activate Sample Tracking

To use the Unique barcode check, Sample Tracking must be set to “ON” in the “System Configuration Editor -> System Settings”:

<figure><img src="../../.gitbook/assets/image (28) (1).png" alt=""><figcaption></figcaption></figure>

\


Specify the “Unique Barcode check” Mode:

“OFF” Mode

Unique barcode management is switched off. Meaning, no check for unique barcodes, no writing to the database will be done.

“Track only” Mode

Unique barcode check will be turned on partially. Barcodes and timestamp are added to the database to be checked in the future, but no checks are performed. If the barcode has been loaded previously, the timestamp will be updated. Meaning there will be writing but not checking of barcodes.

“Check and Track” Mode

Unique barcode check operation is fully turned on. If a barcode is presented a second time within the specified unique barcode duration, a warning is invoked that this barcode has been loaded previously. Meaning it will write at the same time check barcodes.

Specify the Unique Barcode Duration

Click the \['...'] Button if unique barcode duration is selected, to open a wizard which allows specification of the duration parameter.

*   Current run: Barcodes must be unique within the current run.\


    <figure><img src="../../.gitbook/assets/image (29) (1).png" alt=""><figcaption></figcaption></figure>
*   Time in hours: Duration in hours within a barcode must be unique.\


    <figure><img src="../../.gitbook/assets/image (30) (1).png" alt=""><figcaption></figcaption></figure>

## Set the Unique Barcode Check Flag on the Labware:

1.  Open the Context Menu of the specified labware in the Deck Layout (right mouse-click).\


    <figure><img src="../../.gitbook/assets/image (31) (1).png" alt=""><figcaption></figcaption></figure>

    To make the sample carrier barcode itself unique, tick the “Barcode must be unique” Checkbox underneath the barcode mask. Now, the carrier barcode will be controlled at every load step.\


    <figure><img src="../../.gitbook/assets/image (32) (1).png" alt=""><figcaption></figcaption></figure>
2.  To set barcodes on the tubes as unique, select the \[By Position…] Tab.\
    \
    In the example shown below, there are two barcodes that should not be checked for distinction. Every barcode in position 1 and 2 is allowed to appear multiple times, but the barcode mask for these barcodes must be correct.\
    \


    <figure><img src="../../.gitbook/assets/image (33) (1).png" alt=""><figcaption></figcaption></figure>
3. All other positions are marked as “Unique” in the right most column. This will enable the checking for unique barcodes (as long as all other settings are appropriate).
4. To mark all barcodes for checking, check the “Barcode must be unique” Checkbox. Select all positions and click the \[Apply to selected positions] Tab.

## Behavior at Runtime

During runtime, two errors can be raised:\


| First load                     | Second Load                    | Error                      |
| ------------------------------ | ------------------------------ | -------------------------- |
| Unique flag on Labware not set | Unique flag on Labware not set | No error                   |
| Unique flag on Labware not set | Unique flag on Labware set     | Barcode Not Unique Error   |
| Unique flag on Labware set     | Unique flag on Labware set     | Barcode Not Unique Error   |
| Unique flag on Labware set     | Unique flag on Labware not set | Barcode Already Used Error |

This table is true for “Check and Track” when activated within same run or within specified check unique barcode period or when presenting a barcode multiple times.

## Barcode Not Unique Error

<figure><img src="../../.gitbook/assets/image (34) (1).png" alt="" width="288"><figcaption></figcaption></figure>

## Barcode Already Used Error

<figure><img src="../../.gitbook/assets/image (35) (1).png" alt="" width="288"><figcaption></figcaption></figure>
