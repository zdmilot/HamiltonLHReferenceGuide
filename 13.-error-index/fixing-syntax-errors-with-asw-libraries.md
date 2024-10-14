# Fixing Syntax Errors with ASW Libraries

‌Overview

Many VENUS methods rely heavily on the ASW Standard libraries (ASW Global, ASW Trace Level, etc.). These libraries are powerful tools but can potentially cause issues when importing methods that utilize them as duplicate copies can be created. This duplication typically happens if these libraries are used in a sub-method library. HSL syntax errors can then occur because the main method calls one instance of the library while the sub-method libraries call the duplicate

\


The following guide provides information on how to identify and correct such issues.

‌Identifying the Issue

There are multiple ways to determine that the ASW libraries were imported improperly and could cause issues.

\


Opening a method in the Method Editor generates HSL syntax errors that involve the following libraries:

* ASWGlobal
* TraceLevel
*   HSLExtensions



    \


    ![image](blob:https://app.gitbook.com/02aefc0a-9d7a-4891-9f2a-990e5da1cfef)
* The ASW Status Dialog status window doesn’t display during runtime in a method that uses the ASW Status Dialog.

\


‌Uninstall Default and Duplicate Libraries

Open up Control Panel -> Uninstall a program

\


![image](blob:https://app.gitbook.com/8e96775a-960f-426e-a61e-8b97bd91a4e3)

1. Delete the following folders in the C:\Program Files (x86)\HAMILTON\Library directory:
   * ASWStandard
   * ASWStandard Dialogs
   * ASW Status
   *   HSLExtensions

       \

2. Delete any duplicate instances of the libraries found in the C:\Program Files (x86)\HAMILTON\Methods directory:
   * ASWStandard
   * ASWStandard Dialogs
   * HSLExtensions

\


‌Re-install Libraries

Run the installers for the ASW and HSL Extensions Libraries in the following order and confirm they are installed in the default Library directory:

1. ASWStandard
2. ASWGUI
3. HSLExtensions
4. ASW Vector Dialogs (if needed)

\


When opening a method that formerly was linked to libraries in located in the wrong directory, an error may be generated stating that the ASW Global library cannot be found. This can be corrected by re-linking to the library in the default location:

C:\Program Files (x86)\HAMILTON\Library\ASWStandard\ASWGlobal\ASWGlobal.hsl
