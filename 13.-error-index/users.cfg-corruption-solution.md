# Users.cfg Corruption Solution

‌Overview

\


![image](blob:https://app.gitbook.com/c2c83c40-ba2b-476c-9bb6-8fade7dd9589)

This is a common error seen in VENUS. This error may be seen when opening the System Configuration Editor or opening other Hamilton programs. This error is related to changes in the time zone on the PC. To prevent the issue, prior to installing VENUS, make sure that the time zone is set correctly on the PC. If the PC is already configured and VENUS has already been installed, but you encounter this issue, then you will need to follow the instructions below to resolve the error. There are separate instructions depending upon if Hamilton Authentication is disabled or enabled.

\


‌If Hamilton Authentication is disabled:

1. Close all Hamilton applications.
2.  Open the Windows Task Manager (right click on task bar>Task Manager or press CTRL+SHIFT+ESC) and end any running HxUserManager.exe processes.

    \


    ![image](blob:https://app.gitbook.com/f4510511-b5b5-4593-95d6-13b53ffcd276)

    \

3.  Delete \<install>\HAMILTON\Config\Users.cfg

    \

4.  Ensure that the time zone is properly set on the PC.

    \

5. If needed, enable and set up Hamilton Authentication.

\


‌If Hamilton Authentication is enabled:

1. Close all Hamilton applications.
2.  Open the Windows Task Manager (right click on task bar>Task Manager or press CTRL+SHIFT+ESC) and end any running HxUserManager.exe processes.

    \


    ![image](blob:https://app.gitbook.com/6dd9aa1a-0d47-4f15-a4a5-40d7480d3945)

    \

3. Delete \<install>\HAMILTON\Config\Users.cfg
4.  Disable Function Protection from the registry.

    Windows>Start>regedit

    ![image](blob:https://app.gitbook.com/003f5637-9431-4c12-9557-34c2bfc16d6e)
5.  Navigate to Computer\HKEY\_LOCAL\_MACHINE\SOFTWARE\Wow6432Node\Phoenix\Environment And set FunctionProtection to 0

    \


    ![C:\Users\cuevas\_a\Documents\HAMILTON Docs\Software\VENUS\How to\How to disable Function protection in the registry.jpg](blob:https://app.gitbook.com/e5f5f72c-7eca-41cf-bf2c-e3d3b857462f)

    \

6.  Start Method Editor and System Configuration Editor.

    \

7.  Click cancel or close on the Hamilton Log On Prompt.

    \


    ![image](blob:https://app.gitbook.com/3736c6fa-59be-4714-8a5f-e3276af39baa)

    \

8.  Open the System Configuration Editor.

    \


    ![image](blob:https://app.gitbook.com/2deadbec-adab-4032-b981-e7e92d9403f7)
9.  Click cancel or close on the Hamilton Log On Prompt when it shows again.

    \


    ![image](blob:https://app.gitbook.com/62cb3803-e8a8-4867-b29d-c716def2d4fc)

    \

10. Create a new user.

    \


    ![image](blob:https://app.gitbook.com/9f262413-325d-4ce1-9a27-be3d1a71e912)
11. Set new user privileges: IMPORTANT, DON’T SKIP THIS STEP!!!!

    \


    ![image](blob:https://app.gitbook.com/da28de07-2d25-403d-9fec-c0cb8184218a)

    \

12. Enable Function Protection if needed.

\


![image](blob:https://app.gitbook.com/70ae61c3-d22f-43bd-886a-d540d3d03ded)
