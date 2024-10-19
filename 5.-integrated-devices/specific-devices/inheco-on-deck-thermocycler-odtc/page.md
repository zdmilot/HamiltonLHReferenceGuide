# Page

## Introduction

The Inheco ODTC device is a SiLA compliant third-party device and therefore needs to be installed into a network.

The following chapters describe the installation of the device for the Hamilton standard environment.

In case the network topology is different to the one described here, get in contact with Hamilton!



<details>

<summary>Prerequisites</summary>

### Router

The Inheco ODTC device is shipped with a router where all ODTC devices and also the computer is connected to:



<img src="../../../.gitbook/assets/image (25) (1) (1) (1).png" alt="" data-size="original">

There are 10 network connections named ETH1 to ETH10 which have to be used as follows:

* ETH1  : Do not use!
* ETH2  : computer 1
* ETH3  : computer 2 (if available)
* ETH4  : computer 3 (if available)
* ETH5  : computer 4 (if available)
* ETH6  : ODTC device 1
* ETH7  : ODTC device 2 (if available)
* ETH8  : ODTC device 3 (if available)
* ETH9  : ODTC device 4 (if available)
* ETH10: Do not use!

### Computer

The computer shipped with the STAR is equipped with 2 network adapters.

Connect one of the two adapters to the router, the other to the customer's network.

</details>

<details>

<summary>Retrieving device IP address(es)</summary>

Each ODTC device uses an IP address to communicate with the computer.

The router automatically assigns IP adresses to the devices using DHCP.

### Computer setup for retrieving the ODTC IP address(es)

To be sure to configure the right adapter, disconnect the customer network from the computer before executing the follwing steps:

* Click 'Start', then 'Control Panel'
* Click on 'Network and Sharing Center'
* Click on 'Change adapter settings':\
  ![](<../../../.gitbook/assets/image (18) (1) (1) (1) (1).png>)
* Double-click the adapter that is shown as enabled:\
  ![](<../../../.gitbook/assets/image (19) (1) (1) (1) (1).png>)
* Click on 'Properties'
* Select 'Internet protocol version 4 (TCP/IP v4)
* Set the Properties to 'Obtain an IP adress automatically':\
  ![](<../../../.gitbook/assets/image (20) (1) (1) (1) (1).png>)
* Close the two dialogs with OK
* Click on 'Details':\
  ![](<../../../.gitbook/assets/image (21) (1) (1) (1) (1).png>)
* Note the shown IP address for further use in Network Settings

### Retrieving ODTC device IP address(es)

To retrieve the IP address of each ODTC device, execute the following steps:

* start the application 'DeviceFinder (xxxxx).exe' (xxxxx is a five-digit revision number) located in the library directory.
* execute the following steps for each ODTC device:
  * switch on the ODTC device.
  * wait at least 60 seconds to see the retrieved ip address.
  * if address is not found automatically, click button 'Find Device via Name/IP' and supply the string ODTC\_XXXXXX where XXXXXX represents the last 6 characters of the device's MAC address.
  * the string to provide may be found on the label SiLA Service Configuration located on the device controller.
  * note the shown IP address for further use in the device driver software.

</details>



###





## Retrieving device IP address(es)

##

## Network settings



To use the ODTC devices, the network adapter that is connected to the router has to be configured to use a fixed IP address.

### Computer setup for usage of the ODTC devices

To be sure to configure the right adapter, disconnect the customer network from the computer before executing the follwing steps:

* Click 'Start', then 'Control Panel'
* Click on 'Network and Sharing Center'
* Click on 'Change adapter settings':\
  ![](<../../../.gitbook/assets/image (22) (1) (1) (1).png>)
* Double-click the adapter that is shown as enabled:\
  ![](<../../../.gitbook/assets/image (23) (1) (1) (1).png>)
* Click on 'Properties'
* Select 'Internet protocol version 4 (TCP/IP v4)
* Set the Properties to 'Use the following IP address':\
  ![](<../../../.gitbook/assets/image (24) (1) (1) (1).png>)
* Set the value of 'IP-address' to the one of the computer that you noted in chapter Retrieving device IP address(es)
* Set the value of 'Subnet mask' to '255.255.255.0' (filled automatically when you enter the last digit of the IP address)
* Leave the value of 'Default gateway' empty !
* Close the two dialogs with OK
* Close the property dialog with button 'Close'

If you previously unplugged the customer's network cable, connect it to the adapter where you unplugged it.
