# HHS Library

The HHS library provides several functions to control the HHS, such as shaking and heating settings. The functions can be integrated into standard methods of the ML STAR instrument.

To install the library execute the file “InstallHHSLibrary\_Vx.x.exe”. The file can be obtained from a local Hamilton Representative.

After confirming the installation of the addition, the heater shaker library will be installed automatically.

<table data-header-hidden><thead><tr><th width="145"></th><th></th></tr></thead><tbody><tr><td><img src="../.gitbook/assets/image (10) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" data-size="original"></td><td><p>NOTE</p><p><em>The library requires the following Microsoft Package, which will be installed automatically during the setup procedure:</em></p><p><em>Microsoft Visual C++ 2005 Redistributable Package (x86).</em></p></td></tr></tbody></table>



<table><thead><tr><th width="241">Command</th><th width="99">Icon</th><th>Action Performed</th></tr></thead><tbody><tr><td>Create Star Device</td><td><img src="../.gitbook/assets/image (634).png" alt="" data-size="original"></td><td>Creates the device number which must be used as input parameter for each function of this library.</td></tr><tr><td>Create USB Device</td><td><img src="../.gitbook/assets/image (635).png" alt="" data-size="original"></td><td>Creates the device number which must be used as input parameter for each function of this library.</td></tr><tr><td>Terminate</td><td><img src="../.gitbook/assets/image (636).png" alt="" data-size="original"></td><td>The connection to the ML STAR instrument and/or USB device is terminated. Note that this function does not stop the heating or shaking process of the heater shaker.</td></tr><tr><td>Start Shaker</td><td><img src="../.gitbook/assets/image (637).png" alt="" data-size="original"></td><td>This function starts the shaking process. If necessary, the heater shaker will be initialized. Before the shaking process is started, the plate is locked. Shaking has to be stopped by the “Stop Shaker” Command. Terminating the connection will not stop shaking. However, shaking is stopped upon method abort.</td></tr><tr><td>Start All Shaker</td><td><img src="../.gitbook/assets/image (638).png" alt="" data-size="original"></td><td>Start shaking on all initialized shakers. Shakers that have not been initialized are not addressed. The plates are locked before the shaking process.</td></tr><tr><td>Start Shaker Timed</td><td><img src="../.gitbook/assets/image (639).png" alt="" data-size="original"></td><td><p>Start shaking for an indicated time. If necessary, the heater shaker will be initialized. Before the shaking process is started, the plate is locked.</p><p>After shaking, the plate lock has to be opened with the “SetPlateLock” Function.</p></td></tr><tr><td>Start All Shaker Timed</td><td><img src="../.gitbook/assets/image (640).png" alt="" data-size="original"></td><td>Start shaking on all initialized heater shakers for an indicated time. The plates are locked before the shaking process. After shaking, the plate lock has to be opened with the “SetPlateLock” Function.</td></tr><tr><td>Wait For Shaker</td><td><img src="../.gitbook/assets/image (641).png" alt="" data-size="original"></td><td>Wait for the heater shaker to finish. The plate is unlocked after shaking has been stopped. This command is only used in combination with “Start Shaker Timed” or “Start All Shaker Timed”.</td></tr><tr><td>Stop Shaker</td><td><img src="../.gitbook/assets/image (642).png" alt="" data-size="original"></td><td>Stop shaking and unlock plate.</td></tr><tr><td>Stop All Shaker</td><td><img src="../.gitbook/assets/image (643).png" alt="" data-size="original"></td><td>Stop shaking on all heater shakers. The plates will be unlocked subsequently.</td></tr><tr><td>Set shaker parameter</td><td><img src="../.gitbook/assets/image (644).png" alt="" data-size="original"></td><td>Set shaking parameters, such as shaking direction, shaking speed and acceleration.</td></tr><tr><td>Get Shaker Parameter</td><td><img src="../.gitbook/assets/image (645).png" alt="" data-size="original"></td><td>Get shaking parameters, such as shaking direction, shaking speed and acceleration.</td></tr><tr><td>Start Temp Control</td><td><img src="../.gitbook/assets/image (646).png" alt="" data-size="original"></td><td>Start temperature control on the heater shaker (must be greater than ambient temperature plus 5°C). Temperature control has to be stopped by the “Stop Temp Control” Function or will be constantly on. Terminating the connection will not stop heating. However, heating is stopped upon method abort.</td></tr><tr><td>Wait for Temp Control</td><td><img src="../.gitbook/assets/image (647).png" alt="" data-size="original"></td><td>Wait until the heater shaker has reached the set temperature. This function will wait until the defined temperature is reached and is stable for 180 seconds. Only then, the method will continue.</td></tr><tr><td>Stop Temp Control</td><td><img src="../.gitbook/assets/image (650).png" alt="" data-size="original"></td><td>Stop temperature control of the heater shaker.</td></tr><tr><td>Get Temperature</td><td><img src="../.gitbook/assets/image (651).png" alt="" data-size="original"></td><td>Receive the current temperature of the heater shaker.</td></tr><tr><td>Set Temperature Parameter</td><td><img src="../.gitbook/assets/image (649).png" alt="" data-size="original"></td><td>Set parameters for temperature control. In most cases, the default settings can be used and this function is not needed.</td></tr><tr><td>Get Temperature Parameter</td><td><img src="../.gitbook/assets/image (652).png" alt="" data-size="original"></td><td>Receive the parameters for temperature control.</td></tr><tr><td>Get Temperature State</td><td><img src="../.gitbook/assets/image (653).png" alt="" data-size="original"></td><td>Get the status of the temperature control. The temperature should be within a defined temperature range.</td></tr><tr><td>Send Firmware Command</td><td><img src="../.gitbook/assets/image (654).png" alt="" data-size="original"></td><td>Send a firmware command to the heater shaker.</td></tr><tr><td>Set Plate Lock</td><td><img src="../.gitbook/assets/image (655).png" alt="" data-size="original"></td><td>Open or close the plate lock. The plate is always locked automatically before shaking is started, but this command is useful to position and fix the plate in the center of the flat bottom adapter before pipetting, or when using the commands “Start Shaker Timed” or “Start All Shaker Timed” as these commands do not open the plate lock after shaking.</td></tr><tr><td>Set Simulation</td><td><img src="../.gitbook/assets/image (656).png" alt="" data-size="original"></td><td>Set run mode to simulation for all functions in this library. In simulation mode, no signals are sent to the HHS.</td></tr><tr><td>Set USB Trace</td><td><img src="../.gitbook/assets/image (657).png" alt="" data-size="original"></td><td>Turn on/off tracing of communication to and from USB port.</td></tr><tr><td>Begin Monitoring</td><td><img src="../.gitbook/assets/image (658).png" alt="" data-size="original"></td><td>Start to monitor the performance of the HHS. This function monitors the temperature and speed in the background. The tolerated range of the temperature can be set with the function “SetTempParameter”. The tolerated range of speed is defined in this function. The status of the temperature can be requested in a defined interval and is then written to the trace file.</td></tr><tr><td>End Monitoring</td><td><img src="../.gitbook/assets/image (659).png" alt="" data-size="original"></td><td>Get the shaking speed of a HHS.</td></tr><tr><td>Get Shaker Speed</td><td><img src="../.gitbook/assets/image (660).png" alt="" data-size="original"></td><td>Get the shaking speed of a HHS.</td></tr><tr><td>Get Serial Number</td><td><img src="../.gitbook/assets/image (661).png" alt="" data-size="original"></td><td>Get the serial number a HHS.</td></tr><tr><td>Get Firmware Version</td><td><img src="../.gitbook/assets/image (662).png" alt="" data-size="original"></td><td>Get the firmware version of a HHS.</td></tr></tbody></table>

\