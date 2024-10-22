# \[MPE]² Programming

‌The HSL and SILA libraries included in their respective installers consist of commands for each module, as well as general commands like Initialize.&#x20;

## Method Structure

This section describes the general order of the commands in a method using the \[MPE]2 Logistics Module. The example will not describe the commands themselves in depth; refer to sections 6.1 through[ ](file:///Users/zdmilot/Desktop/Pages%20from%20\[MPE]2%20Users%20Manual%20Rev%20E.html#bookmark2)6.5 for descriptions of each command. The outline in this section does not translate into a fully functional method, and is only intended to show the order of the commands.

1. ConnectUsingCOM or ConnectUsingIP
2. IsConnected (optional)
3. Initialize
4. IsInitialized (optional)
5. FilterPlatePlaced
6. ClampFilterPlate
7. CollectionPlatePlaced (if using a collection plate)
8. ProcessFiltertoWasteContainer or ProcessFiltertoCollectionPlate (if using a collection plate)
9. CollectionPlateRemoved
10. RetrieveFilterPlate (if not done during ProcessFilter step)
11. FilterPlateRemoved
12. Disconnect

The two libraries use the same commands with the same input parameters. The function of and required inputs for each command are described in the following sections.

## ‌General Commands

### ConnectUsingCOM

The ConnectUsingCOM command connects to the \[MPE]2 using a USB cable. This command requires input values for five parameters:

* comPort: Enter the port on the controlling computer to which the \[MPE]2 is connected. To find the COM port, open the File Explorer, right-click This PC, and select Manage. In the Computer Management window, select Device Manager. The COM port connections are listed under “Ports (COM & LPT)”.

<figure><img src="../../../.gitbook/assets/image (25) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

Figure 6–1: Obtaining COM port values

* baudRate: Enter the baud rate used to connect to the \[MPE]2. The rate is 921600 Bd by default.
* simulationMode: Indicate whether the device is being run in simulation mode. Enter “1” for simulated and “0” for not simulated.
* deviceId: Select an integer variable to store the device ID. This value will be used to determine which device will receive \[MPE]2 commands. The variable must be declared earlier in the method to be selected.
* mpeOptions: Indicate any additional modules used with the Logistics Module. Each combination of modules is associated with an integer:
* 0: No additional modules
* 1: Reagent Fill Module
* 2: Evaporator Module
* 3: Reagent Fill and Evaporator Modules
* 4: Accessory controller only

### ConnectUsingIP

The ConnectUsingIP command connects to the \[MPE]2 using an Ethernet cable. This command requires inputs for five parameters:

* instrumentName: Enter the address for the \[MPE]2 connection or the name of the device. The address is “192.168.100” by default.
* portNumber: Identify the port used to connect to the \[MPE]2. The port number is set to “2000” by default.
* simulationMode: Indicate whether the device is being run in simulation mode. Enter “1” for simulated or “0” for not simulated.
* deviceId: Select an integer variable to store the device ID. This value will be used to determine which device will receive \[MPE]2 commands. The variable must be declared earlier in the method to be selected.
* mpeOptions: Indicate any additional modules used with the Logistics Module. Each combination of modules is associated with an integer:
* 0: No additional modules
* 1: Reagent Fill Module
* 2: Evaporator Module
* 3: Reagent Fill and Evaporator Modules
* 4: Accessory controller only

### Disconnect

This command is used to disconnect from an \[MPE]2 that was previously connected using one of the Connect commands. If the method will be run again without closing Run

Control, this command must be executed. Its only parameter is “deviceID”, which specifies which device will receive the command.&#x20;

### DisconnectAll

This command disconnects all connected \[MPE]2 devices. It is only available on the SiLA driver for the \[MPE]2, and it has no input parameters.

### GetLastError

GetLastError returns an error message corresponding to the last \[MPE]2 error. This command can be used to manually program error handling by adding recovery commands for different error codes. A guide to the error codes can be found in the help file for the library. The command requires input values for three parameters:

* deviceId: Specify which device will receive the command.
* clearError: Indicate whether the error will be cleared after returning the error message. Enter “1” to clear the error or “0” to leave the error.
* errorMessage: Select a string variable to store the error message. The variable must be declared earlier in the method to be selected.

### Initialize

This command is used to initialize the \[MPE]2 after it has been connected. Initialize must be placed before labware is placed or processed – no labware can be loaded on the \[MPE]2 before it has initialized. The command’s only parameter is “deviceID”, which specifies which device will receive the command.

### InitializeWithParameters

This command performs a smart initialization of the \[MPE]2. A smart initialization only initializes the components required for the method, allowing for a shorter initialization. This command requires the following parameters:

* deviceId: Specify which device will receive the command.
* smart: Indicate whether only the necessary components will be initialized. A value of “1” will enable smart initialization, while “0” will disable it.
* wasteContainerId: Specify the waste bottle port that the Logistics Module is connected to. Enter “0” for the first port, “1” for the second port, and “-1” for no connection.
* vacuumRunTime: Enter the minimum amount of time in seconds to turn on the vacuum pump upon initialization.
* disableVacuumCheck: Enable or disable a check for high vacuum pressure. Disabling the check can make evacuating more viscous fluids easier, while enabling the check can help detect clogs in the system. Enter “1” to disable the vacuum check or “0” to enable it.&#x20;

### IsConnected

The IsConnected command is used to determine whether the \[MPE]2 has been successfully connected following a Connect command. The command requires inputs for two parameters:

* deviceId: Specify which device will receive the command.
* isConnected: Select an integer variable to store the connection status. A value of “1” indicates that the \[MPE]2 is connected, while “0” indicates that the device is not connected. The variable must be declared earlier in the method to be selected.

### IsInitialized

The IsInitialized command is used to determine whether the \[MPE]2 has been successfully initialized following an Initialize command. The command requires inputs for two parameters:

* deviceId: Specify which device will receive the command.
* isConnected: Select an integer variable to store the initialization status. A value of “1” indicates that the \[MPE]2 has been initialized, while “0” indicates that the device has not been initialized. The variable must be declared earlier in the method to be selected.

## Logistics Module Commands

### ClampFilterPlate

This command clamps a filter plate against the \[MPE]2 manifold. In a method, ClampFilterPlate follows a FilterPlatePlaced command, and comes before a ProcessFilter command. Its only parameter is “deviceID”, which specifies which device will receive the command. 2. CollectionPlatePlaced

The CollectionPlatePlaced command tells the \[MPE] that a collection plate has been placed and specifies its dimensions. The command requires input values for three parameters:

* deviceId: Specify which device will receive the command.
* collectionPlateHeight: Enter the height of the collection plate in millimeters.
* offsetFromNozzles: Enter the distance in millimeters between the bottom of the filter plate nozzles and the top of the collection plate. The distance can be positive or negative – a positive distance indicates a gap between the nozzles and the collection

plate, whereas a negative distance indicates that the nozzles protrude into the collection plate.&#x20;

### CollectionPlateRemoved

This command indicates the removal of a collection plate from the \[MPE]2. Its only parameter is “deviceID”, which specifies which device will receive the command. The command requires no direct action from the \[MPE]2.

### FilterPlatePlaced

The FilterPlatePlaced command indicates to the \[MPE]2 that a filter plate has been placed on the filter plate adapter. This command requires input values for three parameters:

* deviceId: Specify which device will receive the command.
* filterHeight: Enter the height of the filter skirt in millimeters.
* nozzleHeight: Enter the full height of the filter plate in millimeters, measured from the top of the plate to the bottom of the nozzles.

### FilterPlateRemoved

This command indicates the removal of a filter plate from the \[MPE]2. Its only parameter is “deviceID”, which specifies which device will receive the command. FilterPlateRemoved must follow a RetrieveFilterPlate command, which unclamps the plate from the manifold. The command requires no direct action from the \[MPE]2. 6. GetVacuumStatus

This command is used to determine whether the vacuum is active. It requires inputs for two parameters:

* deviceId: Specify which device will receive the command.
* rVacuumActive: Select an integer variable to store the vacuum status. A value of “1” indicates that the vacuum is active, whereas “0” indicates that the vacuum is inactive. The variable must be declared earlier in the method to be selected.

### ProcessFiltertoCollectionPlate

This command is one of two processing commands for the Logistics Module. Once filter and collection plates have been placed and clamped, ProcessFiltertoCollectionPlate moves the plates into position and applies pressure. The command requires inputs for three parameters:

* deviceId: Specify which device will receive the command.
* controlPoints: Enter the parameters for processing in the form “Type,Value,Duration”.

“Type” has three possible values: Flow, Pressure, and Idle. Enter “Flow” for the Type to define a mass flow rate of gas through the filter plate. Enter “Pressure” to specify a pressure to be applied to the entire plate. Enter “Idle” to apply no pressure and wait for the specified duration.

“Value” is an integer whose value is different depending on the Type. For Flow, the Value is the mass flow rate in L/min; for Pressure, the Value is the pressure applied to the plate in psi, with an acceptable range of 0-120 psi. The Value is arbitrary for Idle, since no action is being performed, but the input must be an integer to avoid causing an error.

“Duration” is the time in seconds that the \[MPE]2 will process the plate.

* returnPlateToIntegrationArea: Indicate whether the filter plate is returned along with the collection plate to the presentation site after processing is finished. Enter “1” to return the filter plate or “0” to keep the plate clamped to the manifold.

Multiple processes can be performed in one ProcessFiltertoCollectionPlate step by connecting multiple “controlPoints” inputs with semicolons. For example, the input “pressure,15,20;idle,30,45;pressure,60,20” would make the \[MPE]2 apply 15 psi of pressure to the plate for 20 seconds, wait for 45 seconds, then apply 60 psi of pressure for 20 seconds.

Note that the Value field for the “idle” input does not affect the command.&#x20;

### ProcessFiltertoWasteContainer

This command is one of two processing commands for the Logistics Module. Once a filter plate has been placed and clamped, ProcessFiltertoWasteContainer applies pressure to the plate. The command requires inputs for five parameters:

* deviceId: Specify which device will receive the command.
* controlPoints: Enter the parameters for processing in the form “Type,Value,Duration”.

“Type” has three possible values: Flow, Pressure, and Idle. Enter “Flow” for the Type to define a mass flow rate of gas through the filter plate. Enter “Pressure” to specify a pressure to be applied to the entire plate. Enter “Idle” to apply no pressure and wait for the specified duration.

“Value” is an integer whose value is different depending on the Type. For Flow, the Value is the mass flow rate in L/min; for Pressure, the Value is the pressure applied to the plate in psi, with an acceptable range of 0-120 psi. The Value is arbitrary for Idle, since no action is being performed, but the input must be an integer to avoid causing an error.

“Duration” is the time in seconds that the \[MPE]2 will process the plate.

* returnPlateToIntegrationArea: Indicate whether the filter plate is returned to the presentation site after processing is finished. Enter “1” to return the filter plate or “0” to keep the plate clamped to the manifold.
* wasteContainerId: Specify the waste bottle port that the Logistics Module is connected to. Enter “0” for the first port, “1” for the second port, and “-1” for no connection.
* checkForExcessiveVacuum: Enable or disable a check for high vacuum pressure. Disabling the check can make evacuating more viscous fluids easier, while enabling the check can help detect clogs in the system. Enter “1” to enable the vacuum check or “0” to disable it.

### RetrieveFilterPlate

The RetrieveFilterPlate command is used to release the clamp on a processed filter plate and return it to the presentation site. This command is not necessary if the “returnPlatetoIntegrationArea” parameter is enabled in a ProcessFilter command. The only parameter is “deviceID”, which specifies which device will receive the command.

### StartMPEVacuum

This command is used to start the vacuum waste pump without the using the ProcessFiltertoWasteContainer command for an unspecified length of time. This command is used for flushing the waste tubing. It requires inputs for three parameters:

* deviceId: Specify which device will receive the command.
* wasteContainerId: Specify the waste bottle port that the Logistics Module is connected to. Enter “0” for the first port, “1” for the second port, and “-1” for no connection.
* disableVacuumCheck: Enable or disable a check for high vacuum pressure. Disabling the check can make evacuating more viscous fluids easier, while enabling the check can help detect clogs in the system. Enter “1” to disable the vacuum check or “0” to enable it.

### StartVacuum

This command was used to start the vacuum waste pump without the using the ProcessFiltertoWasteContainer command for a specified length of time. In new methods, the StartMPEVacuum command should be used instead. This command requires inputs for four parameters:

* deviceId: Specify which device will receive the command.
* wasteContainerId: Specify the waste bottle port that the Logistics Module is connected to. Enter “0” for the first port, “1” for the second port, and “-1” for no connection.
* seconds: Enter the duration of time in seconds to run the vacuum pump.
* disableVacuumCheck: Enable or disable a check for high vacuum pressure. Disabling the check can make evacuating more viscous fluids easier, while enabling the check can help detect clogs in the system. Enter “1” to disable the vacuum check or “0” to enable it.

### StopVacuum

The StopVacuum command is used to stop and the vacuum waste pump. Note that this command will return an error if the vacuum has not been acquired or maintained since the last StartVacuum command. The only parameter is “deviceID”, which specifies which device will receive the command.

## Reagent Fill Module Commands

### Dispense

The Dispense command is the main processing commands for the Reagent Fill Module. Once the desired plate is in position, this command dispenses the specified liquid to all wells on the plate. It requires inputs for the following parameters:

* deviceId: Specify which device will receive the command.
* sourceId: Specify which reagent to dispense to the plate (1-17).
* wellVolume: Enter the volume of reagent per well in µL to dispense.
* flowRate: Specify how quickly to dispense to the plate in µL/s.
* needleOffset: Enter the desired distance between the top of the wells and the needles in millimeters. Negative values will lower the needles into the wells before dispensing.

### DispenseNonStandard

This command is used to dispense to plates that have well spacing other than 9 mm. It can also be used to only dispense to specific columns on a plate. It requires inputs for the same parameters as the Dispense command, with two additional inputs:

* deviceId: Specify which device will receive the command.
* sourceId: Specify which reagent to dispense to the plate (1-17).
* wellVolume: Enter the volume of reagent per well in µL to dispense.
* flowRate: Specify how quickly to dispense to the plate in µL/s.
* needleOffset: Enter the desired distance between the top of the wells and the needles in millimeters. Negative values will lower the needles into the wells before dispensing.
* edgeToWellOffset: Enter the distance between the edge of the plate and the center of the first well to dispense to in millimeters.
* wellToWellOffsets: Enter an array of distances between rows of wells (measured from center to center) in millimeters.

For example, an edgeToWellOffset value of 13.5 and a wellToWellOffsets array of {9.0, 18.0, 9.0} for a standard microplate would dispense to the first, second, fourth, and fifth columns on a plate.

### Flush

The Flush command pumps deionized water through the manifold to a waste container. The tubes must be flushed before and after a run, and every time the pump switched reagents. The command requires inputs for the following parameters:

* deviceId: Specify which device will receive the command.
* wellVolume: Enter the volume of water per well in µL to dispense.
* flowRate: Specify how quickly to flush the tubes in µL/s.
* wasteContainerId: Specify the waste bottle port that the Logistics Module is connected to. Enter “0” for the first port, “1” for the second port, and “-1” for no connection.

### Prime

This command primes the Reagent Fill Module pump for the specified source bottle to be dispensed. The pump must be primed before using either of the Dispense commands. This command requires inputs for the following parameters:

* deviceId: Specify which device will receive the command.
* sourceId: Specify which reagent to prime for dispensing (1-17).
* wellVolume: Enter the volume of reagent per well in µL to be dispensed.
* flowRate: Specify how quickly to dispense to the plate in µL/s.
* wasteContainerId: Specify the waste bottle port that the Logistics Module is connected to. Enter “0” for the first port, “1” for the second port, and “-1” for no connection.

## Calibration Commands

These commands are used to calibrate the source bottles for the Reagent Fill Module. They must be calibrated upon installation and after any change to the bottle connections. Note that the \[MPE]2Toolkit software on the installation media may also be used to calibrate the source bottles.

### StartContainerCalibration

This command begins the calibration process for the specified source bottle. It requires inputs for three parameters:

* deviceId: Specify which device will receive the command.
* sourceId: Specify the source bottle to be calibrated. The bottles are numbered 1-17. The value must correspond to the source bottle configuration set by the SetSourceConfiguration command.
* volume: Enter the expected liquid capacity in milliliters.

### MeasureEmptyContainer

The MeasureEmptyContainer command calibrates the liquid sensor for the specified source bottle when empty. It requires inputs for three parameters:

* deviceId: Specify which device will receive the command.
* sourceId: Specify the source bottle to be calibrated. The bottles are numbered 1-17.
* emptyReading: Select an integer variable to store the minimum allowable volume in milliliters. The variable must be declared earlier in the method to be selected.

### MeasureFullContainer

The MeasureFullContainer command calibrates the liquid sensor for the specified source bottle when full. It requires inputs for three parameters:

* deviceId: Specify which device will receive the command.
* sourceId: Specify the source bottle to be calibrated. The bottles are numbered 1-17.
* fullReading: Select an integer variable to store the maximum allowable volume in milliliters. The variable must be declared earlier in the method to be selected.

### SaveContainerCalibration

This command saves the calibration data for the specified source bottle. Both the MeasureEmptyContainer and MeasureFullContainer commands must be performed before saving the calibration data. This command requires the following input parameters:

* deviceId: Specify which device will receive the command.
* sourceId: Specify which source bottle’s calibration data will be saved. The bottles are numbered 1-17.

### CancelContainerCalibration

This command cancels the calibration in progress for the specified source bottle. If a calibration is cancelled, the previous calibration values are restored. This command requires the following input parameters:

* deviceId: Specify which device will receive the command.
* sourceId: Specify which source bottle’s calibration will be cancelled. The bottles are numbered 1-17.

### GetContainerCalibration

GetContainerCalibration returns the saved calibration data for the specified source bottle. It requires inputs for the following parameters:

* deviceId: Specify which device will receive the command.
* sourceId: Specify which source bottle’s calibration data will be returned. The bottles are numbered 1-17.
* volume: Select an integer variable to store the bottle’s liquid capacity in milliliters. The variable must be declared earlier in the method to be selected.
* emptyReading: Select an integer variable to store the empty bottle reading. The variable must be declared earlier in the method to be selected.
* fullReading: Select an integer variable to store the full bottle reading. The variable must be declared earlier in the method to be selected.
* calibrationDate: Select a variable to store the date that the specified bottle was last calibrated.

### ClearSourceConfiguration

This command clears calibration data for all source bottles. This command is useful if the bottles need to be connected to different nozzles. Note that the \[MPE]2 must be power cycled after this command is called. This command requires inputs for the following parameters:

* deviceId: Specify which device will receive the command.
* reset: Set to “1” to reset all errors and configuration data immediately.

### GetSourceConfiguration

The GetSourceConfiguration command generates an XML file containing the available calibration data for all source bottles. The file is saved to the Hamilton\Bin\MPE2 folder under Program Files can later be used with the SetSourceConfiguration command. This command’s only parameter is “deviceID”, which specifies which device will receive the command.

### SetSourceConfiguration

This command reads an XML file created by the GetSourceConfiguration command and uses it to calibrate the source bottles. The file must be in the Hamilton\BinMPE2 folder to be read. The only parameter for this command is “deviceID”, which specifies which device will receive the command.

## ‌Evaporator Module Commands

### EvaporatePrepare

This command primes the Evaporator Module for an Evaporate command. An Initialize command is still required before this command is called. This command requires inputs for the following parameters:

* deviceId: Specify which device will receive the command.
* temperature: Enter the desired evaporation temperature in °C.
* pressure: Enter the desired gauge pressure in psi.
* timeout: Enter the amount of time in minutes to allow this command to run. A value of 0 defaults to a five-minute timeout.

### Evaporate

The Evaporate command moves a collection plate to the Evaporator for the specified amount of time after the target temperature and pressure have been reached. The EvaporatePrepare command must be called first to set a temperature and pressure for the evaporation, and a collection plate must be placed on the \[MPE]2 (indicated by a CollectionPlatePlaced command). This command requires inputs for the following parameters:

* deviceId: Specify which device will receive the command.
* plateHeight: Enter the height of the plate in millimeters. This parameter is equivalent to the filterHeight parameter in the FilterPlatePlaced command.
* needleOffset: Enter the distance in millimeters between the needle tips and the top of the plate.
* wellDepth: Enter the depth in millimeters of the plate being evaporated.
* evaporateTime: Enter the duration of the Evaporate step in seconds.

### EvaporateWithRate

This command functions like the Evaporate command, but it moves the plate closer to the Evaporator manifold needles at a specified rate. This feature allows for a consistent

distance between the liquid level in the wells and the needles during evaporation. The command requires inputs for the following parameters:

* deviceId: Specify which device will receive the command.
* plateHeight: Enter the height of the plate in millimeters. This parameter is equivalent to the filterHeight parameter in the FilterPlatePlaced command.
* needleOffset: Enter the initial distance in millimeters between the needle tips and the top of the plate.
* evaporatorTravelDistance: Enter the depth in millimeters of the plate being evaporated.

<table data-header-hidden><thead><tr><th width="145"></th><th></th></tr></thead><tbody><tr><td><img src="../../../.gitbook/assets/image (144) (1).png" alt="" data-size="original"></td><td><p>WARNING</p><p>Subtract the depth of any remaining liquid in the wells from the well depth to avoid contaminating the Evaporator’s needles.l.</p></td></tr></tbody></table>

* evaporateTime: Enter the duration of the Evaporate step in seconds.
* followRate: Enter the rate in mm/s to reduce the distance between the needle tips and the plate. This value must be less than the evaporatorTravelDistance divided by the evaporateTime.

### EvaporateEnd

This command turns off the heater and waits until the Evaporator Module reaches 43°C. Any filter and collection plates must be removed after an Evaporate or EvaporateWithRate command and before this command. EvaporateEnd requires the following input parameters:

* deviceId: Specify which device will receive the command.
* timeout: Enter the amount of time in minutes to allow this command to run. A value of 0 defaults to a twenty-minute timeout.

### GetCurrentHeaterStatus

The GetCurrentHeaterStatus command returns data on the current state of the Evaporator Module. It requires inputs for the following parameters:

* deviceId: Specify which device will receive the command.
* reset: Set to 1 to reset any errors or data that have been generated during the run.
* currentEvaporatorTemperature: Select an integer variable to store the temperature of the Evaporator Module heater in °C. The variable must be declared earlier in the method to be selected.
* currentGasTemperature: Select an integer variable to store the temperature of the air exiting the Evaporator Module in °C. The variable must be declared earlier in the method to be selected.
* heating: Select an integer variable to store the heater status. A value of “1” indicates that the heater is on, while “0” indicates that it is off. The variable must be declared earlier in the method to be selected.

### GetHeaterTemperatureRange

This command returns data about the Evaporator Module’s operation from the current run. It requires inputs for the following parameters:

* deviceId: Specify which device will receive the command.
* reset: Set to 1 to reset any errors or data that have been generated during the run.
* minimumEvaporatorTemperature: Select an integer variable to store the lowest temperature of the Evaporator Module in °C recorded since the last reading. The variable must be declared earlier in the method to be selected.
* maximumEvaporatorTemperature: Select an integer variable to store the highest temperature of the Evaporator Module in °C recorded since the last reading. The variable must be declared earlier in the method to be selected.
* minimumGasTemperature: Select an integer variable to store the lowest air temperature in °C from the Evaporator Module since the last reading. The variable must be declared earlier in the method to be selected.
* maximumGasTemperature: Select an integer variable to store the highest air temperature in °C from the Evaporator Module since the last reading. The variable must be declared earlier in the method to be selected.
* targetTemperature: Select an integer variable to store the temperature set in the EvaporatePrepare command. The variable must be declared earlier in the method to be selected.
* heating: Select an integer variable to store the heater status. A value of “1” indicates that the heater is on, while “0” indicates that it is off. The variable must be declared earlier in the method to be selected.

### GetTemperatureRange

The GetTemperatureRange command returns a quick summary of data on the Evaporator Module’s operation from the current run. It requires inputs for the following parameters:

* deviceId: Specify which device will receive the command.
* minimumEvaporatorTemperature: Select an integer variable to store the lowest temperature setting in °C recorded since the last reading. The variable must be declared earlier in the method to be selected.
* maximumEvaporatorTemperature: Select an integer variable to store the highest temperature setting in °C recorded since the last reading. The variable must be declared earlier in the method to be selected.



## Processing Recommendations

This section offers recommendations to optimize the performance of the \[MPE]2. Methods will vary according to the specific application, but the following recommendations can function as a starting point when programming a new method.

### Sorbent Conditioning

Many filter beds are prepared with conditioning solutions prior to sample capture. This step varies by protocol, depending largely on the type of sorbent material. A typical conditioning step applies pressure for approximately 30 seconds over a range of 5 to 30 psi.

Example controlPoints for a ProcessFilter command:

“pressure,5,5;pressure,15,5;pressure,25,5;pressure,30,10” 2. Sorbent Drying

Applying high pressure is useful for removing all moisture from a sorbent bed before elution. Some sorbent materials are more sensitive, and can be damaged if subjected to pressures above 60 psi. A drying step can take as long as 20 minutes, depending on the relative humidity of the laboratory.

### Sample Capture and Matrix Cleanup

Low pressures over indeterminate periods of time are useful both for binding target analytes and removing interfering compounds. This step is especially dependent on liquid properties; a poor choice of flow rate or pressure can compromise results. Flow rates that are too fast will prevent complete binding between the sorbent and the target compounds.

Example controlPoints for a ProcessFilter command: “pressure,15,7;pressure,20,5”

### Sample Elution

Generally, starting with a low pressure and gradually applying more pressure is the best practice for passing a solvent through. The volume of solvent used is dependent on the strength of the interaction between the target compounds and the sorbent.

Any residual liquid on the bottom of the filter plate nozzles can be a source for cross- contamination. To remove these droplets, a short burst of high pressure (such as 75 psi for 2 seconds) is recommended at the end of the “controlPoints” input.

### High Volume

Too much pressure applied at the beginning of the processing step may cause splashing onto the filter plate gasket. Wells filled with 75% or more can spill over, which can lead to cross-contamination. Starting with a low pressure and gradually applying more pressure will ensure safer sample processing.

Example controlPoints for a ProcessFilter command:

“pressure,5,5;pressure,10,5;pressure,20,5;pressure,30,5”&#x20;

### Viscous Liquids

Processing viscous liquids requires longer processing times, low initial pressures, and high final pressures. Final pressure values at the end of a processing pressure ramp may be

as high as 70 or 80 psi, and the processing time for each section of a step may be as long as 10-15 seconds. These values will vary with the specific liquids and sorbents used.

Example controlPoints for a ProcessFilter command:

“pressure,10,10;pressure,25,10;pressure,55,10”&#x20;

### Volatile Liquids

Lower pressures and shorter processing times are sufficient for volatile liquids. Pressures under 10 psi are often adequate for liquids like ethanol and acetone to pass through a filter bed.

Example controlPoints for a ProcessFilter command:

“pressure,3,5;pressure,7,5;pressure,9,5”
