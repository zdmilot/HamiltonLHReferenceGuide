---
icon: dev
---

# Venus’s Vector Core

<figure><img src="../../.gitbook/assets/image (168).png" alt=""><figcaption></figcaption></figure>

This infographic showcases the efficient utilization of vector backbones in Hamilton liquid handling systems like VENUS and NIMBUS platforms. The vector backbone provides core functionalities such as Run Control, Labware Editor, Liquid Class Editor, and Method Editor. VENUS uses vector files to control both STAR and Vantage platforms, ensuring precise execution of workflows and enhanced pipetting control with Vantage's advanced capabilities.

The utilization of the SQL server and the server commands are aimed to keep this vector up to date for each installation. See [prepare-the-vector-database.md](../page-4/optional-sql-server-installation/prepare-the-vector-database.md "mention") for more information about setup of this database.

## Sample Tracking in v4.1

* Vector Database
* Microsoft SQL Server
* Huge HSL library
* Extended functionality
  * BVS tracking
  * Worklist management
  * Reloading
* 2 versions: Standard & Plus

## Standard / Plus Version

* Standard Version: Part of the HAMILTON Vector Software v4.1
* Plus Version: Additional Feature
  * Support of Remote Database Servers
  * Tracking over multiple Runs

## Architecture

<figure><img src="../../.gitbook/assets/image (29) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

## Database Model

<figure><img src="../../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

## Accessability to Vector Database Contents

All three main parts available via

* COM interfaces
* HSL libraries

<details>

<summary>Tracking</summary>

## Tracking

* Tracking Devices
  * Microlab STAR (incl Starlet & Plus)
  * BVS
* Tracking Actions
  * Load / Unload
  * Volume Moves
  * Transports
  * Custom Actions
* Report Mapping File
* Each action manipulates at least the tables:
  * HxLabwareRunData
  * HxLabware
  * HxLabwareAction
  * HxAction
* Per action specific data is stored in seperate tables
  * HxActionMoveVolume, HxActionMove, etc

</details>

<details>

<summary>Worklist Mangement</summary>

## Worklist Management

* Import of custom worklists
* Automatic assigning of loaded labware to open jobs
* Automatic sequence generating for jobs



### Worklist Handling

#### Available Steps:

*   ### Import Worklist 1)

    Imports a worklist (Text, Excel or Access) into the Vector Database
*   ### Load and Match 2)

    Loads Labware (samples or plates) and generates sequences/arrays based on the loaded labware and its matching worklist items
*   ### Update Sample Status 1)

    Sets the processing state for worklist items to processed. Only used if Load & Match is used multiple times within same run or worklist is used over multiple runs.

    \


    #### Legend:

    1. Data Handling Steps
    2. Microlab Star Smart Steps

### Worklist Handling: Example 1

*   Load sample tubes with barcode and process all samples which are in the worklist\
    ![](<../../.gitbook/assets/image (4) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png>)\


    <figure><img src="../../.gitbook/assets/image (3) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

### Worklist Handling: Example 2

* Load plate and process all hits with a density greater than 0.6. Process each hit with an individual volume and liquid class.\
  \
  ![](<../../.gitbook/assets/image (5) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png>)
*

    <figure><img src="../../.gitbook/assets/image (6) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>



</details>

<details>

<summary>Filtering</summary>

## Filtering

* AT Filter functionality\
  ![](<../../.gitbook/assets/image (7) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png>)

</details>

