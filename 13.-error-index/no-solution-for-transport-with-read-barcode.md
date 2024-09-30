# No solution for transport with read barcode

System cannot transport the labware in inverse grip mode but this mode is required to read the barcode during transport step.

&#x20;

Cause:

_Read plate barcode_ is activated on a transport step and the _Grip direction_ is set to _System_.

If the _Grip direction_ is set to _System,_ the iSWAP will approach a labware with inverse grip direction by default.

&#x20;

Make sure the labware can be accessed in inverse grip direction and the labware can be placed on destination position.

&#x20;

Note:

If the barcode is readable in normal grip direction the _Grip direction_ must be changed from _System_ to _Normal only._
