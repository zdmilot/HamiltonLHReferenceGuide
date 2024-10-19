# Chapter 1: Introduction

The SoftMax® Pro Data Acquisition and Analysis Software supports an automation interface to integrate Molecular Devices® microplate readers and the software with robotic systems from other manufacturers, or to automate the export of data from the SoftMax Pro Software to a Laboratory Information Management System (LIMS) package. Molecular Devices has tested the automation interface but does not provide technical support for specific integration needs. You should consult with a third-party automation company if internal software resources or expertise are not available.

Leading automation vendors can integrate the SoftMax Pro Software and Molecular Devices instruments with their robotics systems. See the Molecular Devices web site for a list of approved robotics partners.

### Intended Audience <a href="#intended-audience" id="intended-audience"></a>

This guide is for people who want to build an automation application that interacts with the SoftMax Pro Software version 7.1.x or later using the automation interface to control the operation of a Molecular Devices instrument.

To use this guide, you must:

![](<../../../../.gitbook/assets/1 (24).png>) Understand the basic concept of object-oriented programming and programming using Microsoft .NET including the use of delegates and events.

![](<../../../../.gitbook/assets/2 (13).png>) Understand assemblies in Microsoft .NET. ![](<../../../../.gitbook/assets/3 (15).png>) Understand namespaces in Microsoft .NET.

![](<../../../../.gitbook/assets/4 (14).png>) Have access to and knowledge of development tools that enable you to create and customize an assembly.

### Updates In This Version <a href="#updates-in-this-version" id="updates-in-this-version"></a>

This version of the automation interface can run scripts written for SoftMax Pro Software version 6.0 and later.

New Commands:

![](<../../../../.gitbook/assets/5 (13).png>) GetAllFolders ![](<../../../../.gitbook/assets/6 (10).png>) GetDocuments

Updated Commands:

![](<../../../../.gitbook/assets/7 (7).png>) none

Obsolete Commands:

![](<../../../../.gitbook/assets/8 (5).png>) int Logon(String userName,String password)

![](<../../../../.gitbook/assets/9 (4).png>) int SelectDatabaseFromFile(String databaseFilePath)

![](<../../../../.gitbook/assets/10 (2).png>) int SelectDatabaseFromTcpIP(String portNumber, String ipAddress) ![](<../../../../.gitbook/assets/11 (2).png>) int SetUserName(String userName)

![](<../../../../.gitbook/assets/12 (2).png>) int SelectDocument(Boolean, Boolean, Boolean) ![](<../../../../.gitbook/assets/13 (2).png>) int SetProtocolFolder(System, String)

### Computer System Requirements <a href="#computer-system-requirements" id="computer-system-requirements"></a>

The computer system requirements are listed in the _SoftMax Pro Data Acquisition and Analysis Software Installation Guides_.

![](<../../../../.gitbook/assets/14 (3).png>) When you run both automation and the SoftMax Pro Software on the same computer, use at least the recommended system configuration.

![](<../../../../.gitbook/assets/15 (3).png>) Molecular Devices recommends that the documents you use in the automation workflow have a small number of sections. You should close documents when they are no longer needed.

![](<../../../../.gitbook/assets/16 (3).png>) An experiment with many plates of data can adversely affect SoftMax Pro Software efficiency. If you cannot increase the computer memory, you should use only one plate per experiment and do not use the computer for other purposes while the SoftMax Pro Software runs.

![](<../../../../.gitbook/assets/17 (3).png>)

**Note:** Microsoft no longer supports the Windows XP, Windows 7, and Windows 8 operating systems. Molecular Devices no longer tests or validates the SoftMax Pro Software on these operating systems.

### Installing the Automation SDK <a href="#installing-the-automation-sdk" id="installing-the-automation-sdk"></a>

The SoftMax Pro Software installation includes the automation SDK and can be found in the file system where you install the SoftMax Pro Software.

The following is the default installation path for the automation SDK:

C:\Program Files (x86)\Molecular Devices\SoftMax Pro \<n.n> Automation SDK

### Automation With the SoftMax Pro Software - GxP Edition <a href="#automation-with-the-softmax-pro-software" id="automation-with-the-softmax-pro-software"></a>

If the target application is the SoftMax Pro Software - GxP edition, /R is required in the program command line (for example, "SoftMaxProApp.exe /R") when you launch the application to avoid the Logon dialog that requires manual entry of username, password, and Project. Send the Logon remote command (/R) to log the user on through the robotic interface. See Logon on page 75.

For the SoftMax Pro Software - GxP edition version 7.1.1 and later, you need to consider the document workflow. See the _SoftMax Pro Data Acquisition and Analysis Software User Guide_.

Manual steps:

![](<../../../../.gitbook/assets/18 (2).png>) Import a protocol from the Protocol Library to the database or create a new document. ![](<../../../../.gitbook/assets/19 (2).png>) Save it as protocol.

![](<../../../../.gitbook/assets/20 (2).png>) Release the protocol after you log in as a user with the equivalent of the Lab Technician Role permissions.

Automation:

&#x20;Use the automation to load the protocol. The software creates a new data document based on the opened protocol.

&#x20;Save the document as a data document.  Run the experiment.
