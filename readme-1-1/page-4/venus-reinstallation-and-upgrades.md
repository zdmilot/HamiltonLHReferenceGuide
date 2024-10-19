---
icon: dev
---

# VENUS Reinstallation and Upgrades

Sometimes the only way to fix systemic issues on systems running VENUS is to re-install VENUS. Additionally, there may be cases where it is required to upgrade VENUS to a newer version. In any case, there can be various issues that may arise during the uninstallation and reinstallation of VENUS on the same PC, related to proper configuration of the Vector database, or incomplete removal/unregistration of files and assemblies from the previous install. This document serves to provide comprehensive instruction for a complete uninstallation and reinstallation process.



## Backup your VENUS files

Before you make attempt to uninstall any component of VENUS, it is imperative that you back up your files essential to running methods. It is highly recommended that all dependent files for a VENUS installation be housed within:

\<install>\HAMILTON

If there are dependent files located outside Hamilton folder, you will need to create pkg exports of all methods you intend to preserve, where you would successively import following reinstallation. For instruction on importing and exporting, reference “QuickGuideExportImport\_Instructions\_v1.pdf”

If all files are housed within the Hamilton folder, then it is simplest to back up the entire folder to an external drive. Once the VENUS upgrade or reinstallation is complete, you can simply copy and paste the contents of the backed-up folder into the new Hamilton folder with special considerations for materials contained in the following folders:

* HAMILTON\Bin
  * Copy nothing
* HAMILTON\Config
  * Copy ONLY ML\_STARLiquids.mdb (this restores all liquid classes)
* HAMILTON\Library
  * If upgrading VENUS, do not change any of the default libraries (files in the root of \<install>\HAMILTON\Library). All non-default library files can be pasted back in

In addition to backing up VENUS files required for method functionality, libraries and device drivers requiring installers will need to be uninstalled and subsequently reinstalled following VENUS reinstallation. In the Programs and Features Windows control panel, take note of any installed application containing ‘Hamilton’ and take note of the version. Collect the appropriate installers for each add-on/driver/library ensuring that the proper version is maintained, and store with the rest of the backup materials.

<figure><img src="../../.gitbook/assets/image (60) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

## How to uninstall Microsoft SQL Server 2014

If you uninstall VENUS without first uninstalling SQL Server, the Hamilton SQL database will not be automatically created and setup in VENUS during reinstallation. You will then need to re-install and create the Hamilton database manually following “SQL Server 2014 Database Manual Installation.pdf” procedure, OR uninstall SQL Server and VENUS again following the correct procedure (recommended), and repeat the VENUS installation.

\


1.  From the Control Panel -> Programs and Features, search for ‘SQL and select to uninstall and remove\


    <div>

    <figure><img src="../../.gitbook/assets/image (63) (1) (1) (1) (1).png" alt="" width="563"><figcaption></figcaption></figure>

     

    <figure><img src="../../.gitbook/assets/image (62) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

    </div>
2.  Go through the Remove SQL Server wizard to remove the HAMILTON SQL server instance as well as all components and features. When prompted for which features to remove, click Select All.

    Note: If there are additional instances of SQL server installed, they must be uninstalled, and their dependent software (ex INSTINCT V) will also need to be reinstalled.

    <div>

    <figure><img src="../../.gitbook/assets/image (67) (1) (1) (1) (1).png" alt="" width="525"><figcaption></figcaption></figure>

     

    <figure><img src="../../.gitbook/assets/image (66) (1) (1) (1) (1).png" alt="" width="563"><figcaption></figcaption></figure>

    </div>
3.  Once the Remove SQL Server wizard is complete, uninstall all remaining SQL components from Windows Programs and Features control panel.

    <figure><img src="../../.gitbook/assets/image (68) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

    \




## How to uninstall VENUS

1. Backup files and uninstall SQL server per the instructions in the previous sections.
2. Search for “Hamilton” in the Programs and Features Windows control panel. Uninstall any VENUS add-on features (Service Packs, PowerSteps, VoV Plugins, TADM, libraries, device drivers)
3. Uninstall the VENUS main program.
4. Run “RemoveHamiltonSoftware.exe” and follow the steps. Note: Do not run this program before VENUS and its components have been uninstalled or you may have to manually remove Windows registry entries.
5. The C:\Program Files (x86)\HAMILTON will still exist. Delete or rename this folder.
6. Delete these registry entries (if remaining) from the Windows Registry:
   * Computer\HKEY\_LOCAL\_MACHINE\SOFTWARE\WOW6432Node\Phoenix
   *   Computer\HKEY\_CURRENT\_USER\SOFTWARE\Hamilton Company\


       <div>

       <figure><img src="../../.gitbook/assets/image (72) (1) (1) (1).png" alt="" width="212"><figcaption></figcaption></figure>

        

       <figure><img src="../../.gitbook/assets/image (70) (1) (1) (1).png" alt="" width="275"><figcaption></figcaption></figure>

        

       <figure><img src="../../.gitbook/assets/image (71) (1) (1) (1).png" alt="" width="335"><figcaption></figcaption></figure>

       </div>
7. Delete anything with the word Hamilton (if remaining) in:
   * C:\Windows\Microsoft.NET\assembly\GAC\_MSIL
   * C:\Windows\assembly
8. Restart computer.
9. Re-install VENUS as administrator ensuring there is an active network connection, make sure to say Yes to when asked to install SQL Server.
10. Re-install any add-on features as administrator (ie: PowerSteps, VoV, TADM, libraries, drivers etc.)
11. You can now replace or merge the new Labware, Method and Library folders with the previous ones. Note: Do not replace other folders such as Bin, Config
12. You can also copy the old liquid class database (“ML\_STARLiquids.mdb”) found in the Config folder to the new Config folder.
13. Some Libraries/Device Drivers may need to be repaired/re-installed. You will get an “Invalid Class Error” during simulation if this is required.

\


## Important Notes for VENUS Installation

1.  From VENUS 4 and more recent versions, Microsoft .NET framework 3.5 is required. For Windows 10, this cannot be installed or activated without an internet connection.\


    <figure><img src="../../.gitbook/assets/image (73) (1) (1).png" alt="" width="563"><figcaption></figcaption></figure>

    In some cases, site-specific IT policies, security software and/or firewalls will prevent the installation of .NET framework 3.5. In these instances, an IT representative will be required to temporarily disable the security features that block installation of .NET framework.
2. If SQL Server Installation won’t complete, you may need to update Microsoft Edge Browser. Some computers ship with an older version that prevents SQL Serve from properly installing. To update Microsoft edge, follow these steps
   1. Go to “Help and Feedback” from the “…” menu in Microsoft Edge
   2. Click “About Microsoft Edge”
   3. Download and install any available updates
3. If installing PowerSteps (VENUS 4) you may get an error during installation about a .NET update error. You can ignore this error and VENUS should complete installation without issue.
4. Sometimes local Group Policy on the PC may be invalid for proper installation of VENUS, particularly when registering assemblies:

<figure><img src="../../.gitbook/assets/image (74) (1) (1).png" alt=""><figcaption></figcaption></figure>

This can be rectified by installing VENUS with an active network connection.
