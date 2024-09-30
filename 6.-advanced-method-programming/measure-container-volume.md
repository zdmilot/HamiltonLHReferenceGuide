# Measure Container Volume

Vector allows you to use a tip to measure the volume within a container.

Why would you do this?

* Troubleshoot false “Insufficient liquid” errors
* Verify you have enough of a particular fluid before starting a pipetting routine
* Verify an amount has been pipetted out of a container (i.e., check the volume before and after pipetting)
*   Check the accuracy of your container definition

    There are three commands available to determine the liquid level in a container:

    * #### GetLastLiquidLevel
      * from the ML\_STAR command set
    * #### MeasureContainerVolume
      * from the HSLML\_STARLib library
    * #### GetContainerVolume
      * from the HSLML\_STARLib library

### Get Last Liquid Level

<figure><img src="../.gitbook/assets/image (36) (1) (1).png" alt=""><figcaption></figcaption></figure>

The GetLastLiquidLevel command returns the _height_ of the liquid level detected during the previous aspirate or dispense step that used LLD.

To get this piece of data, Right-click on the command and select Bind Return Values.

Assign a variable to the value number 3.

<figure><img src="../.gitbook/assets/image (37) (1) (1).png" alt=""><figcaption></figcaption></figure>

To test, use a User Output with this variable. The result is like this:

<figure><img src="../.gitbook/assets/image (38) (1) (1).png" alt=""><figcaption></figcaption></figure>

You then need to use the String library to parse out the heights (111.1, 111.2, 111.3, etc.)

### Measure Container Volume

* Bring the HSLML\_STARLib into your method.
* A Tip Pickup command must already be in the method.
*   Use the MeasureContainerVolume2 command to have the instrument use LLD to detect the liquid surface.

    <figure><img src="../.gitbook/assets/image (39) (1) (1).png" alt=""><figcaption></figcaption></figure>

    Use these values:
* #### ml\_star:
  * Pick ML\_STAR from the drop-down list.
* #### TargetSequence:
  * Pick from the drop-down the sequence that has the liquid you want to measure.
* #### autoIncrement:
  * Type 1, if you plan to use this in a loop and want to march through your sequence.
* #### channelPattern:
  *   In quotes, put in your channel pattern of 1s and 0s, like "11111111".

      Use these values:
* #### cLLDSensitivity:
  * See the Help (click on the "?" button) for values.
* #### pLLDSensitivity:
  * See the Help for values.
* #### MaxHeightDifference:
  * If you select to have both cLLD and pLLD on (values > 0 above), then you must select a mm value for Max Height Difference.
  * Note: you must use 300ul non-filtered tips for this command.

### Get Container Volume

Use GetContainerVolume to retrieve the data generated with the MeasureContainerVolume command.

GetContainerVolume returns the volume in ml of one channel only. So put this command within a loop. Loop a number times equal to the number of channels that did the measuring, and set the value in the GetContainerVolume to the loop counter variable.

Use the \[Bind return value to] field to create a variable for the volume that is returned.

<figure><img src="../.gitbook/assets/image (40) (1) (1).png" alt=""><figcaption></figcaption></figure>

Don’t forget to convert the returned volume from _ml to ul_, depending on what you need to do with that volume data.

Be aware:

If you are using these commands with variable channel pattern, the last liquid level or volume measured is retained in memory.

Don’t make a mistake. You may need to refresh your variables (reset your volumes to zero) to make sure you don’t get erroneous results.

### Troubleshooting

If you find the calculated volumes don’t seem accurate:

* Verify position of bottom of container (use probe to check z=0)
* Adjust container definition
* Check submerge depth
