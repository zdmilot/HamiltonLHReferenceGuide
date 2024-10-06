# iSWAP Transport step



## Command

## iSWAP Transport step

The iSWAP Transport step allows a simple definition of a transport procedure with the iSWAP on a Microlab® STAR with the following features:

* Automatic instrument initialization.
* Optional search of source labware before starting of transport procedure.
* Optional barcode reading during transport.
* Optional search of free position before starting of transport procedure.
* Optional parking of iSWAP after transport procedure.
* Programmable error handling and [walk away behavior](#user-content-fn-1)[^1].
* Full access to define complex movements.
  *   ### iSWAP Complex movement

      Use the iSWAP Complex movement to transport plates to or from shelves, incubators etc.

      &#x20;

      Complex movement parameters

      * Retract distance \[mm] (see figure 1)\
        Actual insertion depth.\
        If insertion depth > 138mm, the iSWAP will approach the target position with outstretched arm.\
        If insertion depth < 138mm, the iSWAP will first try to approach the target position with its arm bent. If the position is not reached in this way, iSWAP will then approach the position with outstretched arm.

      &#x20;

      * Lift-up height \[mm] (see figure 1)\
        Lift-up height of gripped labware item for a collision-free insertion or extraction.

      &#x20;

      * Labware orientation (see figure 2)\
        Defines from which direction the iSWAP may approach labware.\
        The values for setting the variables are displayed in parentheses in the dialog.\
        \
        Note:\
        If labware orientation and iSWAP grip direction do not match, an error will be generated.

      &#x20;![](<../../../../.gitbook/assets/image (438).png>)

      Fig. 1: Complex movement parameters

      &#x20;

      &#x20;![](<../../../../.gitbook/assets/image (437).png>)

      Fig. 2: Labware orientation
* Automatic grip width calculation depending given access height.

&#x20;

Dialogs used to define an iSWAP Transport step:

* Main dialog: iSWAP Transport dialog
* Customize dialog: Tab Get plate advanced, Tab Gripper direction, Tab Complex movement, Tab Lid handling mode, Tab Collision control, Tab Read Barcode
* Error Settings dialog

&#x20;

Step return values:

This step returns 1 result value.

Result value 1 contains the read barcode \<!-- kadovFilePopupInit('a3'); //--> as string (empty string if no barcode was read).

## Dialog Box

This dialog enables parameters to be defined for the iSWAP Transport step.

&#x20;

Get labware from sequence:

The selected sequence defines from which position the iSWAP has to get the labware.

&#x20;

¨ Auto increment

Check this box to enable sequence counting \<!-- kadovFilePopupInit('a1'); //-->  - on 'Get labware from sequence' - by step.

&#x20;

Set teaching data

If the specified 'get labware' sequence has been teached using the iSWAP, the used teaching parameters can be overtaken with this button.

&#x20;

¨ Search source element first

Check this box to search the first available labware within the given sequence.

This option may be useful if working with plate stacks.

&#x20;

¨ Read plate barcode on autoload reader

Check this box to read the barcode of gripped labware. The read barcode \<!-- kadovFilePopupInit('a3'); //--> will be set on tracker database.

&#x20;

Reader position \[track number]:

Track number where the barcode shall be read. This field is only enabled if 'read plate barcode on autoload reader' is activated.

&#x20;

Place labware at sequence:

The selected sequence defines on which position the iSWAP has to place the labware.

&#x20;

¨ Auto increment

Check this box to enable sequence counting \<!-- kadovFilePopupInit('a2'); //-->  - on 'Place labware at sequence' - by step.

&#x20;

Set teaching data

If the specified 'place labware' sequence has been teached using the iSWAP, the used teaching parameters can be overtaken with this button.

&#x20;

¨ Search free position first

Check this box to search a free position - to place the labware - within the given sequence.\
If activated, the iSWAP will lookup for a free position before starting with the transport procedure. This option may be useful if working with plate stacks.

&#x20;

Park iSWAP after labware is placed

Defines whether he iSWAP will be parked after labware was placed.\
The values for setting the variables are displayed in parentheses in the dialog.\
&#x20;

&#x20;

Other Dialog boxes accessible from this page:

* Customize dialog: Tab Get plate advanced, Tab Gripper direction, Tab Complex movement, Tab Lid handling mode, Tab Collision control, Tab Read Barcode
* Error Settings dialog

&#x20;

&#x20;

## Teaching with iSWAP Dialog

This dialog enables parameters to be defined for teaching a labware position.

&#x20;

iSWAP settings

&#x20;

Use labware from sequence

Select a sequence which is available on the deck of Microlab® STAR. The labware on the selected sequence will be used for measure the unknown position.

Note:

The sequences are filtered depending on labware type which is selected to adjust its location. However, make sure the labware physically used for measure the unknown position is of same type as the labware to adjust its location within deck-layout.

&#x20;

Grip on small/large side

* Grip plate on small side (default)\
  The iSWAP will grip the labware item on smaller side.

&#x20;

* Grip plate on large side (only supported for iSWAP with extended grip range)\
  The iSWAP will grip the labware item on larger side.

&#x20;

Grip inverse

If checked, the labware - used for measure the unknown position - will be gripped with inverse mode and the iSWAP approaches the position to teach also with inverse mode.

&#x20;

Grip height \[mm]

Defines the point below the top of labware where the iSWAP will grip the labware. If higher labware (e.g. deep-well plate) is used to measure unknown positions, a minimal grip height is calculated by the system. It's not possible to set the value for grip height below this minimal grip height.

&#x20;

Tolerance \[mm]

Defines the tolerance for the gripping dimensions of a labware item.

If the iSWAP does not detect the labware within this tolerance the instrument will report an error.

&#x20;

Grip width \[mm]

Defines the grip width of a labware item.

&#x20;

Opening width before access \[mm]

Defines the opening width of the iSWAP clamps before access to the labware.

Note:

The value for this parameter has to be greater or equal as the total of parameters 'Grip Width' and 'Tolerance'.

&#x20;

Grip force

Defines the force the iSWAP will use to grip a labware item. Use higher force for heavier labware (e.g. deepwell plate) and lower force for easy to lift labware (e.g. cover).

&#x20;

Approximate target position

&#x20;

x: Approximate target position of labware in x-axis

&#x20;

y: Approximate target position of labware in y-axis

&#x20;

Note:

The iSWAP will approach a target position with its predefined arm bending for a given area on the deck of Microlab® STAR. If the measured labware target position is not within this area, an error occurs and invites to measure the same position again. For this case use the actually measured position values as new approximate target values.

&#x20;

Motion type during run

&#x20;

¨ Complex movement

Check this box to enable Complex movement parameter to be defined.

&#x20;

Collision Control

&#x20;

¨ Enable collision control

Check this box to enable collision control \<!-- kadovFilePopupInit('a1'); //--> for dual arm instruments.

[^1]: The user may define a walk-away error handling which uses predefined default settings for different error situations. These error handling settings can be customized for each command step independently.
