# Error documentation from pylabrobot

`Anti Drop Control Error`

Anti drop controlling out of tolerance. If this error happens then you need to ensure ADC is shut off or is within the bounds of the limits of ADC, the ADC will run out of room on the piston eventually when trying to constantly retract up liquid to not formulate dropletts

####

`Area Already Occupied Error`

Instrument region already reserved.

####

`Barcode Already Used Error`

The barcode read is already loaded as unique barcode ( it's not possible to load the same barcode twice ).

####

`Barcode Error`

Barcode could not be read or is missing.

####

`Barcode Mask Error`

The barcode read doesn't match the barcode mask defined.



`Barcode Not Unique Error`

The barcode read is not unique. Previously loaded labware with same barcode was loaded without unique barcode check.



`Calibrate Error`

No capacitive signal detected during carrier calibration procedure.

####

`Clot Error`

Blood clot detected.

####

`Cover Open Error`

Cover not closed or can not be locked.

####

`Decapper Error`

Decapper lock error while screw / unscrew a cap by twister channels.

####

`Decapper Handling Error`

Decapper station error while lock / unlock a cap.

`Delimiter Error`

Barcode contains character which is used as delimiter in result string.

####

`Execution Error`

A step or a part of a step could not be processed.

####

`Hamilton Deck Resource Error`

Error with any deck object in interface with robot.

####

`Hamilton Error`

Exceptions raised in package pyhamilton

####

`Hamilton Interface Error`

Error in any phase of communication with robot.

####

`Hamilton Return Parse Error`

Return string from instrument was malformed.

####

`Hamilton Step Error`

Errors in steps executed by VENUS software coded in the Hamilton error specification.

####

`Hamilton Syntax Error`

There is a wrong set of parameters or parameter ranges.

####

`Hamilton Timeout Error`

An asynchronous request to the Hamilton robot timed out.

####

`Hardware Error`

Steps lost on one or more hardware components, or component not initialized or not functioning.

####

`Illegal Intervention Error`

Cover was opened or a carrier was removed manually.

####

`Illegal Target Plate Position Error`

Cannot place plate, plate was gripped in a wrong direction.

####

`Impossible To Occupy Area Error`

A region on the instrument cannot be reserved.

####

`Improper Aspiration Or Dispense Error`

The pressure-based aspiration / dispensation control reported an error ( not enough liquid ).

####

`Improper Dispensation Error`

The dispensed volume is out of tolerance (may only occur for Nano Pipettor Dispense steps).

This error is created from main / slave error 02/52 and 02/54.

####

`Insufficient Liquid Error`

Not enough liquid available.

####

`Invalid Err Code Error`

Error code returned from instrument not known.

####

`Kit Lot Expired Error`

Kit Lot expired.

####

`Labware Error`

Labware not available.

####

`Labware Gripped Error`

Labware already gripped.

####

`Labware Lost Error`

Labware lost during transport.

####

`Liquid Level Error`

Liquid surface not detected.

This error is created from main / slave error 06/70, 06/73 and 06/87.

####

`No Carrier Barcode Error`

Carrier barcode could not be read or is missing.

####

`No Carrier Error`

No carrier present for loading.

####

`No Labware Error`

The labware to be loaded was not detected by autoload module.

Note:

May only occur on a Reload Carrier step if the labware property 'MlStarCarPosAreRecognizable' is set to 1.

####

`No Tip Error`

Tip is missing or not picked up.

####

`Not Aspirated Error`

Dispense volume exceeds the aspirated volume.

This error is created from main / slave error 02/54.

####

`Not Detected Error`

Carrier not detected at deck end position.

`Not Executed Error`

There was an error in previous part command.

####

`Parameter Error`

Dispense in jet mode with pressure liquid level detection is not allowed.

####

`Position Error`

The position is out of range.

####

`Pressure LLD Error`

Pressure liquid level detection in a consecutive aspiration is not allowed.

####

`Resource Unavailable Error`

Layout manager found deck resource type not present or all of this type assigned

####

`Slave Error`

Slave error.

####

`TADM Overshot Error`

Overshot of limits during aspirate or dispense.

Note:

On aspirate this error is returned as main error 17.

On dispense this error is returned as main error 4.

####

`TADM Undershot Error`

Undershot of limits during aspirate or dispense.

Note:

On aspirate this error is returned as main error 4.

On dispense this error is returned as main error 17.

####

`Temperature Error`

Incubator temperature out of range.

####

`Tip Present Error`

A tip has already been picked up.

####

`Unexpected Labware Error`

The labware contains unexpected barcode ( may only occur on a Reload Carrier step ).



`Unexpected cLLD Error`

The cLLD detected a liquid level above start height of liquid level search.

####

`Unload Error`

Not possible to unload the carrier due to occupied loading tray position.

####

`Wash Liquid Error`

Waste full or no more wash liquid available.

####

`Wrong Carrier Error`

Wrong carrier barcode detected.

####

`Wrong Labware Error`

The labware to be reloaded contains wrong barcode ( may only occur on a Reload Carrier step ).

####
