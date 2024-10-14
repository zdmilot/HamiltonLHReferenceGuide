# Invalid class string (0x23 - 0x2 - 0x39)

## How to Troubleshoot the HSLStatusWindow Library Issue on Hamilton VENUS

If you're running into an issue with the **HSLStatusWindow** library after migrating a script from a Hamilton STARlet to a larger STAR, you're not alone. Users have reported similar issues when running methods using the HSLStatusWindow library on the STAR. Below, we’ll walk you through common causes and solutions for this error.

#### Common Error: Invalid Class String

The most common issue is receiving an error message like the following:

> **HxHslRunControl2: An error occurred while running Vector. The error description is C:\Program Files (x86)\HAMILTON\Library\HSLStatusWindow.hsl(32): Invalid class string (0x23 - 0x2 - 0x39)**

This error typically occurs when VENUS 4.5 is unable to load the plugin properly.

#### Steps to Troubleshoot

1.  **Check the Installer**

    The error usually points to a problem with the **HSLStatusWindow** library not being installed correctly. Ensure that you’ve run the installer for the library on the STAR, especially if you imported the library via a PKG file. Without the actual installer being run, VENUS may fail to load the necessary files.

    * Verify that you have the correct installer. There are multiple "Status Window" libraries, so identifying the correct one is crucial.
    * If you're unsure about the correct installer, consider getting the original install media for the STAR.\

2.  **Uninstall and Reinstall the Library**

    If the error persists, try **uninstalling** the library and then **reinstalling** it. Here’s how you can approach it:

    * **Uninstall** the current HSLStatusWindow library.
    * Obtain a new copy of the installation files.
    * Reinstall the library from the original installer to avoid corrupted or incomplete installations.\

3. **Check Permissions**\
   Sometimes, the installer may fail due to insufficient permissions on the computer. Make sure that you have administrative rights during installation and check if any security software may be interfering with the library installation.\

4. **Disable the HSLStatusWindow**\
   If reinstalling the library does not work or if you're in a time-sensitive situation, a temporary workaround is to **disable the HSL Status Window** commands in your script. While this removes the ability to use the status window, it may allow your method to run successfully.\

5. **Convert the Deck Type**\
   Another aspect to be mindful of during migration is the deck type. If your script runs fine in simulation but fails during real-time execution, double-check that the correct **deck type** for the STAR is selected. A mismatched deck type can cause unexpected errors during method execution.

***

Original Labautomation.io post about this:\
\
\
[Lab Automation Forums](https://labautomation.io/)

## [HSLStatusWindow library issue](https://labautomation.io/t/hslstatuswindow-library-issue/182)

[Hamilton (Venus)](https://labautomation.io/c/hamilton-venus/7)[MikeMueller](https://labautomation.io/u/MikeMueller) August 30, 2022, 12:57am1

> I am working on a Hamilton where we have migrated a script from a STARlet to a larger STAR. Most everything is running ok through the simulator on the STAR, however, we are running into issues with the HSLStatusWindow library on the STAR. It runs fine on the STARlet. Whether we use the HSL Status Window Init command part of it or one of the commands that writes to the Status Window, we receive an error message HxHslRunControl2 “An error occured while running Vector. The error description is C:\Program Files (x86)\HAMILTON\Library\HSLStatusWindow.hsl(32) : Invalid class string (0x23 - 0x2 - 0x39).” We are running Venus 4.5. We tried uninstalling and reinstalling the library. Then also tried reinstalling the library from the original install disc, but no luck. If I put an HSLStatusWindow.Init command after Initalize at the beginning of a test script, it immediately fails. If I disable the HSL Status Window commands, it runs. Any suggestions?



[KyleCook\_GeNovu](https://labautomation.io/u/KyleCook\_GeNovu) August 30, 2022, 1:30am

> I’ve seen that error when I import a Method containing the StatusWindowLibrary but I don’t also run the Installer on a machine that it was never installed on. You said you tried uninstalling and reinstalling the library though so I’m not sure. The error indicates it is failing to load the plugin.
>
> <img src="https://labautomation.io/uploads/default/original/1X/f47f5a525a273e192d8d0784b0c4848c35eca455.png" alt="image" data-size="original">
>
>



[cyancey](https://labautomation.io/u/cyancey) August 30, 2022, 1:42am3

> 9 out of 10 times that “invalid class string” error is because the library was imported with the PKG file but the installer for the library wasn’t installed.
>
> There are a bunch of different “status window” library’s so it’s tricky to know which one is the correct installer. Worst case you just remove those steps and use the protocol without a status window.
>
> Also, unrelated but make sure you convert the deck type as well. It’ll be fine in sim but will error out when trying to run it in real time.



[EricSindelar\_Hamilton](https://labautomation.io/u/EricSindelar\_Hamilton) August 30, 2022, 12:53pm4

> Hi Mike,
>
> I agree with Cole and Kyle. Something is likely going on with the installer and your computer/permissions that prevent it from registering.
>
> As a side note, for our standardized solutions at Hamilton, we typically use the ASW status dialog library that gets installed with the [ASW GUI installer](https://download.hamiltonsupport.com/wl/?id=4hqcYxNQB0Y19sjltpd3atnNLIrQIwpl). ASW stands for Application SoftWare so any library with that prefix is authored by our internal software team.
>
> \-Eric



