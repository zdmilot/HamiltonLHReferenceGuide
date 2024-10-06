---
icon: dev
---

# Configuration in VENUS

Depending on whether the database was set up by VENUS during the original install or the install was performed manually according to Section 2, configuring the database in VENUS will differ in terms of the username and password combination used. If done via the VENUS installation, a specific username is generated for the login, while a manual install relies on the ‘sa’ account.

\


## ‌ Hamilton System Configuration

* Open Method Editor
* Go to Tools > System Configuration Editor
* Under System Settings (1) click the line titled Vector Database connection (2)
*   Click \[…] on the right side (3)

    ![](<../../.gitbook/assets/image (32).png>)\

* On the Vector Database Connection Settings screen, enter the server name (if using the default VENUS database install or following instructions from Section 2, the Server will be LOCALHOST\HAMILTON) (1)
* Enter a database name (2), typically:
  * Server: LOCALHOST\HAMILTON
  * Database: HamiltonVectorDB
  * Trusted Connection: Yes
  * Username: ‘Hamilton’ if using the default VENUS installation, but if manually installing the database, enter ‘sa’ as the username (4)
  * Password: mkdpw:V43
  * Set Trusted Connection to No (3)
*   If the database was installed manually, Click Prepare Server (6) and follow the remaining instructions – if the database was installed by VENUS during the original install, skip this step, click Test Connection, and then click OK to finish setup

    ![](<../../.gitbook/assets/image (33).png>)\

*   On the Vector Database Server Preparation screen, make sure Create Database

    (1) is checked
* Uncheck the Create Login (2) option
* Set Trusted Connection to No (3)
* Enter the same Username and Password (4) used in the previous screen
*   Click OK (5)

    ![](<../../.gitbook/assets/image (34).png>)\


    \

*   When presented with the “Are you sure you want to prepare the database server?” dialog, click Yes (1)

    ![](<../../.gitbook/assets/image (35).png>)\


    \

*   When presented with the “The server has been successfully prepared” dialog, click

    OK (1)

    ![](<../../.gitbook/assets/image (36).png>)\


    \

*   Back on the Vector Database Connection Settings screen, click Test Connection

    (1) to verify the connection is working (if an error is displayed, make sure you are using the same settings used in the Prepare Server dialog)
* Click OK to acknowledge the pop-up
*   Click OK (2) to complete the setup

    ![](<../../.gitbook/assets/image (37).png>)\




{% file src="../../.gitbook/assets/QuickGuide_PrepareVectorDatabase_v1-2.pdf" %}

{% file src="../../.gitbook/assets/SQL Server Database Manual Installation v1.pdf" %}
