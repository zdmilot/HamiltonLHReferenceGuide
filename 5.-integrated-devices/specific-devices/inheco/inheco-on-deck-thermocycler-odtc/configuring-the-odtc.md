# Configuring the ODTC

To configure the ODTC you need the ODTC device manager.

<figure><img src="../../../../.gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>

this allows you to change configurations of the device and be able to ensure that devices are correctly configured.

After a factory reset the default IP address is `168.254.76.x` with a subnet mask of `255.255.255.0`\
\
Ensure that the network adapter which the ODTC box is connected to is connected where the pc is configured to have an IP address on the same subnet for the example above the ip address would also have to be in the format of `168.254.76.x` and have a unique number for X that is seperate than the device ip address.  the addresses within the 168.254 workspace are called APIPA addresses and are automatically given to devices not accessing the external network. if you want to change this IP address you cannot do so on the device manager but must change it according to the sila pms tool see the following article for this configuration information
