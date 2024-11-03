# Configuring the ODTC



{% file src="../../../../.gitbook/assets/ODTC Device Manager.pdf" %}



To configure the ODTC you need the ODTC device manager.

<figure><img src="../../../../.gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>

this allows you to change configurations of the device and be able to ensure that devices are correctly configured.

After a factory reset the default IP address is `168.254.76.x` with a subnet mask of `255.255.255.0`\
\
Ensure that the network adapter which the ODTC box is connected to is connected where the pc is configured to have an IP address on the same subnet for the example above the ip address would also have to be in the format of `168.254.76.x` and have a unique number for X that is seperate than the device ip address.  the addresses within the 168.254 workspace are called APIPA addresses and are automatically given to devices not accessing the external network. if you want to change this IP address you cannot do so on the device manager but must change it according to the sila pms tool see the following article for this configuration information



#### Step-by-Step Guide to Set Up ODTC with a Static IP Address (Based on Pascal's Notes)

**Prerequisites**

* Access to the ODTC device and the PC that will control it.
* A micro-SD card reader.
* The ODTC Manager application (available from Hamilton).

**1. Resetting Network Settings**

* **Power down the ODTC**: Shut down the ODTC device safely.
* **Remove the SD card**: Locate the micro-SD slot on the ODTC controller box (the slim blue unit). Carefully remove the SD card.
* **Insert SD card into a PC**: Use a PC that has an SD card reader slot or an adapter to access the SD card.

**2. Create a Network Reset File**

* **On the SD card**: Navigate to the SD card’s file system.
* **Create a new file**: In the root directory of the SD card, create a text file named `NetworkReset` (without any file extension).
* **Safely eject the SD card**: Once the file is created, safely eject the SD card from your PC.

**3. Reset the ODTC**

* **Insert the SD card back**: Insert the SD card back into the ODTC.
* **Boot the ODTC**: Power the ODTC back on. This will reset the network settings.

**4. Obtain ODTC Manager**

* **Download and install the ODTC Manager**: Obtain the ODTC Manager software from Hamilton if you haven’t already.
* **Open ODTC Manager**: Launch the ODTC Manager and use the “Device Finder” feature to locate the ODTC on the network.

**5. Identifying IP Address**

* **IP Address Search**: After rebooting, use the ODTC Manager to check for the IP address assigned to the ODTC. You will either find the ODTC in the `192.168.x.x` range (typical for networks with a router) or the `169.254.x.x` range (which Windows assigns when there is no valid IP from DHCP).

**6. Set PC to the Same Subnet**

* **Set PC’s IP Address**:
  * If the ODTC has an IP in the range `169.254.x.x`, configure your PC to be in the same subnet.
  * Example: If the ODTC IP is `169.254.1.5`, assign your PC an IP like `169.254.1.55` (make sure it's not exactly the same as the ODTC IP).
  * **Subnet mask**: Typically set to `255.255.0.0` for the `169.254.x.x` range.

**7. Reboot the Devices**

* **Reboot ODTC**: Once your PC is set to the same subnet, reboot the ODTC for good measure.
* **Restart PC**: Reboot your PC as well to ensure it is using the new IP settings.

**8. Set the Static IP for ODTC**

* **Open ODTC Manager**: Open the ODTC Manager again and connect to the ODTC.
* **Assign a Static IP**:
  * Choose an IP in the range you prefer (e.g., `192.168.1.50`).
  * Set the DNS server to be empty if you do not require internet access for the ODTC.

**9. Reboot and Finalize Settings**

* **Wait a minute**: After setting the new IP, wait about a minute to ensure the settings are applied.
* **Reboot ODTC**: Power cycle the ODTC once more to confirm the settings are in place.
* **Reconfigure PC**: Set your PC’s network settings back to the original configuration (in the same subnet but with a different IP, e.g., `192.168.1.##`).

**10. Test the Connection**

* **Test the static IP**: Try communicating with the ODTC from your PC using the new static IP (`192.168.1.50` or whichever IP you set). Make sure the subnet matches between your PC and the ODTC.

**Troubleshooting Tips**

* **Subnet mismatch**: Ensure the subnet mask is set correctly so that both the PC and the ODTC are on the same subnet.
* **Cable**: For a direct connection between the PC and ODTC without a router, ensure you are using a cross-over Ethernet cable.
* **Device Finder**: Use the ODTC Manager’s "Device Finder" to double-check the ODTC’s IP address if you encounter issues.

This guide should help you successfully configure your ODTC with a static IP address and ensure reliable communication between your PC and the ODTC.
