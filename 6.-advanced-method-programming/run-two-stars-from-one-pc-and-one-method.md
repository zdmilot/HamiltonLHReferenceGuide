# Run Two STARs from One PC and One Method

‌Overview

This guide will assist the user in updating the computer registry to allow for running two STARs within one method on one PC. Administrator privileges are required to make registry modifications.

\


‌How to Run Two STARs from One Method on One PC

1.  ## Open the Registry Editor

    1.  Select the Start Menu then type in “regedit” and select Registry Editor when it appears



    <figure><img src="../.gitbook/assets/image (440).png" alt="" width="200"><figcaption></figcaption></figure>
2. ## Create a second ML\_STAR Instrument
   1. Browse to the ‘ML\_STAR’ registry “Computer\HKEY\_LOCAL\_MACHINE\SOFTWARE\WOW6432Node\Phoenix\Instr uments\ML\_STAR”
   2.  Right-click on the ‘ML\_STAR’ registry and select ‘Export’. Name and save the exported .reg file

       <figure><img src="../.gitbook/assets/image (441).png" alt="" width="432"><figcaption></figcaption></figure>
   3.  Right-click on the ‘ML\_STAR’ registry and select Rename to change the name to ‘ML\_STAR\_2’\


       <figure><img src="../.gitbook/assets/image (442).png" alt="" width="121"><figcaption></figcaption></figure>
   4.  Go to File > Import… and import the previously exported ‘ML\_STAR’ registry


3. Update ‘ML\_STAR\_2’ registry
   1.  Select the ‘ML\_STAR\_2’ registry, and modify the ‘(Default)’ parameter to be ‘Microlab® STAR (no. 2)’

       <figure><img src="../.gitbook/assets/image (443).png" alt=""><figcaption></figcaption></figure>
   2.  Expand the ‘ML\_STAR\_2’ registry and go to the ‘InstCfgFile’ registry. Modify the ‘(Default)’ parameter to be ‘ML\_STAR\_2.cfg’

       <figure><img src="../.gitbook/assets/image (444).png" alt=""><figcaption></figcaption></figure>
   3.  Close the Registry Editor

       \

4. Prepare ‘ML\_STAR\_2’ Config Files
   1.  In File Explorer, browse to the “C:\Program Files (x86)\HAMILTON\Config” folder\


       <figure><img src="../.gitbook/assets/image (447).png" alt="" width="251"><figcaption></figcaption></figure>
   2.  Locate the ‘ML\_STAR.cfg’ and ‘ML\_STAR\_Simulator.cfg’ files.

       Make copies of both files in the same folder
   3. Rename to ‘ML\_STAR\_2.cfg’ and ‘ML\_STAR\_2\_Simulator.cfg’, respectively
   4. Open the ‘HxCfgFilConverter.exe’ software found in the “C:\Program Files (x86)\HAMILTON\Bin” folder
   5.  In the menu on the left, browse to the “C:\Program Files (x86)\HAMILTON\Config” folder, then look for the ‘ML\_STAR\_2.cfg’ file in the menu on the right

       \






       <figure><img src="../.gitbook/assets/image (448).png" alt="" width="552"><figcaption></figcaption></figure>
   6.  Click on the ‘Convert to ASCII’ button on the bottom of the window. The status bar below the button should show ‘success’ when the conversion is complete. Leave the ‘HxCfgFilConverter’ software open and proceed to the next step\


       <figure><img src="../.gitbook/assets/image (449).png" alt="" width="282"><figcaption></figcaption></figure>
   7. Return to the “C:\Program Files (x86)\HAMILTON\Config” folder and open the ‘ML\_STAR\_2.cfg’ file. This can be opened in Notepad or another text editor of choice
   8.  Find the ‘SERIAL\_NUMBER’ key and change to “02”:

       <figure><img src="../.gitbook/assets/image (450).png" alt=""><figcaption></figcaption></figure>

       *   In the ‘ML\_STAR\_2.cfg’ file, search for the word “serial” using the Find function (in Notepad, this is found under the Edit menu or by clicking “Ctrl

           \+ F” on the keyboard)
       * The Find function will jump down to the ‘SERIAL\_NUMBER’ key, which will have a value of “00”. Change this value to “02”
       * Save and close the ‘ML\_STAR\_2.cfg’ file
   9.  Return to the ‘HxCfgFilConverter.exe’ software and confirm that the ‘ML\_STAR\_2.cfg’ file is still selected. Then click ‘Convert to Binary’ and confirm success from the status bar below the button

       <figure><img src="../.gitbook/assets/image (451).png" alt=""><figcaption></figcaption></figure>

       \

5.  ## Modify the second STAR’s USB Serial Number

    \*\*NOTE: before proceeding, only one STAR should be connected to the PC as all STAR’s have a default USB Serial Number of “00”

    1. Connect the second STAR’s USB cable to the PC and power on the STAR
    2. Open the Microlab® STAR Service Software and confirm the second STAR connects properly
    3.  Go to Control > Single command

        <figure><img src="../.gitbook/assets/image (452).png" alt=""><figcaption></figcaption></figure>
    4.  In the window that pops up, send the following commands to the STAR in this order, confirming successful response on each:

        * C0AP
        * C0Anan02
        * C0AP

        <figure><img src="../.gitbook/assets/image (453).png" alt="" width="304"><figcaption></figcaption></figure>
    5.  Exit the STAR Service Software

        \

6. ## Confirm both STARs can connect
   1. Power cycle the second STAR
   2. Connect the first STAR’s USB cable to the PC and power on the first STAR
   3. Open the Microlab® STAR Service Software
   4.  Go to Settings > Port Settings. In the window that pops up, select USB then click the Settings button

       <figure><img src="../.gitbook/assets/image (454).png" alt="" width="286"><figcaption></figcaption></figure>

       <figure><img src="../.gitbook/assets/image (455).png" alt="" width="224"><figcaption></figcaption></figure>
   5.  Confirm that both STARs appear in the Device List\


       <figure><img src="../.gitbook/assets/image (456).png" alt="" width="396"><figcaption></figcaption></figure>
   6. Double-click the first STAR in the Device List (Serial Number: 00), then click the OK button. Make sure to click the OK button on all parent windows to return to the STAR Service Software Main Window, this will allow the software to connect to the first STAR.
   7.  Exit the STAR Service Software


7. Make and test a method in Method Editor
   1. Open Method Editor and create a new Method
   2.  In the Deck Layout Editor, go to the Devices Tab and select Add New Instrument. In the drop-down confirm both ‘ML\_STAR’ and ‘ML\_STAR\_2’ are listed as options

       <figure><img src="../.gitbook/assets/image (457).png" alt="" width="244"><figcaption></figcaption></figure>
   3.  Add both STARs to the Deck Layout and confirm that tabs for each are present on the bottom of the Deck Layout Editor window

       <figure><img src="../.gitbook/assets/image (458).png" alt="" width="189"><figcaption></figcaption></figure>
   4. Switch to the Method and confirm that the Toolbox has commands available for both STARs
   5.  Add Initialize commands for each STAR, then run the method. Confirm that both STARs initialize as expected (for example, if the Initialize command from the ‘ML\_STAR\_2’ command group is called first, then the second STAR should initialize first)\


       <figure><img src="../.gitbook/assets/image (459).png" alt="" width="129"><figcaption></figcaption></figure>
