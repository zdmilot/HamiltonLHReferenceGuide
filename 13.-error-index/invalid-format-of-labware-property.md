# Invalid format of labware property

### Property 'MlStarReadBarcodeOnPositions'

Make sure that the definition of labware property MlStarReadBarcodeOnPositions is correct.

&#x20;

Reasons for such an error:

* The position on the left side of the assignment is not between 1 and MlStarCarCountOfBCPos as defined in the labware properties of the used labware
* The position on the right side of the assignment is not defined on the template
* The position on the right side of the point operator is not defined as a labware position
* The position(s) on the right side of the assignment is/are not defined in current used deck layout

&#x20;

_Example for valid formats:_

* "1=1;3=7;5=11;"  (valid format for a labware which is specified with numerical indexes)
* "1=A3;3=A4;5=A8;"  (valid format for a labware which is specified with alpha-numerical indexes)
* "1=1;5=2.1;5=2.2;10=3;"
* "2=1.C3;5=2.1;6=3;"
