# Understanding and Using the Hamilton Vector Database

The **Hamilton Vector Database** is one of the more complex and lesser-known parts of the VENUS platform, but it can provide powerful insights into your system’s operations, from logfile parsing to usage tracking and telemetry of operations. If you’ve ever found yourself puzzled by how to properly set up and use the Vector Database, you’re not alone. Below is a guide based on community discussions and expert insights to help you get started.

## What is the Vector Database?

The **Vector Database** was introduced in Vector 4.1 and became part of the standard **VENUS** platform starting with Vector 4.2. VENUS stands for **Vector NEw USer Software**. The database functionality allows you to store run-time actions, track samples, and manage worklists, providing a structured way to analyze data from different runs.

## Why Use the Vector Database?

The database offers the ability to:

* **Track usage** across various operations.
* **Parse logfiles** for telemetry data.
* **Centralize data** from multiple instruments when using **Vector Database Plus**.
* **Create custom reports** based on past runs.

However, the setup and usage can be confusing, and official documentation is limited. The community has identified several useful steps to help users configure and utilize this feature effectively.

## Steps to Set Up the Vector Database

1. **Install the Database**\
   If you're using the standard VENUS installation, a database file is created during each run and stored in the **LogFiles** directory. The data is saved in an `.mdf` file, which is the main database file, while the `.ldf` file logs Microsoft SQL Server actions.\
   \
   To expand the functionality, **Vector Database Plus** is available as a separate installer. This version stores all run information in a single database file, making it easier to query and manage historical run data across multiple instruments. Note that **Vector Database Plus** may come at an additional cost.\

2. **Enable Sample Tracking**\
   To start gathering useful data, you need to enable **Sample Tracking** in the system configuration. Once enabled, your methods will begin populating the database with sample and run information. You can view this data using the **Hamilton Vector Data Manager** application.\

3. **Access the Data**\
   Once the database is set up and populated, you can access the data using the **HxVectorDbManager.exe**. This application acts as a viewer for the data stored in the database, allowing you to see the run history and state of labware during each method execution.\
   \
   For more advanced data handling, you can query the SQL database directly, or use Microsoft SQL Server Management Studio (SSMS) if you’re running **Vector Database Plus**.

## Frequently Asked Questions

### **Where is the data stored?**

For a standard VENUS install, the database files are stored in the **LogFiles** directory. The `.mdf` file contains the actual data, and the `.ldf` file logs SQL Server actions.

If you're using **Vector Database Plus**, all the run data is consolidated into a single database file, which is ideal for centralized management and network sharing across multiple instruments.

### **Can I use this to track telemetry and usage?**

Yes, by parsing logfiles and analyzing the data stored in the database, you can track system telemetry and operation usage. This is particularly useful for understanding run performance and optimizing workflows.

### **How do I configure the system for multiple instruments?**

With **Vector Database Plus**, you can store data from multiple instruments in the same database, allowing you to track operations across your entire lab. This is not possible with the standard installation, where each instrument generates its own database file.





***



[Lab Automation Forums](https://labautomation.io/)

[Hamilton (Venus)](https://labautomation.io/c/hamilton-venus/7)[smohler](https://labautomation.io/u/smohler) September 2, 2022, 1:01am

> Okay enough is enough, can someone anywhere provide a step by step guide _screenshots encouraged_ of a how to example of how to use this part of the platform.
>
> This seems like the murkiest, black box, least utilized part of the platform, while at the same time something that has the power to answers a lot of business questions. (Logfile parsing, usage tracking, telemetry of operations)
>
> So what the heck Hamilton… where them docs at, they’re not in any of the trainings🧐



[EricSindelar\_Hamilton](https://labautomation.io/u/EricSindelar\_Hamilton) September 2, 2022, 1:45pm3

> I have shared what materials I have regarding the Vector Database [here](https://download.hamiltonsupport.com/wl/?id=bcZFtm51580iePPUWauvSHq8HSLX505y).
>
> The database functionality was introduced way back in Vector 4.1. With Vector 4.2, Hamilton software was rebranded as VENUS one making it fun for all of us to keep track of our software revisions. Because we enjoy acronyms so much, VENUS stands for **V**ector **NE**w **US**er software.
>
> I also included a brief ppt on Vector Database Plus - a separate installer that allows for more expanded functionality. Vector Database Plus is the Vector Database, which handles sample tracking and runtime actions as well as a way to insert and manage worklists. The difference is that in standard VENUS installs, every run produces its own database file accessible through the SQL Server. With Vector Database Plus, my understanding is that all information gets saved in a single database and you also get a full version of MSSQL Server. The benefit is that for IT purposes, data from all runs are saved in the same file so you can build custom run results to pull data from numerous runs or maybe go back to previous months and produce a result file from a run. All of this is done outside VENUS.
>
> The other thing Vector Database Plus allows for is to store run information from numerous instruments in the same database. This is where the network sharing comes in. This functionality is not possible with the standard install and is moot anyway since you would end up with a network share with thousands of individual database files.
>
> Stateside, the Vector Database Plus installer comes at an additional cost - I’m not sure how this is managed overseas. It would be best for you to work with your local representatives on such matters.
>
> I am not aware of a more “customer-facing” guides, but I can follow up internally. The majority of our setups do not require a deeper dive into this functionality. This explains why it isn’t covered in our basic or even advanced training content. I also don’t explicitly train the applications support team on it either. As such, support will be limited.
>
> All that being said, I hope you find what I posted to be helpful for your efforts.



[smohler](https://labautomation.io/u/smohler) September 2, 2022, 4:40pm

> [![Screen Shot 2022-09-02 at 12.35.02 PM](https://labautomation.io/uploads/default/optimized/1X/3ab5d743ee1dd08d3ce9a7a495ff3db8ed66f52b\_2\_690x251.jpeg)](https://labautomation.io/uploads/default/original/1X/3ab5d743ee1dd08d3ce9a7a495ff3db8ed66f52b.jpeg)
>
> \
> Alright [@EricSindelar\_Hamilton](https://labautomation.io/u/ericsindelar\_hamilton) so it says the Database is on, then I opened up this Hamilton Vector Data Manager and see a DB is attached…but then ummmm
>
> But what’s the next step to not just go to the `LogFiles\` to find out what’s happening on the STARs. There’s gotta be a ton of people also trying to google these get up and running questions as well but just give up quickly which is why I bet Hamilton doesn’t get a lot questions about this stuff&#x20;



3 Likes[EricSindelar\_Hamilton](https://labautomation.io/u/EricSindelar\_Hamilton) September 2, 2022, 6:30pm7

> You’ll need to enable Sample Tracking in the system configuration so there is content. Once that is On and you run some methods, you will see more entries in the Database Manager.



[smohler](https://labautomation.io/u/smohler) September 2, 2022, 7:12pm8

> Okay so now I can get all the device to log their operations in a this database app and I can view it when I run the `Hamilton.HxVectorDbManager.exe` but this app seems to be just a viewer. Where is this structured data living? Are they one of the 3 file written to the log folder or are they somewhere else not that I have enabled this sample tracking?



[EricSindelar\_Hamilton](https://labautomation.io/u/EricSindelar\_Hamilton) September 2, 2022, 7:56pm9

> For standard VENUS installs, it purges everything into a separate database export in the LogFiles directory. The \*.mdf file is the real data ‘keeper’ and contains the data from the Vector database. The \*.ldf is a logfile of the Microsoft SQL Server.
>
> I’m not sure if it will contain everything you are looking for though - my understanding is that it mostly pertains to the state of the labware during the run - the materials I shared provide a broad overview of the functionality and database design.

