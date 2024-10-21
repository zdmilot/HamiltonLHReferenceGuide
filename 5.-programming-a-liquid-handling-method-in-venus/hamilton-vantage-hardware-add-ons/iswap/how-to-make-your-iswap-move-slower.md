# How to make your iSWAP move slower

How to make your iSWAP slowly

To reduce the speed of the iSWAP, you can use firmware commands to lower the default speed values of each axis. That means, you are able to slow down individual axis while leaving all other movements quick.

To do so, enter a firmware command in your method:

![](<../../../.gitbook/assets/0 (8) (1).png>)

The Command “R0AA” is to set the new values (R0 is the CAN bus Node ID of the iSWAP, AA is to store values down in the instruments eeprom)

“zv01000” reduces the speed of the Z-Axis to 01000 increments per second&#x20;



|                              | parameter to send | available range | default value |                           |
| ---------------------------- | ----------------- | --------------- | ------------- | ------------------------- |
| _Z drive commands_           | zv#####           | 50..10000       | 09500         | max. velocity \[incr/sec] |
| _Rotation drive commands_    | wv####            | 20..75000       | 55000         | max. velocity \[incr/sec] |
| _Wrist twist drive commands_ | tv#####           | 20..65000       | 48000         | max. velocity \[incr/sec] |
| _Gripper drive commands_     | gv####            | 20...9999       | 9000          | max. velocity \[incr/sec] |



It is very important that you use exactly the same number as characters as given in the default value,

e.g. 04500 instead of 4500.

It is also extremely important that you set back the speed after the processed step AND in the OnAbort submethod. Otherwise, the EEPROM of the instrument keeps these slow values for all other methods.

## Example:

![](<../../../.gitbook/assets/1 (10) (1).png>)
