# iSWAP

## Plate Handling with iSWAP

iSWAP (internal Swivel Arm Plate Handler) is a robotic arm that transports microplates, covers of microplates, archive plates or filter plates used for the vacuum box to and from positions on the deck of ML STAR.&#x20;

Like the ML STAR pipetting channels, the iSWAP has a “Traverse height” of 145 mm above the deck (245 mm above the origin).&#x20;

### iSWAP Geometry

<figure><img src="../../../.gitbook/assets/image (90) (1) (1).png" alt="" width="375"><figcaption></figcaption></figure>

<table data-header-hidden><thead><tr><th width="145"></th><th></th></tr></thead><tbody><tr><td><img src="../../../.gitbook/assets/image (10) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" data-size="original"></td><td><p>NOTE</p><p>Height for gripping is calculated from the upper rim of the plate. Recommended gripping height for MTP: 3 mm Recommended gripping height for DWP: 13 mm (an error will appear if there is an attempt to grip a Deep Well Plate with a grip height &#x3C; 10mm traverse height).</p></td></tr></tbody></table>

### Special iSWAP Features

Among the special features of iSWAP are:&#x20;

• A torque sensor which signals to the robot how tightly it is gripping a labware object.&#x20;

• The plates can be placed in landscape or portrait orientation.&#x20;

• Load and unload plates to and from a plate stacker on the left side of the instrument outside the working area (with some restrictions, this can also be done on the right side).&#x20;

• Handling plates 100mm below the deck (if iSWAP Rev. ≥ 03. E.g. possible on the ML STARplus without deck extension).&#x20;

Not all features are available on the old iSwap Type.&#x20;

<table data-header-hidden><thead><tr><th width="145"></th><th></th></tr></thead><tbody><tr><td><img src="../../../.gitbook/assets/image (10) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" data-size="original"></td><td><p>NOTE</p><p>Gripping of microplates in landscape orientation is only possible with the Landscape iSWAP P/N 190220. </p><p>Use the “Hamilton System Configuration Editor” to enable the functions of the “Landscape” iSWAP: ML STAR / Simulator configuration / iSWAP / “Large Gripper”. </p></td></tr></tbody></table>

### iSWAP Positions

The iSWAP is mounted on the pipetting arm of the ML STAR.&#x20;

During pipetting, the iSWAP is in park position and does not affect the movement of the pipetting channels.&#x20;

For plate transport steps, the pipetting tools will be moved away so that the greatest possible transport area will be available to the iSWAP. The orientation of the arm and gripper will be automatically calculated by the software according to the Deck Layout and programmed grip direction.&#x20;

Using multi-arm systems can affect the movement range.&#x20;

### Grip and Opening Widths

“Grip width” and “opening width before access” can vary between 72 and 108 (132) mm.&#x20;

Archive and filter plates in particular have to be gripped no more than 28 mm below the upper rim. The lower rim of the plate should be no more than 35 mm below the gripping position, to prevent collision with other labware placed on the deck.

The default grip force is appropriate for common MTPs. It should be set higher for archive plates, and lower for soft plates.

<table data-header-hidden><thead><tr><th width="125"></th><th></th></tr></thead><tbody><tr><td><img src="../../../.gitbook/assets/image (9) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" data-size="original"></td><td><p>ATTENTION</p><p>In order to prevent spillage during transport with iSWAP, it is recommended not to overfill the wells (e.g. fill maximum 80 % of nominal well volume). </p><p><br>The maximum weight to be transported is 300 g. This should not be exceeded. </p><p><br>The rectangular racks should only be lifted from or placed onto carriers with slide guides (see the ML STAR Line Operator’s Manual) <br><img src="../../../.gitbook/assets/image (92) (1) (1).png" alt=""><br>The gripping area should be flat and stable. Ensure that the gripper's clamps will not pick up strips instead, the lower part of the plate's frame. <br><br>Define the correct plate orientation to ensure that plates lifted from MTP stacks via iSWAP can be identified on deck. <br><br>Affix plate barcodes correctly (see Technical Specifications in the Microlab STAR Line Operator’s Manual).</p></td></tr></tbody></table>



### Pick-up by iSWAP

Rectangular racks are always picked up at the short side. The gripper has a preferred gripping direction, which can be modified within the advanced settings of the “GetPlate” and “iSwapTransport” Steps.

### iSWAP Movement

In the case of a complex movement used to transport plates to or from stacks, shelves, etc., a plate once picked up will be moved up in small steps to the lift-up height enabling collision-free insertion or extraction.&#x20;

Then it will be moved in horizontal direction by the retract distance out of a slot. Afterwards (as is the case for a single movement) the iSWAP will be moved in maximum z-position (the greatest possible distance from the labware placed on the deck). The plate will be turned in such a way that the arm of the iSWAP is bent into a compact position for the x/y-transport. The software controls these movements and prevents any collision with the pipetting channels or side panels. \


### Plate Release

For plate release, the orientation of the arm and the gripper will be calculated automatically so that the orientation of position A1 of the plate is in accordance to the Deck Layout. If this is not possible, the plate must be gripped inversely (i.e. from the opposite side). See the VENUS Help Function.

<table data-header-hidden><thead><tr><th width="145"></th><th></th></tr></thead><tbody><tr><td><img src="../../../.gitbook/assets/image (10) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" data-size="original"></td><td><p>NOTE</p><p>During plate placement, the plate will be gently pressed onto the rack. Ensure that strips are fixed securely in the frame.</p></td></tr></tbody></table>

