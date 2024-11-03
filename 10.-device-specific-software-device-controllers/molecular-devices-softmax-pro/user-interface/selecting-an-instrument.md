# Selecting an Instrument

Use the Instrument Connection dialog to connect the SoftMax Pro Software to the microplate reader. See the instrument user guide for instructions to connect the cables between the computer and the instrument. See Supported Instruments and Detection Cartridges on page 316.

**Note:** You can use the software without a physical connection between the computer and the instrument in Offline mode to do data analysis or in Simulator mode to create protocols.

![](<../../../.gitbook/assets/0 (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png>)

![](<../../../.gitbook/assets/1 (2) (1).jpeg>)

To select an instrument:

1. Power on the instrument and wait for the instrument initialization process to complete.
2. In the Ribbon, select the Home tab and click **Instrument** to display the Instrument Connection dialog.
3. If the instrument does not appear in the Available Instruments list, click **Refresh**.
4. In the **Available Instruments** list:

![](<../../../.gitbook/assets/2 (22).png>) Select the communication port to which you connect the instrument or select

**Offline**.

![](<../../../.gitbook/assets/3 (2) (1) (1) (1) (1).png>) To work offline for data analysis, select **Offline**, then click the **Reader** drop-down and select an instrument.

![](<../../../.gitbook/assets/4 (2) (1) (1) (1).png>) To work in simulator mode to create protocols, select **Offline**, click the **Reader** drop- down and select an instrument, then select the **Simulator On** check box.

1. Click **OK**. The Home tab displays an icon for the instrument you select.

![](<../../../.gitbook/assets/5 (1) (1) (1) (1) (1) (1) (1) (1) (1).png>)

**Note:** The ![](<../../../.gitbook/assets/6 (2) (1) (1) (1).png>) icon is for troubleshooting purposes only.

### Instrument Connection Status

![](<../../../.gitbook/assets/7 (1) (1) (1).jpeg>)In the Ribbon, on the Home tab, the instrument icon indicates the status of the connection between the computer and the instrument. If the status indicates the instrument is disconnected, make sure that the instrument is powered on and that the cables between the computer and the instrument are secure.

*

### Instrument Calibration

You should calibrate some instruments before use. See Instrument Calibration on page 352.

### SpectraMax Paradigm Considerations

When you first install the SpectraMax Paradigm, you must remove hardware transport locks as described in the instrument user guide. As a safety precaution, the SoftMax Pro Software controls internal locks to prevent the drawers from opening until the software detects and initializes the instrument. See Removing Software Locks on page 328.

### SpectraMax iD3 and SpectraMax iD5 Considerations

When you use the SoftMax Pro Software to operate the SpectraMax iD3 or SpectraMax iD5, your company network configuration could prevent the connection between the computer and the instrument.

You can use the Ethernet cable to connect the computer directly to the instrument or you can connect the SpectraMax iD3 and SpectraMax iD5 to your company intranet. See SpectraMax iD3 Multi-Mode Microplate Reader on page 317 and SpectraMax iD5 Multi- Mode Microplate Reader on page 320.

You may have to do the following to select the SpectraMax iD3 and SpectraMax iD5:

1. On the SpectraMax iD3 and SpectraMax iD5 instrument touchscreen, navigate to the

**Maintenance** page **System Information** tab and note the instrument IP address.

1. In the SoftMax Pro Software, click ![](<../../../.gitbook/assets/10 (1) (1) (1).jpeg>) to open the Application menu.
2. At the bottom of the Application menu, click the **Options** button to display the SoftMax Pro Options dialog.
3. In the list on the left, click **SpectraMax iDx Control**.
4. Select the **Enable Control of SpectraMax iDx Instruments** check box.
5. Enter the IP address of the instrument in one of the fields. There are five fields so you can enter up to five IP addresses.
6. Click **OK**.
7. Select the **Home** tab and click **Instrument** to display the Instrument Connection dialog.
8. Click **Refresh** if needed and the SpectraMax iD3 and SpectraMax iD5 instruments should appear. If the instrument does not appear, you may have to work with your company network administrator to confirm that your company network configuration permits the communication between the computer and the instrument.

When you use a computer running the SoftMax Pro Software to operate the instrument, the instrument touchscreen is locked.

For users that use the SoftMax Pro Software - GxP edition to operate the instrument, the user must have the following permission to lock and unlock the instrument touchscreen:

![](<../../../.gitbook/assets/11 (15).png>) SoftMax Pro Software - GxP edition version 7.0.3 users require the Sign Signature permission.

![](<../../../.gitbook/assets/12 (1) (1) (1) (1) (1) (1) (1) (1) (1).png>) SoftMax Pro Software - GxP edition version 7.1.1 and later users require the Lock/Unlock Instrument permission.

In the Ribbon, on the GxP tab, users with appropriate permission can use the following icons to lock and unlock the instrument touchscreen:

![](<../../../.gitbook/assets/13 (1) (1) (1) (1) (1) (1) (1) (1).png>) Click ![](<../../../.gitbook/assets/14 (1).jpeg>) **GxP Mode On** to lock the instrument touchscreen and operate the instrument from the computer running the SoftMax Pro Software in GxP mode. This locks the instrument touchscreen for all users and you must operate the instrument from a computer running the SoftMax Pro Software - GxP edition.

![](<../../../.gitbook/assets/15 (12).png>) Click ![](<../../../.gitbook/assets/16 (1) (1).jpeg>) **GxP Mode Off** to release the lock from the instrument touchscreen and allow users to use the instrument touchscreen to run experiments.

![](<../../../.gitbook/assets/17 (1) (1) (1) (1) (1) (1) (1).png>)

**Note:** The instrument remains locked until the user with the appropriate permission

clicks ![](<../../../.gitbook/assets/18 (1) (1) (1).jpeg>) **GxP Mode Off** to stop the GxP mode. You cannot use the Instrument Connection dialog to disconnect from a SpectraMax iD3 and SpectraMax iD5 that is locked in GxP mode.
