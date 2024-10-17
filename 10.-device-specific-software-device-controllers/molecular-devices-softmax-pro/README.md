---
icon: dev
---

# Molecular Devices SoftMax Pro

The SoftMax® Pro Data Acquisition and Analysis Software controls Molecular Devices® spectrophotometers and absorbance, luminescence, and fluorescence microplate readers and detection platforms. This guide describes features available in the SoftMax Pro Software

\- Standard edition version 7.1 and SoftMax Pro Software - GxP edition version 7.1.1. For a complete list of the instruments this release of the SoftMax Pro Software supports, see Supported Instruments on page 316.

The software provides extensive data calculation and analysis capabilities under a Good Manufacturing Practices (GMP), Good Laboratory Practices (GLP) work environment for pharmaceutical, biotechnology, academic, hospital, and government customers.

The Protocol Library contains over 160 protocols that contain instrument settings and formulas. You can customize the protocols in the Protocol Library to facilitate the data analysis and report creation.

SoftMax Pro Software is widely integrated with industry-leading robotics systems.

### Important Installation Information

You should install the SoftMax Pro Software on the computer before you set up the microplate reader. Please be aware that some updates to the SoftMax Pro Software require a purchase. To download the latest version of the software, visit: [www.MolecularDevices.com/SMPdownloadsite](http://www.moleculardevices.com/smpdownloadsite).

**Note:** Installation and usage of the SoftMax Pro Software on the Windows XP and Windows 8 operating systems is no longer supported. The software is neither tested nor validated on Windows XP or Windows 8. Windows 7 with 32 bit operating system is also no longer supported. You can install the SoftMax Pro Software - Standard edition on a Windows 7 with 64 bit operating system, but Windows 10 is strongly recommended.

![](<../../.gitbook/assets/1 (8).png>)

See the following documents for installation instructions:

![](<../../.gitbook/assets/2 (8).png>) _SoftMax Pro Data Acquisition and Analysis Software Standard Edition and MiniMax Imaging Edition Installation Guide_

![](<../../.gitbook/assets/3 (11).png>) _SoftMax Pro Data Acquisition and Analysis Software - GxP Edition - Installation Guide for the Multi Computer Setup_

![](<../../.gitbook/assets/4 (13).png>) _SoftMax Pro Data Acquisition and Analysis Software - GxP Edition - Installation Guide for the Single Computer Setup_

### Uninstalling the Software

Before you uninstall the software, back up your data and documents to a folder outside of the SoftMax Pro Software folder. This method removes related Windows registry information.

To uninstall the software:

1. Click **Start > Control Panel**.
2. Click **Programs and Features**.
3. For the SoftMax Pro Software - Standard edition, in the program list, select **SoftMax Pro 7.n.n**.

For the SoftMax Pro Software - GxP edition, contact Technical Support. See Obtaining Support on page 11.

1. Click **Uninstall** or **Remove**.
2. Follow the prompts to uninstall the program.

### Starting the Software

Power on the instrument and wait for the instrument to complete its start-up sequence before you start the software. You can choose to run the software with the computer connected to the instrument or with the computer not connected to the instrument. When you do not connect the computer to an instrument, you cannot acquire data.

To start the software:

![](<../../.gitbook/assets/5 (8).png>) For the SoftMax Pro Software - Standard edition: Double-click the ![](<../../.gitbook/assets/6 (3).jpeg>) SoftMax Pro icon on the desktop or from the Windows Start menu, click **Start** > **All Programs** > **Molecular Devices** > **SoftMax Pro 7.n.n** > **SoftMax Pro 7.n.n.exe**.

![](<../../.gitbook/assets/7 (6).png>) For the SoftMax Pro Software - GxP edition: Double-click the ![](<../../.gitbook/assets/8 (2).jpeg>) SoftMax Pro GxP icon on the desktop or from the Windows Start menu, click **Start** > **All Programs** > **Molecular Devices** > **SoftMax Pro 7.n.n GxP** > **SoftMax Pro 7.n.n GxP.exe**

![](<../../.gitbook/assets/9 (6).png>) Enter your user name and password, and then click **Log On**. See Logging In To The SoftMax Pro Software - GxP Edition on page 252.

**Note:** When you use the SpectraMax® i3x Multi-Mode Detection Platform, SpectraMax® i3 Multi-Mode Detection Platform, SpectraMax® Paradigm Multi-Mode Microplate Reader, FilterMax® F3 Multi-Mode Microplate Reader, and FilterMax® F5 Multi-Mode Microplate Reader for the first time, the installation process installs the latest instrument firmware updates.

![](<../../.gitbook/assets/10 (4).png>)

The SoftMax Pro Software saves instrument firmware updates on the computer hard drive. If you put a new image on the computer or you replace the computer, this information is lost. However, the software installation and updates automatically install the latest instrument firmware.

Instrument firmware information saves in the following file on the computer:C:\ProgramData\Multimode\Detection Software\Templates\UpdateInfo.xml

### Activating the Software License

Use the Software License Activation dialog to update the SoftMax Pro Software license. The dialog displays when your license is inactive or is ready to expire. The SoftMax Pro Software package includes your software product key. For information about the features of your license or to obtain a new license key, contact Molecular Devices.

#### Computer With Internet Access

To activate the software license on a computer that has access to the Internet:

*
  1. In the Ribbon, select the **Help** tab, and then click ![](<../../.gitbook/assets/11 (3).jpeg>) **Software License** to display the Software License Activation dialog.
  2. Click **Activate** to display the Activate Online dialog.
  3. In the **Product Key** field, enter the product key from the SoftMax Pro Software package.
  4. Click **Activate Online**, and then follow the prompts to activate the license.

#### Computer Without Internet Access

To activate the product key offline, you need the product key, a computer that has access to the Internet, and a USB drive to transfer the files between the computers.

To activate the software license for a computer that has does not have access to the Internet:

On the computer that has access to the Internet, go to: [https://smplicensing.moleculardevices.com](https://smplicensing.moleculardevices.com/)

Follow the prompts to activate the license.

### Automation Mode

You can use Application Programming Interface (API) command scripts to automate the SoftMax Pro Software.

To start Automation mode:

1. Select the **Operations** tab in the Ribbon.
2. Click ![](<../../.gitbook/assets/12 (6).png>) **Automation Mode**.

Automation mode prevents user interaction and the software displays the following dialog in front of the main window.

![](<../../.gitbook/assets/13 (1).jpeg>)

When the software acquires data, the Plate section displays in the main window behind the automation mode dialog and displays the data.

The **Automation Messages** area displays relevant information. To stop the automation process, click **Terminate**.

The StakMax® Microplate Handling System is an integrated microplate handler for use with Molecular Devices microplate readers, to provide simple, powerful, walk-away benchtop automation. The StakMax Microplate Handling System uses the SoftMax Pro Software Automation mode and the StakMax Software has a scripting tool. See StakMax Microplate Handling System on page 341.

### Automation Scripts

You can script and run the automation commands in the SoftMax Pro Software through the automation API. For experienced automation programmers, the _SoftMax Pro Data Acquisition and Analysis Software Automation API Reference Guide_ provides information about the available commands and parameters. The SoftMax Pro Software also supports a Microsoft Excel Add-In to write and run Excel Workflows.

Legacy scripts must use the Windows message WM\_COPYDATA command. The WM\_ SETTEXT command is not supported. Legacy scripts might not work correctly with the current automation interface. If your legacy script does not work properly, you should use the most recent version of the automation commands to rewrite the script.

To let the software accept legacy commands from scripts written for the SoftMax Pro Software automation interface version 5.x:

1. Select the **Operations** tab.
2. Click **Automation Mode**.

### SoftMax Pro Excel Workflows

The SoftMax Pro Automation SDK is the underlying mechanism SoftMax Pro Excel workflows uses to access SoftMax Pro Software functionality.

The SoftMax Pro Excel workflows expand the industry-leading handling of plate format data by the SoftMax Pro Software with Excel-based handling of list format data. Use the SoftMax Pro Excel workflows to run discontinuous kinetic reads, multiplexed reads, kinetic well scan reads, and temperature-triggered reads.

After you install the custom Add-In in Excel, you can run and edit the Excel workflows or you can create your own workflows. The installation places the workflows in the same folder as the Excel Add-In files.

![](<../../.gitbook/assets/14 (4).png>) For a 32-bit installation, the workflows are in the following folder:

#### C:\Program Files\Molecular Devices\SoftMax Pro 7.n.n Automation SDK\ExcelAddIn

![](<../../.gitbook/assets/15 (3).png>) For a 64-bit installation, the workflows are in the following folder: **C:\Program Files (x86)\Molecular Devices\SoftMax Pro 7.n.n Automation SDK\ExcelAddIn**

The Excel workflow files have a .xlsm extension.

Before you run or edit an Excel workflow, save a copy of the workflow on your computer.

### Barcode Reader

The software allows you to use a barcode reader as an input device. When you place the cursor in a text field and then use the barcode reader to read a barcode, the barcode reader passes the text embedded in the barcode to the text field.

Before you use a barcode reader with the software, make sure you install the correct driver and that the barcode reader functions correctly. To test a barcode reader, open a text editor, such as Notepad, and then use the barcode reader to read a barcode. If the reader functions correctly, the text embedded in the barcode appears in the text editor.

Barcodes can have several different formats, such as MSI or Pharmacode. The barcode reader you use must support the type of barcode to read. See the documentation that comes with your barcode reader.

