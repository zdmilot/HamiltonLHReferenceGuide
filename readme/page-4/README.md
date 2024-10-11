# Venus 4 Installation

<details>

<summary>1. Installation Preparation</summary>

1.  Select yes when prompted to install the SQL database.

    ![](<../../.gitbook/assets/6 (2).png>)

    ![](<../../.gitbook/assets/5 (2).png>)


2.  Close the Portable WinCDEmu. The installation drive is now mounted on your computer. Open the drive and select the Microlab\_Star folder. Right click on the setup application and select run as administrator. (Note: Administrator rights are needed to install the software properly.)

    ![](<../../.gitbook/assets/4 (2).png>)


3.  Select mount image, mount the Microlab STAR Software VENUS four base package 4.5.0.5217 and select open.\


    ![](<../../.gitbook/assets/3 (2).png>)


4.  Select yes when prompted to install the Portable WINCDEmu Driver.

    ![](<../../.gitbook/assets/2 (1) (1).png>)


5.  Open the Portable WinCDEmu-4.0. application located in the Venus 4 software folde

    <figure><img src="../../.gitbook/assets/1 (1) (1).png" alt="" width="449"><figcaption></figcaption></figure>



</details>

<details>

<summary>2. Microsoft SQL Server Installation</summary>

Using VENUS Software requires access to a Microsoft SQL Server. If the “Microsoft SQL Server 2014 SP2 Express Edition” is not installed at this point, a prompt will be displayed requiring a location and to access information from the Microsoft SQL Server after completion of the software installation.

1.  During installation, a prompt will be displayed asking if the SQL Server 2014 Service Pack 2 (SP2) shal be installed.

    <figure><img src="../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" width="267"><figcaption></figcaption></figure>
2. Click \[Yes] to continue. If \[No] is chosen, please prepare the following information to be able to use another SQL Server:
   * Microsoft SQL Server Location
   * Database User Name and Password
3.  Click \[Next >] to continue.

    <figure><img src="../../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" width="378"><figcaption></figcaption></figure>
4.  Click \[Yes] to continue after the virus protection software and all other applications have been closed.

    <figure><img src="../../.gitbook/assets/image (3) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" width="378"><figcaption></figcaption></figure>
5.  Click \[Yes] to continue.

    <figure><img src="../../.gitbook/assets/image (4) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" width="378"><figcaption></figcaption></figure>
6.  If necessary, change the installation destination and click \[Next >] to continue.

    <figure><img src="../../.gitbook/assets/image (5) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" width="378"><figcaption></figcaption></figure>

</details>

<details>

<summary>3. ‌Instrument Selection</summary>

1. Select the instrument from the dialog shown. This will install one of the following instrument deck layouts as the default layout.
2.  Click \[Next >] to continue.

    <figure><img src="../../.gitbook/assets/image (6) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" width="378"><figcaption></figcaption></figure>
3.  Click \[Install] to continue with the installation process.

    <figure><img src="../../.gitbook/assets/image (7) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" width="378"><figcaption></figcaption></figure>
4.  Specify the laboratory name and click \[Next >] to confirm the name.

    <figure><img src="../../.gitbook/assets/image (8) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" width="378"><figcaption></figcaption></figure>
5. The installation of the VENUS Software will now start.

<img src="../../.gitbook/assets/image (9) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" data-size="original">



</details>

<details>

<summary>4. ‌21 CFR Part 11 Security Settings‌</summary>

1.  The security requirements can be defined in the following screens:

    <figure><img src="../../.gitbook/assets/image (10) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" width="378"><figcaption></figcaption></figure>

    1. **Restrict Functionality by User logon**\
       For more information about the controlled access functionality, refer to Section 2.4 Authentication Systems. The access rights of the current user are monitored. By installation default, it is set to: OFF
    2. **Record (all) File Names in the Runtime Trace**\
       All the linked file names such as deck layout, liquid classes, labware, etc. are logged (Log File) at the end of each method run. By installation default, it is set to: OFF
    3. **Use File Checksums to Validate Files**\
       Verify the checksum of the method and of all the linked files such as the deck layout, liquid classes, labware, etc. If a file is corrupted, the software will detect it. Enable/disable checksum verification of files. By installation default, it is set to: ON If "Record (all) file names in the runtime trace" is selected, the screen shown below is displayed.\\
2.  Click \[Finish] to complete the installation.

    <figure><img src="../../.gitbook/assets/image (11) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" width="378"><figcaption></figcaption></figure>
3.  Select the security requirements that are needed and click \[Next >] to continue.\\

    <figure><img src="../../.gitbook/assets/image (12) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" width="378"><figcaption></figcaption></figure>

    1. **Enable Versioning and Validation of Files**\
       By installation default, it is set to: OFF
    2. **Enable Viewing of File History**\
       By installation default, it is set to: OFF\
       If "Enable viewing of file history" is selected, the screen shown below is displayed. 4. Select the security requirements that are needed and click \[Next >] to continue. • Force Audit Trail for All File Changes By installation
4.  Select the security requirements that are needed and click \[Next >] to continue.

    <figure><img src="../../.gitbook/assets/image (13) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" width="378"><figcaption></figcaption></figure>

    1. **Force Audit Trail for All File Changes**\
       By installation default, it is set to: OFF
5.  Click \[Finish] to complete the installation of the VENUS Software.

    <figure><img src="../../.gitbook/assets/image (14) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" width="378"><figcaption></figcaption></figure>

\\

</details>

<details>

<summary>5. ‌Support Software</summary>

After the successful installation of VENUS Software, the installation program for the Hamilton Support Software will start automatically.

1.  Select the labware, libraries and methods which are needed for the daily work by ticking the appropriate boxes. Click \[Next >] to continue.

    <figure><img src="../../.gitbook/assets/image (15) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" width="341"><figcaption></figcaption></figure>
2.  Click \[Install] to begin the installation of the selected features for the Hamilton Support Software.\\

    <figure><img src="../../.gitbook/assets/image (16) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" width="378"><figcaption></figcaption></figure>
3.  The installation of the features will take a few minutes.

    <figure><img src="../../.gitbook/assets/image (17) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" width="378"><figcaption></figcaption></figure>
4.  Click \[Finish] to complete the installation of the Hamilton Support Software.\\

    <figure><img src="../../.gitbook/assets/image (18) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" width="378"><figcaption></figcaption></figure>
5.  After the successful installation of VENUS Software, find the Version Information under “Windows -> Start -> All Programs -> HAMILTON -> Version Info”. This tool provides information about the currently installed VENUS Software.

    <figure><img src="../../.gitbook/assets/image (19) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" width="360"><figcaption></figcaption></figure>

\\

</details>





klm
