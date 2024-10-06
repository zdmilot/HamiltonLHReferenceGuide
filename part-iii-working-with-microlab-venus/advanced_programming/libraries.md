# Libraries

*   ### _Using Libraries‌_

    \


    _A library is a collection of standard functions which the programmer can choose from when writing methods in addition to the toolbox elements. The best-known functions are the mathematical functions. For these, VENUS Software provides a mathematical function library. There are several other libraries that can be found to be useful. If the library required hasn’t been installed yet, install it through "Tools  Hamilton Support Software..."._

    _To use library functions in a method, include the appropriate library. Follow these steps:_

    1. _Select "Method  Libraries..." in the Labware Editor to open the dialog seen below._
    2.  _To add a library, click the Browse Button \[...] at the center of the table highlighted below or click the \[Add Library...] Button._

        \


        ![image](../../.gitbook/assets/Image\_694.png)

        \

    3. _In the file selection box, select the required library to be imported. Click \[OK]._
    4. _Repeat steps 2 through 4 to import all the libraries needed._
    5. _Click \[OK] to close the dialog. The selected library functions are available under their own group tab in the toolbox and can be used like standard commands._
    6.  _To remove libraries, select the libraries to be removed and click the \[Remove Library] Button._

        \


        ![Originalbild anzeigen](../../.gitbook/assets/Image\_695.gif)

        _NOTE_

        _If a method uses at least on function of a library, the library cannot be removed._

        \


        _VENUS Software supports two kinds of libraries: HSL Libraries (.hsl) and Sub-method Libraries (.smt)._

        _A library function can also be self-written and can be used like any standard library through the following:_

        * _Graphical Method Editor (to create a Sub-method library)_
        * _HSL Method Editor (to create an HSL library)_
    7.  #### _‌Array Library‌_

        \


        \


        ![array library](../../.gitbook/assets/Image\_696.gif)

        \

    8.  #### _‌Barcode Library‌_

        _Array Library is an old library. Its functions should not be used anymore. All array-related steps can be found in the General Steps. Arrays can be used directly in most steps._

        \


        _The HSLBarcodeReader library supports the Metrologic barcode scanner Orbit/MS7120 for read operations over the serial interface RS232._

        \


        | Command            | Icon                                                                      | Action Performed                                                                              |
        | ------------------ | ------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
        | Del Com Buffer     | <p><br></p><p><img src="../../.gitbook/assets/Image_697.gif" alt="1"></p> | Deletes the input buffer.                                                                     |
        | Read               | <p><br></p><p><img src="../../.gitbook/assets/Image_698.gif" alt="2"></p> | Gets read barcode from Metrologic barcode scanner Orbit/MS7120.                               |
        | Set Com Port       | <p><br></p><p><img src="../../.gitbook/assets/Image_699.gif" alt="3"></p> | Sets the serial port on which the Metrologic barcode scanner Orbit/MS7120 is plugged.         |
        | Set Error Recovery | <p><br></p><p><img src="../../.gitbook/assets/Image_700.gif" alt="4"></p> | Sets a flag that indicates how to react on a reading error                                    |
        | Set Simulation     | <p><br></p><p><img src="../../.gitbook/assets/Image_701.gif" alt="5"></p> | Defines whether the Metrologic barcode scanner shall be simulated instead of reading barcodes |
        | Set Timeout        | <p><br></p><p><img src="../../.gitbook/assets/Image_702.gif" alt="6"></p> | Sets the new timeout for all read operations of Metrologic barcode scanner Orbit/MS7120.      |
    9.  #### _‌Deck Visualization Library‌_

        \


        _The deck visualization library updates lists and views._

        \


        | Command               | Icon                                                                      | Action Performed                                             |
        | --------------------- | ------------------------------------------------------------------------- | ------------------------------------------------------------ |
        | Update Loaded Labware | <p><br></p><p><img src="../../.gitbook/assets/Image_703.gif" alt="1"></p> | Updates the list of loaded labware and updates the view.     |
        | Update Used Labware   | <p><br></p><p><img src="../../.gitbook/assets/Image_704.gif" alt="2"></p> | Updates the list of labware being used and updates the view. |
        | Update Used Positions | <p><br></p><p><img src="../../.gitbook/assets/Image_705.gif" alt="3"></p> | Updates the list of loaded labware and updates the view.     |

        \

    10. #### _‌Device Library‌_

        \


        _The device library offers a set of commands to collect labware and device details._

        \


        | Command                     | Icon                                                                                               | Action Performed                                                                                                                                                                                                                                                                  |
        | --------------------------- | -------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
        | DevAddContainerTo Rack      | <p><br></p><p><img src="../../.gitbook/assets/Image_706.jpg" alt="ProgmanPics/DevLib_all.bmp"></p> | Replaces a container on a rectangular pre-loaded rack.                                                                                                                                                                                                                            |
        | DevAddLabware               | <p><br></p><p><img src="../../.gitbook/assets/Image_707.jpg" alt="ProgmanPics/DevLib_all.bmp"></p> | Adds given labware to Deck Layout using deck coordinates.                                                                                                                                                                                                                         |
        | DevAddLabware ToTemplate    | <p><br></p><p><img src="../../.gitbook/assets/Image_708.jpg" alt="ProgmanPics/DevLib_all.bmp"></p> | Adds given labware to deck site on named template.                                                                                                                                                                                                                                |
        | DevAddPreloaded Labware     | <p><br></p><p><img src="../../.gitbook/assets/Image_709.jpg" alt="ProgmanPics/DevLib_all.bmp"></p> | Adds given labware including any preloaded labware to Deck Layout using deck coordinates.                                                                                                                                                                                         |
        | DevAddSequence              | <p><br></p><p><img src="../../.gitbook/assets/Image_710.jpg" alt="ProgmanPics/DevLib_all.bmp"></p> | Adds a sequence to the collection holding the editable sequences of the device.                                                                                                                                                                                                   |
        | DevAddSequence2             | <p><br></p><p><img src="../../.gitbook/assets/Image_711.jpg" alt="ProgmanPics/DevLib_all.bmp"></p> | Adds a sequence to the collection holding the editable sequences of the device.                                                                                                                                                                                                   |
        | DevCompute ContainerVolume  | <p><br></p><p><img src="../../.gitbook/assets/Image_712.jpg" alt="ProgmanPics/DevLib_all.bmp"></p> | Calculates the volume in ml for the container at the given position and the given internal height. The function does NOT support connected containers.                                                                                                                            |
        | DevCompute ContainerVolume2 | <p><br></p><p><img src="../../.gitbook/assets/Image_713.jpg" alt="ProgmanPics/DevLib_all.bmp"></p> | Calculates the volume in ml for the container at the given position and the given internal height. The function supports connected containers.                                                                                                                                    |
        | DevCopyReset Sequence       | <p><br></p><p><img src="../../.gitbook/assets/Image_714.jpg" alt="ProgmanPics/DevLib_all.bmp"></p> | <p>Reloads a copy of the original deck sequence with the name sequenceName from the Deck Layout file into the sequence object sequenceObj. All indexes, limits and positions are re-initialized. The sequence must exist.</p><p>The original deck sequence remains unchanged.</p> |

        | Command                      | Icon                                                                                               | Action Performed                                                                                                                                                                                                                                                                                                                         |
        | ---------------------------- | -------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
        | DevEditSequences             | <p><br></p><p><img src="../../.gitbook/assets/Image_715.jpg" alt="ProgmanPics/DevLib_all.bmp"></p> | <p>Displays the “Edit Sequence” Dialog which shows the Deck Layout with all the sequence positions of the sequences set by the DevAddSequence() or the DevAddSequence2() functions.</p><p>The “Edit Sequence” Dialog allows it to enabled / disabled sequence positions on the Deck Layout in a graphical manner by using the mouse.</p> |
        | DevEditSequences2            | <p><br></p><p><img src="../../.gitbook/assets/Image_716.jpg" alt="ProgmanPics/DevLib_all.bmp"></p> | <p>Displays the “Edit Sequence” Dialog which shows the Deck Layout with all the sequence positions of the sequences set by the DevAddSequence() or the DevAddSequence2() functions.</p><p>The “Edit Sequence” Dialog allows it to enabled / disabled sequence positions on the Deck Layout in a graphical manner by using the mouse.</p> |
        | DevGetBarcodeData            | <p><br></p><p><img src="../../.gitbook/assets/Image_717.jpg" alt="ProgmanPics/DevLib_all.bmp"></p> | <p>Gets the barcode mask for the instance of labware at</p><p>a position.</p>                                                                                                                                                                                                                                                            |
        | DevGetBarcodeData2           | <p><br></p><p><img src="../../.gitbook/assets/Image_718.jpg" alt="ProgmanPics/DevLib_all.bmp"></p> | Gets the barcode masks for the instances of labware at positions.                                                                                                                                                                                                                                                                        |
        | DevGetBarcodeData3           | <p><br></p><p><img src="../../.gitbook/assets/Image_719.jpg" alt="ProgmanPics/DevLib_all.bmp"></p> | Gets the barcode masks for the instances of labware at positions.                                                                                                                                                                                                                                                                        |
        | DevGetCfgValueWith Key       | <p><br></p><p><img src="../../.gitbook/assets/Image_720.jpg" alt="ProgmanPics/DevLib_all.bmp"></p> | Returns the configuration value for the instrument mapped to a given key (integer, float, or string).                                                                                                                                                                                                                                    |
        | DevGetDeckLayoutFile Name    | <p><br></p><p><img src="../../.gitbook/assets/Image_721.jpg" alt="ProgmanPics/DevLib_all.bmp"></p> | Returns the absolute Deck Layout file name (string; may be empty for a device without Deck Layout).                                                                                                                                                                                                                                      |
        | DevGetInstrument Name        | <p><br></p><p><img src="../../.gitbook/assets/Image_722.jpg" alt="ProgmanPics/DevLib_all.bmp"></p> | Returns the property value for a property key of a labware.                                                                                                                                                                                                                                                                              |
        | DevGetLabwareData            | <p><br></p><p><img src="../../.gitbook/assets/Image_723.jpg" alt="ProgmanPics/DevLib_all.bmp"></p> | Obtains the position of the given labware item from the Deck Layout using deck coordinates.                                                                                                                                                                                                                                              |
        | DevGetLabware Position       | <p><br></p><p><img src="../../.gitbook/assets/Image_724.jpg" alt="ProgmanPics/DevLib_all.bmp"></p> | Obtains the position of the given labware item from the Deck Layout using deck coordinates.                                                                                                                                                                                                                                              |
        | DevGetLabware Positionex     | <p><br></p><p><img src="../../.gitbook/assets/Image_725.jpg" alt="ProgmanPics/DevLib_all.bmp"></p> | Obtains the position of the given labware item from the Deck Layout using deck coordinates.                                                                                                                                                                                                                                              |
        | DevGetLabware Positionex2    | <p><br></p><p><img src="../../.gitbook/assets/Image_726.jpg" alt="ProgmanPics/DevLib_all.bmp"></p> | Obtains the position information of the given labware item from the Deck Layout using deck coordinates.                                                                                                                                                                                                                                  |
        | DevGetPosition LabwareNameAt | <p><br></p><p><img src="../../.gitbook/assets/Image_727.jpg" alt="ProgmanPics/DevLib_all.bmp"></p> | Retrieves the template site with associated labware name or labware name with associated position name at a given index, retrieved during a previous call to the function Get Positions Labware Names.                                                                                                                                   |
        | DevGetPosition LabwareNames  | <p><br></p><p><img src="../../.gitbook/assets/Image_728.jpg" alt="ProgmanPics/DevLib_all.bmp"></p> | Retrieves template sites with associated labware names or labware names with associated position names of all positions on the given labware which are referenced by the specified sequence.                                                                                                                                             |

        | Command                                 | Icon                                                                                               | Action Performed                                                                                                                                                 |
        | --------------------------------------- | -------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------- |
        | DevGetReleaseVersion                    | <p><br></p><p><img src="../../.gitbook/assets/Image_729.jpg" alt="ProgmanPics/DevLib_all.bmp"></p> | <p>Returns the release version for the instrument,</p><p>e.g. 3.0.0.630 (string).</p>                                                                            |
        | DevGetSequence                          | <p><br></p><p><img src="../../.gitbook/assets/Image_730.jpg" alt="ProgmanPics/DevLib_all.bmp"></p> | Gets a copy of the deck sequence with the name sequenceName.                                                                                                     |
        | DevGetSequenceRef                       | <p><br></p><p><img src="../../.gitbook/assets/Image_731.jpg" alt="ProgmanPics/DevLib_all.bmp"></p> | Gets a reference to the deck sequence with the name seqId.                                                                                                       |
        | DevGetTemplate LabwareNameAt            | <p><br></p><p><img src="../../.gitbook/assets/Image_732.jpg" alt="ProgmanPics/DevLib_all.bmp"></p> | Returns the labware name with associated template name at a given index.                                                                                         |
        | DevGetTemplateLabware Names             | <p><br></p><p><img src="../../.gitbook/assets/Image_733.jpg" alt="ProgmanPics/DevLib_all.bmp"></p> | Queries labware names with associated template name.                                                                                                             |
        | DevIsValidLabwareFor CurrentDeck-Layout | <p><br></p><p><img src="../../.gitbook/assets/Image_734.jpg" alt="ProgmanPics/DevLib_all.bmp"></p> | Checks whether the given labware is valid for the current Deck Layout.                                                                                           |
        | DevPause                                | <p><br></p><p><img src="../../.gitbook/assets/Image_735.jpg" alt="ProgmanPics/DevLib_all.bmp"></p> | Suspends the program execution at the current position.                                                                                                          |
        | DevRemoveLabware                        | <p><br></p><p><img src="../../.gitbook/assets/Image_736.jpg" alt="ProgmanPics/DevLib_all.bmp"></p> | Removes given labware from the deck.                                                                                                                             |
        | DevRemoveLabware FromTemplate           | <p><br></p><p><img src="../../.gitbook/assets/Image_737.jpg" alt="ProgmanPics/DevLib_all.bmp"></p> | Removes given labware from named template.                                                                                                                       |
        | DevRemoveSequences                      | <p><br></p><p><img src="../../.gitbook/assets/Image_738.jpg" alt="ProgmanPics/DevLib_all.bmp"></p> | Removes all sequences from the collection holding the editable sequences of the device.                                                                          |
        | DevResetSequence                        | <p><br></p><p><img src="../../.gitbook/assets/Image_739.jpg" alt="ProgmanPics/DevLib_all.bmp"></p> | Reloads the original deck sequence with the name seqId from the Deck Layout file, all indexes, limits and positions are re-initialized. The sequence must exist. |
        | DevSetBarcodeData                       | <p><br></p><p><img src="../../.gitbook/assets/Image_740.jpg" alt="ProgmanPics/DevLib_all.bmp"></p> | <p>Sets the barcode mask for the instance of labware at</p><p>a position.</p>                                                                                    |
        | DevSetBarcodeData2                      | <p><br></p><p><img src="../../.gitbook/assets/Image_741.jpg" alt="ProgmanPics/DevLib_all.bmp"></p> | Sets the barcode masks for the instances of labware at positions.                                                                                                |
        | DevSetBarcodeData3                      | <p><br></p><p><img src="../../.gitbook/assets/Image_742.jpg" alt="ProgmanPics/DevLib_all.bmp"></p> | Sets the barcode masks for the instances of labware at positions.                                                                                                |
    11. #### _‌Error Library‌_

        \


        _The error library contains functions to display and manage errors._

        \


        | Command           | Icon                                                                                                  | Action Performed                                                                                                                                                                                                      |
        | ----------------- | ----------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
        | ErrClear          | <p><br></p><p><img src="../../.gitbook/assets/Image_743.jpg" alt="ProgmanPics/BtnErrLib_all.bmp"></p> | Clears all property settings of the err object.                                                                                                                                                                       |
        | ErrCode           | <p><br></p><p><img src="../../.gitbook/assets/Image_744.jpg" alt="ProgmanPics/BtnErrLib_all.bmp"></p> | Extracts a numeric value that specifies the code of a phoenix error.                                                                                                                                                  |
        | ErrDisplay Error  | <p><br></p><p><img src="../../.gitbook/assets/Image_745.jpg" alt="ProgmanPics/BtnErrLib_all.bmp"></p> | Displays an error in a message box.                                                                                                                                                                                   |
        | ErrGetDataAt      | <p><br></p><p><img src="../../.gitbook/assets/Image_746.jpg" alt="ProgmanPics/BtnErrLib_all.bmp"></p> | Returns the element at the specified index from the data stored in the error object. If the index is 0, the function returns the size of the data stored in the error object.                                         |
        | ErrGetDescription | <p><br></p><p><img src="../../.gitbook/assets/Image_747.jpg" alt="ProgmanPics/BtnErrLib_all.bmp"></p> | Returns a descriptive string associated with an error.                                                                                                                                                                |
        | ErrGetId          | <p><br></p><p><img src="../../.gitbook/assets/Image_748.jpg" alt="ProgmanPics/BtnErrLib_all.bmp"></p> | Returns a numeric value that specifies an error.                                                                                                                                                                      |
        | ErrMajor          | <p><br></p><p><img src="../../.gitbook/assets/Image_749.jpg" alt="ProgmanPics/BtnErrLib_all.bmp"></p> | <p>Extracts a numeric value that specifies the major ID of</p><p>a phoenix error.</p>                                                                                                                                 |
        | ErrMinor          | <p><br></p><p><img src="../../.gitbook/assets/Image_750.jpg" alt="ProgmanPics/BtnErrLib_all.bmp"></p> | <p>Extracts a numeric value that specifies the minor ID of</p><p>a phoenix error.</p>                                                                                                                                 |
        | ErrRaise          | <p><br></p><p><img src="../../.gitbook/assets/Image_751.jpg" alt="ProgmanPics/BtnErrLib_all.bmp"></p> | Generates a run-time error. The error will be traced automatically.                                                                                                                                                   |
        | ErrRaiseLast      | <p><br></p><p><img src="../../.gitbook/assets/Image_752.jpg" alt="ProgmanPics/BtnErrLib_all.bmp"></p> | Re-generates the current run-time error.                                                                                                                                                                              |
        | ErrSetDataAt      | <p><br></p><p><img src="../../.gitbook/assets/Image_753.jpg" alt="ProgmanPics/BtnErrLib_all.bmp"></p> | Sets the element in the data stored in the error object at the specified index (size of data not allowed to grow if 0 < index). If the index is 0, the function sets the size of the data stored in the error object. |
        | ErrSetDescription | <p><br></p><p><img src="../../.gitbook/assets/Image_754.jpg" alt="ProgmanPics/BtnErrLib_all.bmp"></p> | Sets a descriptive string associated with an error.                                                                                                                                                                   |
        | ErrSetId          | <p><br></p><p><img src="../../.gitbook/assets/Image_755.jpg" alt="ProgmanPics/BtnErrLib_all.bmp"></p> | Sets a numeric value that specifies an error.                                                                                                                                                                         |
    12. #### _‌File Library‌_

        \


        _The file library contains all commands necessary for a method to handle files._

        \


        | Command              | Icon                                                                                                  | Action Performed                                                                                                                                                                                                                                               |
        | -------------------- | ----------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
        | FilEof               | <p><br></p><p><img src="../../.gitbook/assets/Image_756.jpg" alt="ProgmanPics/BtnFilLib_all.bmp"></p> | Indicates that the end of file (Eof) is reached.                                                                                                                                                                                                               |
        | FilFindFile          | <p><br></p><p><img src="../../.gitbook/assets/Image_757.jpg" alt="ProgmanPics/BtnFilLib_all.bmp"></p> | Starts a file search.                                                                                                                                                                                                                                          |
        | FilFindNextFile      | <p><br></p><p><img src="../../.gitbook/assets/Image_758.jpg" alt="ProgmanPics/BtnFilLib_all.bmp"></p> | Continues a file search from a previous call to FilFindFile.                                                                                                                                                                                                   |
        | FilFormatBarcodeFile | <p><br></p><p><img src="../../.gitbook/assets/Image_759.jpg" alt="ProgmanPics/BtnFilLib_all.bmp"></p> | Converts the weakly formatted barcode file, written as ASCII text file during the LoadCarrier operation, into a strongly formatted barcode file. The strongly formatted barcode file may be an ASCII text file, a Microsoft Excel, or a Microsoft Access file. |
        | FilGetBinPath        | <p><br></p><p><img src="../../.gitbook/assets/Image_760.jpg" alt="ProgmanPics/BtnFilLib_all.bmp"></p> | Retrieves the path to the Hamilton\Bin folder.                                                                                                                                                                                                                 |
        | FilGetCommState      | <p><br></p><p><img src="../../.gitbook/assets/Image_761.jpg" alt="ProgmanPics/BtnFilLib_all.bmp"></p> | Retrieves the configuration information for a specified communication resource. The entries of the structure that retrieves the configuration information must be accessible in the global scope.                                                              |
        | FilGetCommTimeouts   | <p><br></p><p><img src="../../.gitbook/assets/Image_762.jpg" alt="ProgmanPics/BtnFilLib_all.bmp"></p> | <p>Retrieves the time-out parameters for all read and write operations for a specified communication resource.</p><p>The entries of the structure that retrieve the configuration information must be accessible in the global scope.</p>                      |
        | FilGetConfigPath     | <p><br></p><p><img src="../../.gitbook/assets/Image_763.jpg" alt="ProgmanPics/BtnFilLib_all.bmp"></p> | Retrieves the path to the Hamilton\Config folder.                                                                                                                                                                                                              |
        | FilGetLibraryPath    | <p><br></p><p><img src="../../.gitbook/assets/Image_764.jpg" alt="ProgmanPics/BtnFilLib_all.bmp"></p> | Retrieves the path to the Hamilton\Library folder.                                                                                                                                                                                                             |
        | FilGetLogFilePath    | <p><br></p><p><img src="../../.gitbook/assets/Image_765.jpg" alt="ProgmanPics/BtnFilLib_all.bmp"></p> | Retrieves the path to the Hamilton\Logfiles folder where runtime generated log files are stored.                                                                                                                                                               |
        | FilGetMethodsPath    | <p><br></p><p><img src="../../.gitbook/assets/Image_766.jpg" alt="ProgmanPics/BtnFilLib_all.bmp"></p> | Retrieves the path to the Hamilton\Methods folder where all the methods are stored.                                                                                                                                                                            |
        | FilGetSystemPath     | <p><br></p><p><img src="../../.gitbook/assets/Image_767.jpg" alt="ProgmanPics/BtnFilLib_all.bmp"></p> | Retrieves the path to the Hamilton\System folder.                                                                                                                                                                                                              |
        | FilIsNull            | <p><br></p><p><img src="../../.gitbook/assets/Image_768.jpg" alt="ProgmanPics/BtnFilLib_all.bmp"></p> | Returns non-zero if the variable is a null value (SQL style Null).                                                                                                                                                                                             |

        | Command            | Icon                                                                                                  | Action Performed                                                                                                                                                                                                                                                                    |
        | ------------------ | ----------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
        | FilReadString      | <p><br></p><p><img src="../../.gitbook/assets/Image_769.jpg" alt="ProgmanPics/BtnFilLib_all.bmp"></p> | Reads the next record from the file data source as string-valued data. Row data, but no schema data, is saved to the string. After calling FilReadString, the next unread record becomes the current record, or the Eof property is set to hslTrue if there are no more records.    |
        | FilRemoveFields    | <p><br></p><p><img src="../../.gitbook/assets/Image_770.jpg" alt="ProgmanPics/BtnFilLib_all.bmp"></p> | Removes all fields from a record definition.                                                                                                                                                                                                                                        |
        | FilSearchPath      | <p><br></p><p><img src="../../.gitbook/assets/Image_771.jpg" alt="ProgmanPics/BtnFilLib_all.bmp"></p> | Searches for the specified file.                                                                                                                                                                                                                                                    |
        | FilSetCommState    | <p><br></p><p><img src="../../.gitbook/assets/Image_772.jpg" alt="ProgmanPics/BtnFilLib_all.bmp"></p> | Configures a communication resource according to the specifications in a structure that contains the configuration information. Each entry in the structure is optional and overwrites the default value in parentheses.                                                            |
        | FilSetCommTimeouts | <p><br></p><p><img src="../../.gitbook/assets/Image_773.jpg" alt="ProgmanPics/BtnFilLib_all.bmp"></p> | <p>Sets the time-out parameters for all read and write operations on a specified communication resource.</p><p>The structure that contains the time-out information is as shown below. Each entry in the structure is optional and overwrites the default value in parentheses.</p> |
        | FilUpdateRecord    | <p><br></p><p><img src="../../.gitbook/assets/Image_774.jpg" alt="ProgmanPics/BtnFilLib_all.bmp"></p> | Updates the current record of the file object with the values of the variable objects specified in the record definition. The current record remains current after calling the FilUpdateRecord function. The provider must support UPDATE.                                          |
        | FilWriteString     | <p><br></p><p><img src="../../.gitbook/assets/Image_775.gif" alt="FilLib"></p>                        | Writes a string to the end of the file data source. After calling the FilWriteString function, the new record becomes the current record.                                                                                                                                           |

        \

    13. #### _‌ML STAR DC Wash Station Library‌_

        \


        _The “HSLDcWasher” Prefix has been removed for a better overview._

        \


        | Command              | Icon                                                                                                                            | Action Performed                                                                                                                                                                                        |
        | -------------------- | ------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
        | WashSettings         | <p><br></p><p><img src="../../.gitbook/assets/Image_776.jpg" alt="../ProgmanPics/BtnDCWashstationWashSettings.bmp"></p>         | Sets independent wash parameters for each DC wash station needle sequence.                                                                                                                              |
        | NeedleWash           | <p><br></p><p><img src="../../.gitbook/assets/Image_777.jpg" alt="../ProgmanPics/BtnDCWashstationNeedleWash.bmp"></p>           | Washes the already picked up needles in the DC wash station.                                                                                                                                            |
        | NeedleWash2          | <p><br></p><p><img src="../../.gitbook/assets/Image_778.gif" alt="../ProgmanPics/BtnDCWashstationNeedleWash2.bmp"></p>          | <p>Washes the already picked up needles in the</p><p>DC wash station. Other than the NeedleWash step the NeedelWash2 step allows to specify further parameters used for dispensing the rest volume.</p> |
        | EmptyFillWashChamber | <p><br></p><p><img src="../../.gitbook/assets/Image_779.gif" alt="../ProgmanPics/BtnDCWashstationEmptyFillWashChamber.bmp"></p> | Either refills or to drains the wash chamber after last wash cycle.                                                                                                                                     |
    14. #### _‌Kit Lot Library‌_

        \


        _The "HSLKitLotLib.hsl" Library provides remarkable functions that handles barcodes of kit lots for the ML STAR._

        _The “HSLKitLot” Prefix has been removed for a better overview._

        \


        | Command               | Icon                                                                      | Action Performed                                                                               |
        | --------------------- | ------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- |
        | Check Barcode         | <p><br></p><p><img src="../../.gitbook/assets/Image_780.gif" alt="1"></p> | Check if a barcode fits a particular mask.                                                     |
        | Check Kit Lot         | <p><br></p><p><img src="../../.gitbook/assets/Image_781.gif" alt="2"></p> | Check if kit lot contained in a barcode is valid.                                              |
        | Get Kit Lot Value     | <p><br></p><p><img src="../../.gitbook/assets/Image_782.gif" alt="3"></p> | Get an arbitrary value from kit lot.                                                           |
        | Set Access Repetition | <p><br></p><p><img src="../../.gitbook/assets/Image_783.gif" alt="4"></p> | Set the number of denied access attempts for a kit lot file.                                   |
        | SetDateColName        | <p><br></p><p><img src="../../.gitbook/assets/Image_784.gif" alt="4"></p> | Define the name of the column in the kit lot file which contains the kit lot expiry date.      |
        | SetIdColName          | <p><br></p><p><img src="../../.gitbook/assets/Image_785.gif" alt="4"></p> | Define the name of the column in the kit lot file which contains the kit lot identifier.       |
        | SetKitlotFile         | <p><br></p><p><img src="../../.gitbook/assets/Image_786.gif" alt="4"></p> | Define the name of the kit lot file.                                                           |
        | SetKitlotPath         | <p><br></p><p><img src="../../.gitbook/assets/Image_787.gif" alt="4"></p> | Define the location of the kit lot file.                                                       |
        | SetTableName          | <p><br></p><p><img src="../../.gitbook/assets/Image_788.gif" alt="4"></p> | Define the name of the Excel sheet in the kit lot file which contains the kit lot information. |
        | SetTimeColName        | <p><br></p><p><img src="../../.gitbook/assets/Image_789.gif" alt="4"></p> | Define the name of the column in the kit lot file which contains the kit lot expiry time.      |
        | SplitBarcode          | <p><br></p><p><img src="../../.gitbook/assets/Image_790.gif" alt="5"></p> | Extract a substring of a barcode.                                                              |
    15. #### _‌Labware State Library‌_

        \


        _The HSL Labware State Library provides labware state management and labware controlling functions._

        _The “HSLLabwState” Prefix has been removed for a better overview._

        \


        | Command                      | Icon                                                                                                        | Action Performed                                                                                                                                                                                                   |
        | ---------------------------- | ----------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
        | AddLabware SourceBarcode     | <p><br></p><p><img src="../../.gitbook/assets/Image_791.jpg" alt="ProgmanPics/BtnLabwareState_all.bmp"></p> | Adds an additional barcode as source barcode of the labware at the current position of the given sequence.                                                                                                         |
        | GetLabwareBarcode            | <p><br></p><p><img src="../../.gitbook/assets/Image_792.jpg" alt="ProgmanPics/BtnLabwareState_all.bmp"></p> | Returns the barcode of the labware at the current position of the given sequence.                                                                                                                                  |
        | GetLabwareBarcode Mask       | <p><br></p><p><img src="../../.gitbook/assets/Image_793.jpg" alt="ProgmanPics/BtnLabwareState_all.bmp"></p> | Returns the barcode mask of the labware at the current position of the given sequence.                                                                                                                             |
        | GetLabwareExpNumOf ProcSteps | <p><br></p><p><img src="../../.gitbook/assets/Image_794.jpg" alt="ProgmanPics/BtnLabwareState_all.bmp"></p> | Retrieves the expected number of processed steps for the labware at the current position of the given sequence.                                                                                                    |
        | GetLabwareId                 | <p><br></p><p><img src="../../.gitbook/assets/Image_795.jpg" alt="ProgmanPics/BtnLabwareState_all.bmp"></p> | Returns the labware id for the current position of the given sequence.                                                                                                                                             |
        | GetLabwareLastAction State   | <p><br></p><p><img src="../../.gitbook/assets/Image_796.jpg" alt="ProgmanPics/BtnLabwareState_all.bmp"></p> | Retrieves the action state of the last performed action for the labware at the current position of the given sequence.                                                                                             |
        | GetLabwareLast SourceBarcode | <p><br></p><p><img src="../../.gitbook/assets/Image_797.jpg" alt="ProgmanPics/BtnLabwareState_all.bmp"></p> | <p>Returns the last known source barcode of the labware</p><p>at the current position of the given sequence.</p>                                                                                                   |
        | GetLabwareNumOf ProcSteps    | <p><br></p><p><img src="../../.gitbook/assets/Image_798.jpg" alt="ProgmanPics/BtnLabwareState_all.bmp"></p> | Retrieves the number of processed steps of the labware at the current position of the given sequence.                                                                                                              |
        | GetLabwareRelation           | <p><br></p><p><img src="../../.gitbook/assets/Image_799.jpg" alt="ProgmanPics/BtnLabwareState_all.bmp"></p> | Returns the labware id of the chosen parent of the labware at the current position of the given sequence.                                                                                                          |
        | GetLabwareSource Barcodes    | <p><br></p><p><img src="../../.gitbook/assets/Image_800.jpg" alt="ProgmanPics/BtnLabwareState_all.bmp"></p> | <p>Returns an array with all source barcodes of the labware at the current position of the given sequence.</p><p>This function uses the sample tracker. It will cause an error if sample tracking is disabled.</p> |
        | GetLabwareSummary State      | <p><br></p><p><img src="../../.gitbook/assets/Image_801.jpg" alt="ProgmanPics/BtnLabwareState_all.bmp"></p> | Retrieves the current summary state of the labware at the current position of the given sequence.                                                                                                                  |
        | GetLabwareVisibility         | <p><br></p><p><img src="../../.gitbook/assets/Image_802.jpg" alt="ProgmanPics/BtnLabwareState_all.bmp"></p> | Returns the visibility of the labware at the current position of the given sequence.                                                                                                                               |
        | GetLabwareVolume             | <p><br></p><p><img src="../../.gitbook/assets/Image_803.jpg" alt="ProgmanPics/BtnLabwareState_all.bmp"></p> | Retrieves the volume of the labware at the current position of the given sequence.                                                                                                                                 |
        | Is Labware Connected         | <p><br></p><p><img src="../../.gitbook/assets/Image_804.jpg" alt="ProgmanPics/BtnLabwareState_all.bmp"></p> | <p>Returns hslTrue, if the labware at the current position</p><p>of the given sequence is part of a connected container definition, else hslFalse.</p>                                                             |

        | Command                           | Icon                                                                                                        | Action Performed                                                                                                |
        | --------------------------------- | ----------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------- |
        | Set Labware Barcode               | <p><br></p><p><img src="../../.gitbook/assets/Image_805.jpg" alt="ProgmanPics/BtnLabwareState_all.bmp"></p> | Sets a new barcode for the labware at the current position of the given sequence.                               |
        | Set Labware Barcode Mask          | <p><br></p><p><img src="../../.gitbook/assets/Image_806.jpg" alt="ProgmanPics/BtnLabwareState_all.bmp"></p> | Sets a new barcode mask for the labware at the current position of the given sequence.                          |
        | Set Labware Exp Num Of Proc Steps | <p><br></p><p><img src="../../.gitbook/assets/Image_807.jpg" alt="ProgmanPics/BtnLabwareState_all.bmp"></p> | Sets the expected number of processed steps for the labware at the current position of the given sequence.      |
        | Set Labware Summary State         | <p><br></p><p><img src="../../.gitbook/assets/Image_808.jpg" alt="ProgmanPics/BtnLabwareState_all.bmp"></p> | <p>Overwrites the current summary state of the labware</p><p>at the current position of the given sequence.</p> |
        | Set Labware Visibility            | <p><br></p><p><img src="../../.gitbook/assets/Image_809.jpg" alt="ProgmanPics/BtnLabwareState_all.bmp"></p> | <p>Sets the visibility of the labware at the current position</p><p>of the given sequence.</p>                  |
        | Set Labware Volume                | <p><br></p><p><img src="../../.gitbook/assets/Image_810.jpg" alt="ProgmanPics/BtnLabwareState_all.bmp"></p> | <p>Sets the volume of the labware at the current position</p><p>of the given sequence.</p>                      |

        \

    16. #### _‌ML STAR Library‌_

        \


        _The “HSLML\_STAR” Prefix has been removed for a better overview_

        \


        | Command                                  | Icon                                                                          | Action Performed                                                                                        |
        | ---------------------------------------- | ----------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- |
        | AntiDropletControl\_1000ulChannel\_On    | <p><br></p><p><img src="../../.gitbook/assets/Image_811.jpg" alt="image"></p> | Activates the Anti-Droplet Control (ADC) on the 1000μl-pipetting channels.                              |
        | AntiDropletControl\_1000ulChannel\_Off   | <p><br></p><p><img src="../../.gitbook/assets/Image_812.jpg" alt="image"></p> | Deactivates the Anti-Droplet Control (ADC) on the 1000μl-pipetting channels.                            |
        | AntiDropletControl\_5mlChannel\_On       | <p><br></p><p><img src="../../.gitbook/assets/Image_813.jpg" alt="image"></p> | Activates the Anti-Droplet Control (ADC) on the 5ml-pipetting channels.                                 |
        | AntiDropletControl\_5mlChannel\_Off      | <p><br></p><p><img src="../../.gitbook/assets/Image_814.jpg" alt="image"></p> | Deactivates the Anti-Droplet Control (ADC) on the 5ml-pipetting channels.                               |
        | AspirationMonitoring\_1000ulChannel\_Off | <p><br></p><p><img src="../../.gitbook/assets/Image_815.jpg" alt="image"></p> | Disables the aspiration and clot detection monitoring with the ‘pLLD’ on the 1000μl-pipetting channels. |
        | AspirationMonitoring\_1000ulChannel\_On  | <p><br></p><p><img src="../../.gitbook/assets/Image_816.jpg" alt="image"></p> | Enables the aspiration and clot detection monitoring with the ‘pLLD’ on the 1000μl-pipetting channels.  |
        | AspirationMonitoring\_5mlChannel\_Off    | <p><br></p><p><img src="../../.gitbook/assets/Image_817.jpg" alt="image"></p> | Disables the aspiration and clot detection monitoring with the ‘pLLD’ on the 5ml-pipetting channels.    |
        | AspirationMonitoring\_5mlChannel\_On     | <p><br></p><p><img src="../../.gitbook/assets/Image_818.jpg" alt="image"></p> | Enables the aspiration and clot detection monitoring with the ‘pLLD’ on the 5ml-pipetting channels.     |

        | Command                                     | Icon                                                                                                                           | Action Performed                                                                                                                                                                                                                      |
        | ------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
        | ClotDetectionMonitoring\_1000µlChannel\_Off | <p><br></p><p><img src="../../.gitbook/assets/Image_819.jpg" alt="image"></p>                                                  | Disables the clot detection monitoring with the ‘cLLD’ on the 1000μl-pipetting channels.                                                                                                                                              |
        | ClotDetectionMonitoring\_1000µlChannel\_On  | <p><br></p><p><img src="../../.gitbook/assets/Image_820.jpg" alt="image"></p>                                                  | Enables the clot detection monitoring with the ‘cLLD’ on the 1000μl-pipetting channels.                                                                                                                                               |
        | ClotDetectionMonitoring\_5mlChannel\_Off    | <p><br></p><p><img src="../../.gitbook/assets/Image_821.jpg" alt="image"></p>                                                  | Disables the clot detection monitoring with the ‘cLLD’ on the 5ml-pipetting channels.                                                                                                                                                 |
        | ClotDetectionMonitoring\_5mlChannel\_On     | <p><br></p><p><img src="../../.gitbook/assets/Image_822.jpg" alt="image"></p>                                                  | Enables the clot detection monitoring with the ‘cLLD’ on the 5ml-pipetting channels.                                                                                                                                                  |
        | CreateATBarcodefile                         | <p><br></p><p><img src="../../.gitbook/assets/Image_823.gif" alt="ProgmanPics/BtnMLStarCreateATBarcodeFile.bmp"></p>           | Creates an AT Barcode file for a MTP with the AT Barcode filter program.                                                                                                                                                              |
        | DeleteBarcodeFile                           | <p><br></p><p><img src="../../.gitbook/assets/Image_824.gif" alt="ProgmanPics/BtnMLStarDeleteBarcodeFile.bmp"></p>             | Deletes an existing barcode file.                                                                                                                                                                                                     |
        | ExecuteWorklist                             | <p><br></p><p><img src="../../.gitbook/assets/Image_825.gif" alt="ProgmanPics/BtnMLStarExecuteWorklist.bmp"></p>               | Executes a worklist written in the Gemini worklist file format (Gemini Worklist File Schema Information).                                                                                                                             |
        | FormatBarcodeFile                           | <p><br></p><p><img src="../../.gitbook/assets/Image_826.gif" alt="ProgmanPics/BtnMLStarFormatBarcodeFile.bmp"></p>             | Converts the mixed formatted barcode file 'barcodeFileName', written as ASCII text file by the LoadCarrier step, into a single formatted barcode file 'formattedBarcodeFileName' using the Formatted Barcode File Schema Information. |
        | GetContainerVolume                          | <p><br></p><p><img src="../../.gitbook/assets/Image_827.gif" alt="ProgmanPics/BtnMLStarGetContainerVolume.bmp"></p>            | Retrieves the volume \[ml] of the container measured by the n-th channel during the previous MeasureContainerVolume operation.                                                                                                        |
        | GetInstrumentType                           | <p><br></p><p><img src="../../.gitbook/assets/Image_828.jpg" alt="ProgmanPics/BtnMLStarGetInstrumentType.bmp"></p>             | <p>Gets the type of the connected instrument of type ML-STAR.</p><p>Use this function only when no global device is defined.</p>                                                                                                      |
        | GetInstrumentType\_GlobalDevice             | <p><br></p><p><img src="../../.gitbook/assets/Image_829.jpg" alt="ProgmanPics/BtnMLStarGetInstrumentTypeGlobalDevice.bmp"></p> | Gets the type of the passed instrument.                                                                                                                                                                                               |
        | IsSimulatorMode                             | <p><br></p><p><img src="../../.gitbook/assets/Image_830.jpg" alt="ProgmanPics/BtnMLStarIsSimulatorMode.bmp"></p>               | Probes whether the past instrument is in simulator mode or whether it is connected to a real instrument.                                                                                                                              |
        | MeasureContainerVolume2                     | <p><br></p><p><img src="../../.gitbook/assets/Image_831.jpg" alt="ProgmanPics/BtnMLStarMeasureContainerVolume2.bmp"></p>       | The MeasureContainerVolume function measures the volume \[ml] of the container(s) beginning at the current position of a given sequence and using the given pipetting channel pattern.                                                |
        | SetBarcodeTypes                             | <p><br></p><p><img src="../../.gitbook/assets/Image_832.gif" alt="ProgmanPics/BtnMLStarSetBarcodeTypes.bmp"></p>               | Sets the barcode types.                                                                                                                                                                                                               |

        | Command                             | Icon                                                                          | Action Performed                                                                                                               |
        | ----------------------------------- | ----------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------ |
        | SetPressureThreshold\_1000ulChannel | <p><br></p><p><img src="../../.gitbook/assets/Image_833.gif" alt="image"></p> | Sets the pressure threshold for the aspiration and clot detection monitoring with the ‘pLLD’ on the 1000μl-pipetting channels. |
        | SetPressureThreshold\_5mlChannel    | <p><br></p><p><img src="../../.gitbook/assets/Image_834.gif" alt="image"></p> | Sets the pressure threshold for the aspiration and clot detection monitoring with the ‘pLLD’ on the 5ml-pipetting channels.    |

        \

    17. #### _‌Mapping Report Library‌_

        \


        _The HSL mapping report library provides functions to create mapped report files for the labware out of the sample tracking database within a method run._

        _The “HSLMAPREPORT” Prefix has been removed for a better overview._

        \


        | Command                  | Icon                                                                                                                         | Action Performed                                                                                                                                                                                                                                                           |
        | ------------------------ | ---------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
        | AddFilterSequence        | <p><br></p><p><img src="../../.gitbook/assets/Image_835.gif" alt="ProgmanPics/BtnMapReportAddFilterSequence.bmp"></p>        | Adds the specified filter sequence to the list of filters influencing the report file formatter. Once one or more filter sequences are set, only information about positions that match with a position in one of the filter sequences appears in the mapping report file. |
        | RemoveAllFilterSequences | <p><br></p><p><img src="../../.gitbook/assets/Image_836.gif" alt="ProgmanPics/BtnMapReportRemoveAllFilterSequences.bmp"></p> | Removes all filter sequences from the list of filters influencing the report file formatter.                                                                                                                                                                               |
        | GenerateMappingFile      | <p><br></p><p><img src="../../.gitbook/assets/Image_837.gif" alt="ProgmanPics/BtnMapReportGenerateMappingFile.bmp"></p>      | Creates the report-mapping files.                                                                                                                                                                                                                                          |
        | GetListSeparator         | <p><br></p><p><img src="../../.gitbook/assets/Image_838.gif" alt="ProgmanPics/BtnMapReportGetListSeparator.bmp"></p>         | Returns the list-separator, used as column- delimiter within the character separated value (.csv) report-mapping file.                                                                                                                                                     |
        | DeleteFile               | <p><br></p><p><img src="../../.gitbook/assets/Image_839.jpg" alt="ProgmanPics/BtnMapReportDeleteFile.bmp"></p>               | Deletes the specified file.                                                                                                                                                                                                                                                |
        | SetElementBarcode        | <p><br></p><p><img src="../../.gitbook/assets/Image_840.gif" alt="ProgmanPics/BtnMapReportSetElementBarcode.bmp"></p>        | Sets the barcode to the associated labware within the sample tracking database.                                                                                                                                                                                            |
        | RemoveElement            | <p><br></p><p><img src="../../.gitbook/assets/Image_841.gif" alt="ProgmanPics/BtnMapReportRemoveElement.bmp"></p>            | Removes the given labware from the access of sample tracking.                                                                                                                                                                                                              |
    18. #### _‌ML STAR Step Return Library‌_

        \


        _The step return library establishes functions to parse the result of the most frequently used ML STAR step return values._

        _The “StepReturn” Prefix has been removed on each command for a better overview._

        \


        | Command               | Icon                                                                                                               | Action Performed                                                                                                                                                                             |
        | --------------------- | ------------------------------------------------------------------------------------------------------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
        | GetErrorCode          | <p><br></p><p><img src="../../.gitbook/assets/Image_842.gif" alt="../ProgmanPics/BtnMLStarStepReturn_all.bmp"></p> | Returns the error contained in the step return value (integer).                                                                                                                              |
        | GetNumberOfPositions  | <p><br></p><p><img src="../../.gitbook/assets/Image_843.gif" alt="../ProgmanPics/BtnMLStarStepReturn_all.bmp"></p> | Retrieves the number of positions (number of block delimiters) in the given step return value (integer).                                                                                     |
        | GetPosition           | <p><br></p><p><img src="../../.gitbook/assets/Image_844.gif" alt="../ProgmanPics/BtnMLStarStepReturn_all.bmp"></p> | Retrieves the num value for a specified position (block delimiter number) (integer).                                                                                                         |
        | GetMainError          | <p><br></p><p><img src="../../.gitbook/assets/Image_845.gif" alt="../ProgmanPics/BtnMLStarStepReturn_all.bmp"></p> | Retrieves the main error for a specified position (integer).                                                                                                                                 |
        | GetSlaveError         | <p><br></p><p><img src="../../.gitbook/assets/Image_846.gif" alt="../ProgmanPics/BtnMLStarStepReturn_all.bmp"></p> | Retrieves the slave error for a specified position (integer).                                                                                                                                |
        | GetRecoveryButton     | <p><br></p><p><img src="../../.gitbook/assets/Image_847.gif" alt="../ProgmanPics/BtnMLStarStepReturn_all.bmp"></p> | Retrieves the ID of the recovery button for a specified position (integer).                                                                                                                  |
        | GetBarcode            | <p><br></p><p><img src="../../.gitbook/assets/Image_848.gif" alt="../ProgmanPics/BtnMLStarStepReturn_all.bmp"></p> | Retrieves the barcode for a specified position (string).                                                                                                                                     |
        | GetBarcodeMask        | <p><br></p><p><img src="../../.gitbook/assets/Image_849.gif" alt="../ProgmanPics/BtnMLStarStepReturn_all.bmp"></p> | Retrieves the barcode mask for a specified position (string).                                                                                                                                |
        | GetBarcodePosition    | <p><br></p><p><img src="../../.gitbook/assets/Image_850.gif" alt="../ProgmanPics/BtnMLStarStepReturn_all.bmp"></p> | Retrieves the barcode position for a specified position (string).                                                                                                                            |
        | GetLastLiquidLevel    | <p><br></p><p><img src="../../.gitbook/assets/Image_851.gif" alt="../ProgmanPics/BtnMLStarStepReturn_all.bmp"></p> | Retrieves the last liquid level for a specified position (float).                                                                                                                            |
        | GetLabwareId          | <p><br></p><p><img src="../../.gitbook/assets/Image_852.gif" alt="../ProgmanPics/BtnMLStarStepReturn_all.bmp"></p> | Retrieves the labware identifier for a specified position (string).                                                                                                                          |
        | GetPositionId         | <p><br></p><p><img src="../../.gitbook/assets/Image_853.gif" alt="../ProgmanPics/BtnMLStarStepReturn_all.bmp"></p> | Retrieves the position identifier for a specified position (string).                                                                                                                         |
        | GetLabwarePositionIds | <p><br></p><p><img src="../../.gitbook/assets/Image_854.gif" alt="../ProgmanPics/BtnMLStarStepReturn_all.bmp"></p> | Retrieves the labware identifiers with associated position identifiers for a specified position (array of variables).                                                                        |
        | GetPositionFromNum    | <p><br></p><p><img src="../../.gitbook/assets/Image_855.gif" alt="../ProgmanPics/BtnMLStarStepReturn_all.bmp"></p> | Searches a step return value for the first match of a specified num value (integer). Returns the one- based position (block delimiter number) of the first match of the specified num value. |
        | GetStepData           | <p><br></p><p><img src="../../.gitbook/assets/Image_856.gif" alt="../ProgmanPics/BtnMLStarStepReturn_all.bmp"></p> | Generic function to retrieve the step data for a specified position (string).                                                                                                                |
        | SetFieldDelimiter     | <p><br></p><p><img src="../../.gitbook/assets/Image_857.gif" alt="../ProgmanPics/BtnMLStarStepReturn_all.bmp"></p> | Sets a new field delimiter for the step return (initial value is ",").                                                                                                                       |

        | Command             | Icon                                                                                                               | Action Performed                                                                                                        |
        | ------------------- | ------------------------------------------------------------------------------------------------------------------ | ----------------------------------------------------------------------------------------------------------------------- |
        | SetBlockDelimiter   | <p><br></p><p><img src="../../.gitbook/assets/Image_858.gif" alt="../ProgmanPics/BtnMLStarStepReturn_all.bmp"></p> | Sets a new block delimiter for the step return (initial value is "\[").                                                 |
        | SetFieldDelimiterEx | <p><br></p><p><img src="../../.gitbook/assets/Image_859.gif" alt="../ProgmanPics/BtnMLStarStepReturn_all.bmp"></p> | Sets the field delimiter for the step return as specified in the instrument configuration file (initial value is ",").  |
        | SetBlockDelimiterEx | <p><br></p><p><img src="../../.gitbook/assets/Image_860.gif" alt="StepReturn"></p>                                 | Sets the block delimiter for the step return as specified in the instrument configuration file (initial value is "\["). |

        \

    19. #### _‌Math Library‌_

        \


        _The math library establishes functions for basic and advanced mathematical operations._

        \


        | Command       | Icon                                                                                                     | Action Performed                                                                                    |
        | ------------- | -------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- |
        | MthACos       | <p><br></p><p><img src="../../.gitbook/assets/Image_861.gif" alt="../ProgmanPics/BtnMthLib_all.bmp"></p> | Returns the arccosine of a number.                                                                  |
        | MthASin       | <p><br></p><p><img src="../../.gitbook/assets/Image_862.gif" alt="../ProgmanPics/BtnMthLib_all.bmp"></p> | Returns the arcsine of a number.                                                                    |
        | MthATan       | <p><br></p><p><img src="../../.gitbook/assets/Image_863.gif" alt="../ProgmanPics/BtnMthLib_all.bmp"></p> | Returns the arctangent of a number.                                                                 |
        | MthBitwiseAND | <p><br></p><p><img src="../../.gitbook/assets/Image_864.gif" alt="../ProgmanPics/BtnMthLib_all.bmp"></p> | Performs a bitwise conjunction on two expressions.                                                  |
        | MthBitwiseNOT | <p><br></p><p><img src="../../.gitbook/assets/Image_865.gif" alt="../ProgmanPics/BtnMthLib_all.bmp"></p> | Performs a bitwise NOT (negation) on an expression.                                                 |
        | MthBitwiseOR  | <p><br></p><p><img src="../../.gitbook/assets/Image_866.gif" alt="../ProgmanPics/BtnMthLib_all.bmp"></p> | Performs a bitwise disjunction on two expressions.                                                  |
        | MthBitwiseXOR | <p><br></p><p><img src="../../.gitbook/assets/Image_867.gif" alt="../ProgmanPics/BtnMthLib_all.bmp"></p> | Performs a bitwise exclusive OR on two expressions.                                                 |
        | MthCeiling    | <p><br></p><p><img src="../../.gitbook/assets/Image_868.gif" alt="../ProgmanPics/BtnMthLib_all.bmp"></p> | Returns the next highest integer that is greater than or equal to the specified numeric expression. |
        | MthCos        | <p><br></p><p><img src="../../.gitbook/assets/Image_869.gif" alt="../ProgmanPics/BtnMthLib_all.bmp"></p> | Returns the cosine of an angle.                                                                     |
        | MthDec        | <p><br></p><p><img src="../../.gitbook/assets/Image_870.gif" alt="../ProgmanPics/BtnMthLib_all.bmp"></p> | Decrements the value of a number by one.                                                            |
        | MthEqual      | <p><br></p><p><img src="../../.gitbook/assets/Image_871.gif" alt="../ProgmanPics/BtnMthLib_all.bmp"></p> | Returns a Boolean value indicating the result of the comparison.                                    |
        | MthERandDraw  | <p><br></p><p><img src="../../.gitbook/assets/Image_872.gif" alt="../ProgmanPics/BtnMthLib_all.bmp"></p> | Draws a new random number from the exponential distribution.                                        |
        | MthERandInit  | <p><br></p><p><img src="../../.gitbook/assets/Image_873.gif" alt="../ProgmanPics/BtnMthLib_all.bmp"></p> | Initializes the exponential distribution                                                            |

        | Command               | Icon                                                                                                     | Action Performed                                                                                                               |
        | --------------------- | -------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------ |
        | MthExp                | <p><br></p><p><img src="../../.gitbook/assets/Image_874.gif" alt="../ProgmanPics/BtnMthLib_all.bmp"></p> | Returns e (the base of natural logarithms) raised to a power.                                                                  |
        | MthFCeiling           | <p><br></p><p><img src="../../.gitbook/assets/Image_875.gif" alt="../ProgmanPics/BtnMthLib_all.bmp"></p> | Returns a float value representing the next highest integer that is greater than or equal to the specified numeric expression. |
        | MthFloor              | <p><br></p><p><img src="../../.gitbook/assets/Image_876.gif" alt="../ProgmanPics/BtnMthLib_all.bmp"></p> | Returns the nearest integer that is less than or equal to the specified numeric expression.                                    |
        | MthFFloor             | <p><br></p><p><img src="../../.gitbook/assets/Image_877.gif" alt="../ProgmanPics/BtnMthLib_all.bmp"></p> | Returns a float value representing the nearest integer that is less than or equal to the specified numeric expression.         |
        | MthGreaterThan        | <p><br></p><p><img src="../../.gitbook/assets/Image_878.gif" alt="../ProgmanPics/BtnMthLib_all.bmp"></p> | Returns a Boolean value indicating the result of the comparison.                                                               |
        | MthGreaterThanOrEqual | <p><br></p><p><img src="../../.gitbook/assets/Image_879.gif" alt="../ProgmanPics/BtnMthLib_all.bmp"></p> | Returns a Boolean value indicating the result of the comparison.                                                               |
        | MthInc                | <p><br></p><p><img src="../../.gitbook/assets/Image_880.gif" alt="../ProgmanPics/BtnMthLib_all.bmp"></p> | Increments the value of a number by one.                                                                                       |
        | MthLessThan           | <p><br></p><p><img src="../../.gitbook/assets/Image_881.gif" alt="../ProgmanPics/BtnMthLib_all.bmp"></p> | Returns a Boolean value indicating the result of the comparison.                                                               |
        | MthLessThanOrEqual    | <p><br></p><p><img src="../../.gitbook/assets/Image_882.gif" alt="../ProgmanPics/BtnMthLib_all.bmp"></p> | Returns a Boolean value indicating the result of the comparison.                                                               |
        | MthLog10              | <p><br></p><p><img src="../../.gitbook/assets/Image_883.gif" alt="../ProgmanPics/BtnMthLib_all.bmp"></p> | Returns the base 10 logarithm of a number.                                                                                     |
        | MthLogicalAND         | <p><br></p><p><img src="../../.gitbook/assets/Image_884.gif" alt="../ProgmanPics/BtnMthLib_all.bmp"></p> | Performs a logical conjunction on two expressions.                                                                             |
        | MthLogicalNOT         | <p><br></p><p><img src="../../.gitbook/assets/Image_885.gif" alt="../ProgmanPics/BtnMthLib_all.bmp"></p> | Performs a logical negation on an expression.                                                                                  |
        | MthLogicalOR          | <p><br></p><p><img src="../../.gitbook/assets/Image_886.gif" alt="../ProgmanPics/BtnMthLib_all.bmp"></p> | Performs a logical disjunction on two expressions.                                                                             |
        | MthLog                | <p><br></p><p><img src="../../.gitbook/assets/Image_887.gif" alt="../ProgmanPics/BtnMthLib_all.bmp"></p> | Returns the natural logarithm of a number.                                                                                     |
        | MthMax                | <p><br></p><p><img src="../../.gitbook/assets/Image_888.gif" alt="../ProgmanPics/BtnMthLib_all.bmp"></p> | Returns the greater of two supplied numeric (or string) expressions.                                                           |
        | MthMin                | <p><br></p><p><img src="../../.gitbook/assets/Image_889.gif" alt="../ProgmanPics/BtnMthLib_all.bmp"></p> | Returns the lesser of two supplied numeric (or string) expressions.                                                            |
        | MthNotEqual           | <p><br></p><p><img src="../../.gitbook/assets/Image_890.gif" alt="../ProgmanPics/BtnMthLib_all.bmp"></p> | Returns a Boolean value indicating the result of the comparison.                                                               |
        | MthNRandDraw          | <p><br></p><p><img src="../../.gitbook/assets/Image_891.gif" alt="../ProgmanPics/BtnMthLib_all.bmp"></p> | Draws a new random number from the normal distribution.                                                                        |
        | MthNRandInit          | <p><br></p><p><img src="../../.gitbook/assets/Image_892.gif" alt="../ProgmanPics/BtnMthLib_all.bmp"></p> | Initializes the normal distribution.                                                                                           |

        | Command       | Icon                                                                                                     | Action Performed                                                                                                                        |
        | ------------- | -------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- |
        | MthPow        | <p><br></p><p><img src="../../.gitbook/assets/Image_893.gif" alt="../ProgmanPics/BtnMthLib_all.bmp"></p> | Returns the value of a base expression taken to a specified power.                                                                      |
        | MthURandInit  | <p><br></p><p><img src="../../.gitbook/assets/Image_894.gif" alt="../ProgmanPics/BtnMthLib_all.bmp"></p> | Initializes the uniform distribution.                                                                                                   |
        | MthURandDraw  | <p><br></p><p><img src="../../.gitbook/assets/Image_895.gif" alt="../ProgmanPics/BtnMthLib_all.bmp"></p> | Draws a new random number from the uniform distribution.                                                                                |
        | MthTan        | <p><br></p><p><img src="../../.gitbook/assets/Image_896.gif" alt="../ProgmanPics/BtnMthLib_all.bmp"></p> | Returns the tangent of an angle.                                                                                                        |
        | MthSin        | <p><br></p><p><img src="../../.gitbook/assets/Image_897.gif" alt="../ProgmanPics/BtnMthLib_all.bmp"></p> | Returns the sine of an angle.                                                                                                           |
        | MthShiftRight | <p><br></p><p><img src="../../.gitbook/assets/Image_898.gif" alt="../ProgmanPics/BtnMthLib_all.bmp"></p> | The bitwise shift-right operator shifts its first operand to the right (>>) by the number of positions specified by the second operand. |
        | MthShiftLeft  | <p><br></p><p><img src="../../.gitbook/assets/Image_899.gif" alt="../ProgmanPics/BtnMthLib_all.bmp"></p> | The bitwise shift-left operator shifts its first operand to the right (<<) by the number of positions specified by the second operand.  |
        | MthRound      | <p><br></p><p><img src="../../.gitbook/assets/Image_900.gif" alt="../ProgmanPics/BtnMthLib_all.bmp"></p> | Returns a number rounded to a specified number of decimal places.                                                                       |
        | MthR01Init    | <p><br></p><p><img src="../../.gitbook/assets/Image_901.gif" alt="../ProgmanPics/BtnMthLib_all.bmp"></p> | Initializes the random number generator.                                                                                                |
        | MthR01Draw    | <p><br></p><p><img src="../../.gitbook/assets/Image_902.gif" alt="../ProgmanPics/BtnMthLib_all.bmp"></p> | Draws a new random number.                                                                                                              |
    20. #### _‌Object Library‌_

        \


        _The object library provides functions for handling automation objects. The “Object” Prefix has been removed for a better overview_

        | Command               | Icon                                                                                                      | Action Performed                                                                                                                                                                                                    |
        | --------------------- | --------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
        | CreateObject          | <p><br></p><p><img src="../../.gitbook/assets/Image_903.gif" alt="ProgmanPics/ObjLib_all.bmp"></p>        | Creates a reference to an automation object.                                                                                                                                                                        |
        | ReleaseObject         | <p><br></p><p><img src="../../.gitbook/assets/Image_904.gif" alt="ProgmanPics/ObjLib_releaseObj.bmp"></p> | Releases the reference to an automation object.                                                                                                                                                                     |
        | IsNull                | <p><br></p><p><img src="../../.gitbook/assets/Image_905.gif" alt="ProgmanPics/ObjLib_all.bmp"></p>        | Returns true if the object is null (i.e. the object is not bound to an automation object), otherwise false.                                                                                                         |
        | PropertyGet           | <p><br></p><p><img src="../../.gitbook/assets/Image_906.gif" alt="ProgmanPics/ObjLib_all.bmp"></p>        | Obtains the value of the specified property of an automation object.                                                                                                                                                |
        | PropertySet           | <p><br></p><p><img src="../../.gitbook/assets/Image_907.gif" alt="ProgmanPics/ObjLib_all.bmp"></p>        | Sets the value of the specified property of an automation object.                                                                                                                                                   |
        | Invoke0               | <p><br></p><p><img src="../../.gitbook/assets/Image_908.gif" alt="ProgmanPics/ObjLib_all.bmp"></p>        | <p>Provides access to those functions exposed</p><p>by an automation object that take no arguments.</p>                                                                                                             |
        | Invoke1               | <p><br></p><p><img src="../../.gitbook/assets/Image_909.gif" alt="ProgmanPics/ObjLib_all.bmp"></p>        | <p>Provides access to those functions exposed</p><p>by an automation object that take one argument.</p>                                                                                                             |
        | Invoke2               | <p><br></p><p><img src="../../.gitbook/assets/Image_910.gif" alt="ProgmanPics/ObjLib_all.bmp"></p>        | <p>Provides access to those functions exposed</p><p>by an automation object that take two arguments.</p>                                                                                                            |
        | Invoke3               | <p><br></p><p><img src="../../.gitbook/assets/Image_911.gif" alt="ProgmanPics/ObjLib_all.bmp"></p>        | Provides access to those functions exposed by an automation object that take three arguments.                                                                                                                       |
        | Invoke4               | <p><br></p><p><img src="../../.gitbook/assets/Image_912.gif" alt="ProgmanPics/ObjLib_all.bmp"></p>        | <p>Provides access to those functions exposed</p><p>by an automation object that take four arguments.</p>                                                                                                           |
        | Invoke5               | <p><br></p><p><img src="../../.gitbook/assets/Image_913.gif" alt="ProgmanPics/ObjLib_all.bmp"></p>        | <p>Provides access to those functions exposed</p><p>by an automation object that take five arguments.</p>                                                                                                           |
        | SetResultObject       | <p><br></p><p><img src="../../.gitbook/assets/Image_914.gif" alt="ProgmanPics/ObjLib_all.bmp"></p>        | Specifies an object to be used to store the result of the next call to one of the invoke functions.                                                                                                                 |
        | ResetResultObject     | <p><br></p><p><img src="../../.gitbook/assets/Image_915.gif" alt="ProgmanPics/ObjLib_all.bmp"></p>        | Resets the result object previously set by a call to the SetResultObject.                                                                                                                                           |
        | SetNumberOfParameters | <p><br></p><p><img src="../../.gitbook/assets/Image_916.gif" alt="ProgmanPics/ObjLib_all.bmp"></p>        | Sets the number of parameters of the collection holding the parameters to be passed in the next call to the Invoke function to a function exposed by an automation object. A maximum of 20 parameters is supported. |
        | GetNumberOfParameters | <p><br></p><p><img src="../../.gitbook/assets/Image_917.gif" alt="ProgmanPics/ObjLib_all.bmp"></p>        | Gets the number of parameters of the collection holding the parameters to be passed in the next call to the Invoke function to a function exposed by an automation object.                                          |

        | Command             | Icon                                                                                               | Action Performed                                                                                                                                                                                           |
        | ------------------- | -------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
        | AddParameter        | <p><br></p><p><img src="../../.gitbook/assets/Image_918.gif" alt="ProgmanPics/ObjLib_all.bmp"></p> | Adds a new parameter to the collection holding the parameters to be passed in the next call to the Invoke function to a function exposed by an automation object. A maximum of 20 parameters is supported. |
        | SetParameterAt      | <p><br></p><p><img src="../../.gitbook/assets/Image_919.gif" alt="ProgmanPics/ObjLib_all.bmp"></p> | Sets the value of a parameter for a given index; number of parameters not allowed to grow.                                                                                                                 |
        | GetParameterAt      | <p><br></p><p><img src="../../.gitbook/assets/Image_920.gif" alt="ProgmanPics/ObjLib_all.bmp"></p> | Gets the value of a parameter for a given index.                                                                                                                                                           |
        | RemoveAllParameters | <p><br></p><p><img src="../../.gitbook/assets/Image_921.gif" alt="ProgmanPics/ObjLib_all.bmp"></p> | Removes all parameters from the collection holding the parameters to be passed in the next call to the Invoke function to a function exposed by an automation object.                                      |
        | Invoke              | <p><br></p><p><img src="../../.gitbook/assets/Image_922.gif" alt="ProgmanPics/ObjLib_all.bmp"></p> | Access to the functions exposed by an automation object.                                                                                                                                                   |
        | EnumNext            | <p><br></p><p><img src="../../.gitbook/assets/Image_923.gif" alt="ProgmanPics/ObjLib_all.bmp"></p> | Retrieves the next item in the enumeration sequence.                                                                                                                                                       |
        | EnumReset           | <p><br></p><p><img src="../../.gitbook/assets/Image_924.gif" alt="ProgmanPics/ObjLib_all.bmp"></p> | Resets the enumeration sequence to the beginning.                                                                                                                                                          |
    21. #### _‌Report Library‌_

        \


        _The HSL report library provides functions to create report files for labware out of the sample tracking database within a method run (e.g.: a comma separated value result file (.csv) or an AT barcode file)._

        _The “HSLReport” Prefix has been removed for a better overview._

        \


        | Command                    | Icon                                                                                                                     | Action Performed                                                                                      |
        | -------------------------- | ------------------------------------------------------------------------------------------------------------------------ | ----------------------------------------------------------------------------------------------------- |
        | AddToReportList            | <p><br></p><p><img src="../../.gitbook/assets/Image_925.gif" alt="../ProgmanPics/BtnAddToReportList.bmp"></p>            | Adds labware within the given sequence to an internal report list.                                    |
        | AddToReportListFromLabware | <p><br></p><p><img src="../../.gitbook/assets/Image_926.gif" alt="../ProgmanPics/BtnAddToReportListFromLabware.bmp"></p> | Adds labware within the given sequence to an internal report list.                                    |
        | Create ATBarcode File      | <p><br></p><p><img src="../../.gitbook/assets/Image_927.gif" alt="../ProgmanPics/BtnCreateAtBarcodeFile.bmp"></p>        | Executes the Hamilton AT-file filter program HxATFilter in quiet mode, to create the AT barcode file. |

        \


        ![Originalbild anzeigen](../../.gitbook/assets/Image\_928.gif)

        _NOTE_

        _In creating an AT-Barcode file for vials containing more than one barcode (for example sample + reagent were dispensed into this well, both came from containers with a barcode), the last barcode in the pipetting order will be written into the AT-Barcode file._

        _To prevent overwriting, a sample barcode of a reagent barcode (reagent dispensed after the sample) has to be deleted. To do this, set an empty string as a barcode for the container using the SetLabwareBarcode command from the HSLLabwareState library between loading and pipetting._

        \

    22. #### _‌Sequence Library‌_

        \


        _The sequence library is very helpful for advanced sequence creation and handling._

        \


        | Command           | Icon                                                                                                          | Action Performed                                                                                                                                                             |
        | ----------------- | ------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
        | SeqAdd            | <p><br></p><p><img src="../../.gitbook/assets/Image_929.jpg" alt="../ProgmanPics/BtnSequenceLib_all.bmp"></p> | Adds the labware item with the name labwareId and the positionId at the end of the sequence.                                                                                 |
        | SeqAddEx          | <p><br></p><p><img src="../../.gitbook/assets/Image_930.jpg" alt="../ProgmanPics/BtnSequenceLib_all.bmp"></p> | Adds the labware item with the name labwareId and the positionId at the end of the sequence. For multi Deck Layouts. There is an additional parameter called device context. |
        | SeqCopySequence   | <p><br></p><p><img src="../../.gitbook/assets/Image_931.jpg" alt="../ProgmanPics/BtnSequenceLib_all.bmp"></p> | Overwrites the state of the target sequence object with the state of another sequence.                                                                                       |
        | SeqEdit           | <p><br></p><p><img src="../../.gitbook/assets/Image_932.jpg" alt="../ProgmanPics/BtnSequenceLib_all.bmp"></p> | Provides a way to edit a sequence graphically.                                                                                                                               |
        | SeqEdit2          | <p><br></p><p><img src="../../.gitbook/assets/Image_933.jpg" alt="../ProgmanPics/BtnSequenceLib_all.bmp"></p> | Provides a way to edit a sequence graphically.                                                                                                                               |
        | SeqEqualSequences | <p><br></p><p><img src="../../.gitbook/assets/Image_934.jpg" alt="../ProgmanPics/BtnSequenceLib_all.bmp"></p> | Determines whether the specified sequences are equal.                                                                                                                        |

        | Command                            | Icon                                                                                                          | Action Performed                                                                                                                           |
        | ---------------------------------- | ------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
        | SeqGetLabwareId                    | <p><br></p><p><img src="../../.gitbook/assets/Image_935.jpg" alt="../ProgmanPics/BtnSequenceLib_all.bmp"></p> | Returns the labware identifier of the item at the current position.                                                                        |
        | SeqGetLabwareIds                   | <p><br></p><p><img src="../../.gitbook/assets/Image_936.jpg" alt="../ProgmanPics/BtnSequenceLib_all.bmp"></p> | Retrieves the unique labware names of a sequence.                                                                                          |
        | SeqGetMax                          | <p><br></p><p><img src="../../.gitbook/assets/Image_937.jpg" alt="../ProgmanPics/BtnSequenceLib_all.bmp"></p> | Returns the maximum number of positions/labware, which is allowed to be processed per step.                                                |
        | SeqGetName                         | <p><br></p><p><img src="../../.gitbook/assets/Image_938.jpg" alt="../ProgmanPics/BtnSequenceLib_all.bmp"></p> | Retrieves the name of the sequence.                                                                                                        |
        | SeqGetNext                         | <p><br></p><p><img src="../../.gitbook/assets/Image_939.jpg" alt="../ProgmanPics/BtnSequenceLib_all.bmp"></p> | Sets the current position on the next position in iteration order.                                                                         |
        | SeqGetPositionCountForCurr Labware | <p><br></p><p><img src="../../.gitbook/assets/Image_940.jpg" alt="../ProgmanPics/BtnSequenceLib_all.bmp"></p> | Returns the position count remaining for the current labware.                                                                              |
        | SeqGetPositionId                   | <p><br></p><p><img src="../../.gitbook/assets/Image_941.jpg" alt="../ProgmanPics/BtnSequenceLib_all.bmp"></p> | Returns the position identifier of the item at the current position.                                                                       |
        | SeqGetProperty                     | <p><br></p><p><img src="../../.gitbook/assets/Image_942.jpg" alt="../ProgmanPics/BtnSequenceLib_all.bmp"></p> | Gets at the specified sequence position the value associated with the specified property.                                                  |
        | SeqGetTotal                        | <p><br></p><p><img src="../../.gitbook/assets/Image_943.jpg" alt="../ProgmanPics/BtnSequenceLib_all.bmp"></p> | Returns the total number of positions in this sequence.                                                                                    |
        | SeqGetUsedPositions                | <p><br></p><p><img src="../../.gitbook/assets/Image_944.jpg" alt="../ProgmanPics/BtnSequenceLib_all.bmp"></p> | Returns the number of positions/labware in a sequence, which has been processed by the last step.                                          |
        | SeqIncrement                       | <p><br></p><p><img src="../../.gitbook/assets/Image_945.jpg" alt="../ProgmanPics/BtnSequenceLib_all.bmp"></p> | Increments the current position by increment positions/labware in iteration order.                                                         |
        | SeqInsertAt                        | <p><br></p><p><img src="../../.gitbook/assets/Image_946.jpg" alt="../ProgmanPics/BtnSequenceLib_all.bmp"></p> | Inserts given labware item after position pos.                                                                                             |
        | SeqLookupPosition                  | <p><br></p><p><img src="../../.gitbook/assets/Image_947.jpg" alt="../ProgmanPics/BtnSequenceLib_all.bmp"></p> | Looks up a given labware position.                                                                                                         |
        | SeqMPH48SortLike96                 | <p><br></p><p><img src="../../.gitbook/assets/Image_948.jpg" alt="../ProgmanPics/BtnSequenceLib_all.bmp"></p> | Sorts a single or multi-(384)plate sequence in such a way that a 96 position pipetting pattern is preserved when pipetting with an MPH 48. |
        | SeqOperatorAssignSeq               | <p><br></p><p><img src="../../.gitbook/assets/Image_949.jpg" alt="../ProgmanPics/BtnSequenceLib_all.bmp"></p> | Assigns another sequence to the target sequence.                                                                                           |
        | SeqOperatorDec                     | <p><br></p><p><img src="../../.gitbook/assets/Image_950.jpg" alt="../ProgmanPics/BtnSequenceLib_all.bmp"></p> | <p>The decrement operator decrements the current position of the specified sequence object to current</p><p>- used.</p>                    |
        | SeqOperatorInc                     | <p><br></p><p><img src="../../.gitbook/assets/Image_951.jpg" alt="../ProgmanPics/BtnSequenceLib_all.bmp"></p> | <p>The increment operator increments the current position of the specified sequence object to current</p><p>- used.</p>                    |

        | Command                 | Icon                                                                                                          | Action Performed                                                                                                                   |
        | ----------------------- | ------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------- |
        | SeqReadCurrentPosition  | <p><br></p><p><img src="../../.gitbook/assets/Image_952.jpg" alt="../ProgmanPics/BtnSequenceLib_all.bmp"></p> | Reads an existing record in the database table containing the persistent current positions of sequences.                           |
        | SeqReadFromFile         | <p><br></p><p><img src="../../.gitbook/assets/Image_953.jpg" alt="../ProgmanPics/BtnSequenceLib_all.bmp"></p> | Initializes the sequence instance data from a configuration file.                                                                  |
        | SeqRemoveAll            | <p><br></p><p><img src="../../.gitbook/assets/Image_954.jpg" alt="../ProgmanPics/BtnSequenceLib_all.bmp"></p> | Removes all labware items from the given sequence.                                                                                 |
        | SeqRemoveAt             | <p><br></p><p><img src="../../.gitbook/assets/Image_955.jpg" alt="../ProgmanPics/BtnSequenceLib_all.bmp"></p> | Removes the labware item at a given position.                                                                                      |
        | SeqRemoveAllProperties  | <p><br></p><p><img src="../../.gitbook/assets/Image_956.jpg" alt="../ProgmanPics/BtnSequenceLib_all.bmp"></p> | Removes at the specified sequence position all properties.                                                                         |
        | SeqRemoveProperty       | <p><br></p><p><img src="../../.gitbook/assets/Image_957.jpg" alt="../ProgmanPics/BtnSequenceLib_all.bmp"></p> | Removes at the specified sequence position the specified property.                                                                 |
        | SeqResetSequenceIndexes | <p><br></p><p><img src="../../.gitbook/assets/Image_958.jpg" alt="../ProgmanPics/BtnSequenceLib_all.bmp"></p> | Resets all indexes (current position, end position and max positions) of the given sequence.                                       |
        | SeqSetMax               | <p><br></p><p><img src="../../.gitbook/assets/Image_959.jpg" alt="../ProgmanPics/BtnSequenceLib_all.bmp"></p> | Sets the maximum number of positions/labware, which is allowed to be processed per step.                                           |
        | SeqSetProperty          | <p><br></p><p><img src="../../.gitbook/assets/Image_960.jpg" alt="../ProgmanPics/BtnSequenceLib_all.bmp"></p> | Sets at the specified sequence position the specified property to the specified value.                                             |
        | SeqSetPropertyRange     | <p><br></p><p><img src="../../.gitbook/assets/Image_961.jpg" alt="../ProgmanPics/BtnSequenceLib_all.bmp"></p> | Sets at the specified sequence positions the specified property to the specified value.                                            |
        | SeqSetUsedPositions     | <p><br></p><p><img src="../../.gitbook/assets/Image_962.jpg" alt="../ProgmanPics/BtnSequenceLib_all.bmp"></p> | Sets the number of positions/labware in a sequence, which has been processed by the last single step.                              |
        | SeqWriteCurrentPosition | <p><br></p><p><img src="../../.gitbook/assets/Image_963.jpg" alt="../ProgmanPics/BtnSequenceLib_all.bmp"></p> | Appends a new record or updates an existing record in the database table containing the persistent current positions of sequences. |
        | SeqWriteToFile          | <p><br></p><p><img src="../../.gitbook/assets/Image_964.jpg" alt="../ProgmanPics/BtnSequenceLib_all.bmp"></p> | Writes the sequence instance data to a configuration file.                                                                         |
    23. #### _‌String Library‌_

        \


        _The string library provides several functions to concatenate, fill, search and modify strings._

        \


        | Command         | Icon                                                                                                                                                     | Action Performed                                                                                                                                      |
        | --------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------- |
        | StrAsciiToStr   | <p><br></p><p><img src="../../.gitbook/assets/Image_965.gif" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\StringLib_all.bmp"></p> | Converts the given ASCII code (integer) to a character (string).                                                                                      |
        | StrConcat12     | <p><br></p><p><img src="../../.gitbook/assets/Image_966.gif" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\StringLib_all.bmp"></p> | <p>Returns the concatenation of the arguments.</p><p>If an argument is not of a string type, it is first converted to a string and then concated.</p> |
        | StrConcat2      | <p><br></p><p><img src="../../.gitbook/assets/Image_967.gif" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\StringLib_all.bmp"></p> | Returns the concatenation of the arguments.                                                                                                           |
        | StrConcat4      | <p><br></p><p><img src="../../.gitbook/assets/Image_968.gif" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\StringLib_all.bmp"></p> | Returns the concatenation of the arguments.                                                                                                           |
        | StrConcat8      | <p><br></p><p><img src="../../.gitbook/assets/Image_969.gif" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\StringLib_all.bmp"></p> | Returns the concatenation of the arguments.                                                                                                           |
        | StrEvaluateExpr | <p><br></p><p><img src="../../.gitbook/assets/Image_970.gif" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\StringLib_all.bmp"></p> | Evaluates an expression. All variables referenced inside the expression must have global scope.                                                       |
        | StrFillLeft     | <p><br></p><p><img src="../../.gitbook/assets/Image_971.gif" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\StringLib_all.bmp"></p> | Fills leading characters to the string.                                                                                                               |
        | StrFillRight    | <p><br></p><p><img src="../../.gitbook/assets/Image_972.gif" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\StringLib_all.bmp"></p> | Fills trailing characters to the string.                                                                                                              |
        | StrFind         | <p><br></p><p><img src="../../.gitbook/assets/Image_973.gif" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\StringLib_all.bmp"></p> | Searches the string for the first match of a sub- string.                                                                                             |
        | StrFStr         | <p><br></p><p><img src="../../.gitbook/assets/Image_974.gif" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\StringLib_all.bmp"></p> | Converts the floating point number into the corresponding character string.                                                                           |
        | StrFStrEx       | <p><br></p><p><img src="../../.gitbook/assets/Image_975.gif" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\StringLib_all.bmp"></p> | Converts the floating point number into the corresponding character string.                                                                           |
        | StrFVal         | <p><br></p><p><img src="../../.gitbook/assets/Image_976.gif" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\StringLib_all.bmp"></p> | Converts the sequence of digits, contained in the character string str, into the corresponding integer.                                               |
        | StrGetLength    | <p><br></p><p><img src="../../.gitbook/assets/Image_977.gif" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\StringLib_all.bmp"></p> | Returns the number of characters in a string object.                                                                                                  |
        | StrGetType      | <p><br></p><p><img src="../../.gitbook/assets/Image_978.gif" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\StringLib_all.bmp"></p> | Retrieves the type of the value of a variable.                                                                                                        |
        | StrHexIStr      | <p><br></p><p><img src="../../.gitbook/assets/Image_979.gif" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\StringLib_all.bmp"></p> | Converts the integer number into the corresponding hexadecimal character string.                                                                      |
        | StrIsDigit      | <p><br></p><p><img src="../../.gitbook/assets/Image_980.gif" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\StringLib_all.bmp"></p> | Determines if the specified character (string) is a digit.                                                                                            |
        | StrIStr         | <p><br></p><p><img src="../../.gitbook/assets/Image_981.gif" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\StringLib_all.bmp"></p> | Converts the integer number into the corresponding character string.                                                                                  |

        | Command          | Icon                                                                                                                                                     | Action Performed                                                                                                                                                                                                                                                                                                                                                                                                                         |
        | ---------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
        | StrIVal          | <p><br></p><p><img src="../../.gitbook/assets/Image_982.gif" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\StringLib_all.bmp"></p> | Converts the sequence of digits, contained in the character string str, into the corresponding integer. The sequence of digits is interpreted decimal. If the sequence begins with 0x, it is interpreted hexadecimal.                                                                                                                                                                                                                    |
        | StrLeft          | <p><br></p><p><img src="../../.gitbook/assets/Image_983.gif" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\StringLib_all.bmp"></p> | Extracts the first (that is, leftmost) count characters from the string object and returns a copy of the extracted sub-string. If count exceeds the string length, then the entire string is extracted.                                                                                                                                                                                                                                  |
        | StrMakeLower     | <p><br></p><p><img src="../../.gitbook/assets/Image_984.gif" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\StringLib_all.bmp"></p> | Converts the string object to a lowercase string.                                                                                                                                                                                                                                                                                                                                                                                        |
        | StrMakeUpper     | <p><br></p><p><img src="../../.gitbook/assets/Image_985.gif" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\StringLib_all.bmp"></p> | Converts the string object to an uppercase string.                                                                                                                                                                                                                                                                                                                                                                                       |
        | StrMid           | <p><br></p><p><img src="../../.gitbook/assets/Image_986.gif" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\StringLib_all.bmp"></p> | Extracts a sub-string of length count characters from the string object, starting at position first (zero-based). The function returns a copy of the extracted sub-string.                                                                                                                                                                                                                                                               |
        | StrReplace       | <p><br></p><p><img src="../../.gitbook/assets/Image_987.gif" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\StringLib_all.bmp"></p> | Replaces indicated sub-strings with another sub-string.                                                                                                                                                                                                                                                                                                                                                                                  |
        | StrReverseFind   | <p><br></p><p><img src="../../.gitbook/assets/Image_988.gif" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\StringLib_all.bmp"></p> | Searches a string object for the last match of a sub-string.                                                                                                                                                                                                                                                                                                                                                                             |
        | StrRight         | <p><br></p><p><img src="../../.gitbook/assets/Image_989.gif" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\StringLib_all.bmp"></p> | Extracts the last (that is, rightmost) count characters from the string object and returns a copy of the extracted sub-string. If count exceeds the string length, then the entire string is extracted.                                                                                                                                                                                                                                  |
        | StrSpanExcluding | <p><br></p><p><img src="../../.gitbook/assets/Image_990.gif" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\StringLib_all.bmp"></p> | Can be used to search the string for the first occurrence of any character in the specified set subStr. StrSpanExcluding extracts and returns all characters preceding the first occurrence of a character from subStr (in other words, the character from subStr and all characters following it in the string, are not returned). If no character from subStr is found in the string, then StrSpanExcluding returns the entire string. |
        | StrStrToAscii    | <p><br></p><p><img src="../../.gitbook/assets/Image_991.gif" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\StringLib_all.bmp"></p> | Converts the given character (string) to an ASCII code (integer).                                                                                                                                                                                                                                                                                                                                                                        |
        | StrTrimLeft      | <p><br></p><p><img src="../../.gitbook/assets/Image_992.gif" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\StringLib_all.bmp"></p> | Trims leading whitespace characters from the string (removes newline, space, tab, and user- defined characters).                                                                                                                                                                                                                                                                                                                         |
        | StrTrimRight     | <p><br></p><p><img src="../../.gitbook/assets/Image_993.gif" alt="StringLib"></p>                                                                        | Trims trailing whitespace characters from the string (removes newline, space, tab, and user- defined characters).                                                                                                                                                                                                                                                                                                                        |
    24. #### _‌Time Library‌_

        \


        _The time library allows getting time and date information from the computer._

        \


        | Command             | Icon                                                                                                                                                   | Action Performed                                   |
        | ------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------ | -------------------------------------------------- |
        | TimGetTime          | <p><br></p><p><img src="../../.gitbook/assets/Image_994.gif" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\timeLib_all.bmp"></p> | Returns the current time (string).                 |
        | TimGetDate          | <p><br></p><p><img src="../../.gitbook/assets/Image_995.gif" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\timeLib_all.bmp"></p> | Returns the current date (string).                 |
        | TimGetFormattedTime | <p><br></p><p><img src="../../.gitbook/assets/Image_996.gif" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\timeLib_all.bmp"></p> | Returns a string that contains the formatted time. |
        | TimGetFormattedDate | <p><br></p><p><img src="../../.gitbook/assets/Image_997.gif" alt="TimeLib"></p>                                                                        | Returns a string that contains the formatted date. |

        \

    25. #### _‌Synchronize Library‌_

        \


        _The synchronize library is used to handle critical sections in methods._

        _The “SynLib” Prefix has been removed on some commands for a better overview._

        \


        | Command                      | Icon                                                                                                                                                               | Action Performed                                                                                                                 |
        | ---------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------ | -------------------------------------------------------------------------------------------------------------------------------- |
        | SynInitializeCriticalSection | <p><br></p><p><img src="../../.gitbook/assets/Image_998.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\SynEnterCriticalSection.bmp"></p> | This function initializes a critical section object.                                                                             |
        | SynEnterCriticalSection      | <p><br></p><p><img src="../../.gitbook/assets/Image_999.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\SynEnterCriticalSection.bmp"></p> | Waits for ownership of the specified critical section object. The function returns when the calling thread is granted ownership. |
        | SynLeaveCriticalSection      | <p><br></p><p><img src="../../.gitbook/assets/Image_1000.gif" alt="1"></p>                                                                                         | Releases ownership of the specified critical section object.                                                                     |
        | Connect                      | <p><br></p><p><img src="../../.gitbook/assets/Image_1001.gif" alt="3"></p>                                                                                         | Opens a connection to another computer in a network. Every computer gets its own connection.                                     |
        | CloseConnection              | <p><br></p><p><img src="../../.gitbook/assets/Image_1002.gif" alt="2"></p>                                                                                         | Closes the connection with the specific SyncHandle.                                                                              |
        | SendData                     | <p><br></p><p><img src="../../.gitbook/assets/Image_1003.gif" alt="7"></p>                                                                                         | Sends the string in the variable DataToSend to the connection with the specific SyncHandle.                                      |
        | GetReceivedData              | <p><br></p><p><img src="../../.gitbook/assets/Image_1004.gif" alt="5"></p>                                                                                         | Reads data out of the local buffer from the specific SyncHandle.                                                                 |
        | GetAllReceivedData           | <p><br></p><p><img src="../../.gitbook/assets/Image_1005.gif" alt="4"></p>                                                                                         | Reads all data out of the local buffer from the specific SyncHandle.                                                             |
        | ResetBuffer                  | <p><br></p><p><img src="../../.gitbook/assets/Image_1006.gif" alt="6"></p>                                                                                         | Resets and clears the incoming data buffer from the specific SyncHandle.                                                         |
    26. #### _‌Tip Counting Library‌_

        \


        _The tip counting library provides all functions to store the available amount of tips for following methods. This is useful if a method does not use up all tips on the deck. After a new start of a method, the instrument will continue using the next available tip._

        _The “TipCount” Prefix has been removed for a better overview._

        \


        | Command | Icon                                                                                                                                                        | Action Performed                                                                                                                   |
        | ------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------- |
        | Write2  | <p><br></p><p><img src="../../.gitbook/assets/Image_1007.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\CountingLib_all.bmp"></p> | Writes the indexes from the given sequence to the element counter database in the system directory.                                |
        | Read2   | <p><br></p><p><img src="../../.gitbook/assets/Image_1008.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\CountingLib_all.bmp"></p> | Reads the indexes from the element counter database in the System directory into the given sequence.                               |
        | Edit2   | <p><br></p><p><img src="../../.gitbook/assets/Image_1009.gif" alt="TipCounting"></p>                                                                        | Reads the indexes from the element counter database into the given sequence and prompts the user to edit the sequence graphically. |

        \

    27. #### _‌Trace Library‌_

        \


        _The trace library allows using functions to write into the trace window._

        \


        | Command              | Icon                                                                                                                                                     | Action Performed                                                                                                        |
        | -------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------- |
        | TrcFormatTrace       | <p><br></p><p><img src="../../.gitbook/assets/Image_1010.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\TraceLib_all.bmp"></p> | Function to trace 2 formatted strings.                                                                                  |
        | TrcFormatTrace4      | <p><br></p><p><img src="../../.gitbook/assets/Image_1011.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\TraceLib_all.bmp"></p> | Function to trace 4 formatted strings.                                                                                  |
        | TrcFormatTrace8      | <p><br></p><p><img src="../../.gitbook/assets/Image_1012.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\TraceLib_all.bmp"></p> | Function to trace 8 formatted strings.                                                                                  |
        | TrcFormatTrace12     | <p><br></p><p><img src="../../.gitbook/assets/Image_1013.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\TraceLib_all.bmp"></p> | Function to trace 12 formatted strings.                                                                                 |
        | TrcGetMethodFileName | <p><br></p><p><img src="../../.gitbook/assets/Image_1014.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\TraceLib_all.bmp"></p> | Retrieves the path and name of the topmost HSL source file that includes the current HSL source file.                   |
        | TrcInputBox          | <p><br></p><p><img src="../../.gitbook/assets/Image_1015.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\TraceLib_all.bmp"></p> | Displays the input request prompt in a dialog box and returns with the value of the specified type entered by the user. |
        | TrcMessageBox        | <p><br></p><p><img src="../../.gitbook/assets/Image_1016.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\TraceLib_all.bmp"></p> | Displays a message in a message box and returns with a value, which identifies the button selected by the user.         |
        | TrcTrace             | <p><br></p><p><img src="../../.gitbook/assets/Image_1017.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\TraceLib_all.bmp"></p> | Trace function with two arguments.                                                                                      |
        | TrcTrace4            | <p><br></p><p><img src="../../.gitbook/assets/Image_1018.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\TraceLib_all.bmp"></p> | Trace function with four arguments.                                                                                     |
        | TrcTrace8            | <p><br></p><p><img src="../../.gitbook/assets/Image_1019.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\TraceLib_all.bmp"></p> | Trace function with eight arguments.                                                                                    |

        | Command          | Icon                                                                                                                                                     | Action Performed                             |
        | ---------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------- |
        | TrcTrace12       | <p><br></p><p><img src="../../.gitbook/assets/Image_1020.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\TraceLib_all.bmp"></p> | Trace function with twelve arguments.        |
        | TrcTraceSequence | <p><br></p><p><img src="../../.gitbook/assets/Image_1021.gif" alt="Trace"></p>                                                                           | Traces the attributes of the given sequence. |

        \

    28. #### _‌Utility Library‌_

        \


        _The utility library is a collection of several useful commands to perform requests and more. The “Util” Prefix has been removed for a better overview._

        | Command                 | Icon                                                                                                                                                                       | Action Performed                                                                                       |
        | ----------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------ |
        | Abs                     | <p><br></p><p><img src="../../.gitbook/assets/Image_1022.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\UtilLib_Most.bmp"></p>                   | Returns a value of the same type that is passed to it specifying the absolute value of a number.       |
        | AddCheckSum             | <p><br></p><p><img src="../../.gitbook/assets/Image_1023.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\UtilLib_Most.bmp"></p>                   | Computes the checksum of the specified file and writes the checksum value to the end of the file.      |
        | AsyncShell              | <p><br></p><p><img src="../../.gitbook/assets/Image_1024.gif" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\UtilLib_AsynchShell.bmp"></p>            | Runs an executable (exe, com, bat). This function runs other programs asynchronously.                  |
        | GetBarcodeJoker         | <p><br></p><p><img src="../../.gitbook/assets/Image_1025.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\UtilLib_Most.bmp"></p>                   | Returns the value for the barcode joker mapped to the given key (string).                              |
        | GetEmailAddressOfSender | <p><br></p><p><img src="../../.gitbook/assets/Image_1026.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\UtilLibGeteMailAddressOfSender.bmp"></p> | Get configured sender address for e-mails to be transmitted.                                           |
        | GetHWnd                 | <p><br></p><p><img src="../../.gitbook/assets/Image_1027.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\UtilLib_Most.bmp"></p>                   | Returns the application’s main window handle.                                                          |
        | GetIVDSystem            | <p><br></p><p><img src="../../.gitbook/assets/Image_1028.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\UtilLib_Most.bmp"></p>                   | Retrieves the IVD system installed flag from the system registry (integer).                            |
        | GetLanguage             | <p><br></p><p><img src="../../.gitbook/assets/Image_1029.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\UtilLib_Most.bmp"></p>                   | Retrieves the Phoenix language.                                                                        |
        | GetSMTPServerHostName   | <p><br></p><p><img src="../../.gitbook/assets/Image_1030.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\UtilLibGeteMailAddressOfSender.bmp"></p> | Request the configured SMTP server host name.                                                          |
        | GetSimulationMode       | <p><br></p><p><img src="../../.gitbook/assets/Image_1031.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\UtilLib_Most.bmp"></p>                   | Returns the simulation mode (0 = simulation off, 1 = full simulation)                                  |
        | GetTimeScaleFactor      | <p><br></p><p><img src="../../.gitbook/assets/Image_1032.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\UtilLib_Most.bmp"></p>                   | Returns the current time scale factor for activities/task durations (float; defaults to 1.0).          |
        | GetTimerViewName        | <p><br></p><p><img src="../../.gitbook/assets/Image_1033.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\UtilLib_Most.bmp"></p>                   | Returns the view name of the given timer.                                                              |
        | GetUniqueRunId          | <p><br></p><p><img src="../../.gitbook/assets/Image_1034.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\UtilLib_Most.bmp"></p>                   | Returns the unique ID of the current run.                                                              |
        | GetUserName             | <p><br></p><p><img src="../../.gitbook/assets/Image_1035.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\UtilLib_Most.bmp"></p>                   | Retrieves the name of the current user. This is the name of the user currently logged onto the system. |

        | Command                | Icon                                                                                                                                                                       | Action Performed                                                                                                                                                                                            |
        | ---------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
        | IsFloat                | <p><br></p><p><img src="../../.gitbook/assets/Image_1036.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\UtilLib_Most.bmp"></p>                   | Returns true if the variable var is a float.                                                                                                                                                                |
        | IsInteger              | <p><br></p><p><img src="../../.gitbook/assets/Image_1037.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\UtilLib_Most.bmp"></p>                   | Returns true if the variable var is an integer.                                                                                                                                                             |
        | IsNegative             | <p><br></p><p><img src="../../.gitbook/assets/Image_1038.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\UtilLib_Most.bmp"></p>                   | Returns true if number is negative.                                                                                                                                                                         |
        | IsNumber               | <p><br></p><p><img src="../../.gitbook/assets/Image_1039.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\UtilLib_Most.bmp"></p>                   | Returns true if the variable var is a numeric expression.                                                                                                                                                   |
        | IsString               | <p><br></p><p><img src="../../.gitbook/assets/Image_1040.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\UtilLib_Most.bmp"></p>                   | Returns true if the variable var is a string.                                                                                                                                                               |
        | Lock                   | <p><br></p><p><img src="../../.gitbook/assets/Image_1041.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\UtilLib_Most.bmp"></p>                   | Lock() and Unlock() are functions that enclose a series of HSL statements so that a group of HSL statements can be executed without interruption.                                                           |
        | Lookup                 | <p><br></p><p><img src="../../.gitbook/assets/Image_1042.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\UtilLib_Most.bmp"></p>                   | Returns true if the array of variables contains the specified value, and if true, the parameter contains the index in the array of the found element.                                                       |
        | Max                    | <p><br></p><p><img src="../../.gitbook/assets/Image_1043.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\UtilLib_Most.bmp"></p>                   | Returns the greater of two expressions (numeric or string).                                                                                                                                                 |
        | Min                    | <p><br></p><p><img src="../../.gitbook/assets/Image_1044.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\UtilLib_Most.bmp"></p>                   | Returns the lower of two expressions (numeric or string).                                                                                                                                                   |
        | Pause                  | <p><br></p><p><img src="../../.gitbook/assets/Image_1045.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\UtilLib_Most.bmp"></p>                   | Suspends the program execution at the next position where the Lock() and Unlock() functions match exactly.                                                                                                  |
        | RegisterAbortHandler   | <p><br></p><p><img src="../../.gitbook/assets/Image_1046.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\UtilLib_Most.bmp"></p>                   | Registers abortHandler as a custom HSL function called before a method will be aborted. One or more abort handlers can be registered.                                                                       |
        | SendEMail              | <p><br></p><p><img src="../../.gitbook/assets/Image_1047.gif" alt="4"></p>                                                                                                 | Send an e-mail through an SMTP server.                                                                                                                                                                      |
        | SetEMailAdressOfSender | <p><br></p><p><img src="../../.gitbook/assets/Image_1048.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\UtilLibGeteMailAddressOfSender.bmp"></p> | Overwrite configured sender address for e-mails to be transmitted.                                                                                                                                          |
        | SetSMTPServerHostName  | <p><br></p><p><img src="../../.gitbook/assets/Image_1049.gif" alt="3"></p>                                                                                                 | Overwrite configured SMTP server host name.                                                                                                                                                                 |
        | SetTimeScaleFactor     | <p><br></p><p><img src="../../.gitbook/assets/Image_1050.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\UtilLib_Most.bmp"></p>                   | Sets the current time scale factor (float; defaults to 1.0). If the simulation mode is switched on, the time scale factor is used to scale task dependencies and activity durations                         |
        | SetTimerViewName       | <p><br></p><p><img src="../../.gitbook/assets/Image_1051.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\UtilLib_Most.bmp"></p>                   | Sets the view name of the given timer.                                                                                                                                                                      |
        | Sort                   | <p><br></p><p><img src="../../.gitbook/assets/Image_1052.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\UtilLib_Most.bmp"></p>                   | <p>This sort algorithm acts on so called associative arrays (hash), which are built by two arrays.</p><p>One array contains the keys, the other the corresponding values. This function sorts the keys.</p> |

        | Command                | Icon                                                                                                                                                     | Action Performed                                                                                                                                  |
        | ---------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------- |
        | SyncShell              | <p><br></p><p><img src="../../.gitbook/assets/Image_1053.gif" alt="2"></p>                                                                               | Runs an executable (exe, com, bat). This function runs other programs synchronously.                                                              |
        | Unlock                 | <p><br></p><p><img src="../../.gitbook/assets/Image_1054.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\UtilLib_Most.bmp"></p> | Lock() and Unlock() are functions that enclose a series of HSL statements so that a group of HSL statements can be executed without interruption. |
        | UnregisterAbortHandler | <p><br></p><p><img src="../../.gitbook/assets/Image_1055.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\UtilLib_Most.bmp"></p> | Unregisters abortHandler as a custom HSL function called before a method will be aborted                                                          |
        | VerifyCheckSum         | <p><br></p><p><img src="../../.gitbook/assets/Image_1056.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\UtilLib_Most.bmp"></p> | Verifies the checksum value of the specified file.                                                                                                |

        \

    29. #### _‌Utility Library 2‌_

        \


        _The HSL utility library 2 is an extension library to the core HSL utility library._

        _The “Util2:”, “Util2: Debug” and “Util2: Error” Prefixes have all been removed for a better overview._

        \


        | Command                       | Icon                                                                                                                                                     | Action Performed                                                                                                                                                              |
        | ----------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
        | CheckValueType                | <p><br></p><p><img src="../../.gitbook/assets/Image_1057.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\UtilLib_Most.bmp"></p> | Checks a variable to be of a given type.                                                                                                                                      |
        | CheckValueRange               | <p><br></p><p><img src="../../.gitbook/assets/Image_1058.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\UtilLib_Most.bmp"></p> | Checks a variable to be in a given (open) range.                                                                                                                              |
        | CheckValueRangeMinMax         | <p><br></p><p><img src="../../.gitbook/assets/Image_1059.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\UtilLib_Most.bmp"></p> | Checks a variable to be in a given (closed) range.                                                                                                                            |
        | CheckValueTypeAndRange        | <p><br></p><p><img src="../../.gitbook/assets/Image_1060.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\UtilLib_Most.bmp"></p> | Checks a variable to be of a given type and to be in a given (open) range.                                                                                                    |
        | CheckValueTypeAndRange MinMax | <p><br></p><p><img src="../../.gitbook/assets/Image_1061.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\UtilLib_Most.bmp"></p> | Checks a variable to be of a given type and to be in a given (closed) range.                                                                                                  |
        | VarArrCheckIndex              | <p><br></p><p><img src="../../.gitbook/assets/Image_1062.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\UtilLib_Most.bmp"></p> | Generates a runtime error with detailed description if the index is invalid for the given variable array.                                                                     |
        | SeqArrCheckIndex              | <p><br></p><p><img src="../../.gitbook/assets/Image_1063.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\UtilLib_Most.bmp"></p> | Generates a runtime error with detailed description if the index is invalid for the given sequence array.                                                                     |
        | VarArrGetAt                   | <p><br></p><p><img src="../../.gitbook/assets/Image_1064.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\UtilLib_Most.bmp"></p> | Returns a copy of the array element at the given index and raises a runtime error with a detailed description if the specified index is invalid for the given variable array. |
        | SeqArrGetAt                   | <p><br></p><p><img src="../../.gitbook/assets/Image_1065.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\UtilLib_Most.bmp"></p> | Returns a copy of the array element at the given index and raises a runtime error with a detailed description if the specified index is invalid for the given sequence array. |
        | ToString                      | <p><br></p><p><img src="../../.gitbook/assets/Image_1066.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\UtilLib_Most.bmp"></p> | Returns a string that represents the value of a given variable.                                                                                                               |

        | Command                           | Icon                                                                                                                                                     | Action Performed                                                                                      |
        | --------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------- |
        | RoundVolume                       | <p><br></p><p><img src="../../.gitbook/assets/Image_1067.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\UtilLib_Most.bmp"></p> | Rounds the given volume to one decimal place.                                                         |
        | RoundVolumeUp                     | <p><br></p><p><img src="../../.gitbook/assets/Image_1068.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\UtilLib_Most.bmp"></p> | Rounds the given volume up to one decimal place.                                                      |
        | RoundVolumeDown                   | <p><br></p><p><img src="../../.gitbook/assets/Image_1069.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\UtilLib_Most.bmp"></p> | Rounds the given volume down to one decimal place.                                                    |
        | GetLabwarePosXYZ                  | <p><br></p><p><img src="../../.gitbook/assets/Image_1070.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\UtilLib_Most.bmp"></p> | Obtains the position of the given labware item from the Deck Layout using deck coordinates.           |
        | RaiseRuntimeError                 | <p><br></p><p><img src="../../.gitbook/assets/Image_1071.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\UtilLib_Most.bmp"></p> | Raises a runtime error.                                                                               |
        | RaiseRuntimeErrorInclPrevErrDe sc | <p><br></p><p><img src="../../.gitbook/assets/Image_1072.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\UtilLib_Most.bmp"></p> | Raises a runtime error with an error description that includes the description of the previous error. |
        | RaiseLast                         | <p><br></p><p><img src="../../.gitbook/assets/Image_1073.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\UtilLib_Most.bmp"></p> | Re-throws the current runtime error.                                                                  |
        | MakeHxResult                      | <p><br></p><p><img src="../../.gitbook/assets/Image_1074.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\UtilLib_Most.bmp"></p> | Returns an HxResult value given a major ID, a minor ID and an error code.                             |
        | TraceSequence                     | <p><br></p><p><img src="../../.gitbook/assets/Image_1075.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\UtilLib_Most.bmp"></p> | Traces the name, the indexes and all labware and position IDs of the given sequence.                  |
        | TraceSequenceAndData\_1           | <p><br></p><p><img src="../../.gitbook/assets/Image_1076.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\UtilLib_Most.bmp"></p> | Traces the given sequence and additional sequence data.                                               |
        | TraceSequenceAndData\_2           | <p><br></p><p><img src="../../.gitbook/assets/Image_1077.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\UtilLib_Most.bmp"></p> | Traces the given sequence and additional sequence data.                                               |
        | TraceSequencesAndData\_1          | <p><br></p><p><img src="../../.gitbook/assets/Image_1078.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\UtilLib_Most.bmp"></p> | Traces the given sequences and additional sequence data.                                              |
        | TraceSequencesAndData\_2          | <p><br></p><p><img src="../../.gitbook/assets/Image_1079.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\UtilLib_Most.bmp"></p> | Traces the given sequences and additional sequence data.                                              |
        | TraceArray                        | <p><br></p><p><img src="../../.gitbook/assets/Image_1080.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\UtilLib_Most.bmp"></p> | Traces the elements of the given array.                                                               |
        | TraceArray\_2                     | <p><br></p><p><img src="../../.gitbook/assets/Image_1081.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\UtilLib_Most.bmp"></p> | Traces the elements of the given arrays.                                                              |
        | TraceArray\_3                     | <p><br></p><p><img src="../../.gitbook/assets/Image_1082.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\UtilLib_Most.bmp"></p> | Traces the elements of the given arrays.                                                              |
        | TraceArray\_4                     | <p><br></p><p><img src="../../.gitbook/assets/Image_1083.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\UtilLib_Most.bmp"></p> | Traces the elements of the given arrays.                                                              |
        | SetTraceArraySettings             | <p><br></p><p><img src="../../.gitbook/assets/Image_1084.gif" alt="1"></p>                                                                               | Sets the current settings to trace multiple arrays.                                                   |
    30. #### _‌HHS Library‌_

        \


        _The HHS library provides several functions to control the HHS, such as shaking and heating settings. The functions can be integrated into standard methods of the ML STAR instrument._

        _To install the library execute the file “InstallHHSLibrary\_Vx.x.exe”. The file can be obtained from a local Hamilton Representative._

        _After confirming the installation of the addition, the heater shaker library will be installed automatically._

        \


        ![Originalbild anzeigen](../../.gitbook/assets/Image\_1085.jpg)

        _NOTE_

        _The library requires the following Microsoft Package, which will be installed automatically during the setup procedure:_

        _Microsoft Visual C++ 2005 Redistributable Package (x86)._

        \


        | Command                | Icon                                                                                                 | Action Performed                                                                                                                                                                                                                                                                                                    |
        | ---------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
        | Create Star Device     | <p><br></p><p><img src="../../.gitbook/assets/Image_1086.gif" alt="HslMlStarHamHeaterShakerLib"></p> | Creates the device number which must be used as input parameter for each function of this library.                                                                                                                                                                                                                  |
        | Create USB Device      | <p><br></p><p><img src="../../.gitbook/assets/Image_1087.gif" alt="HslHamHeaterShakerLib"></p>       | Creates the device number which must be used as input parameter for each function of this library.                                                                                                                                                                                                                  |
        | Terminate              | <p><br></p><p><img src="../../.gitbook/assets/Image_1088.gif" alt="HslMlStarHamHeaterShakerLib"></p> | The connection to the ML STAR instrument and/or USB device is terminated. Note that this function does not stop the heating or shaking process of the heater shaker.                                                                                                                                                |
        | Start Shaker           | <p><br></p><p><img src="../../.gitbook/assets/Image_1089.gif" alt="HslMlStarHamHeaterShakerLib"></p> | This function starts the shaking process. If necessary, the heater shaker will be initialized. Before the shaking process is started, the plate is locked. Shaking has to be stopped by the “Stop Shaker” Command. Terminating the connection will not stop shaking. However, shaking is stopped upon method abort. |
        | Start All Shaker       | <p><br></p><p><img src="../../.gitbook/assets/Image_1090.gif" alt="HslMlStarHamHeaterShakerLib"></p> | Start shaking on all initialized shakers. Shakers that have not been initialized are not addressed. The plates are locked before the shaking process.                                                                                                                                                               |
        | Start Shaker Timed     | <p><br></p><p><img src="../../.gitbook/assets/Image_1091.gif" alt="HslMlStarHamHeaterShakerLib"></p> | <p>Start shaking for an indicated time. If necessary, the heater shaker will be initialized. Before the shaking process is started, the plate is locked.</p><p>After shaking, the plate lock has to be opened with the “SetPlateLock” Function.</p>                                                                 |
        | Start All Shaker Timed | <p><br></p><p><img src="../../.gitbook/assets/Image_1092.gif" alt="HslMlStarHamHeaterShakerLib"></p> | Start shaking on all initialized heater shakers for an indicated time. The plates are locked before the shaking process. After shaking, the plate lock has to be opened with the “SetPlateLock” Function.                                                                                                           |

        | Command                   | Icon                                                                                                 | Action Performed                                                                                                                                                                                                                                                                                         |
        | ------------------------- | ---------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
        | Wait For Shaker           | <p><br></p><p><img src="../../.gitbook/assets/Image_1093.gif" alt="HslMlStarHamHeaterShakerLib"></p> | Wait for the heater shaker to finish. The plate is unlocked after shaking has been stopped. This command is only used in combination with “Start Shaker Timed” or “Start All Shaker Timed”.                                                                                                              |
        | Stop Shaker               | <p><br></p><p><img src="../../.gitbook/assets/Image_1094.gif" alt="HslMlStarHamHeaterShakerLib"></p> | Stop shaking and unlock plate.                                                                                                                                                                                                                                                                           |
        | Stop All Shaker           | <p><br></p><p><img src="../../.gitbook/assets/Image_1095.gif" alt="HslMlStarHamHeaterShakerLib"></p> | Stop shaking on all heater shakers. The plates will be unlocked subsequently.                                                                                                                                                                                                                            |
        | Set shaker parameter      | <p><br></p><p><img src="../../.gitbook/assets/Image_1096.jpg" alt="HslMlStarHamHeaterShakerLib"></p> | Set shaking parameters, such as shaking direction, shaking speed and acceleration.                                                                                                                                                                                                                       |
        | Get Shaker Parameter      | <p><br></p><p><img src="../../.gitbook/assets/Image_1097.jpg" alt="HslMlStarHamHeaterShakerLib"></p> | Get shaking parameters, such as shaking direction, shaking speed and acceleration.                                                                                                                                                                                                                       |
        | Start Temp Control        | <p><br></p><p><img src="../../.gitbook/assets/Image_1098.gif" alt="HslMlStarHamHeaterShakerLib"></p> | Start temperature control on the heater shaker (must be greater than ambient temperature plus 5°C). Temperature control has to be stopped by the “Stop Temp Control” Function or will be constantly on. Terminating the connection will not stop heating. However, heating is stopped upon method abort. |
        | Wait for Temp Control     | <p><br></p><p><img src="../../.gitbook/assets/Image_1099.gif" alt="HslMlStarHamHeaterShakerLib"></p> | Wait until the heater shaker has reached the set temperature. This function will wait until the defined temperature is reached and is stable for 180 seconds. Only then, the method will continue.                                                                                                       |
        | Stop Temp Control         | <p><br></p><p><img src="../../.gitbook/assets/Image_1100.gif" alt="HslMlStarHamHeaterShakerLib"></p> | Stop temperature control of the heater shaker.                                                                                                                                                                                                                                                           |
        | Get Temperature           | <p><br></p><p><img src="../../.gitbook/assets/Image_1101.jpg" alt="HslMlStarHamHeaterShakerLib"></p> | Receive the current temperature of the heater shaker.                                                                                                                                                                                                                                                    |
        | Set Temperature Parameter | <p><br></p><p><img src="../../.gitbook/assets/Image_1102.jpg" alt="HslMlStarHamHeaterShakerLib"></p> | Set parameters for temperature control. In most cases, the default settings can be used and this function is not needed.                                                                                                                                                                                 |
        | Get Temperature Parameter | <p><br></p><p><img src="../../.gitbook/assets/Image_1103.jpg" alt="HslMlStarHamHeaterShakerLib"></p> | Receive the parameters for temperature control.                                                                                                                                                                                                                                                          |
        | Get Temperature State     | <p><br></p><p><img src="../../.gitbook/assets/Image_1104.jpg" alt="HslMlStarHamHeaterShakerLib"></p> | Get the status of the temperature control. The temperature should be within a defined temperature range.                                                                                                                                                                                                 |
        | Send Firmware Command     | <p><br></p><p><img src="../../.gitbook/assets/Image_1105.jpg" alt="HslMlStarHamHeaterShakerLib"></p> | Send a firmware command to the heater shaker.                                                                                                                                                                                                                                                            |

        | Command              | Icon                                                                                                 | Action Performed                                                                                                                                                                                                                                                                                                                                                               |
        | -------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
        | Set Plate Lock       | <p><br></p><p><img src="../../.gitbook/assets/Image_1106.gif" alt="HslMlStarHamHeaterShakerLib"></p> | Open or close the plate lock. The plate is always locked automatically before shaking is started, but this command is useful to position and fix the plate in the center of the flat bottom adapter before pipetting, or when using the commands “Start Shaker Timed” or “Start All Shaker Timed” as these commands do not open the plate lock after shaking.                  |
        | Set Simulation       | <p><br></p><p><img src="../../.gitbook/assets/Image_1107.gif" alt="HslMlStarHamHeaterShakerLib"></p> | Set run mode to simulation for all functions in this library. In simulation mode, no signals are sent to the HHS.                                                                                                                                                                                                                                                              |
        | Set USB Trace        | <p><br></p><p><img src="../../.gitbook/assets/Image_1108.gif" alt="HslMlStarHamHeaterShakerLib"></p> | Turn on/off tracing of communication to and from USB port.                                                                                                                                                                                                                                                                                                                     |
        | Begin Monitoring     | <p><br></p><p><img src="../../.gitbook/assets/Image_1109.gif" alt="HslHamHeaterShakerLib"></p>       | Start to monitor the performance of the HHS. This function monitors the temperature and speed in the background. The tolerated range of the temperature can be set with the function “SetTempParameter”. The tolerated range of speed is defined in this function. The status of the temperature can be requested in a defined interval and is then written to the trace file. |
        | End Monitoring       | <p><br></p><p><img src="../../.gitbook/assets/Image_1110.jpg" alt="HslHamHeaterShakerLib"></p>       | Get the shaking speed of a HHS.                                                                                                                                                                                                                                                                                                                                                |
        | Get Shaker Speed     | <p><br></p><p><img src="../../.gitbook/assets/Image_1111.gif" alt="HslHamHeaterShakerLib"></p>       | Get the shaking speed of a HHS.                                                                                                                                                                                                                                                                                                                                                |
        | Get Serial Number    | <p><br></p><p><img src="../../.gitbook/assets/Image_1112.gif" alt="HslHamHeaterShakerLib"></p>       | Get the serial number a HHS.                                                                                                                                                                                                                                                                                                                                                   |
        | Get Firmware Version | <p><br></p><p><img src="../../.gitbook/assets/Image_1113.gif" alt="HslHamHeaterShakerLib"></p>       | Get the firmware version of a HHS.                                                                                                                                                                                                                                                                                                                                             |
    31. #### _‌HSL VacuumBrandPump / ML STAR BVS Library‌_

        \


        _The ML STAR BVS Library allows controlling up to four BVS / CVS units simultaneously. There are two categories of functions provided:_

        _High Level Functions_

        _The high level functions control the whole vacuum process including tracking of the vacuum action to the Hamilton Database._

        _The use of HighLevelFunctions is recommended. High level functions have the prefix HSLStarBVSLib._

        \


        ![Originalbild anzeigen](../../.gitbook/assets/Image\_1114.gif)

        _NOTE_

        _The BVS Library can also be used for CVS._

        \

    32. #### _‌Low Level Functions‌_

        \


        _These functions reflect the command set of the “BVS pump controller” directly. These commands are old and are not recommended to be used anymore._

        _Low level functions have the prefix HSLVacuuBrandPump._

        \


        | Command               | Icon                                                                                                                                                              | Action Performed                                                                                             |
        | --------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------ |
        | BVSAbort              | <p><br></p><p><img src="../../.gitbook/assets/Image_1115.jpg" alt="BVS_Abort"></p>                                                                                | This function is used to stop all pump units and shut down their connections in an abort handler.            |
        | BVSGetAmbientPressure | <p><br></p><p><img src="../../.gitbook/assets/Image_1116.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\BVSgetAmbientPressure.bmp"></p> | Returns the ambient pressure measured with the specified pump unit.                                          |
        | BVSGetSimulationMode  | <p><br></p><p><img src="../../.gitbook/assets/Image_1117.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\BVSGetSimulationMode.bmp"></p>  | Returns whether simulation mode is set for the specified BVS / CVS or not.                                   |
        | BVSInitialize         | <p><br></p><p><img src="../../.gitbook/assets/Image_1118.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\BVSInitialize.bmp"></p>         | Initializes the connection to the specified BVS / CVS.                                                       |
        | BVSSetSimulationMode  | <p><br></p><p><img src="../../.gitbook/assets/Image_1119.gif" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\BVSsetSimulationMode.bmp"></p>  | Sets the specified BVS / CVS to simulation mode.                                                             |
        | BVSTerminate          | <p><br></p><p><img src="../../.gitbook/assets/Image_1120.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\BVSTerminate.bmp"></p>          | Closes the connection to the specified BVS / CVS.                                                            |
        | BVSTrack              | <p><br></p><p><img src="../../.gitbook/assets/Image_1121.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\BVSTrack.bmp"></p>              | Tracks a BVS / CVS volume move to the database.                                                              |
        | BVSVacuum             | <p><br></p><p><img src="../../.gitbook/assets/Image_1122.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\BVSvacuum.bmp"></p>             | Runs the vacuum process on the specified BVS / CVS.                                                          |
        | BVSVacuumTrack        | <p><br></p><p><img src="../../.gitbook/assets/Image_1123.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\BVSvacuumTrack.bmp"></p>        | <p>Runs the vacuum process on the specified BVS / CVS.</p><p>The volume move is tracked to the Database.</p> |

        | Command                | Icon                                                                                                                                                               | Action Performed                                                                                                                                                              |
        | ---------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
        | Initialize             | <p><br></p><p><img src="../../.gitbook/assets/Image_1124.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\BVS__Initialize.bmp"></p>        | Using this function the communication port will be initialized. The pumping unit will be requested for errors to ensure the communication works.                              |
        | OpenAirAdmittanceValve | <p><br></p><p><img src="../../.gitbook/assets/Image_1125.gif" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\OpenAirAdmittanceValve.bmp"></p> | Allows opening the air admittance valve.                                                                                                                                      |
        | ReqActualPressure      | <p><br></p><p><img src="../../.gitbook/assets/Image_1126.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\ReqActualPRessure.bmp"></p>      | Requests the actual pressure in the system and the measured value will be returned.                                                                                           |
        | StartPressureControl   | <p><br></p><p><img src="../../.gitbook/assets/Image_1127.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\StartPressureControl.bmp"></p>   | Prepares the pumping control unit for a pressure controlled execution of the pump and starts the pump.                                                                        |
        | StopPumpImmediately    | <p><br></p><p><img src="../../.gitbook/assets/Image_1128.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\StopPumpImmediately.bmp"></p>    | <p>A running pump started with the function StartPressureControl() can be stopped immediately</p><p>at any time calling this function.</p>                                    |
        | Terminate              | <p><br></p><p><img src="../../.gitbook/assets/Image_1129.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\Terminate.bmp"></p>              | Releases system resources occupied by the function Initialize().                                                                                                              |
        | WaitForPumpStopped     | <p><br></p><p><img src="../../.gitbook/assets/Image_1130.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\WaitForPumpStopped.bmp"></p>     | This function allows synchronization of pumping action and other actions which can be executed after the pump was started with a call of the function StartPressureControl(). |

        \


        ![Originalbild anzeigen](../../.gitbook/assets/Image\_1131.gif)

        _NOTE_

        _Do not mix high level functions and low level functions in the same method. Make sure to specify the library name._

        \

    33. #### _‌Vector Database Tracking Library‌_

        \


        _The HSL database tracking library allows accessing and manipulating tracking data in the database._

        _The prefixes “VectorDB\_Deck:”, “VectorDB\_Labware:”, “VectorDB\_LabwareType:”, “VectorDB\_Run:”, “VectorDB\_Experiment:” and “VectorDB\_TrackAction:” have all been removed for a better overview._

        \


        | Command                    | Icon                                                                                                                                                             | Action Performed                                                          |
        | -------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------- |
        | AssignLabwareToJob         | <p><br></p><p><img src="../../.gitbook/assets/Image_1132.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\VectorDbTracking_all.bmp"></p> | Assigns the given job to the given labware.                               |
        | AssignLoadedLabware ToJobs | <p><br></p><p><img src="../../.gitbook/assets/Image_1133.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\VectorDbTracking_all.bmp"></p> | Assigns labware loaded on given deck to corresponding 'Unprocessed' jobs. |
        | GetDeckID                  | <p><br></p><p><img src="../../.gitbook/assets/Image_1134.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\VectorDbTracking_all.bmp"></p> | Retrieves the deck ID given an instrument name.                           |
        | GetDeckID2                 | <p><br></p><p><img src="../../.gitbook/assets/Image_1135.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\VectorDbTracking_all.bmp"></p> | Retrieves the deck ID given an instrument.                                |

        | Command                               | Icon                                                                                                                                                             | Action Performed                                                                                 |
        | ------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------ |
        | GetAllLabwareOnDeck                   | <p><br></p><p><img src="../../.gitbook/assets/Image_1136.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\VectorDbTracking_all.bmp"></p> | Retrieves all loaded labware given a deck ID.                                                    |
        | IsLabwareLoaded                       | <p><br></p><p><img src="../../.gitbook/assets/Image_1137.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\VectorDbTracking_all.bmp"></p> | Returns the ID of the labware if the labware is loaded at the given position on the given deck.  |
        | IsLabwareLoadedByLabwareIdPo sitionId | <p><br></p><p><img src="../../.gitbook/assets/Image_1138.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\VectorDbTracking_all.bmp"></p> | Returns the ID of the labware if the labware is loaded at the given position on the given deck.  |
        | IsBarcodeLoaded                       | <p><br></p><p><img src="../../.gitbook/assets/Image_1139.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\VectorDbTracking_all.bmp"></p> | Returns the ID of the labware with the given barcode if the barcode is loaded on the given deck. |
        | GetElementID                          | <p><br></p><p><img src="../../.gitbook/assets/Image_1140.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\VectorDbTracking_all.bmp"></p> | Retrieves the ElementID given a labware access name.                                             |
        | GetElementIDByDeckIDLabwareI d        | <p><br></p><p><img src="../../.gitbook/assets/Image_1141.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\VectorDbTracking_all.bmp"></p> | Retrieves the ElementID for the given labware and deck.                                          |
        | GetElementIDByDeckIDLabwareI d        | <p><br></p><p><img src="../../.gitbook/assets/Image_1142.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\VectorDbTracking_all.bmp"></p> | Retrieves the ElementID for the given labware and deck.                                          |
        | GetLabwareLoadingTime                 | <p><br></p><p><img src="../../.gitbook/assets/Image_1143.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\VectorDbTracking_all.bmp"></p> | Retrieves the labware loading time given a labware access name.                                  |
        | GetLabwareLoadingTimeByElem entID     | <p><br></p><p><img src="../../.gitbook/assets/Image_1144.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\VectorDbTracking_all.bmp"></p> | Retrieves the labware loading time on given deck for given labware.                              |
        | GetLabware                            | <p><br></p><p><img src="../../.gitbook/assets/Image_1145.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\VectorDbTracking_all.bmp"></p> | Retrieves labware details information given a labware access name.                               |
        | GetLabwareByElementID                 | <p><br></p><p><img src="../../.gitbook/assets/Image_1146.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\VectorDbTracking_all.bmp"></p> | Retrieves labware details information given an element ID.                                       |
        | GetLabwareBarcode                     | <p><br></p><p><img src="../../.gitbook/assets/Image_1147.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\VectorDbTracking_all.bmp"></p> | Retrieves the barcode given a labware access name.                                               |
        | GetLabwareBarcodeByElementID          | <p><br></p><p><img src="../../.gitbook/assets/Image_1148.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\VectorDbTracking_all.bmp"></p> | Retrieves the barcode given an element ID.                                                       |
        | GetLabwareVolume                      | <p><br></p><p><img src="../../.gitbook/assets/Image_1149.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\VectorDbTracking_all.bmp"></p> | Retrieves the volume given a labware access name.                                                |
        | GetLabwareVolumeByElementID           | <p><br></p><p><img src="../../.gitbook/assets/Image_1150.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\VectorDbTracking_all.bmp"></p> | Retrieves the volume given an element ID.                                                        |
    34. #### _‌Vector Database Worklist Management Library‌_

        \


        _The HSL vector database worklist management library allows accessing and manipulating worklist data in the vector database._

        _The “VectorDB” Prefix has been removed for a better overview._

        \


        | Command                              | Icon                                                                                                                                                             | Action Performed                                                                                  |
        | ------------------------------------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------- |
        | AddJob                               | <p><br></p><p><img src="../../.gitbook/assets/Image_1151.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\VectorDbTracking_all.bmp"></p> | Adds a new job to the vector database.                                                            |
        | AddJobAdditionalData                 | <p><br></p><p><img src="../../.gitbook/assets/Image_1152.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\VectorDbTracking_all.bmp"></p> | Adds additional data for the specified job to the vector database.                                |
        | RemoveJob                            | <p><br></p><p><img src="../../.gitbook/assets/Image_1153.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\VectorDbTracking_all.bmp"></p> | Removes the specified job from the vector database.                                               |
        | RemoveJobAdditionalData              | <p><br></p><p><img src="../../.gitbook/assets/Image_1154.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\VectorDbTracking_all.bmp"></p> | Removes additional data for the specified job from the vector database.                           |
        | RemoveAllJobs                        | <p><br></p><p><img src="../../.gitbook/assets/Image_1155.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\VectorDbTracking_all.bmp"></p> | Removes all jobs (including additional data) that match the given state from the vector database. |
        | GetJobs                              | <p><br></p><p><img src="../../.gitbook/assets/Image_1156.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\VectorDbTracking_all.bmp"></p> | Returns information about all jobs in the vector database that match the given job state.         |
        | GetJobIDs                            | <p><br></p><p><img src="../../.gitbook/assets/Image_1157.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\VectorDbTracking_all.bmp"></p> | Returns all job IDs that match the given filter in the given sort order.                          |
        | GetJob                               | <p><br></p><p><img src="../../.gitbook/assets/Image_1158.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\VectorDbTracking_all.bmp"></p> | Returns information about the specified job from the vector database.                             |
        | GetJobAdditionalData                 | <p><br></p><p><img src="../../.gitbook/assets/Image_1159.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\VectorDbTracking_all.bmp"></p> | Returns information about the additional data for the specified job from the vector database.     |
        | GetJobsSortedByPriority              | <p><br></p><p><img src="../../.gitbook/assets/Image_1160.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\VectorDbTracking_all.bmp"></p> | Returns information about all jobs in the vector database that match the given criteria.          |
        | GetJobsForLabware                    | <p><br></p><p><img src="../../.gitbook/assets/Image_1161.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\VectorDbTracking_all.bmp"></p> | Returns information about all jobs in the vector database that match the given criteria.          |
        | GetJobsForLabware SortedByPriority   | <p><br></p><p><img src="../../.gitbook/assets/Image_1162.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\VectorDbTracking_all.bmp"></p> | Returns information about all jobs in the vector database that match the given criteria.          |
        | GetJobsForBarcode                    | <p><br></p><p><img src="../../.gitbook/assets/Image_1163.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\VectorDbTracking_all.bmp"></p> | Returns information about all jobs in the vector database that match the given barcode criteria.  |
        | GetJobsForBarcode SortedByPriority   | <p><br></p><p><img src="../../.gitbook/assets/Image_1164.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\VectorDbTracking_all.bmp"></p> | Returns information about all jobs in the vector database that match the given priority criteria. |
        | GetJobsForElementID                  | <p><br></p><p><img src="../../.gitbook/assets/Image_1165.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\VectorDbTracking_all.bmp"></p> | Returns information about all jobs in the vector database that match the given element criteria.  |
        | GetJobsForElementID SortedByPriority | <p><br></p><p><img src="../../.gitbook/assets/Image_1166.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\VectorDbTracking_all.bmp"></p> | Returns information about all jobs in the vector database that match the given criteria.          |
        | GetJobState                          | <p><br></p><p><img src="../../.gitbook/assets/Image_1167.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\VectorDbTracking_all.bmp"></p> | Gets the state of the specified job from the vector database.                                     |

        | Command                | Icon                                                                                                                                                             | Action Performed                                                  |
        | ---------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------- |
        | SetJobState            | <p><br></p><p><img src="../../.gitbook/assets/Image_1168.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\VectorDbTracking_all.bmp"></p> | Sets the state of the specified job in the vector database.       |
        | RemoveJobsForLabware   | <p><br></p><p><img src="../../.gitbook/assets/Image_1169.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\VectorDbTracking_all.bmp"></p> | Removes information about all jobs that match the given criteria. |
        | RemoveJobsForBarcode   | <p><br></p><p><img src="../../.gitbook/assets/Image_1170.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\VectorDbTracking_all.bmp"></p> | Removes information about all jobs that match the given criteria. |
        | RemoveJobsForElementID | <p><br></p><p><img src="../../.gitbook/assets/Image_1171.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\VectorDbTracking_all.bmp"></p> | Removes information about all jobs that match the given criteria. |

        \

    35. #### _‌Data Handling Steps‌_

        \


        _Data handling steps are standard procedures for data and file handling._

        _The data handling steps have to be activated by clicking on “Method  Instrument and Smart Steps…”_

        \


        | Command             | Icon                                                                                                                                                             | Action Performed                                                              |
        | ------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------- |
        | GenerateMappingFile | <p><br></p><p><img src="../../.gitbook/assets/Image_1172.gif" alt="3"></p>                                                                                       | Creates mapped report file(s) for labware within a method run.                |
        | SetLabwareBarcode   | <p><br></p><p><img src="../../.gitbook/assets/Image_1173.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\BtnSetLabwareBarcode.bmp"></p> | Set the barcode for a labware within the sample tracking database.            |
        | RemoveLabware       | <p><br></p><p><img src="../../.gitbook/assets/Image_1174.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\BtnRemoveLabware.bmp"></p>     | Removes labware from the access of sample tracking.                           |
        | ImportWorklist      | <p><br></p><p><img src="../../.gitbook/assets/Image_1175.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\BtnImportWorklist.bmp"></p>    | Imports worklist data from files into the vector database.                    |
        | UpdateJobStatus     | <p><br></p><p><img src="../../.gitbook/assets/Image_1176.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\BtnUpdateJobStatus.bmp"></p>   | Set the job status of a sample contained in the worklist data to ‘Processed’. |



\


