# BioNex HiG Centrifuge

The BioNex Solutions HiG 4 Automated Centrifuge is specifically designed for integration and use within a robotic laboratory. This centrifuge ensures vibrational stability even with imbalances of up to 50 grams and features a dual-bucket design which accommodates a wide range of microplate configurations, including deep well and filter plate assemblies.

**Basic Usage**

The basic flow of the driver should look something like this:

* Connect
* Home
* Spin
* IsSpinning (poll until IsSpinning is false)
* Disconnect

