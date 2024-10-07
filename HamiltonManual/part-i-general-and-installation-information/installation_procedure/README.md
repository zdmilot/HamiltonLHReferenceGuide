# VENUS Software Installation Procedure

1. To back-up methods, etc., rename the Hamilton sub-directory to HAM or any other name that can easily be recalled. After doing so, proceed with the installation.
2. Insert the VENUS Software supplied on a USB Stick into a USB Port.
3. If the installation does not start automatically, select the SETUP.EXE program file found in the USB Stick. Follow the instructions during installation carefully.

<table data-header-hidden><thead><tr><th width="145"></th><th></th></tr></thead><tbody><tr><td><img src="../../.gitbook/manual-images/assets/image (1) (1) (1).png" alt="" data-size="original"></td><td><p>NOTE</p><p>VENUS Software is validated for the following Windows™ operating systems: Windows 7 (32-bit or 64-bit)</p><p>Windows 10 (32-bit or 64-bit)</p></td></tr><tr><td><img src="../../.gitbook/manual-images/assets/image (23).png" alt=""></td><td><p>ATTENTION</p><p>Administrator access to the computer must be allowed before any software installation.</p></td></tr><tr><td><img src="../../.gitbook/manual-images/assets/image (23).png" alt=""></td><td><p>ATTENTION</p><p>Disable all antivirus programs before installation. Scripts used in the installation process can interfere with the virus protection software.</p></td></tr></tbody></table>

<table data-header-hidden><thead><tr><th width="145"></th><th></th></tr></thead><tbody><tr><td><img src="../../.gitbook/manual-images/assets/image (23).png" alt=""></td><td><p>ATTENTION</p><p>When installing the software on Windows™ 7, make sure to set the “User Account Control Settings” to default.</p></td></tr><tr><td><img src="../../.gitbook/manual-images/assets/image (23).png" alt=""></td><td><p>ATTENTION</p><p>As a safety precaution, before upgrading the system with the new software version, make sure to create back-up copies of the methods, user-defined labware, liquid classes, etc. The easiest way to do so is to export the method/workflows into a package file (refer to Method Export and Import).</p></td></tr><tr><td><img src="../../.gitbook/manual-images/assets/image (23).png" alt=""></td><td><p>ATTENTION</p><p>The installation may vary depending on the operating system used. Some necessary software prerequisites (delivered with VENUS Software) may require a reboot of the PC during installation.</p><p>If a software prerequisite is already part of the operating system, it will not be installed twice.</p></td></tr><tr><td><img src="../../.gitbook/manual-images/assets/image (23).png" alt=""></td><td><p>ATTENTION</p><p>“Microsoft SQL Server 2014 SP2 Express Edition” has a limited storage capacity of 10GB.</p><p>Make sure that the SQL Server is maintained on a regular basis within routine use.isite is already part of the operating system, it will not be installed twice.</p></td></tr><tr><td><img src="../../.gitbook/manual-images/assets/image (23).png" alt=""></td><td><p>ATTENTION</p><p>Remember to re-enable the virus protection software after successfully installing VENUS Software.</p></td></tr><tr><td><img src="../../.gitbook/manual-images/assets/image (23).png" alt=""></td><td><p>ATTENTION</p><p>If the option ‘Restrict functionality by user logon’ is used, access rights must be defined after software installation. See Section 2.4 Authentication Systems.</p></td></tr><tr><td><img src="../../.gitbook/manual-images/assets/image (1) (1) (1).png" alt="" data-size="original"></td><td><p>NOTE</p><p>The chosen settings (except the selected instrument) are configurable via the Configuration Editor at a later time, if necessary.</p></td></tr></tbody></table>

## ‌InstallShield Wizard

<details>

<summary>1. Installation Preparation</summary>

1. The installation begins with certain preparation steps.\
   ![](<../../.gitbook/manual-images/assets/image (4) (1) (1).png>)

</details>

<details>

<summary>2. Microsoft SQL Server Installation</summary>

Using VENUS Software requires access to a Microsoft SQL Server. If the “Microsoft SQL Server 2014 SP2 Express Edition” is not installed at this point, a prompt will be displayed requiring a location and to access information from the Microsoft SQL Server after completion of the software installation.

1.  During installation, a prompt will be displayed asking if the SQL Server 2014 Service Pack 2 (SP2) shal be installed.

    <figure><img src="../../.gitbook/manual-images/assets/image (5) (1) (1).png" alt="" width="267"><figcaption></figcaption></figure>
2. Click \[Yes] to continue. If \[No] is chosen, please prepare the following information to be able to use another SQL Server:
   * Microsoft SQL Server Location
   * Database User Name and Password
3.  Click \[Next >] to continue.

    <figure><img src="../../.gitbook/manual-images/assets/image (6) (1) (1).png" alt="" width="378"><figcaption></figcaption></figure>
4.  Click \[Yes] to continue after the virus protection software and all other applications have been closed.

    <figure><img src="../../.gitbook/manual-images/assets/image (7) (1) (1).png" alt="" width="378"><figcaption></figcaption></figure>
5.  Click \[Yes] to continue.

    <figure><img src="../../.gitbook/manual-images/assets/image (8) (1) (1).png" alt="" width="378"><figcaption></figcaption></figure>
6.  If necessary, change the installation destination and click \[Next >] to continue.

    <figure><img src="../../.gitbook/manual-images/assets/image (9) (1).png" alt="" width="378"><figcaption></figcaption></figure>

</details>

<details>

<summary>3. ‌Instrument Selection</summary>

1. Select the instrument from the dialog shown. This will install one of the following instrument deck layouts as the default layout.
2.  Click \[Next >] to continue.

    <figure><img src="../../.gitbook/manual-images/assets/image (10) (1).png" alt="" width="378"><figcaption></figcaption></figure>
3.  Click \[Install] to continue with the installation process.

    <figure><img src="../../.gitbook/manual-images/assets/image (11) (1).png" alt="" width="378"><figcaption></figcaption></figure>
4.  Specify the laboratory name and click \[Next >] to confirm the name.

    <figure><img src="../../.gitbook/manual-images/assets/image (12) (1).png" alt="" width="378"><figcaption></figcaption></figure>
5. The installation of the VENUS Software will now start.

<img src="../../.gitbook/manual-images/assets/image (13) (1).png" alt="" data-size="original">

\\

</details>

<details>

<summary>4. ‌21 CFR Part 11 Security Settings‌</summary>

1.  The security requirements can be defined in the following screens:

    <figure><img src="../../.gitbook/manual-images/assets/image (16) (1).png" alt="" width="378"><figcaption></figcaption></figure>

    1. **Restrict Functionality by User logon**\
       For more information about the controlled access functionality, refer to Section 2.4 Authentication Systems. The access rights of the current user are monitored. By installation default, it is set to: OFF
    2. **Record (all) File Names in the Runtime Trace**\
       All the linked file names such as deck layout, liquid classes, labware, etc. are logged (Log File) at the end of each method run. By installation default, it is set to: OFF
    3. **Use File Checksums to Validate Files**\
       Verify the checksum of the method and of all the linked files such as the deck layout, liquid classes, labware, etc. If a file is corrupted, the software will detect it. Enable/disable checksum verification of files. By installation default, it is set to: ON If "Record (all) file names in the runtime trace" is selected, the screen shown below is displayed.\\
2.  Click \[Finish] to complete the installation.

    <figure><img src="../../.gitbook/manual-images/assets/image (17) (1).png" alt="" width="378"><figcaption></figcaption></figure>
3.  Select the security requirements that are needed and click \[Next >] to continue.\\

    <figure><img src="../../.gitbook/manual-images/assets/image (18) (1).png" alt="" width="378"><figcaption></figcaption></figure>

    1. **Enable Versioning and Validation of Files**\
       By installation default, it is set to: OFF
    2. **Enable Viewing of File History**\
       By installation default, it is set to: OFF\
       If "Enable viewing of file history" is selected, the screen shown below is displayed. 4. Select the security requirements that are needed and click \[Next >] to continue. • Force Audit Trail for All File Changes By installation
4.  Select the security requirements that are needed and click \[Next >] to continue.

    <figure><img src="../../.gitbook/manual-images/assets/image (19) (1).png" alt="" width="378"><figcaption></figcaption></figure>

    1. **Force Audit Trail for All File Changes**\
       By installation default, it is set to: OFF
5.  Click \[Finish] to complete the installation of the VENUS Software.

    <figure><img src="../../.gitbook/manual-images/assets/image (20) (1).png" alt="" width="378"><figcaption></figcaption></figure>

\\

</details>

<details>

<summary>5. ‌Support Software</summary>

After the successful installation of VENUS Software, the installation program for the Hamilton Support Software will start automatically.

1.  Select the labware, libraries and methods which are needed for the daily work by ticking the appropriate boxes. Click \[Next >] to continue.

    <figure><img src="../../.gitbook/manual-images/assets/image (21) (1).png" alt="" width="341"><figcaption></figcaption></figure>
2.  Click \[Install] to begin the installation of the selected features for the Hamilton Support Software.\\

    <figure><img src="../../.gitbook/manual-images/assets/image (24).png" alt="" width="378"><figcaption></figcaption></figure>
3.  The installation of the features will take a few minutes.

    <figure><img src="../../.gitbook/manual-images/assets/image (25).png" alt="" width="378"><figcaption></figcaption></figure>
4.  Click \[Finish] to complete the installation of the Hamilton Support Software.\\

    <figure><img src="../../.gitbook/manual-images/assets/image (26).png" alt="" width="378"><figcaption></figcaption></figure>
5.  After the successful installation of VENUS Software, find the Version Information under “Windows -> Start -> All Programs -> HAMILTON -> Version Info”. This tool provides information about the currently installed VENUS Software.

    <figure><img src="../../.gitbook/manual-images/assets/image (27).png" alt="" width="360"><figcaption></figcaption></figure>

\\

</details>





klm
