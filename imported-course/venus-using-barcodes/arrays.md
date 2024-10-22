# Arrays

## Arrays

* Primary method for handling barcode values during runtime:
  * Barcodes loaded onto the system (one per sequence, extracted from the DB).
  * Barcodes read from a worklist column.
* **HSLExtensions::Array Library** includes:
  * Compare: Returns whether two arrays match or not.
  * ContainsDuplicates: Checks for non-unique values in an array.
  * ContainsValue: Returns if a value exists in an array.
  * FindValue: Returns positions where a value is found in an array.

## Matching Barcodes to a Worklist

* Sequences remain essential even when worklists replace LabwareID or PositionID.
* A **Load Sequence** represents everything a user could load.
* A **Processing Sequence** represents what is to be processed, created during worklist file handling.
