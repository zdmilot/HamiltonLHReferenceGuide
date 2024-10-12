# SiLA Communication Protocols

{% embed url="https://en.wikipedia.org/wiki/Standardization_in_Lab_Automation" %}

The consortium for Standardization in Lab Automation (SiLA) is a not-for-profit membership organization formed by software suppliers, system integrators and pharma/biotech companies. It develops and introduces new device and data interface standards allowing rapid integration of lab automation hardware and data management systems. Highly skilled experts of member companies contribute in SiLA's technical work groups. Membership is open for institutions, corporations and individuals active in the life science lab automation industry. The SiLA consortium provides professional training, support and certification services to suppliers and system integrators implementing SiLA compliant interfaces.

## Mission

SiLA is the global initiative to standardize software interfaces in the field of life science research instrumentation, like autosamplers, and laboratory automation. Instigated by the pharmaceutical industry's need for flexible laboratory automation, the initiative is supported by major device and software suppliers worldwide.

## Background

Understanding the mechanisms of life requires extensive, often repetitive, experimentation. Laboratory automation, therefore, has become instrumental to the progress of the life sciences. Industry provides commercial laboratory devices to perform increasingly sophisticated tasks. However, combining equipment from different providers to work in concert often proves impossible. Exporting captured data from proprietary software for further analysis can be frustrating or impossible. This situation leads to a waste of resources: Available equipment needs to be replaced for compatibility reasons, software drivers have to be purchased or developed, and data conversion is time-consuming. Such technical obstacles impede the development of higher level autonomous experimentation systems. SiLA enables researchers to focus on their scientific questions by reducing equipment connectivity effort to a minimum. This is achieved by using proven, tested and maintained documentation and code.

## History

Advancements seen on the home consumer electronics marked like USB or UPnP triggered the idea of applying a similar approach to the laboratory automation environment. Why was it possible to easily upload pictures from any digital camera on any computer but in the same time not even thinkable to replace a lab device (e.g.: a Shaker) of one brand with a Shaker of a different brand? Analyzing the situation led to the conclusion that the incompatibility was a result of missing interface definitions. The idea of a standardized interface based on the Common Command Set (CCS) concept was born. However, SiLA 1.x has some limitations: It is based on XML/Soap which is considered as outdated. Getting started with SiLA 1.x is not an easy process. This led to the proposition of a spin-off group of the SiLA consortium to develop a new standard: SiLA 2. Learning from SiLA 1.x and taking many concepts from it, SiLA 2 had the vision of being as accessible as possible. A major goal is to create a community constantly working on the development of new Features.

### SiLA 2

| Date | Event                                                                                                           |
| ---- | --------------------------------------------------------------------------------------------------------------- |
| 2022 | Official [SiLA 2 version 1.1](https://drive.google.com/file/d/1CP\_MTFmGZ89kkSfIXtPNQly97U1rcnuP/view) Release. |
| 2019 | Official [SiLA 2 version 1.0](https://drive.google.com/file/d/1QWrSD4-YBMwT9HTBzJe3TlBbJSGqq\_LC/view) Release. |
| 2018 | Release Candidate of SiLA 2.                                                                                    |
| 2017 | Successful Proof of Concept (PoC) of SiLA 2.                                                                    |
| 2016 | Official announcement of SiLA 2.                                                                                |

### SiLA 1.x

| Date | Event                                                             |
| ---- | ----------------------------------------------------------------- |
| 2013 | Release of the Device Control & Data Interface Specification 1.3. |
| 2012 | Release of the Device Control & Data Interface Specification 1.2. |
| 2010 | Release of the Device Control & Data Interface Specification 1.1. |
| 2009 | Release of the Device Control & Data Interface Specification 1.0. |

### Organization

| Date | Event                                                                                         |
| ---- | --------------------------------------------------------------------------------------------- |
| 2014 | Partnership with the Analytical Information Markup Language (AnIML).                          |
| 2008 | Foundation of SiLA Consortium as a not-for-profit membership organization.                    |
| 2007 | Successful Proof of Concept (PoC) of the Common Command Set concept by Hamilton and Novartis. |

## SiLA 2

SiLA 2 addresses control and data interfaces between devices and process management, LIMS and Enterprise Systems. It is built to connect systems in a laboratory, such as laboratory information management systems, electronic lab notebooks, chromatography software and laboratory devices such as balances, pipettors and various other analytical instruments. Enhancing the first standard SiLA 1.x by adopting proven concepts and applying already existing open standards and protocols in a "lean and mean" manner, SiLA 2 is designed to enable plug-and-play operations in the laboratory.

### Technical background <a href="#technical_background" id="technical_background"></a>

SiLA 2 considers every entity in the modern laboratory as a service. Focus on behaviour and service oriented design structures leads to the Feature Definition Language (FDL). SiLA 2 is based on a microservice architecture. Relying on HTTP/2, SiLA uses Protocol Buffers to serialize payload data. Furthermore, SiLA 2 uses the wire format provided by gRPC.

### Structures

SiLA 2 can split up into a Core and Feature level. The SiLA Core is written and maintained by the SiLA 2 Working group. SiLA Features are specific extensions that may change and evolve in any way. SiLA's basic structure consists of a client – server communication model. The SiLA Server (≙ web server) exposes all its capabilities to the SiLA Client (≙ web client). Capabilities of the SiLA Server are grouped together as SiLA Features.

### Features

The Feature concept serves as a common communication base for subject matter experts (SME), IT experts and end users. Each Feature is described by its Feature Definition, an XML-file containing information about parameters, interactions, data types, return values, etc. It exposes a certain number of Commands which model actions that can be performed by the SiLA Server.

### Cloud connectivity

SiLA 2 offers cloud functionality. For connecting, the SiLA-Client and SiLA-Server switch roles and a “reverse-channel” will be established – This way the connection will be initialized by the SiLA-Server which can reside in a local network. Cloud capabilities are given while maintaining regulated security policies and safety by relying on standard gRPC and HTTP/2 connection handling and security models.

## SiLA 1.x

SiLA 1.x has been used from 2009 until 2018. But getting started with SiLA 1.x is not an easy process. Furthermore, As SiLA 1.x is based on XML/Soap which is considered outdated. It is now replaced by SiLA 2.

### SiLA 1.x – Device Interface Standard <a href="#sila_1.x_-_device_interface_standard" id="sila_1.x_-_device_interface_standard"></a>

The SiLA device interface standard covers all ISO/OSI levels of the device control interface from physical to application layer. The interface standard is based on web service/SOAP communication with the devices. Commands are generally executed in asynchronous manner with an immediate response and a delayed event after completion of the command processing or after an error. Error recovery procedures are also supported and the general behavior of the devices is managed by a state machine. The state machine enables also complex behaviors like parallel processing of commands and command queuing. By supporting three different integration levels, SiLA provides a unique, standardized interface between lab automation devices and process management systems so that also legacy devices can be integrated in SiLA compliant systems. SiLA compliance can be achieved by providing native, directly embedded SiLA device interfaces or by software only SiLA drivers and/or interface converters. The SiLA Device Control and Data Interface Standard eases and accelerates the integration and adaptation of systems through generic Device Class Interfaces providing Common Command Sets.

### SiLA 1.x – Common Command Dictionary <a href="#sila_1.x_-_common_command_dictionary" id="sila_1.x_-_common_command_dictionary"></a>

By grouping devices of the same functionality device classes can be created. SiLA Common Command Sets define commands for these device classes. SiLA defines the command names, the number of parameters and their names as well as the return data. Since commands and parameters are described in the WSDL documentation tag of the commands web service, a process management software (PMS) can automatically generate a list available commands for each device. SiLA has defined about 30 device classes and a command library with about 100 commands. Commands range from mandatory commands that are needed to make transitions in the state machine, over required commands for the specific device class, to optional commands for which not every device in the device class might provide the functionality. In addition guidelines for the implementation of supplier-specific device commands and parameters are provided. Some commands are applicable for almost every device class. For example, the commands SetParameter, GetParameter, ExecuteMethod are widely used. Also PrepareForOutput and PrepareForInput are common because they enable the transport mechanisms to transfer labware items from device to device. The mandatory commands include operations like Reset, Initialize, Abort and Pause. In addition locking a device for exclusive use is provided.

SiLA has formed a not-for-profit membership organisation. SiLA requires members to pay annual membership dues. Details on membership classes and related fees can be found [here](https://sila-standard.com/join-us/).

## Organisation structure <a href="#organisation_structure" id="organisation_structure"></a>

SiLA is a not-for-profit membership corporation with global footprint. Membership is open for institutions, corporations and individuals active in the life science lab automation industry. The SiLA consortium provides professional training, support and certification services to suppliers and system integrators implementing SiLA compliant interfaces.

## External Links

* [ILT on Standardisation in Lab Automation](https://ilt.hsr.ch/Standardisation-in-Lab-Automat.12357.0.html)
* [Camunda as component in control software](http://unitelabs.ch/technology/control-software)
* [NIH on SiLA: Basic standards for rapid integration in laboratory automation.](https://www.ncbi.nlm.nih.gov/pubmed/22357556)
* [Researchgate on SiLA: Basic Standards for Rapid Integration in Laboratory Automation](https://www.researchgate.net/publication/221854198\_SiLA\_Basic\_Standards\_for\_Rapid\_Integration\_in\_Laboratory\_Automation)
* [SiLA 2 Hands-on](https://medium.com/@matthieu.croissant/sila-2-hands-on-bringing-automation-to-the-laboratory-dacc12df7152)
* [Autonomous Robot running with SiLA](https://www.linkedin.com/posts/bryn-roberts-685171\_labautomation-robotic-autonomous-activity-6582897402808676353-b4TK)
* [Roche's Camunda-based AutoLab software](https://www.youtube.com/watch?v=B-LU1Tq7qYw)
* [Implementing a digital infrastructure for the lab using a central laboratory server and the SiLA2 communication standard, _Engineering in Life Sciences_](https://onlinelibrary.wiley.com/doi/full/10.1002/elsc.202000053)

## Sources

* [SiLA homepage](http://www.sila-standard.org/)
* [SiLA 2 Specification version 1.1](https://drive.google.com/file/d/1CP\_MTFmGZ89kkSfIXtPNQly97U1rcnuP/view)
* [SiLA 2 GitLab](https://gitlab.com/SiLA2/)
* [Official SiLA 2 Documentation](https://sila2.gitlab.io/sila\_base/)
