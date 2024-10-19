# GxP Admin Software

Use the GxP Admin Software to create users and to assign each user to at least one Project. You can assign a user to multiple Projects and the user can have a different set of Role permissions for each Project. A Project restricts what documents the user can access within the SoftMax Pro Software - GxP edition and a Role restricts what the user can do with the documents. See Default Roles on page 259.

Each user action triggers an event and all events are added to the GxP Admin Software system audit trail for compliance purposes. See Audit Trail on page 272.

See the _GxP Admin Software User Guide_ for how to manage users, Projects, and Roles.

### SoftMax Pro Software - GxP Edition

The SoftMax Pro Software - GxP edition is very similar to the SoftMax Pro Software - Standard edition for data collection and analysis of the data from a Molecular Devices microplate reader. Exceptions include a requirement that the user must enter a user name and password and then select a Project to use the SoftMax Pro Software - GxP edition. Users with the SoftMax Pro Access permission are assigned to at least one Project and their Role in each Project restricts what the user can do in the software.

The SoftMax Pro Software - GxP edition creates an audit trail for each document. The document-specific audit trail records the events that users trigger as they interact with the document. See Document Audit Trail on page 273.

### Administratively Controlled Access <a href="#administratively-controlled-access" id="administratively-controlled-access"></a>

The GxP Admin Portal Software is the interactive user interface for the GxP Admin Software. Use the GxP Admin Portal to create users. You grant each user Access permissions to allow them to use the software applications to which they need access. You then assign each user with the SoftMax Pro Access permission to Projects that limit their access to documents. For each Project, you assign the user to a Role that allows them to perform the tasks for which they are responsible.

The computer that runs the SoftMax Pro Software - GxP edition must be able to access the server that contains the GxP Admin Software to enforce the features that are under administrative control.

### Projects - Document Access Restrictions

Each user with the SoftMax Pro Access permission must be a member of at least one Project. Use Projects to limit which documents the user can access. Each user can be a member of multiple Projects.

### Roles - Workflow Permissions

Each user with the SoftMax Pro Access permission can have one Role in each Project. Each user can be a member of multiple Projects and can have a different Role in each Project. Use Roles to restrict the user's responsibilities in the SoftMax Pro Software - GxP edition.

Role permissions are grouped into the following categories:

#### Document Access Permissions

Use Document Access permissions to manage what users can do with documents.

![](<../../../.gitbook/assets/3 (9) (1).png>) **Open Imported** - Allows users to open documents that have the status: Imported.

![](<../../../.gitbook/assets/4 (7) (1).png>) **Open In Work** - Allows users to open documents that have the status: In Work.

![](<../../../.gitbook/assets/5 (9) (1).png>) **Open Review Pending** - Allows users to open documents that have the status: Review Pending.

![](<../../../.gitbook/assets/6 (9) (1).png>) **Open Reviewed** - Allows users to open documents that have the status: Reviewed. ![](<../../../.gitbook/assets/7 (9).png>) **Open Released** - Allows users to open documents that have the status: Released. ![](<../../../.gitbook/assets/8 (8).png>) **Open Outdated** - Allows users to open documents that have the status: Outdated.

![](<../../../.gitbook/assets/9 (7).png>) **Open In Progress** - Allows users to open documents that have the status: In Progress.

![](<../../../.gitbook/assets/10 (5).png>) **Open Approval Pending** - Allows users to open documents that have the status: Approval Pending.

![](<../../../.gitbook/assets/11 (7).png>) **Open Approved** - Allows users to open documents that have the status: Approved.

![](<../../../.gitbook/assets/12 (6).png>) **Open Canceled** - Allows users to open documents that have the status: Canceled.

#### Document Workflow Permissions

Use Document Workflow permissions to manage what users can do in the document workflow.

![](<../../../.gitbook/assets/13 (5).png>) **Set Review Pending** - Allows users to set documents to the status: Review Pending.

![](<../../../.gitbook/assets/14 (6).png>) **Set Reviewed** - Allows users to set documents to the status: Reviewed.

![](<../../../.gitbook/assets/15 (5).png>) **Released Protocol** - Allows users to release a document as a protocol which sets the document status to Released.

![](<../../../.gitbook/assets/16 (4) (1).png>) **Set Outdated** - Allows users to set documents to the status: Outdated.

![](<../../../.gitbook/assets/17 (4) (1).png>) **Generate Compliance Data** - Allows users to generate compliance data. For example, (using the system default Roles) this user would be the Lab Technician who can open a protocol document with the status Released. The software prompts the user to save the document as a data document and assigns the document the status In Progress. The user then runs the assay to generate compliance data.

![](<../../../.gitbook/assets/18 (6).png>) **Set Approval Pending** - Allows users to set documents to the status: Approval Pending.

![](<../../../.gitbook/assets/19 (5).png>) **Set Approved** - Allows users to set documents to the status: Approved.

![](<../../../.gitbook/assets/20 (5).png>) **Set Canceled** - Allows users to set documents to the status: Canceled.

#### Document Editing Permissions

Use Document Editing permissions to manage what users can do with documents.

&#x20;**Edit Reader Settings** - Allows users to define microplate reader acquisition settings.

&#x20;**Edit Notes Text** - Allows users to edit Note sections in the experiments in documents.

&#x20;**Read Empty Plates/Cuvettes** - Allows users to read empty Plate sections and empty Cuvette Set sections.

&#x20;**Function Editor** - Allows users to create custom curve fit functions.

&#x20;**Overwrite Plate/Cuvette Data** - Allows users to overwrite the data in Plate sections and Cuvette Set sections.

&#x20;**Edit Graphs, Summaries, and Reductions** - Allows users to edit Graph sections and to edit Summary formulas and Reduction formulas.

&#x20;**Assign Plate Layouts** - Allows users to assign plate layouts.

&#x20;**Edit Sample and Group Information** - Allows users to edit sample and Group section information.

&#x20;**Add/Delete Groups** - Allows users to add and delete Group sections from the experiments in documents.

&#x20;**Edit Formulas** - Allows users to edit formulas in documents.

&#x20;**Edit Print Options** - Allows users to edit the print options.

&#x20;**Lock/Unlock Sections** - Allows users to lock and unlock sections in the experiments in documents.

&#x20;**Mask/Unmask Wells** - Allows users to mask and unmask wells.

&#x20;**Create/Save As Data Document** - Allows users to save data documents to the database.

&#x20;**Create/Save As Protocol** - Allows users to save protocol documents to the database.

&#x20;**Change Auto Save Settings** - Allows users to change Auto Save settings.

&#x20;**Change Auto Export Settings** - Allows users to change Auto Export settings.

#### Statements & Signatures Permissions

Use Statement and Signatures permissions to manage what users can do with the statements.

&#x20;**Add/Modify Statements** - Allows users to edit statements.

&#x20;**Sign Statements** - Allows users to sign statements.

&#x20;**Revoke Own Signature** - Allows users to remove only their own signatures from statements.

&#x20;**Revoke Any Signature** - Allows users to remove any signature from statements.

#### Document Management Permissions

Use Document Management permissions to manage what users can do with the documents in the database.

&#x20;**Rename Document** - Allows users to rename documents.

&#x20;**Move Document** - Allows users to move documents to different folders in the database.

&#x20;**Delete Document** - Allows users to delete documents from the database.

&#x20;**Unlock Document** - Allows users to unlock documents.

&#x20;**Import Documents** - Allows users to import documents into the database.

&#x20;**Export Documents** - Allows users to export documents out of the database.

#### Folder Management Permissions

Use Folder Access permissions to manage what users can do with the document storage folders in the database.

&#x20;**Add Folder** - Allows users to create new folders in the database.  **Rename Folder** - Allows users to rename folders in the database.  **Move Folder** - Allows users to move folders in the database.

&#x20;**Delete Empty Folder** - Allows users to delete empty folders from the database.

&#x20;**Hide/Unhide Folder** - Allows users to hide and unhide folders and to use hidden folders in the database.

#### Instrument Permissions

Use Instrument permissions to manage what users can do with the microplate reader.

&#x20;**Lock/Unlock Instrument** - Allows users of the SpectraMax® iD3 Multi-Mode Microplate Reader and the SpectraMax® iD5 Multi-Mode Microplate Reader to lock and unlock the instrument touchscreen.

&#x20;**Instrument Simulator** - Allows users to simulate the connection between the SoftMax Pro GxP Software and an instrument.

### Logging In To The SoftMax Pro Software - GxP Edition

When you start the SoftMax Pro Software - GxP edition, the SoftMax Pro GxP Log On dialog displays.

To log on to the SoftMax Pro Software - GxP edition:

1. In the **\<User ID>** field, enter your user name.
2. In the **\<Password>** field, enter your password (case sensitive).
3. Click **Next** to display the Please Select a Project dialog.
4. Select a Project and click **Log In**.

### Logging On From Within The Software

In the Ribbon, on the GxP tab, use the icons to log out of the software and then log on to a different Project or as a different user.

*
  1. In the Ribbon, select the **GxP** tab.
  2. Click  **User Log Off** to log off. The SoftMax Pro GxP Log On dialog displays.
  3. Follow the steps above to log on.

### SpectraMax iD3 or iD5 Considerations

For users that use the SoftMax Pro Software - GxP edition to operate the instrument, the user must have the following permission to lock and unlock the instrument touchscreen:

&#x20;SoftMax Pro Software - GxP edition version 7.0.3 users require the Sign Signature permission.

&#x20;SoftMax Pro Software - GxP edition version 7.1.1 and later users require the Lock/Unlock Instrument permission.

In the Ribbon, on the GxP tab, users with appropriate permission can use the following icons to lock and unlock the instrument touchscreen:

&#x20;Click  **GxP Mode On** to lock the instrument touchscreen and operate the instrument from the computer running the SoftMax Pro Software in GxP mode. This locks the instrument touchscreen for all users and you must operate the instrument from a computer running the SoftMax Pro Software - GxP edition.

&#x20;Click  **GxP Mode Off** to release the lock from the instrument touchscreen and allow users to use the instrument touchscreen to run experiments.



**Note:** The instrument remains locked until the user with the appropriate permission

clicks  **GxP Mode Off** to stop the GxP mode. You cannot use the Instrument Connection dialog to disconnect from a SpectraMax iD3 and SpectraMax iD5 that is locked in GxP mode.

### Locking and Unlocking Sections

The SoftMax Pro Software - GxP edition allows users with the Lock/Unlock Sections permission to lock sections in an experiment to prevent changes. Users who do not have this permission cannot delete or edit a locked section. You can print locked sections with the document.

Select a section in the Navigation Tree and click  above the Navigation Tree to lock the section you select. Click  again to unlock the section.

Select an experiment in the Navigation Tree and click  above the Navigation Tree to lock all the sections in the experiment.

You cannot overwrite the data in a locked Plate section, but if a Plate section has no data, data can be acquired and added to the section.

### Account Information

Use the User Account Information dialog to view information about the user who is logged on.

To view user account information:

1. In the Ribbon, select the **GxP** tab.
2. Click  **Account Information** to display the User Account Information dialog.  The top section displays the user name and the time the user logged on.

&#x20;The middle section displays the contact information for the GxP Admin Software administrator.

&#x20;The lower section displays the permissions assigned to the user based on their Role in the Project they select upon log on.

1. Click **Close**.

### User Lock Session

Use the Session Is Currently Locked dialog to unlock your SoftMax Pro Software - GxP edition session after the software locks you out due to inactivity. The GxP Admin Software administrator defines how long you must remain inactive before the software locks your session.

**Note:** The software continues to collect data even when the user is locked out due to inactivity.



If your session is locked due to inactivity, do the following to unlock your session.

1. The Session Is Currently Locked dialog displays when your session is locked due to inactivity. You can also select the **GxP** tab and click  **User Lock Session** to display the Session Is Currently Locked dialog.
2. In the **Password** field, enter your password.
3. Click one of the following:

&#x20;Click **Verify** to verify your credentials and unlock the software.  Click **Stop Read** to stop a read in progress.

&#x20;Click **Close SMP** to close the SoftMax Pro Software - GxP edition and end the session (password not required).
