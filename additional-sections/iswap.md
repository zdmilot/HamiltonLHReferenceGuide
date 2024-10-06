# iSWAP

1.  ### _‌Plate Handling with iSWAP‌_

    \


    ![image](../.gitbook/assets/Image\_1501.png)

    _iSWAP (internal Swivel Arm Plate Handler) is a robotic arm that transports microplates, covers of microplates, archive plates or filter plates used for the vacuum box to and from positions on the deck of ML STAR._

    _Like the ML STAR pipetting channels, the iSWAP has a “Traverse height” of 145 mm above the deck (245 mm above the origin)._

    \


    1.  #### _‌iSWAP Geometry‌_

        \


        ![image](../.gitbook/assets/Image\_1502.png)

        _138 mm_

        _iSWAP gripper with clamps_

        _A1_

        _72 - 106 mm_

        _Rectangular rack (i.e. MTP)_

        _+180°_

        \


        _+Y_

        _8 mm_

        _+X_

        _138 mm_

        _30.5 mm_

        _89 mm_

        _35 mm_

        _≤ 33 mm_

        _13 mm_

        _maximum 1 mm_

        _+Z_

        _24 mm_

        _vertical range for gripped rack_

        _153 mm_

        _≤ 35 mm_

        _(horizontal) barcode_

        _reading range_

        _+X_

        _iSWAP arm (swivel-mounted by ± 90°)_

        _Reference point for x- and y-movement of iSWAP_

        _Reference point for iSWAP_

_iSWAP hand (field of traverse - 90° /+180, relative to the arm)_

_Geometrical definitions of iSWAP_

![Originalbild anzeigen](../.gitbook/assets/Image\_1503.jpg)

_NOTE_

_Height for gripping is calculated from the upper rim of the plate. Recommended gripping height for MTP: 3 mm_

_Recommended gripping height for DWP: 13 mm_

_(an error will appear if there is an attempt to grip a Deep Well Plate with a grip height < 10mm traverse height)._

\


1.
   1.
      1.  #### _‌Special iSWAP Features‌_

          \


          _Among the special features of iSWAP are:_

          * _A torque sensor which signals to the robot how tightly it is gripping a labware object._
          * _The plates can be placed in landscape or portrait orientation._
          * _Load and unload plates to and from a plate stacker on the left side of the instrument outside the working area (with some restrictions, this can also be done on the right side)._
          * _Handling plates 100mm below the deck (if iSWAP Rev. ≥ 03. E.g. possible on the ML STARplus without deck extension)._

          _Not all features are available on the old iSwap Type._

          \


          ![Originalbild anzeigen](../.gitbook/assets/Image\_1504.jpg)

          _NOTE_

          _Gripping of microplates in landscape orientation is only possible with the Landscape iSWAP P/N 190220._

          _Use the “Hamilton System Configuration Editor” to enable the functions of the “Landscape” iSWAP: ML STAR / Simulator configuration / iSWAP / “Large Gripper”._

          \

      2.  #### _‌iSWAP Positions‌_

          \


          _The iSWAP is mounted on the pipetting arm of the ML STAR._

          _During pipetting, the iSWAP is in park position and does not affect the movement of the pipetting channels._

          _For plate transport steps, the pipetting tools will be moved away so that the greatest possible transport area will be available to the iSWAP. The orientation of the arm and gripper will be automatically calculated by the software according to the Deck Layout and programmed grip direction._

          _Using multi-arm systems can affect the movement range._

          \

      3.  #### _‌Grip and Opening Widths‌_

          \


          _“Grip width” and “opening width before access” can vary between 72 and 108 (132) mm._

          _Archive and filter plates in particular have to be gripped no more than 28 mm below the upper rim. The lower rim of the plate should be no more than 35 mm below the gripping position, to prevent collision with other labware placed on the deck._
      4.  #### _‌Grip Force‌_

          \


          _The default grip force is appropriate for common MTPs. It should be set higher for archive plates, and lower for soft plates._

          \


          ![image](../.gitbook/assets/Image\_1505.png)

          _ATTENTION_

          _In order to prevent spillage during transport with iSWAP, it is recommended not to overfill the wells (e.g. fill maximum 80 % of nominal well volume)._

          _The maximum weight to be transported is 300 g. This should not be exceeded._

          _The rectangular racks should only be lifted from or placed onto carriers with slide guides (see the ML STAR Line Operator’s Manual)._

          \


          ![image](../.gitbook/assets/Image\_1506.png)

          _The gripping area should be flat and stable. Ensure that the gripper's clamps will not pick up strips instead, the lower part of the plate's frame._

          _Define the correct plate orientation to ensure that plates lifted from MTP stacks via iSWAP can be identified on deck._

          _Affix plate barcodes correctly (see Technical  Specifications  in  the Microlab STAR Line Operator’s Manual)._

          \

      5.  #### _‌Pick-up by iSWAP‌_

          \


          _Rectangular racks are always picked up at the short side. The gripper has a preferred gripping direction, which can be modified within the advanced settings of the “GetPlate” and “iSwapTransport” Steps._

          \

      6.  #### _‌iSWAP Movement‌_

          \


          _In the case of a complex movement used to transport plates to or from stacks, shelves, etc., a plate once picked up will be moved up in small steps to the lift-up height enabling collision-free insertion or extraction._

          _Then it will be moved in horizontal direction by the retract distance out of a slot. Afterwards (as is the case for a single movement) the iSWAP will be moved in maximum z-position (the greatest possible distance from the labware placed on the deck). The plate will be turned in such a way that the arm of the iSWAP is bent into a compact position for the x/y-transport. The software controls these movements and prevents any collision with the pipetting channels or side panels._
      7.  #### _‌Plate Release‌_

          \


          _For plate release, the orientation of the arm and the gripper will be calculated automatically so that the orientation of position A1 of the plate is in accordance to the Deck Layout. If this is not possible, the plate must be gripped inversely (i.e. from the opposite side). See the VENUS Help Function._

          \


          ![Originalbild anzeigen](../.gitbook/assets/Image\_1507.jpg)

          _NOTE_

          _During plate placement, the plate will be gently pressed onto the rack. Ensure that strips are fixed securely in the frame._

          \

      8.  #### _‌Accessible Areas‌_

          \


          _The iSWAP can be used over the whole deck area and the adjoining zones. The table below lists the coordinates of the accessible area relative to the zero point of the ML STAR:_

          \


          | X-Movement Pipetting Arm | Minimum Absolute Position              | Maximum Absolute Position |           |           |
          | ------------------------ | -------------------------------------- | ------------------------- | --------- | --------- |
          | STARlet                  | STAR                                   | STARPlus                  |           |           |
          | 173050/51                | - 206 mm                               | + 1038 mm                 | + 1578 mm | + 2208 mm |
          | 173052                   | - 118 mm                               | + 1250 mm                 | + 1790 mm | + 2420 mm |
          | 173054                   | Depending on Dual Arm Configuration 1) | + 1215 mm                 | + 1755 mm | + 2385 mm |

          _1) Left: Modular Arm 173050/51;_

          _Right: iSWAP Arm (173054), min. absolute Pos: +121 mm Left: 96 Arm 173053;_

          _Right: iSWAP Arm (173054), min. absolute pos: -87 mm_

          \


          | <p>X-Movement Pipetting Arm</p><p>Channels</p>                                                                   | Minimum absolute Position                                                                             | Maximum Absolute Position                                                                             | Remarks                                   |
          | ---------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------- | ----------------------------------------- |
          | <p>173050/51</p><p>4 Channels</p><p>8 Channels</p><p>12 Channels</p><p>16 Channels</p><p>173052</p><p>173054</p> | <p><br></p><p>- 221 mm</p><p>- 185 mm</p><p>- 149 mm</p><p>- 113 mm</p><p>- 257 mm</p><p>- 257 mm</p> | <p><br></p><p>+ 605 mm</p><p>+ 605 mm</p><p>+ 605 mm</p><p>+ 605 mm</p><p>+ 605 mm</p><p>+ 605 mm</p> | On all platforms (STARlet STAR, STARplus) |

          ![Originalbild anzeigen](../.gitbook/assets/Image\_1508.jpg)

          _NOTE_

          _The minimal and maximal absolute positions of the x- and y-movement cannot be reached by the default settings of transport commands. Use the settings of “Complex movement” in the transport commands._

          _The standard configuration of an ML STAR Series instrument is WITH acrylic covers. The maximal and minimal absolute positions of the x-movement can only be reached if the acrylic glass shields (left, right) are removed._

          _This is not only a mechanical issue. The instrument configuration has to be changed as well. Please contact a Hamilton Representative._

          \


          | Movement         | Minimum absolute Position  | Maximum Absolute Position      | Remarks                                                                                                                                                                           |
          | ---------------- | -------------------------- | ------------------------------ | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
          | Z-Movement       | <p>+ 100 mm</p><p>0 mm</p> | <p>+ 282 mm</p><p>+ 282 mm</p> | <p>iSWAP (P/N 182600) Rev. 00 – 02</p><p>iSWAP (P/N 182600) Rev. ≥ 03 and Landscape iSWAP (P/N 190220)</p><p>Position of clamp tips, if there is no inhibition by the labware</p> |
          | Gripper Movement | <p>72 mm</p><p>72 mm</p>   | <p>108 mm</p><p>132 mm</p>     | <p>iSWAP (P/N 182600)</p><p>Landscape iSWAP (P/N 190220) Default: 82 mm</p>                                                                                                       |
          | Arm Rotation     | - 90°                      | + 90°                          | [See ](iswap.md#bookmark480)[Section 15.1.1 iSWAP Geometry](iswap.md#bookmark480)                                                                                                 |
          | Hand Rotation    | - 90°                      | + 90°                          | [See ](iswap.md#bookmark480)[Section 15.1.1 iSWAP Geometry](iswap.md#bookmark480)                                                                                                 |

          _Coordinates of Accessible Area_

          _Certain plate orientations and gripping directions prevent the iSWAP from reaching the zones on both sides. For these cases, an easy method is recommended for plate transport._

          \


          ![image](../.gitbook/assets/Image\_1509.png)

          _ATTENTION_

          _If a plate has to be gripped down low on the deck, enough space must also be left on the deck for the arm and gripper of iSWAP._

          \

      9.  #### _‌Sequence Definitions for Transport Steps‌_

          \


          [_The iSWAP works on the basis of sequences (see_ ](iswap.md#bookmark486)[_Section 15.1.7 iSWAP_ ](iswap.md#bookmark486)_Movement). Plates are moved from one position to another, each defined by its own sequence. The labware definition remains fixed on the deck, but the plates change sequences. To make this possible, definition of target and source plate positions must be of the same labware type._

          _After processing of a sequence, the current position will be set to the next labware ID. If the same plate should be transported several times, select sequence counting '(0) Manually' or set the current position back to the previous position._

          ![Originalbild anzeigen](../.gitbook/assets/Image\_1510.jpg)

          _NOTE_

          _Sequence positions for transport steps are always differentiated by the labware ID. The current position of the transport sequence is to set the next labware ID in the sequence._

          \


          ![image](../.gitbook/assets/Image\_1511.gif) ![image](../.gitbook/assets/Image\_1512.gif)

          _In the example above, after the transport of plate Source\_1, the current position will be set to plate Source\_2 (line 5); and after transport of plate Soure\_2 to plate Source\_3 (line 9)._

          _It is recommended to define separate sequences for transport and pipetting, because the behavior of transport and pipetting is different._

          \


          ![Originalbild anzeigen](../.gitbook/assets/Image\_1513.jpg)

          _NOTE_

          _The orientation of the plate depends on plate positioning on the deck and not on sequences. The orientation can be changed under the “Labware” Tab by the function ”Adjust Labware Position” – “Rotation”)._
      10. #### _‌Command Description‌_

          \


          _The following tables give a brief overview of the available ML STAR-specific iSWAP commands._

          \


          1.  _‌Easy Steps_

              \


              | Transport: Easy Steps |                                                                                                    |                               |
              | --------------------- | -------------------------------------------------------------------------------------------------- | ----------------------------- |
              | Command               | Icon                                                                                               | Action Performed              |
              | iSWAP Transport       | <p><br></p><p><img src="../.gitbook/assets/Image_1514.jpg" alt="NewIMAGES/iswaptransport.bmp"></p> | Transport a plate with iSWAP. |

              \

          2.  _‌Single Steps_

              \


              | Transport: Single Steps        |                                                                                                              |                                                                                                   |
              | ------------------------------ | ------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------- |
              | Command                        | Icon                                                                                                         | Action Performed                                                                                  |
              | iSWAP Get Plate                | <p><br></p><p><img src="../.gitbook/assets/Image_1515.gif" alt="NewIMAGES/cmdgetPlate.bmp"></p>              | Picks up a plate from the defined position.                                                       |
              | iSWAP Place Plate              | <p><br></p><p><img src="../.gitbook/assets/Image_1516.gif" alt="NewIMAGES/cmdplacePlate.bmp"></p>            | Sets a plate down in a defined position.                                                          |
              | iSWAP Move Plate               | <p><br></p><p><img src="../.gitbook/assets/Image_1517.gif" alt="NewIMAGES/cmdmovePlate.bmp"></p>             | Transfers a plate to another sequence.                                                            |
              | iSWAP Open Gripper             | <p><br></p><p><img src="../.gitbook/assets/Image_1518.jpg" alt="NewIMAGES/cmdopenGripper.bmp"></p>           | Spreads the fingers of iSWAP’s robotic hand.                                                      |
              | iSWAP Close Gripper            | <p><br></p><p><img src="../.gitbook/assets/Image_1519.gif" alt="28"></p>                                     | Closes the fingers of iSWAP’s robotic hand.                                                       |
              | iSWAP Read Plate Barcode       | <p><br></p><p><img src="../.gitbook/assets/Image_1520.jpg" alt="NewIMAGES/cmdreadBarcode.bmp"></p>           | iSWAP transports the labware item it is holding to the barcode reader so its barcode can be read. |
              | iSWAP Get First Plate Position | <p><br></p><p><img src="../.gitbook/assets/Image_1521.gif" alt="NewIMAGES/CmdgetfirstPlatePosition.bmp"></p> | Sequence over several plates is checked for the first plate position.                             |
              | iSWAP Park                     | <p><br></p><p><img src="../.gitbook/assets/Image_1522.jpg" alt="NewIMAGES/cmdparkiswap.bmp"></p>             | Parks the iSWAP under the pipetting arm.                                                          |
   2.  ### _‌Programming the iSWAP‌_

       \


       _The following example demonstrates the use of iSWAP with Microlab STAR. A plate is transported from a stacker to a processing position. Here, its plate barcodes is also read. After pipetting some reagent, the plate is brought to a reader and read (simulated). Then, the plate is transported to an output stack._

       _Creating the Deck Layout_

       _Use the “Search Labware” Field to add the following carriers to the deck: “PLT\_CAR\_L4ST\_LOW\_A00\_4x9\_Nunc96“_

       ![image](../.gitbook/assets/Image\_1523.png)

       _”TIP\_CAR\_480\_ST\_A00”_

       _“RGT\_CAR\_3R\_A01”_

       &#x20;                                                                       &#x20;

       _“PLT\_CAR\_L5MD\_A00“ with 1, “Nun\_96\_Fl\_Lb” on position 1. Name it “Processing”. “Nun\_96\_Fl\_Lb”. Use the coordinates x = -70 / y = 350 / z = 160) and name it “Reader”._

       \


       _iSWAP Deck Layout_

       \


       ![Originalbild anzeigen](../.gitbook/assets/Image\_1524.jpg)

       _NOTE_

       _To save deck space, the stacker carrier can be positioned 4 tracks to the left of the deck (track positions –3 to +3), and the plates will still be fully accessible by the iSWAP._

       _Creating the Sequences_

       1. _Click the “Sequences” Tab and create the following sequences:_
       2.  _On the foremost plate stack, select only the well A1 of all 9 plates. Make sure the stamp tool is set to “Single position select” and the sorting option is “Top Down” as shown below._

           \


           ![Seite\_390\_Graphik](../.gitbook/assets/Image\_1525.jpg)

           \

       3.  _This means that the stack from top to bottom is used as a SOURCE stack._

           \


           ![image](../.gitbook/assets/Image\_1526.gif)

           \

       4.  _In the “Advanced” Window, check if the plate on top (the one with the highest z-coordinate is on sequence position one. Save the sequence as ‘InputStack’._

           \


           ![image](../.gitbook/assets/Image\_1527.jpg)

           \

       5. _Do the same for the output stack on position 4. But this time, sort the sequence to start with the deepest position (sorting option is “Descending”)._
       6. _Save this sequence as “OutputStack”_
       7. _Rename the sequence “rgt\_cont\_120ml\_a00\_0001” to “Reagent”._

       _Creating the Method_

       _To create the required method:_

       1.  _Drag and drop an “iSwap Transport” Step into the method. Since this is an Easy Step, an initialize step is not needed to initialize the instrument._

           \


           ![image](../.gitbook/assets/Image\_1528.jpg)

           \

       2. _Set the ‘InputStack’ sequence as the get sequence. Activate the ‘Auto increment’ to make sure the current position points to the next plate after getting this one._
       3. _Setting the ‘Search source labware first’ will force the iSWAP to check where the first free position is. This is especially helpful if the loading state of a stack is not known. The iSWAP will check this and set the current position according to the first free position._
       4. _Activate the ‘Read plate barcode’ box to identify the plate. The Autoload will move to track 12 to read the plate’s barcode. If the default settings from this step are being used then there is no risk of collision. That means that the barcode reading with iSWAP is possible even on a fully loaded deck._
       5. _Set the “Parking the iSWAP after labware is placed” to On._
       6.  _Use a “Aliquote” Smart Step to pipette 50μl of reagent over the full plate. Even if the sequence of the Reagent trough is used up, it will still restart at the beginning, since the Radio Button is set to \[No, reuse the sequence from the beginning if necessary]:_

           \


           ![image](../.gitbook/assets/Image\_1529.jpg)
       7.  _Also make sure the “Initial sequence manipulation” are set as follows:_

           \


           ![image](../.gitbook/assets/Image\_1530.jpg)

           \

       8.  _Because the sequence ‘Processing’ is used both for pipetting and transport, the “Final sequence manipulation” should be used as follows:_

           \


           ![image](../.gitbook/assets/Image\_1531.jpg)

           \

       9. _Now, use an “iSwapTransport” Step to bring the plate from the “Processing” Position to the “Reader” Position. Do not park the iSWAP._
       10. _Since there is no reader connected, a comment step is used to simulate this._
       11. _After reading, the plate has to be taken at the reader position and brought to the output stack. Make sure the “Auto increment” is only set at the “Output Stack” Place Sequence._
       12. _To have all plates processed, create a loop and move all steps inside. The loop limitation should be the sequence ‘InputStack’._

           \


           ![image](../.gitbook/assets/Image\_1532.jpg)
       13. _To make the method perfect, add an iSWAP park step at the end (the transport step in line 6 was set to park iSWAP = Off)._
       14. _When all of the steps have been done, the method should look like this:_

       \


       ![image](../.gitbook/assets/Image\_1533.jpg)

       \

   3.  ### _‌Helpful Hints‌_

       \


       1.  #### _‌Define Special Labware Data / Parameters Only Once‌_

           \


           ![Originalbild anzeigen](../.gitbook/assets/Image\_1534.jpg)

           _NOTE_

           _It is possible to unmark the “Generate default deck sequence” in the “Labware” Tab. In this case, no default sequences are created._

           _This option is helpful if many special sequences have to be created._

           \


           _If the default values for GripForce, GripWidth, GripHeigth, OpeningWidthBeforeAccess (because an own new plate labware has been created or the method must use different values) are not used, it would seem sensible to save these parameters in a variable. This can be done by selecting “View”  “Variables” in the Method Editor._

           \


           ![image](../.gitbook/assets/Image\_1535.jpg)

           1.  _To create a new variable, enter the Context Menu with a right mouse click and select “New”. The dialog box below will then appear and can be filled out._

               \


               ![image](../.gitbook/assets/Image\_1536.jpg)

               \

           2.  _It is now possible to create many variables as needed._

               \


               ![image](../.gitbook/assets/Image\_1537.gif)
           3. _These variables can now be used in all iSWAP or CO-RE gripper commands for the special plate._
           4. _If there are multiple grip commands for this plate in the method, it is much faster to change these values once in the variable definition. Of course, every plate type needs its own parameters._
       2.  #### _‌Move to Positions Outside of the Slot Area‌_

           \


           _The iSWAP is able to reach positions outside the slot area or below the deck’s surface (check the specifications for the exact range)._

           _Use the “AdjustPosition” Function (double click on the labware) to move a plate outside the slot area. Find the position using the \[Move Probe]._

           \


           ![image](../.gitbook/assets/Image\_1538.png)

           \


           _If a collision is possible (e.g. with the housing of a reader), select “Complex Movement” as the “Movement Type” and define a “Retract Distance” greater than the plate length. Refer to the image below._

           \


           ![image](../.gitbook/assets/Image\_1539.jpg)

           \


           _All bending and turning moves are now executed in a way which is directed away from the housing. The iSWAP will drive to the position using x-drive._
