# Authentication Systems

Hamilton provides two independent authentication systems for the Hamilton software:

* Operating System Authentication System
* Hamilton Authentication System

<table data-header-hidden><thead><tr><th width="145"></th><th></th></tr></thead><tbody><tr><td><img src="../../.gitbook/assets/image (9) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""></td><td><p>ATTENTION </p><p>Access rights must first be defined for the “Lab Service” before any changes can be made in the System Configuration Editor. </p></td></tr></tbody></table>



## ‌Choosing the Authentication System‌

1.  Open the system configuration editor.

    <figure><img src="../../.gitbook/assets/image (130) (1) (1).png" alt="" width="352"><figcaption></figcaption></figure>
2. Proceed to “Security Settings” and specify the settings shown below.
3. Click the “Function Protection” entry to enable it.
4. Select the desired authentication system.
5.  Click the “File -> Save Changes” Menu, to save the changes made.\


    <figure><img src="../../.gitbook/assets/image (131) (1) (1).png" alt="" width="375"><figcaption></figcaption></figure>



## ‌Operating System Authentication System‌



VENUS Software has five different levels of access authorization.

| Group                                     | User                                 | Authorization                                                |
| ----------------------------------------- | ------------------------------------ | ------------------------------------------------------------ |
| “Lab Operator”                            | Routine User                         | Operators may run any method                                 |
| “Lab Operator 2”                          | Routine User                         | Operators 2 may run any method and move elements on the deck |
| <p><br></p><p>“Lab method programmer”</p> | Method Programmer Laboratory Manager | Method programmers may modify method and labware definitions |
| <p><br></p><p>“Lab Remote Service”</p>    | LAN Manager PC Administrator         | <p><br></p><p>Remote Service</p>                             |
| <p><br></p><p>“Lab Service”</p>           | Service Engineer Laboratory Manager  | Hamilton Trained Field Service Engineer                      |

\


1.  Start by navigating through the explorer. Right click on “Computer” and select “Manage” from the list.

    <figure><img src="../../.gitbook/assets/image (132) (1) (1).png" alt="" width="372"><figcaption></figcaption></figure>
2.  The “Computer Management” Window will be displayed.

    <figure><img src="../../.gitbook/assets/image (133) (1) (1).png" alt="" width="375"><figcaption></figcaption></figure>
3.  Open “Local Users and Groups”.

    <figure><img src="../../.gitbook/assets/image (134) (1) (1).png" alt="" width="375"><figcaption></figcaption></figure>
4.  Click on “Groups“, to display the list of defined groups. Groups such as “Lab Operator“, “Lab Operator2“, “Lab Method programmer“ and “Lab Service“ can be found on the list.

    <figure><img src="../../.gitbook/assets/image (135) (1) (1).png" alt="" width="375"><figcaption></figcaption></figure>

    Here, all users engaged in routine laboratory work (members of the “Lab Operator” group) must be keyed in to obtain the appropriate access rights.
5.  Double-click on “Lab Operator”. The “Lab Operator Properties” window will appear. Click the \[Add] Button.\


    <figure><img src="../../.gitbook/assets/image (136) (1) (1).png" alt="" width="311"><figcaption></figcaption></figure>

    <table data-header-hidden><thead><tr><th width="145"></th><th></th></tr></thead><tbody><tr><td><img src="../../.gitbook/assets/image (9) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""></td><td><p>ATTENTION</p><p>Decide if the user is to be defined only locally or also for the domain (when the PC is in a network environment).</p></td></tr></tbody></table>

    \

6.  On the “Select Users” Screen, click the \[Locations…] Button.\


    <figure><img src="../../.gitbook/assets/image (137) (1) (1).png" alt="" width="354"><figcaption></figcaption></figure>

    \
    Select the correct “Location” source for the laboratory and click \[OK].
7.  The entry “From this location” in the “Select Users” Window is then filled in.\


    <figure><img src="../../.gitbook/assets/image (138) (1) (1).png" alt="" width="385"><figcaption></figcaption></figure>

    \


    <table data-header-hidden><thead><tr><th width="145"></th><th></th></tr></thead><tbody><tr><td><img src="../../.gitbook/assets/image (10) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""></td><td><p>NOTE </p><p>The content on the “Locations” Screen will be different for each customer location.</p></td></tr></tbody></table>

    \

8.  Click the \[Advanced] Button.\


    <figure><img src="../../.gitbook/assets/image (139) (1) (1).png" alt="" width="354"><figcaption></figcaption></figure>
9.  Either click \[Find Now], or type the complete name or the beginning of a name in the “Common Queries” Text Field, this will search for a matching name. Click \[OK].\


    <figure><img src="../../.gitbook/assets/image (140) (1) (1).png" alt="" width="305"><figcaption></figcaption></figure>
10. Once the name is found, select \[OK], and the person will be added to the “Select Users” screen.\


    <figure><img src="../../.gitbook/assets/image (141) (1) (1).png" alt="" width="354"><figcaption></figcaption></figure>
11. Repeat the previous steps to add additional names. Once all required names are included, click \[OK].
12. The selected user will then be added to the members list. Click \[OK] to finish.

    <figure><img src="../../.gitbook/assets/image (142) (1) (1).png" alt="" width="311"><figcaption></figcaption></figure>
13. After defining the access rights, log off and then log on again. Check that the installation was successful by logging on with every specified user.\
    \


    <table data-header-hidden><thead><tr><th width="145"></th><th></th></tr></thead><tbody><tr><td><img src="../../.gitbook/assets/image (9) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""></td><td><p>ATTENTION</p><p>Unregistered users cannot operate the VENUS Software – not even LAN administrators. The following error message is displayed in the case of unauthorized access attempts:<br><img src="../../.gitbook/assets/image (143) (1) (1).png" alt=""></p></td></tr></tbody></table>





## Hamilton Authentication System‌

The Hamilton authentication system is a log-on system implemented by the Hamilton Software to apply user rights independently from the operating system.

<table data-header-hidden><thead><tr><th width="145"></th><th></th></tr></thead><tbody><tr><td><img src="../../.gitbook/assets/image (9) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""></td><td><p>ATTENTION</p><p>The Hamilton authentication system does not comply with 21 CFR Part 11.</p></td></tr></tbody></table>



Hamilton Software has four different levels of access authorization.

| Group                                     | User                                 | Authorization                                                |
| ----------------------------------------- | ------------------------------------ | ------------------------------------------------------------ |
| “Lab Operator”                            | Routine User                         | Operators may run any method                                 |
| “Lab Operator 2”                          | Routine User                         | Operators 2 may run any method and move elements on the deck |
| <p><br></p><p>“Lab Method Programmer”</p> | Method Programmer Laboratory Manager | Method programmers may modify method and labware definitions |
| <p><br></p><p>“Lab Remote Service”</p>    | LAN Manager PC Administrator         | <p><br></p><p>Remote Service</p>                             |
| <p><br></p><p>“Lab Service”</p>           | Service Engineer Laboratory Manager  | Hamilton Trained Field Service Engineer                      |

1.  Open the system configuration editor.

    <figure><img src="../../.gitbook/assets/image (144) (1) (1).png" alt="" width="352"><figcaption></figcaption></figure>
2.  Proceed to the security settings. Click the text field beside the “Authentication System” label and select “Hamilton Authentication System” from the list.

    <figure><img src="../../.gitbook/assets/image (145) (1).png" alt="" width="563"><figcaption></figcaption></figure>
3.  Click the “File -> Save Changes” Menu, to save changes. A confirmation dialog will be displayed.

    <figure><img src="../../.gitbook/assets/image (146) (1).png" alt="" width="350"><figcaption></figcaption></figure>
4.  If the system was installed without “Function Protection” (disabled by default) the “Security Settings” message dialog shown below will appear.

    <figure><img src="../../.gitbook/assets/image (147) (1).png" alt="" width="344"><figcaption></figcaption></figure>
5.  To save the settings, click \[Yes].

    <figure><img src="../../.gitbook/assets/image (148) (1).png" alt="" width="337"><figcaption></figcaption></figure>
6.  Confirm that no other Hamilton applications are running by clicking \[Yes].


7.  To log in as administrator, type the user name and password of the default login:

    <figure><img src="../../.gitbook/assets/image (149) (1).png" alt="" width="295"><figcaption></figcaption></figure>

    User: administrator

    Password: Hamilton

    <table data-header-hidden><thead><tr><th width="145"></th><th></th></tr></thead><tbody><tr><td><img src="../../.gitbook/assets/image (10) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" data-size="original"></td><td><p>NOTE</p><p>Remember that user names and passwords are case-sensitive.</p></td></tr></tbody></table>


8.  Proceed to the “Manage Users” Tab in the system configuration editor to define the user rights.

    <figure><img src="../../.gitbook/assets/image (150) (1).png" alt="" width="563"><figcaption></figcaption></figure>
9.  Go to “Action -> Create new User”

    <figure><img src="../../.gitbook/assets/image (151) (1).png" alt="" width="563"><figcaption></figcaption></figure>
10. Fill the text fields with the required information and click \[OK].

    <figure><img src="../../.gitbook/assets/image (152) (1).png" alt="" width="300"><figcaption></figcaption></figure>
11. The “Permissions” for the user can be changed at the bottom of the window after creating the user as highlighted on the image shown below.

    <figure><img src="../../.gitbook/assets/image (153) (1).png" alt="" width="563"><figcaption></figcaption></figure>

\


