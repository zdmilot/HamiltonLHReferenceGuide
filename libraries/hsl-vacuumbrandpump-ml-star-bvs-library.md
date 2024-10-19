# HSL VacuumBrandPump / ML STAR BVS Library

The ML STAR BVS Library allows controlling up to four BVS / CVS units simultaneously. There are two categories of functions provided:

High Level Functions

The high level functions control the whole vacuum process including tracking of the vacuum action to the Hamilton Database.

The use of HighLevelFunctions is recommended. High level functions have the prefix HSLStarBVSLib.\


<table data-header-hidden><thead><tr><th width="125"></th><th></th></tr></thead><tbody><tr><td><img src="../.gitbook/assets/image (10) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" data-size="original"></td><td><p>NOTE</p><p><em>Different tip sizes, liquid classes and shoot numbers may require different sThe BVS Library can also be used for CVS.</em></p></td></tr></tbody></table>



## Low Level Functions

These functions reflect the command set of the “BVS pump controller” directly. These commands are old and are not recommended to be used anymore.

Low level functions have the prefix HSLVacuuBrandPump.

| Command                | Icon                                                                       | Action Performed                                                                                                                                                              |
| ---------------------- | -------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| BVSAbort               | <img src="../.gitbook/assets/image (673).png" alt="" data-size="original"> | This function is used to stop all pump units and shut down their connections in an abort handler.                                                                             |
| BVSGetAmbientPressure  | <img src="../.gitbook/assets/image (674).png" alt="" data-size="original"> | Returns the ambient pressure measured with the specified pump unit.                                                                                                           |
| BVSGetSimulationMode   | <img src="../.gitbook/assets/image (675).png" alt="" data-size="original"> | Returns whether simulation mode is set for the specified BVS / CVS or not.                                                                                                    |
| BVSInitialize          | <img src="../.gitbook/assets/image (677).png" alt="" data-size="original"> | Initializes the connection to the specified BVS / CVS.                                                                                                                        |
| BVSSetSimulationMode   | <img src="../.gitbook/assets/image (678).png" alt="" data-size="original"> | Sets the specified BVS / CVS to simulation mode.                                                                                                                              |
| BVSTerminate           | <img src="../.gitbook/assets/image (679).png" alt="" data-size="original"> | Closes the connection to the specified BVS / CVS.                                                                                                                             |
| BVSTrack               | <img src="../.gitbook/assets/image (680).png" alt="" data-size="original"> | Tracks a BVS / CVS volume move to the database.                                                                                                                               |
| BVSVacuum              | <img src="../.gitbook/assets/image (681).png" alt="" data-size="original"> | Runs the vacuum process on the specified BVS / CVS.                                                                                                                           |
| BVSVacuumTrack         | <img src="../.gitbook/assets/image (682).png" alt="" data-size="original"> | <p>Runs the vacuum process on the specified BVS / CVS.</p><p>The volume move is tracked to the Database.</p>                                                                  |
| Initialize             | <img src="../.gitbook/assets/image (683).png" alt="" data-size="original"> | Using this function the communication port will be initialized. The pumping unit will be requested for errors to ensure the communication works.                              |
| OpenAirAdmittanceValve | <img src="../.gitbook/assets/image (684).png" alt="" data-size="original"> | Allows opening the air admittance valve.                                                                                                                                      |
| ReqActualPressure      | <img src="../.gitbook/assets/image (685).png" alt="" data-size="original"> | Requests the actual pressure in the system and the measured value will be returned.                                                                                           |
| StartPressureControl   | <img src="../.gitbook/assets/image (686).png" alt="" data-size="original"> | Prepares the pumping control unit for a pressure controlled execution of the pump and starts the pump.                                                                        |
| StopPumpImmediately    | <img src="../.gitbook/assets/image (687).png" alt="" data-size="original"> | <p>A running pump started with the function StartPressureControl() can be stopped immediately</p><p>at any time calling this function.</p>                                    |
| Terminate              | <img src="../.gitbook/assets/image (688).png" alt="" data-size="original"> | Releases system resources occupied by the function Initialize().                                                                                                              |
| WaitForPumpStopped     | <img src="../.gitbook/assets/image (689).png" alt="" data-size="original"> | This function allows synchronization of pumping action and other actions which can be executed after the pump was started with a call of the function StartPressureControl(). |

\


<table data-header-hidden><thead><tr><th width="125"></th><th></th></tr></thead><tbody><tr><td><img src="../.gitbook/assets/image (10) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" data-size="original"></td><td><p>NOTE</p><p><em>Do not mix high level functions and low level functions in the same method. Make sure to specify the library name.</em></p></td></tr></tbody></table>

