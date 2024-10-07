# Loading Labware / Labware Handling

1.  ## _Loading Labware‌_

    _There are two options to load labware on the deck: Autoload and manual load. In both cases, always have the needed carriers ready. The following table shows the possible course of action:_

    \


    | Method contains “Load Carrier” Commands | <p><br></p><p>Autoload Instrument</p>                                                                                                                                                                                          | <p><br></p><p>Manual Load Instrument</p>                                                                       |
    | --------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | -------------------------------------------------------------------------------------------------------------- |
    | Yes                                     | <p>Run the method.</p><p>Insert carriers in the tracks of the Autoload tray where indicated by LEDs.</p><p>Click “Load” in the dialog.</p><p>Possibility to manipulate sequences.</p><p>Carriers are loaded automatically.</p> | <p>Run the method.</p><p>The instrument will prompt a message to load the carriers manually onto the deck.</p> |
    | No                                      | <p>Load the carriers manually into their positions on the deck.</p><p>Run the method.</p>                                                                                                                                      | <p>Load the carriers manually into their positions on the deck.</p><p>Run the method.</p>                      |

    \


    ![Originalbild anzeigen](../.gitbook/manual-images/assets/Image\_1476.jpg)

    _NOTE_

    _If no “Load carrier” Commands are specified in the method, no checking of carrier presence is possible._

    1.  ### _‌Autoload‌_

        \


        _When using the Autoload option, make sure to load the carriers with the appropriate labware first._

        \


        _With “Load Carrier” Commands in the method_

        1.  _If the “Load Carrier” Commands have been incorporated into the method: start the “Run Screen” as described in the following sections, and run the method._

            _The correct positions for the insertion of carriers will be highlighted by the green LEDs._

            ![image](../.gitbook/manual-images/assets/Image\_1477.png)

            _Autoload Tray_

_Stop Hooks_

1.  _Insert the carriers into the tracks of the Autoload tray until they touch the stop hooks on the far side of the tray._

    _These pictures are made from the rear of the instrument._
2. _Click \[Load] in the dialog._

_The carriers are loaded onto the deck automatically by the “Load Carrier” Command in the method. At the same time, the barcodes of carriers and labware are read and stored in a file._

\


![Originalbild anzeigen](../.gitbook/manual-images/assets/Image\_1478.jpg)

_NOTE_

_If “Sample Tracking” is enabled (in the system configuration editor), the barcodes will be written to the Database._

\


_Another way for loading is to place the carriers onto the defined positions of the Autoload tray before starting the method. Loading and barcode reading will then be performed without user input._

\


_Without “Load Carrier” Commands in the method_

1. _If there have been no “Load Carrier” Commands incorporated into the method, the carriers must be loaded manually into the positions on the deck defined in the Deck Layout before the run is started._
2. _Make sure that the carriers are inserted completely, until they touch the rear connectors._
3.
   1.  ### _‌Manual Load‌_

       \


       _In order to load the ML STAR, fill the carriers with the appropriate labware first._

       \


       _With “Load Carrier” Commands in the Method_

       1. _If the “Load Carrier” Commands have been incorporated into the method, start the run. The instrument will prompt a message to load the carriers manually onto the deck._
       2. _Make sure the carriers are inserted completely, until they lock in the rear snaps. A magnetic sensor checks whether the carriers have been loaded correctly._

       \


       ![image](../.gitbook/manual-images/assets/Image\_1479.png)

       \


       _Magnetic pill at the carrier triggers the hall sensor of the carrier presence sensor board_

_Without “Load Carrier” Commands in the Method_

1. _If there have been no “Load Carrier” Commands incorporated into the method, load the carriers manually into the positions on the deck defined in the Deck Layout before the run is started._
2. _Make sure that the carriers are inserted completely, until they touch the rear snaps._

\


1.
   1.  ### _‌Command Description‌_

       \


       _The following tables give a brief overview of the available ML STAR-specific loading commands._

       1.  #### _‌Single Steps‌_

           \


           <table data-header-hidden><thead><tr><th width="150"></th><th></th><th></th></tr></thead><tbody><tr><td>Preparation</td><td></td><td></td></tr><tr><td>Command</td><td>Icon</td><td>Action Performed</td></tr><tr><td>Load Carrier</td><td><p><br></p><p><img src="../.gitbook/manual-images/assets/Image_1480.jpg" alt="NewIMAGES/loadcarrier.bmp"></p></td><td>Load a carrier on the deck.</td></tr><tr><td>Unload Carrier</td><td><p><br></p><p><img src="../.gitbook/manual-images/assets/Image_1481.jpg" alt="NewIMAGES/UnloadCarrier.bmp"></p></td><td>Unload a carrier from the deck.</td></tr><tr><td>Reload carrier</td><td><p><br></p><p><img src="../.gitbook/manual-images/assets/Image_1482.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\ReloadCarrier.bmp"></p></td><td>Used to load, unload or reload a carrier.</td></tr><tr><td>Lock/Unlock Front Cover</td><td><p><br></p><p><img src="../.gitbook/manual-images/assets/Image_1483.jpg" alt="NewIMAGES/LockFrontCover.bmp"></p></td><td>Locks/unlocks the front cover.</td></tr><tr><td>Initialize</td><td><p><br></p><p><img src="../.gitbook/manual-images/assets/Image_1484.jpg" alt="NewIMAGES/BtnInitialize.bmp"></p></td><td>Initialize the instrument.</td></tr><tr><td>Move Auto Load</td><td><p><br></p><p><img src="../.gitbook/manual-images/assets/Image_1485.jpg" alt="NewIMAGES/cmdmoveautoload.bmp"></p></td><td>Moves the autoload to a selected track number.</td></tr><tr><td>Calibrate Carrier</td><td><p><br></p><p><img src="../.gitbook/manual-images/assets/Image_1486.jpg" alt="NewIMAGES/btncalibrate.bmp"></p></td><td>Calibrate precise position of a high-density Microplate (1536 wells) before asp/disp.</td></tr></tbody></table>

           \

       2.  #### _‌Smart Steps‌_

           \


           | ML\_STAR Smart Steps  |                                                                                                                                                       |                                                                                                                                                                                              |
           | --------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
           | Command               | Icon                                                                                                                                                  | Action performed                                                                                                                                                                             |
           | Advanced Load setting | <p><br></p><p><img src="../.gitbook/manual-images/assets/Image_1487.jpg" alt="AdvSet"></p>                                                                          | Define other settings than the default of the load steps.                                                                                                                                    |
           | Load                  | <p><br></p><p><img src="../.gitbook/manual-images/assets/Image_1488.jpg" alt="NewIMAGES/btnload.jpg"></p>                                                           | Load carrier on deck.                                                                                                                                                                        |
           | Unload                | <p><br></p><p><img src="../.gitbook/manual-images/assets/Image_1489.jpg" alt="NewIMAGES/btnunload.jpg"></p>                                                         | Remove carrier from deck.                                                                                                                                                                    |
           | Load and match        | <p><br></p><p><img src="../.gitbook/manual-images/assets/Image_1490.jpg" alt="I:\Documents\Kunden\Hamilton\scharfeVersionProgMan\ProgmanPics\LoadAndMatch.bmp"></p> | Load samples and match loading information with worklist information, to generate data for use in the following process steps. An “Import Worklist” must be performed prior to this command. |

           \

   2.  ### _‌Barcode Reading / Identification‌_

       \


       _Carriers, containers, racks and tip racks can be identified by a barcode. The reader device scanning the barcodes is mounted on the Autoload slide. The system must allow specification of ranges (barcode mask) for plausibility checking of barcode information._

       1.  #### _‌Supported Barcode Types‌_

           \


           _The following bar code abbreviations can be read by the Autoload Option:_

           * _ISBT standard_
           * _Code 128 (subset B and C)_
           * _Code 39_
           * _Codabar_
           * _Code 2 of 5 Interleaved_
           * _UPC A/E_
           * _JAN/EAN8_

           \


           _The barcodes to be read can be enabled through the “Tools  System Configuration Editor _

           _ML STAR” Menu section._

           \


           ![image](../.gitbook/manual-images/assets/Image\_1491.jpg)

           \


           ![Originalbild anzeigen](../.gitbook/manual-images/assets/Image\_1492.jpg)

           _NOTE_

           _Enable only barcode types which will be used on the system. Disabling the unused barcode types will improve the reliability of the readings._

           \

       2.  #### _‌Unique Barcodes‌_

           \


           _The unique barcode check controls if a barcode has already been used on the system. To use this function, four settings must be made:_

           1. _Activate sample tracking._
           2. _Specify the unique barcode check mode._
           3. _Specify the duration of the check period._
           4. _Set the unique barcode flag on the desired labware positions._

           _As soon as the unique barcode checking is set to “Track only” or “Check and Track”, all read barcodes will be written to the data base with a timestamp (when it was loaded)._

           _Every load step will now refer to this database and check if the barcode has been loaded during the specified check duration._

           \


           _Activate Sample Tracking_

           _To use the Unique barcode check, Sample Tracking must be set to “ON” in the “System Configuration Editor  System Settings”:_

           \


           ![image](../.gitbook/manual-images/assets/Image\_1493.jpg)

           \


           _Specify the “Unique Barcode check” Mode:_

           _“OFF” Mode_

           _Unique barcode management is switched off. Meaning, no check for unique barcodes, no writing to the database will be done._

           _“Track only” Mode_

           _Unique barcode check will be turned on partially. Barcodes and timestamp are added to the database to be checked in the future, but no checks are performed. If the barcode has been loaded previously, the timestamp will be updated. Meaning there will be writing but not checking of barcodes._

           _“Check and Track” Mode_

           _Unique barcode check operation is fully turned on. If a barcode is presented a second time within the specified unique barcode duration, a warning is invoked that this barcode has been loaded previously. Meaning it will write at the same time check barcodes._

           _Specify the Unique Barcode Duration_

           _Click the \['...'] Button if unique barcode duration is selected, to open a wizard which allows specification of the duration parameter._

           *   _Current run: Barcodes must be unique within the current run._

               \


               ![image](../.gitbook/manual-images/assets/Image\_1494.gif)
           * _Time in hours: Duration in hours within a barcode must be unique._

           \


           ![image](../.gitbook/manual-images/assets/Image\_1495.gif)

           \


           _Set the Unique Barcode Check Flag on the Labware:_

           1.  _Open the Context Menu of the specified labware in the Deck Layout (right mouse-click)._

               \


               ![image](../.gitbook/manual-images/assets/Image\_1496.jpg)

               \


               _To make the sample carrier barcode itself unique, tick the “Barcode must be unique” Checkbox underneath the barcode mask. Now, the carrier barcode will be controlled at every load step._

               \


               ![image](../.gitbook/manual-images/assets/Image\_1497.jpg)
           2.  _To set barcodes on the tubes as unique, select the \[By Position…] Tab._

               _In the example shown below, there are two barcodes that should not be checked for distinction. Every barcode in position 1 and 2 is allowed to appear multiple times, but the barcode mask for these barcodes must be correct._

               \


               ![12-12-2012 14-08-11](../.gitbook/manual-images/assets/Image\_1498.png)

               \

           3. _All other positions are marked as “Unique” in the right most column. This will enable the checking for unique barcodes (as long as all other settings are appropriate)._
           4. _To mark all barcodes for checking, check the “Barcode must be unique” Checkbox. Select all positions and click the \[Apply to selected positions] Tab._

           _Behavior at Runtime_

           _During runtime, two errors can be raised:_

           \


           | First load                     | Second Load                    | Error                      |
           | ------------------------------ | ------------------------------ | -------------------------- |
           | Unique flag on Labware not set | Unique flag on Labware not set | No error                   |
           | Unique flag on Labware not set | Unique flag on Labware set     | Barcode Not Unique Error   |
           | Unique flag on Labware set     | Unique flag on Labware set     | Barcode Not Unique Error   |
           | Unique flag on Labware set     | Unique flag on Labware not set | Barcode Already Used Error |

           _This table is true for “Check and Track” when activated within same run or within specified check unique barcode period or when presenting a barcode multiple times._

           _Barcode Not Unique Error_

           \


           ![image](../.gitbook/manual-images/assets/Image\_1499.jpg)

           \


           _Barcode Already Used Error_

           \


           ![image](../.gitbook/manual-images/assets/Image\_1500.jpg)
