# The Lab Automation Software Landscape

Entering the world of lab automation, you’ll find yourself in an overwhelming environment of software suites and tools and interfaces—each more proprietary than the last. Somehow you find that each tool is totally dependent on and yet incompatible with its neighbor, like a digital rat king that feeds solely on money and spreadsheets. What does such a beast look like? Something like this.

![A diagram illustrating how different lab automation software tools might interact with each other.](https://theautomatedlab.com/assets/images/content/software-landscape-diagram.png)

Here is a guide to the types of software you may encounter, what they do, and what to be prepared for when navigating your lab’s software stack.

#### Automation Execution

As an automation engineer, this is your primary domain. This umbrella includes the software that is directly responsible for making equipment work. It will look different depending on the level of automation and the diversity of devices implemented in your lab.

**Device Control Software**

This is the category of software responsible for controlling a specific device. I have broken this down into loosely defined categories for educational purposes.

**"Standard"**

Many lab devices come with some kind of desktop software that is either necessary or helpful for operation of the device. This vendor-provided software generally has a graphical user interface (GUI) for inputting instructions as well as a programmable interface (API) that enables other software to communicate with the device. A well-documented API is one of the features that makes a lab device “automation-friendly”.

**Liquid Handlers**

Liquid handlers are generally the most complex category of lab automation devices, and they come with powerful and expensive software to match. This software includes some kind of programming language for writing liquid handling scripts, some kind of scheduling software to coordinate the on-deck robot(s), and a number of bells and whistles that may or may not provide you any value.

**Analytical Devices**

Analytical devices—devices whose function is to produce meaningful scientific data from samples—generally come with desktop software that allows for users to both define the analysis script and to view and analyze the data produced by the device, as raw data output may be difficult if not impossible for a human to understand.

**Single-Function Devices**

Single-function devices like plate sealers and peelers may not require software on an external computer in order to function. These devices often have a physical interface (a touchscreen or buttons) for standalone operation as well as an API.

**Device Drivers**

Device drivers are where we get a bit into the weeds and out of scope for the average lab automation engineer. If you are familiar with drivers _outside_ the world of lab automation, please read carefully and hold your boos. Within lab automation, we use device driver to refer to software that enables one piece of software to communicate with a device API. These are generally written in C# or python, rather than C or C++. For the uninitiated, device driver also refers to the low-level programming that makes your mouse or keyboard work. The function is similar in both cases, but the expertise is extremely different. Listen. I didn’t invent the term, I’m just propagating it.

#### Scheduling Software

Scheduling Software is the mastermind that sits atop an integrated automation system and sequences events across devices. Its only required function is to schedule and execute tasks, but scheduling software products often include a rich feature set given their importance in scaling up lab automation. Features may include:

* Visual programming language for defining automated processes
* Error alerting and resolution graphical user interface (GUI)
* Device control and robot teaching GUI
* Barcode tracking
* Capture and consolidation of driver logs
* Data handling
* LIMS/ELN/MES integration API

#### Data Infrastructure

Data is often overlooked in the lab automation pipeline, despite it being the main reason we do lab work. I’ll focus on two categories of data in the lab automation landscape: analytical and process data.

**Analytical Data**

Analytical data is the information that we seek to glean from an experiment. These are the data produced by analytical devices like plate readers, ddPCR machines, chromatography machines, etc. Making this data accessible to the end user or customer should be top priority when assessing data infrastructure.

**Process Data**

Process data is the information about what happened during an automated process. This data is valuable for quality control, troubleshooting, and performance tracking of automated processes, but is often not trivial to collect given the diverse array of software and hardware that could generate this category of data.

#### Lab Management

Now we’re getting to software components that are squarely outside the domain of the Automation Engineer. However, they may be a critical part of your lab’s software ecosystem, and therefore a constraint on how automation and data handling is implemented.

![](https://theautomatedlab.com/assets/images/content/venn-diagram-software.png)

**Lab Inventory Management System (LIMS)**

A LIMS is operator-facing software for managing and tracking lab supplies, equipment, and samples. Your lab’s LIMS software will (hopefully) be quite specific to the type of lab work performed in your lab. In an ideal automated lab, there is automatically transfer of data from LIMS to automation equipment and vice versa as processes are requested and data is generated. This ideal is rarely realized.

**Electronic Lab Notebook (ELN)**

An ELN is operator-facing software that attempts to mimic and improve upon the traditional paper lab notebook. Features and usage vary wildly across products and labs, and so it may or may not require integration with automation infrastructure.

**Manufacturing Execution System (MES) & Lab Execution System (LES)**

MES Software is relatively new to lab environments, becoming more relevant as biotechnology matures as an industry. Emerging from the world of industrial manufacturing and automation, its focus is on coordination of large-scale, routine processes like the manufacturing of pharmaceuticals, food, and electronics. Few organization have achieved anything close to factory-scale lab automation, and these are the teams trying to figure out what an MES looks like in a lab setting.

While the MES is old, the LES is new. I include both in this category as it is not yet clear to me how they will shape out in the world of lab automation.

***

Source: [https://theautomatedlab.com/article.html?content=automation-software-landscape](https://theautomatedlab.com/article.html?content=automation-software-landscape)
