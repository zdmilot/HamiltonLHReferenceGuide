# Hamilton Vantage CAP - HEPA Filtration

This is the help file for the Hamilton Vantage CAP Venus driver. All information regarding the driver's functions and version history will be found in this file.

***



This CAP is monitored and controlled via venus and is installed typically within the AC power of the device itself. This means if the device goes offline or needs to be power cycled then the CAP will shut off. To avoid this you can plug the CAP independently to the outlet or power bank to be able to retain the power state throughout the power cycle. Do know that when using a system with two CAPs integrated one works as the master controller and the other works as a proxy. This allows for a single TCP/IP connection to be made to the CAP. In this instance there might be issues with connecting to the devices upon power cycle if they are using outside power. if this happens power cycle them accordingly
