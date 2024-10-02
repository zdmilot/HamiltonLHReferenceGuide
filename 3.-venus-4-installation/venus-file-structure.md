---
icon: dev
---

# Venus file structure

The Hamilton Venus software, widely used for lab automation, organizes its files into various folders and subdirectories. These folders contain vital resources, including methods, labware definitions, libraries, configuration files, and graphical elements necessary for operating Hamilton’s liquid handling robots like the STAR series. Understanding the file structure helps streamline the integration of new methods, labware, and customization of operations, ensuring efficient use of the automation platform.

Here’s a breakdown of key directories and their content, based on the command-line structure of the Venus software installation:

## Key Directories

#### 1. **Bin Directory**

* **Path:** `C:\Program Files (x86)\HAMILTON\Bin`
* **Contents:**
  * Subdirectories such as **BioNex HiG** and **Hamilton MPE2** store device-specific binaries for hardware integration.
  * Contains libraries and executables necessary for the main software operation.
  * The **ICL** versions (**ICLv6.0.0.218**, **ICLv6.3.0.297**) hold different versions of Hamilton’s Integrated Control Library, facilitating robotic arm and peripheral equipment communication.

#### 2. **Config Directory**

* **Path:** `C:\Program Files (x86)\HAMILTON\Config`
* **Contents:**
  * Configuration files essential for system-wide settings and operations of Venus software.
  * Stores preferences for system behavior and can be customized based on specific lab requirements.

#### 3. **Graphic Directory**

* **Path:** `C:\Program Files (x86)\HAMILTON\Graphic`
* **Contents:**
  * Subfolders like **Instrument** and **PipettingDevice** house graphical representations used by the software to display equipment and devices on the graphical user interface (GUI). These graphics are important for visual setup during method design.

#### 4. **Help Directory**

* **Path:** `C:\Program Files (x86)\HAMILTON\Help`
* **Contents:**
  * Documentation and help files to guide users on different aspects of the Venus software.

#### 5. **LabWare Directory**

* **Path:** `C:\Program Files (x86)\HAMILTON\LabWare`
* **Contents:**
  * Contains definitions of various labware such as plates, tubes, and consumables from different manufacturers (e.g., **Eppendorf**, **Falcon**, **Corning-Costar**).
  * Subdirectories like **ML\_STAR** house specific labware definitions for Hamilton STAR systems.
    * Example: **ML\_STAR/384CoReHead** contains labware definitions specific to the 384-channel Co-RE head.
  * The **Bitmaps** folder may store graphical assets for labware, which are displayed during method creation.

#### 6. **Language Directory**

* **Path:** `C:\Program Files (x86)\HAMILTON\Language`
* **Contents:**
  * Localization and language support files for the Venus software, allowing users to operate the software in multiple languages.

#### 7. **Library Directory**

* **Path:** `C:\Program Files (x86)\HAMILTON\Library`
* **Contents:**
  * This folder holds critical libraries for specific devices and functionalities:
    * **Agilent PlateLoc**: Contains files and scripts for integrating Agilent PlateLoc Sealer.
    * **ASWStandard**: Contains Hamilton’s standard automation libraries, with **TraceLevel** managing logging and error reporting.
    * **Firmware Libraries** and **Hamilton DriverTools**: Store necessary tools and drivers to interface with hardware and firmware.

#### 8. **Methods Directory**

* **Path:** `C:\Program Files (x86)\HAMILTON\Methods`
* **Contents:**
  * Core directory for storing automation methods and workflows. These methods define the steps a Hamilton robot performs during an experiment or process.
  * Subdirectories include:
    * **Library Demo Methods**: Contains example methods for training or demonstration purposes, such as dialogs for user input and status tracking.
    * **HSLLabwrAccess**: Facilitates access to specific labware during method execution.
    * **Device Tests**: Methods designed to test and validate hardware like pipetting heads and carriers.
  * Method scripts in this folder guide the robotic system through tasks such as liquid handling, dispensing, and device operation.

#### 9. **Packages and Files Directory**

* **Path:** `C:\Program Files (x86)\HAMILTON\Packages and Files`
* **Contents:**
  * Stores software packages and files that Venus uses for various operations, including custom files required for specific methods.

#### 10. **System Directory**

* **Path:** `C:\Program Files (x86)\HAMILTON\System`
* **Contents:**
  * Core system files for the Venus software. These files are essential for running the application and should not be modified.

#### 11. **MethodManager2 Directory**

* **Path:** `C:\Program Files (x86)\HAMILTON\MethodManager2_v1.0`
* **Contents:**
  * **Method Manager 2** allows users to manage, edit, and organize methods within the Venus environment.
  * Subfolders like **db** (database) and **html** provide backend functionality for managing method-related data.

#### 12. **SiLA Directory**

* **Path:** `C:\Program Files (x86)\HAMILTON\SiLA`
* **Contents:**
  * Contains drivers for SiLA-compliant devices, including the **Hamilton Driver for BioMed Microplate Reader**. SiLA (Standardization in Lab Automation) promotes device interoperability, enabling seamless integration of SiLA devices.

#### 13. **Uninstall Directory**

* **Path:** `C:\Program Files (x86)\HAMILTON\Uninstall`
* **Contents:**
  * Stores files required for removing the Venus software or specific components from the system.

## Eample File Tree Structure:&#x20;

Understanding the file structure of the Hamilton Venus software allows users to efficiently manage and expand the automation platform. Below is an example of the file system installed in Windows using the tree command:

```
C:\Program Files (x86)\HAMILTON>tree
Folder PATH listing for volume OS
Volume serial number is 4AC5-F73A
C:.
├───Bin
│   ├───1033
│   ├───BioNex HiG
│   ├───Hamilton MPE2
│   ├───ICLv6.0.0.218
│   ├───ICLv6.3.0.297
│   └───VectorCustomDialogs
├───Config
├───Graphic
│   ├───Instrument
│   └───PipettingDevice
├───Help
├───LabWare
│   ├───Abegene_MIDI
│   ├───Ansys
│   ├───Bitmaps
│   ├───Corning-Costar
│   ├───Dynex
│   ├───Eppendorf
│   ├───Falcon
│   ├───Greiner
│   ├───Hamilton
│   ├───IST
│   ├───Kayco_Dallas
│   ├───Labsystems
│   ├───Limbro
│   ├───Macherey-Nagel
│   ├───Matrix
│   ├───MJ_Research
│   ├───ML_STAR
│   │   ├───384CoReHead
│   │   ├───96COREHEAD
│   │   ├───AutoLys
│   │   ├───BVS
│   │   ├───CO-RE-GRIP
│   │   ├───CORE
│   │   │   └───PLT_CAR_L5_DWP_G
│   │   ├───Deck-adaptor-templates
│   │   ├───HamHeaterShaker
│   │   ├───MFXCreation
│   │   ├───MultiFlexCarrier
│   │   ├───Nano
│   │   ├───NGS STAR ODTC Carrier
│   │   │   ├───2021-04-23_Updated Biorad Plate Definition
│   │   │   └───Ham_1_NB_Lid_ODTC_V1.0
│   │   ├───Plate
│   │   ├───Puncher
│   │   ├───Quad Core Grips
│   │   │   └───Quad Core Grips
│   │   ├───Reagent
│   │   ├───Stack
│   │   ├───Tips
│   │   ├───VacuTube
│   │   │   └───XFiles
│   │   └───Washstation
│   ├───Nimbus
│   │   └───HighDensityDeck
│   ├───Nunc
│   ├───Perkin-Elmer
│   ├───Polyfiltronic
│   ├───Qiagen
│   ├───Rainin
│   └───UPMC
│       └───SMP_CAR_32_Blue_Adapters_Flip_Top_Tube
├───Language
├───Library
│   ├───Agilent PlateLoc
│   ├───Alpha Numeric Conversion
│   ├───ASWStandard
│   │   ├───ASWGlobal
│   │   └───TraceLevel
│   ├───ASWStandardDialogs
│   │   ├───ASWIconSet
│   │   │   ├───128x128
│   │   │   │   ├───hamilton
│   │   │   │   └───settings
│   │   │   ├───16x16
│   │   │   │   ├───hamilton
│   │   │   │   └───status-led
│   │   │   ├───22x22
│   │   │   │   ├───actions
│   │   │   │   ├───devices
│   │   │   │   ├───edit
│   │   │   │   ├───hamilton
│   │   │   │   ├───messageboxes
│   │   │   │   ├───misc
│   │   │   │   ├───runcontrol
│   │   │   │   ├───settings
│   │   │   │   ├───status-led
│   │   │   │   ├───system
│   │   │   │   ├───usermanagement
│   │   │   │   └───zoom
│   │   │   ├───32x32
│   │   │   │   ├───actions
│   │   │   │   ├───devices
│   │   │   │   ├───edit
│   │   │   │   ├───hamilton
│   │   │   │   ├───labware
│   │   │   │   ├───liquidhandling
│   │   │   │   ├───messageboxes
│   │   │   │   ├───misc
│   │   │   │   ├───runcontrol
│   │   │   │   ├───settings
│   │   │   │   ├───system
│   │   │   │   ├───usermanagement
│   │   │   │   └───zoom
│   │   │   ├───64x64
│   │   │   │   ├───actions
│   │   │   │   ├───devices
│   │   │   │   ├───edit
│   │   │   │   ├───hamilton
│   │   │   │   ├───messageboxes
│   │   │   │   ├───misc
│   │   │   │   ├───settings
│   │   │   │   ├───system
│   │   │   │   └───usermanagement
│   │   │   └───ICO
│   │   ├───de
│   │   ├───es
│   │   ├───it
│   │   └───Templates
│   │       ├───MvvmTemplate
│   │       │   └───lib
│   │       └───SimpleTemplate
│   │           └───lib
│   ├───BioNex HiG
│   │   └───Dependencies
│   ├───Edit File Attributes
│   ├───Firmware Libraries
│   ├───Hamilton DriverTools
│   ├───Hamilton MPE2
│   │   └───Dependencies
│   ├───Hamilton SerialInterface
│   ├───HSLExtensions
│   │   └───Framework
│   ├───HSLLabwrAccess
│   │   └───Resources
│   ├───Inheco ODTC
│   │   ├───DeviceScripts
│   │   │   └───Neu
│   │   └───Tool
│   ├───Labware Properties
│   │   └───Resources
│   ├───MPE
│   ├───SmartStepCustomizedErrorHandling
│   ├───SMT
│   ├───SMTs
│   ├───STAR Tools
│   │   └───Resources
│   │       └───SubMethods
│   ├───Templates
│   ├───Vantage Tools
│   │   └───Resources
│   │       ├───IDL Macro File
│   │       └───SubMethods
│   ├───VectorCustomDialogs
│   │   ├───ASWIconSet
│   │   │   ├───128x128
│   │   │   │   ├───hamilton
│   │   │   │   └───settings
│   │   │   ├───16x16
│   │   │   │   ├───hamilton
│   │   │   │   └───status-led
│   │   │   ├───22x22
│   │   │   │   ├───actions
│   │   │   │   ├───devices
│   │   │   │   ├───edit
│   │   │   │   ├───hamilton
│   │   │   │   ├───messageboxes
│   │   │   │   ├───misc
│   │   │   │   ├───runcontrol
│   │   │   │   ├───settings
│   │   │   │   ├───status-led
│   │   │   │   ├───system
│   │   │   │   ├───usermanagement
│   │   │   │   └───zoom
│   │   │   ├───32x32
│   │   │   │   ├───actions
│   │   │   │   ├───devices
│   │   │   │   ├───edit
│   │   │   │   ├───hamilton
│   │   │   │   ├───labware
│   │   │   │   ├───liquidhandling
│   │   │   │   ├───messageboxes
│   │   │   │   ├───misc
│   │   │   │   ├───runcontrol
│   │   │   │   ├───settings
│   │   │   │   ├───system
│   │   │   │   ├───usermanagement
│   │   │   │   └───zoom
│   │   │   ├───64x64
│   │   │   │   ├───actions
│   │   │   │   ├───devices
│   │   │   │   ├───edit
│   │   │   │   ├───hamilton
│   │   │   │   ├───messageboxes
│   │   │   │   ├───misc
│   │   │   │   ├───settings
│   │   │   │   ├───system
│   │   │   │   ├───usermanagement
│   │   │   │   └───zoom
│   │   │   └───ICO
│   │   ├───ColorGuides
│   │   ├───de
│   │   ├───es
│   │   ├───ExampleThemes
│   │   │   ├───ExampleTheme_Blue_Inverted
│   │   │   ├───ExampleTheme_Gray_Green
│   │   │   ├───ExampleTheme_Orange
│   │   │   └───HamiltonTheme
│   │   ├───fr
│   │   ├───hu
│   │   ├───it
│   │   ├───pt-BR
│   │   ├───ro
│   │   ├───ru
│   │   ├───sv
│   │   └───zh-Hans
│   └───VoV_Lights
├───LogFiles
│   └───Inheco ODTC
├───MethodManager2_v1.0
│   └───Method Manager 2
│       ├───db
│       ├───html
│       │   ├───css
│       │   ├───img
│       │   ├───js
│       │   │   └───custom
│       │   └───webfonts
│       ├───locales
│       ├───node_modules
│       │   ├───.bin
│       │   ├───ansi-styles
│       │   ├───chalk
│       │   ├───diskdb
│       │   │   └───lib
│       │   ├───edge-cs
│       │   │   ├───lib
│       │   │   │   └───bootstrap
│       │   │   ├───src
│       │   │   │   ├───edge-cs
│       │   │   │   │   └───Properties
│       │   │   │   └───Edge.js.CSharp
│       │   │   └───tools
│       │   ├───edge-js
│       │   │   ├───build
│       │   │   │   └───Release
│       │   │   │       └───obj
│       │   │   │           ├───build_managed
│       │   │   │           │   └───build_managed.tlog
│       │   │   │           ├───edge_coreclr
│       │   │   │           │   └───edge_coreclr.tlog
│       │   │   │           └───edge_nativeclr
│       │   │   │               └───edge_nativeclr.tlog
│       │   │   ├───lib
│       │   │   │   ├───bootstrap
│       │   │   │   │   ├───bin
│       │   │   │   │   │   └───Release
│       │   │   │   │   │       └───netcoreapp1.1
│       │   │   │   │   └───obj
│       │   │   │   │       └───Release
│       │   │   │   │           └───netcoreapp1.1
│       │   │   │   └───native
│       │   │   │       └───win32
│       │   │   │           ├───ia32
│       │   │   │           │   ├───10.14.0
│       │   │   │           │   ├───12.13.0
│       │   │   │           │   ├───14.3.0
│       │   │   │           │   └───15.5.0
│       │   │   │           └───x64
│       │   │   │               ├───10.14.0
│       │   │   │               ├───12.13.0
│       │   │   │               ├───14.3.0
│       │   │   │               └───15.5.0
│       │   │   ├───performance
│       │   │   │   └───BookService
│       │   │   │       └───Properties
│       │   │   ├───samples
│       │   │   ├───src
│       │   │   │   ├───common
│       │   │   │   ├───CoreCLREmbedding
│       │   │   │   │   ├───cpprest
│       │   │   │   │   │   └───include
│       │   │   │   │   ├───deps
│       │   │   │   │   ├───fxr
│       │   │   │   │   ├───host
│       │   │   │   │   ├───json
│       │   │   │   │   │   └───casablanca
│       │   │   │   │   │       ├───include
│       │   │   │   │   │       │   └───cpprest
│       │   │   │   │   │       │       └───details
│       │   │   │   │   │       └───src
│       │   │   │   │   │           ├───json
│       │   │   │   │   │           └───utilities
│       │   │   │   │   └───pal
│       │   │   │   ├───dotnet
│       │   │   │   ├───double
│       │   │   │   │   ├───Edge.js
│       │   │   │   │   │   ├───bin
│       │   │   │   │   │   │   └───Release
│       │   │   │   │   │   │       └───netcoreapp1.1
│       │   │   │   │   │   ├───dotnet
│       │   │   │   │   │   ├───dotnetcore
│       │   │   │   │   │   └───obj
│       │   │   │   │   │       └───Release
│       │   │   │   │   │           └───netcoreapp1.1
│       │   │   │   │   └───Edge.js.CSharp
│       │   │   │   │       ├───bin
│       │   │   │   │       │   └───Release
│       │   │   │   │       │       └───netcoreapp1.1
│       │   │   │   │       └───obj
│       │   │   │   │           └───Release
│       │   │   │   │               └───netcoreapp1.1
│       │   │   │   └───mono
│       │   │   ├───stress
│       │   │   ├───test
│       │   │   │   └───double
│       │   │   │       ├───double_stress
│       │   │   │       │   └───Properties
│       │   │   │       └───double_test
│       │   │   │           └───Properties
│       │   │   └───tools
│       │   │       └───nuget
│       │   │           └───tools
│       │   ├───has-color
│       │   ├───image-size
│       │   │   ├───bin
│       │   │   └───dist
│       │   │       └───types
│       │   ├───inherits
│       │   ├───merge
│       │   ├───nan
│       │   │   ├───doc
│       │   │   └───tools
│       │   ├───node-uuid
│       │   │   ├───benchmark
│       │   │   ├───bin
│       │   │   ├───lib
│       │   │   └───test
│       │   ├───queue
│       │   └───strip-ansi
│       └───swiftshader
├───Methods
│   ├───Device Tests
│   ├───HSLLabwrAccess
│   ├───Library Demo Methods
│   │   ├───ASWStandardDialogs
│   │   │   ├───CheckBoxDialog
│   │   │   ├───DemoPictures
│   │   │   ├───DirectoryBrowserDialog
│   │   │   ├───DoubleInputDialog
│   │   │   ├───ErrorDialog
│   │   │   ├───ImageRadioButtonDialog
│   │   │   ├───InputDialog
│   │   │   ├───ListDialog
│   │   │   ├───ListSelectDialog
│   │   │   ├───LoadingDialog
│   │   │   ├───LoginDialog
│   │   │   ├───MessageDialog
│   │   │   ├───MessageDialogWithImage
│   │   │   ├───RadioButtonDialog
│   │   │   └───WorklistDialog
│   │   ├───AswStatusDialog
│   │   ├───HSLLabwrAccess
│   │   │   └───Labware
│   │   │       ├───Carrier
│   │   │       ├───Nunc 384 Well
│   │   │       ├───Nunc 96 Wells
│   │   │       ├───Nun_12_FB_MTP
│   │   │       ├───Nun_24_Fl_L
│   │   │       └───Nun_6_FB_MTP_15000
│   │   └───VectorCustomDialogs
│   │       ├───CheckBoxDialog
│   │       ├───DemoPictures
│   │       ├───DirectoryBrowserDialog
│   │       ├───DoubleInputDialog
│   │       ├───ErrorDialog
│   │       ├───FileBrowseDialog
│   │       ├───ImageRadioButtonDialog
│   │       ├───InitializeVectorCustomDialogs
│   │       ├───InitializeVectorCustomDialogsWithCustomTheme
│   │       ├───InitializeVectorCustomDialogsWithIconSet
│   │       ├───InitializeVectorCustomDialogsWithIconSetAndTheme
│   │       ├───InputDialog
│   │       ├───ListDialog
│   │       ├───ListSelectDialog
│   │       ├───LoadingDialog
│   │       ├───LoginDialog
│   │       ├───MessageDialog
│   │       ├───MessageDialogWithImage
│   │       ├───RadioButtonDialog
│   │       ├───Sound
│   │       ├───StatusDialog
│   │       ├───UpdateCustomTheme
│   │       └───UpdateCustomThemeFromDefaultLocation
│   ├───VM
│   └───[MPE]2
│       └───Resources
│           ├───Configuration
│           ├───Images
│           ├───Labware
│           │   ├───Collection
│           │   └───Filter
│           ├───Library
│           ├───Manuals
│           └───Process
│               ├───Complete
│               ├───Evaporate
│               ├───Filter
│               └───Reagent
├───Packages and Files
│   ├───Archive
│   └───Positions
├───SiLA
│   └───Hamilton Driver for BioMed Microplate Reader
├───System
├───Uninstall
│   └───HSLLabwrAccess
└───XRPService
    ├───Inf
    │   ├───CP210x_W10
    │   │   ├───arm
    │   │   ├───arm64
    │   │   ├───x64
    │   │   └───x86
    │   ├───CP210x_W7
    │   │   ├───x64
    │   │   └───x86
    │   └───CP210x_WXP
    │       ├───x64
    │       └───x86
    └───Language
```
