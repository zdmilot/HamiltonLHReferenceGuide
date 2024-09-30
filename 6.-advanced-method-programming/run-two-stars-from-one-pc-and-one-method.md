# Run Two STARs from One PC and One Method

‌Overview

This guide will assist the user in updating the computer registry to allow for running two STARs within one method on one PC. Administrator privileges are required to make registry modifications.

\


‌How to Run Two STARs from One Method on One PC

![image](blob:https://app.gitbook.com/043eda4f-2d0e-4819-9508-efe843d21168)

1. ## Open the Registry Editor
   1.  Select the Start Menu then type in “regedit” and select Registry Editor when it appears

       \

2. ## Create a second ML\_STAR Instrument
   1. Browse to the ‘ML\_STAR’ registry “Computer\HKEY\_LOCAL\_MACHINE\SOFTWARE\WOW6432Node\Phoenix\Instr uments\ML\_STAR”
   2.  Right-click on the ‘ML\_STAR’ registry and select ‘Export’. Name and save the exported .reg file

       \


       ![Graphical user interface, application, table  Description automatically generated](blob:https://app.gitbook.com/6bcb1f01-f8f3-4018-91ac-13529d1f2342)

       ![image](blob:https://app.gitbook.com/f0259f56-1b5b-48e9-b2cf-ac36a3b458a8)
   3. Right-click on the ‘ML\_STAR’ registry and select Rename to change the name to ‘ML\_STAR\_2’
   4.  Go to File > Import… and import the previously exported ‘ML\_STAR’ registry

       \

3. ## Update ‘ML\_STAR\_2’ registry
   1.  Select the ‘ML\_STAR\_2’ registry, and modify the ‘(Default)’ parameter to be ‘Microlab® STAR (no. 2)’

       \


       ![Graphical user interface, application, Word  Description automatically generated](blob:https://app.gitbook.com/f77c08d1-178c-4400-a4bf-fa7b5b334066)
   2.  Expand the ‘ML\_STAR\_2’ registry and go to the ‘InstCfgFile’ registry. Modify the ‘(Default)’ parameter to be ‘ML\_STAR\_2.cfg’

       \


       ![Graphical user interface, text, application  Description automatically generated](blob:https://app.gitbook.com/ee2f2fab-6f45-4464-9ee1-50f91e5a7d85)
   3.  Close the Registry Editor

       \


       ![image](blob:https://app.gitbook.com/7666db03-acbf-4715-a388-8ff2f7cf92ac)
4. ## Prepare ‘ML\_STAR\_2’ Config Files
   1. In File Explorer, browse to the “C:\Program Files (x86)\HAMILTON\Config” folder
   2.  Locate the ‘ML\_STAR.cfg’ and ‘ML\_STAR\_Simulator.cfg’ files.

       Make copies of both files in the same folder
   3. Rename to ‘ML\_STAR\_2.cfg’ and ‘ML\_STAR\_2\_Simulator.cfg’, respectively
   4. Open the ‘HxCfgFilConverter.exe’ software found in the “C:\Program Files (x86)\HAMILTON\Bin” folder
   5.  In the menu on the left, browse to the “C:\Program Files (x86)\HAMILTON\Config” folder, then look for the ‘ML\_STAR\_2.cfg’ file in the menu on the right

       \


       ![Graphical user interface, text, application  Description automatically generated](blob:https://app.gitbook.com/7aa2cbe8-4c3c-473c-ba9d-62348657fd42)

       ![image](blob:https://app.gitbook.com/8230eb7a-45b9-4b0f-9b0f-5d34f194ec90)
   6. Click on the ‘Convert to ASCII’ button on the bottom of the window. The status bar below the button should show ‘success’ when the conversion is complete. Leave the ‘HxCfgFilConverter’ software open and proceed to the next step
   7. Return to the “C:\Program Files (x86)\HAMILTON\Config” folder and open the ‘ML\_STAR\_2.cfg’ file. This can be opened in Notepad or another text editor of choice
   8.  Find the ‘SERIAL\_NUMBER’ key and change to “02”:

       ![image](blob:https://app.gitbook.com/6a95bd5e-d046-460a-afff-60aa42fbde4e)

       *   In the ‘ML\_STAR\_2.cfg’ file, search for the word “serial” using the Find function (in Notepad, this is found under the Edit menu or by clicking “Ctrl

           \+ F” on the keyboard)
       * The Find function will jump down to the ‘SERIAL\_NUMBER’ key, which will have a value of “00”. Change this value to “02”
       * Save and close the ‘ML\_STAR\_2.cfg’ file
   9.  Return to the ‘HxCfgFilConverter.exe’ software and confirm that the ‘ML\_STAR\_2.cfg’ file is still selected. Then click ‘Convert to Binary’ and confirm success from the status bar below the button

       \


       ![Graphical user interface  Description automatically generated with medium confidence](blob:https://app.gitbook.com/a013cf59-4b57-481d-82f1-7910adde34a9)

       \

5.  ## Modify the second STAR’s USB Serial Number

    \*\*NOTE: before proceeding, only one STAR should be connected to the PC as all STAR’s have a default USB Serial Number of “00”

    ![image](blob:https://app.gitbook.com/741f6928-3876-4542-aa7a-b4830e9630af)

    1. Connect the second STAR’s USB cable to the PC and power on the STAR
    2. Open the Microlab® STAR Service Software and confirm the second STAR connects properly
    3.  Go to Control > Single command

        ![image](blob:https://app.gitbook.com/cb759014-6dc4-47a1-9171-6afc9be71754)
    4. In the window that pops up, send the following commands to the STAR in this order, confirming successful response on each:
       * C0AP
       * C0Anan02
       * C0AP
    5.  Exit the STAR Service Software

        \

6.  ## Confirm both STARs can connect

    ![image](blob:https://app.gitbook.com/d96a5742-f10f-421c-b5a0-ec8ec00a3754)

    1. Power cycle the second STAR
    2. Connect the first STAR’s USB cable to the PC and power on the first STAR
    3. Open the Microlab® STAR Service Software
    4.  Go to Settings > Port Settings. In the window that pops up, select USB then click the Settings button

        \


        ![Graphical user interface, application, Word  Description automatically generated](blob:https://app.gitbook.com/8e0bfb50-2655-4d42-a230-6bd518b81289)
    5.  Confirm that both STARs appear in the Device List

        \


        ![Graphical user interface, application  Description automatically generated](blob:https://app.gitbook.com/b778ae13-5026-4102-ba66-2a4bd9ef8c57)
    6. Double-click the first STAR in the Device List (Serial Number: 00), then click the OK button. Make sure to click the OK button on all parent windows to return to the STAR Service Software Main Window, this will allow the software to connect to the first STAR.
    7.  Exit the STAR Service Software

        \


        ![image](blob:https://app.gitbook.com/f8078d53-9390-4c02-9125-7de0c2fc7fe6)
7. ## Make and test a method in Method Editor
   1. Open Method Editor and create a new Method
   2.  In the Deck Layout Editor, go to the Devices Tab and select Add New Instrument. In the drop-down confirm both ‘ML\_STAR’ and ‘ML\_STAR\_2’ are listed as options

       ![image](blob:https://app.gitbook.com/a209c7fd-0956-477b-a8a9-2391d88add64)
   3.  Add both STARs to the Deck Layout and confirm that tabs for each are present on the bottom of the Deck Layout Editor window

       ![image](blob:https://app.gitbook.com/f2911003-fa31-460c-b08d-b4289a79d552)
   4. Switch to the Method and confirm that the Toolbox has commands available for both STARs
   5. Add Initialize commands for each STAR, then run the method. Confirm that both STARs initialize as expected (for example, if the Initialize command from the ‘ML\_STAR\_2’ command group is called first, then the second STAR should initialize first)
