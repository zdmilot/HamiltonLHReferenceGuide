# Tube-gripper‌

<figure><img src="../../.gitbook/assets/image (463).png" alt=""><figcaption></figcaption></figure>

_This section provides all necessary information about the tube-gripper. This tool can be used to move tubes to a barcode reader (if the Autoload option is not installed), to load/unload tubes to an integrated centrifuge, to pick specific tubes from multiple carriers into one target carrier, to move tubes to a balance (measuring evaporation), etc._

_This tool is mounted on a pipetting channel and can be moved over the deck in the same way as the pipetting channels._

## _**‌Using the Tube-gripper Steps‌**_

_First, make sure that the tube-gripper is activated in the Hamilton System Configuration Editor. Set both the tube-gripper and the Autoload option line to ‘Available’ as shown below:_

![](<../../.gitbook/assets/image (464).png>)



_In the Method Editor, the tube-gripper steps are found:_

<figure><img src="../../.gitbook/assets/image (465).png" alt=""><figcaption></figcaption></figure>

### _“Tube Grip Get”_

_This step is used to pick a tube. The parameters to pass are the following:_

* _Sequence (where to get the tube)_
* _Sequence counting (manually, to leave the current position untouched)_
* _Grip height in mm, measured from the top of the tube_
*   _Opening width before access in mm (maximum = 24mm)_

    <figure><img src="../../.gitbook/assets/image (467).png" alt=""><figcaption></figcaption></figure>





### _“Tube Grip Place”_

_This step is used to place a gripped tube. The parameters to pass are the following:_

* _Sequence (where to put the tube)_
* _Sequence counting (manually, to leave the current position untouched)_
*   _Relative clamp open width in mm._

    <figure><img src="../../.gitbook/assets/image (468).png" alt=""><figcaption></figcaption></figure>



<table data-header-hidden><thead><tr><th width="145"></th><th></th></tr></thead><tbody><tr><td><img src="../../.gitbook/assets/image (10) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" data-size="original"></td><td><p>NOTE</p><p>The relative clamp open width is a relative value. If the gripped tube requires a clamp position of 20mm, there is only 4mm left to open (because 24mm is the maximum opening width).</p></td></tr></tbody></table>



### _“Tube Grip Move”_

_This step is used to move a gripped tube to a specific position without opening the clamp. This could be used e.g. to move the tube in front of an external barcode reader._

_The parameter to pass is the:_

*   _Sequence (where to move \[and hold] the tube)._

    _Keep in mind that the step will move the tube to the current position of the sequence that has been passed._



<figure><img src="../../.gitbook/assets/image (469).png" alt=""><figcaption></figcaption></figure>



### _“Tube Grip Read Barcode”_

_This step is used to move a gripped tube to a specific position without opening the clamp. This step will grip a tube and bring it to the Autoload barcode reader for reading._

_The parameter to pass is the:_

* _Reader position \[track number]_

_This value specifies the track, where the Autoload barcode reader will move to. After the movement to this position, the tube-gripper will bring the tube in front of the reader and read the barcode._\
\


<figure><img src="../../.gitbook/assets/image (470).png" alt=""><figcaption></figcaption></figure>

_In order to link the value of the barcode to a variable, the return value of the step has to be linked._

1.  _To do so, right-click the Tube Grip Read Barcode in the method and select ‘Bind Return values’:_

    <figure><img src="../../.gitbook/assets/image (471).png" alt=""><figcaption></figcaption></figure>


2.  _A window opens to link the different return values to variables. The value from line 4 (which is the barcode) will be used in the example as seen in the image below._

    <figure><img src="../../.gitbook/assets/image (472).png" alt=""><figcaption></figcaption></figure>


3. _Type in or select a variable that will hold the value of the barcode. Finish with \[OK]._\
   ![](<../../.gitbook/assets/image (473).png>)

<table data-header-hidden><thead><tr><th width="145"></th><th></th></tr></thead><tbody><tr><td><img src="../../.gitbook/assets/image (10) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" data-size="original"></td><td><p>NOTE</p><p>The tube-gripper is able to grip tubes with an outer diameter of 8 to 22mm. The tube-gripper clamps need additional space when gripping tubes with large diameter (15 – 22mm). In an event like this, leave a space on the left and right of the tube carrier.</p></td></tr></tbody></table>

