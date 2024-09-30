---
icon: dev
---

# Prepare the Vector Database

‌Overview

This guide will assist the user in preparing VENUS's SQL database as a local Administrator. If a login with credentials is required or the below steps do not resolve the issue, please refer to the SQL Server Database Manual Installation Guide.

\


‌How to Prepare the Vector Database

1. ## Open Method Editor and run the System Configuration Editor from the Tools drop-down
2. ## Accessing the DB connection
   1. Select System Settings from the options on the left
   2.  Under the Sample Tracking settings, select the "…" for the Vector Database connection entry

       \


       ![image](blob:https://app.gitbook.com/6bf05b5d-27a5-4a53-844b-4cec76912b12)

       \

3. ## Vector Database Connection Settings: Trusted
   1. Local Admin login (recommended)
   2. To be used when there is a single user login to the Hamilton PC
   3.  This will connect the database to the current Windows user (only)

       ![image](blob:https://app.gitbook.com/b4a5dfab-14b9-47be-9aaf-aa0a39dc8fc5)
   4. Perform the following steps:
      * Server: LOCALHOST\HAMILTON
      * Database: HamiltonVectorDB
      * Trusted Connection: Yes
      * Username: Can be left blank
      * Password: Can be left blank
   5. Once the connection settings are established, select "Prepare Server"
   6.  Refer to the VENUS Programmer's Manual and the SQL Server Database Manual Installation Guide for additional connection settings.

       \


       ![image](blob:https://app.gitbook.com/b2ecd478-dc96-4681-b9b4-0cafb73b3038)
4. ## Server Preparation: Trusted
   1. Perform the following steps:
      * Ensure "Create Database" is selected
      * De-Select "Create Login"
      * Set Trusted Connection to "Yes"
      * Username: Can be left blank
      * Password: Can be left blank
   2. Select "OK"
   3. Select "Yes" when prompted
   4.  Select "OK" once the server preparation is complete

       \

5. ## Test the connection
   1. Return to the Vector Database Connection Settings window, and select "Test Connection"
   2.  Select "OK" once the test is complete

       \


       ![image](blob:https://app.gitbook.com/343bd627-5bf7-43a6-938c-268ef8a15ec3)

       \

6. ## If the connection test fails, ensure that the DB Startup Type is set to "Automatic Start"
   1. Open windows services (services.msc)
   2. Navigate to and select "SQL Server (HAMILTON)"
   3. From the "Startup-type:" drop-down, select "Automatic" and then click "Apply" and finally "OK"

\


![image](blob:https://app.gitbook.com/c7479bc7-d875-4525-b7a9-c2208f6826be)
