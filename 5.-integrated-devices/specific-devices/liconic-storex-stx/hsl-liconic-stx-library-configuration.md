# HSL Liconic STX Library Configuration

Configure the STX devices as follows:

&#x20;

## Defining COM port for Units

Open the file "Unit1.LNI" and "Unit2.LNI" resp. (in the HAMILTON\Bin directory) in a text editor like notepad. Then change the line UnitComPort=x to the desired COM port number. UnitID=1 or UnitID=2 resp. is the unit ID needed calling library functions to a device. Do not change the UnitId's!

&#x20;

## Defining Inventory partitions

Open the file "Unit1.LNI" and "Unit2.LNI" resp. (in the HAMILTON\Bin directory) in a text editor like notepad. Then name the partition and assign a cassette or a series of cassettes. For example:

> `[Partitions]`\
> `A=1`\
> `B=2-4`

In the file fragment above partition "A" holds cassette 1, partition "B" holds cassettes 2, 3, and 4. Next be sure that the part "CassettesConfiguration" holds the entry "UseCassConfTable=0" as follows:

> `[CassettesConfiguration]`\
> `UseCassConfTable=0`&#x20;

## Setting TCP port number

Open the file "DriverConfig.LNI" (in the HAMILTON\Bin directory) in a text editor like notepad. Then change the line port=x to the desired port number.

## Restarting the server

After changing any LNI-file, do the following:

1\. Left click on the Liconic GUI trayicon

![](blob:https://app.gitbook.com/f63396ad-ab09-4c5c-98cb-96e582aad4d6)

2\. Close the Liconic GUI

![](blob:https://app.gitbook.com/c6006ccb-22e8-49b1-8720-746acb969b79)

3\. Restart the Liconic GUI (located in common startup folder)

![](blob:https://app.gitbook.com/bd113b31-3b8b-4f73-92f0-b2d55a52032e)

