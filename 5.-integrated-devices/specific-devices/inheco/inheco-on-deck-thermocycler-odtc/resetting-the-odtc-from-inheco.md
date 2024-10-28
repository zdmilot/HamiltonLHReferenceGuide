# Resetting the ODTC (FROM INHECO)

## ResetNetwork explanation

A .txt file with the name of ResetNetwork.txt is needed for the reset of the ODTC. This file is blank but the title is case sensitive and must be placed on the root folder of the µSD card

This .txt file (which is empty as the name is the command) needs to be copied to the µSD card of the PCU and as soon as the PCU starts with this the IP settings are on default (dynamic IP) again. The reset was successful if the .txt file is not on the µSD card anymore (deleted during reset) after you have restarted the PCU. After the reset was performed the ODTC will have dynamic IP address again. If you need it as static IP you need to reconfigure it according to your company standards.
