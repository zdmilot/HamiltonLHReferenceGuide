---
icon: dev
description: >-
  This guide will assist the user in preparing VENUS's SQL database as a local
  Administrator.
---

# Prepare the Vector Database

If a login with credentials is required or the below steps do not resolve the issue, please refer to the [SQL Server Database Manual Installation Guide](https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FSJm30951AW7z9xuqm5sS%2Fuploads%2F7u2NZxAL6Csgn7CE07Ry%2FSQL%20Server%20Database%20Manual%20Installation%20v1.pdf?alt=media\&token=3f0491d9-bfb2-4cc8-8d6b-f457d913d9f0).



‌How to Prepare the Vector Database

1. Open Method Editor and run the System Configuration Editor from the Tools drop-down
2. Accessing the DB connection
   1. Select System Settings from the options on the left
   2.  Under the Sample Tracking settings, select the "…" for the Vector Database connection entry

       \


       <figure><img src="../.gitbook/assets/image (8) (1) (1) (1).png" alt="" width="343"><figcaption></figcaption></figure>

       \

3. Vector Database Connection Settings: Trusted
   1. Local Admin login (recommended)
   2. To be used when there is a single user login to the Hamilton PC
   3.  This will connect the database to the current Windows user (only)

       <figure><img src="../.gitbook/assets/image (9) (1) (1) (1).png" alt="" width="281"><figcaption></figcaption></figure>
   4. Perform the following steps:
      * Server: LOCALHOST\HAMILTON
      * Database: HamiltonVectorDB
      * Trusted Connection: Yes
      * Username: Can be left blank
      * Password: Can be left blank
   5. Once the connection settings are established, select "Prepare Server"
   6. Refer to the VENUS Programmer's Manual and the SQL Server Database Manual Installation Guide for additional connection settings.
4.  Server Preparation: Trusted



    <figure><img src="../.gitbook/assets/image (10) (1) (1) (1).png" alt="" width="178"><figcaption></figcaption></figure>

    1. Perform the following steps:
       * Ensure "Create Database" is selected
       * De-Select "Create Login"
       * Set Trusted Connection to "Yes"
       * Username: Can be left blank
       * Password: Can be left blank
    2. Select "OK"
    3. Select "Yes" when prompted
    4.  Select "OK" once the server preparation is complete


5. Test the connection
   1. Return to the Vector Database Connection Settings window, and select "Test Connection"
   2.  Select "OK" once the test is complete

       \


       <figure><img src="../.gitbook/assets/image (11) (1) (1) (1).png" alt="" width="281"><figcaption></figcaption></figure>

       \

6. If the connection test fails, ensure that the DB Startup Type is set to "Automatic Start"
   1. Open windows services (services.msc)
   2. Navigate to and select "SQL Server (HAMILTON)"
   3. From the "Startup-type:" drop-down, select "Automatic" and then click "Apply" and finally "OK"

<figure><img src="../.gitbook/assets/image (12) (1) (1) (1).png" alt="" width="254"><figcaption></figcaption></figure>



{% file src="../.gitbook/assets/QuickGuide_PrepareVectorDatabase_v1-2.pdf" %}

{% file src="../.gitbook/assets/SQL Server Database Manual Installation v1.pdf" %}
