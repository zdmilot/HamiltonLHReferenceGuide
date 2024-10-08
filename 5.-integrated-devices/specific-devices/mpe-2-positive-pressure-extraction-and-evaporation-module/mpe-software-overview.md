# \[MPE]² Software Overview

When used as a benchtop device, the \[MPE]² utilizes Hamilton’s Vector software. This software is used primarily to control Hamilton’s liquid handling platforms, but it can also be used to program methods for the \[MPE]² as a benchtop device.&#x20;

The software is composed of several different editors. The following editors are relevant for the \[MPE]² when used as a benchtop device:&#x20;

* The Method Editor allows the user to create custom methods that drive the \[MPE]². It is accessed via the Hamilton Method Editor icon on the desktop.\
  ![](<../../../.gitbook/assets/image (22) (1).png>)
* The System Configuration Editor allows the user to change the system settings. From the Method Editor, click Tools > System Configuration Editor.\
  ![](<../../../.gitbook/assets/image (23) (1).png>)\
  \


## Running a Method

The following procedure applies to an \[MPE]² used as a benchtop device. If using the \[MPE]2 as part of an integration with a liquid handling platform, refer to the Operator’s Manual for that platform, as each platform has different loading procedures.

1. Turn on the Control Box, then the ACME if the Evaporator or Reagent Fill Modules will be used. Make sure to turn on the Control Box first, or the \[MPE]² will only recognize the Logistics Module.
2. Flush the tubes with deionized water or methanol for 2-5 minutes. The tubes must be flushed at the beginning and end of every day. Refer to section 7.3 for details. WARNING: Verify that the waste bottle is empty before starting a run.
3. Prepare the required filter and collection plates for the run. To make sure that the filter and collection plates are compatible with the \[MPE]², refer to section 5.3.
4. Open the Hamilton Run Control program and use File > Open to find the desired method. Methods are stored by default in C:\Program Files (x86) > Hamilton > Methods.
5. Click on View and select the desired view windows. Once these windows are opened, they can be resized and rearranged as necessary, as shown in Figure 5–4. The views can also be turned on and off by clicking the appropriate toggle buttons on the right side of the icon bar. \
   ![](<../../../.gitbook/assets/image (24) (1).png>)
   1. The Method View shows which steps are being performed.&#x20;
   2. The Deck View normally shows a colorized model of the deck as the method runs. A deck layout is only present when integrated with an instrument running the Vector software.&#x20;
   3. The Trace View shows the traces for each step as they are executed.\

6. Compare the deck view with what is on the deck of the \[MPE]² and make sure they match before starting the method. Click on the deck and use the mouse wheel to zoom in on the deck view, or use the view buttons in the View menu.&#x20;
7. Click the Start button at the top of the Run Control window. The F5 key can also be used to start a method. Figure 5–4: Run Control buttons&#x20;
8. To pause a run, click the blue Pause button at the top of the Run Control window. The \[MPE]² will finish the last command it received and then come to a stop. To resume after a pause, click the Pause button again.&#x20;
9. To abort a run, click the red Abort button at the top of the Run Control window. A confirmation dialog will appear. Click OK. The \[MPE]² will finish the last command it received, come to a stop, and the method will be aborted. Aborted methods must be restarted from the beginning.
