# Installation of SQL Server

Microsoft SQL Server Express 2014 is automatically installed by the VENUS installer during a typical installation. If an issue resulted in the database failing to install or requires the reinstallation of the database without performing a full reinstallation of VENUS, the SQL Server installation media can be found within the VENUS installation media.

\


USB, ISO, and DVD media of the VENUS software install all include the Microlab\_STAR folder containing the software installations. To manually install SQL Server:

* Navigate to: Microlab\_STAR\SQLServer2014\x64\
  \
  Note: If using 32-bit version of Windows, use Microlab\_STAR\SQLServer2014\x86\
  \

* Right-click Setup.exe and select Run as administrator
* Wait while the SQL Server 2014 software prepares the necessary files

<figure><img src="../../../.gitbook/assets/image (19) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

*   Once the SQL Server Installation Center screen appears, verify you are on the

    Installation (1) menu by clicking on the text
* Click the hyperlink New SQL Server stand-alone installation or add features to an existing installation (2)

<figure><img src="../../../.gitbook/assets/image (20) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

* Click on the checkbox for I accept the license terms (1)
*   Click Next (2)

    ![](<../../../.gitbook/assets/image (21) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png>)\

*   If presented with a Microsoft Update or Product Updates screen, click Next (1)

    \
    ![](<../../../.gitbook/assets/image (22) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png>)
*   Wait while the installer prepares various files

    ![](<../../../.gitbook/assets/image (23) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png>)\

*   Make sure all available features are selected (1) and click Next (2)

    ![](<../../../.gitbook/assets/image (24) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png>)\

* Select Named instance (1)
* Enter the name HAMILTON as the instance name (2)
* Click the text box for Instance ID, it should automatically update to HAMILTON (3)
*   Click Next (4)

    ![](<../../../.gitbook/assets/image (25) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png>)\

* Depending on IT policies, the SYSTEM account may need to be used to run the SQL Server Database Engine:
  * Click the drop-down for the Account Name (1)
  * Click <\<Browse…>> (2)
  * Enter the word ‘SYSTEM’ into the objects text box (3)
  * Click Check Names (4) and the text should now be underlined
  * Click OK (5)
*   Click Next (6)

    ![](<../../../.gitbook/assets/image (26) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png>)\

* Click Mixed Mode (SQL Server authentication and Windows authentication) (1)
* Enter the password ‘mkdpw:V43’ into both password boxes (2)
* Click Add Current User and/or Add (3) if Windows accounts need to be added, but we will be using the ‘sa’ account specified above that section in this guide
*   Click Next (4)

    ![](<../../../.gitbook/assets/image (27) (1) (1) (1) (1) (1) (1).png>)\

*   Wait for the software to install, the screen will display the progress

    ![](<../../../.gitbook/assets/image (28) (1) (1) (1) (1) (1) (1).png>)\

*   Once installed, click Close (1)

    ![](<../../../.gitbook/assets/image (29) (1) (1) (1) (1) (1) (1).png>)\


\
