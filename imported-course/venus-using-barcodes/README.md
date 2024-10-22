# Venus Using Barcodes



## Load Carrier Single Step

<figure><img src="../../.gitbook/assets/image (860).png" alt=""><figcaption></figcaption></figure>

* Scans carrier at the positions indicated (`?` = All), customizable with strings.
* Control over barcode `.txt` file created.
  * By default, appends to the same file each run.
  * Using variable-based names can ensure file uniqueness.
* `StepReturnLib` can be used to parse collected information.

## Obtaining Barcodes: Single Step

* **Enable Sample Tracking:**
  * Go to `Tools` → `System Configuration Editor` → `System Settings` → `Sample Tracking`.
  * When enabled, creates local database files adjacent to the trace file.
  * Also enables the generation of mapping files.

<figure><img src="../../.gitbook/assets/image (862).png" alt=""><figcaption></figcaption></figure>

* **Enabling Smart Steps - New Toolbox Groups:**
  * Method → Instruments and Smart Steps:
    * Microlab Smart Steps: Load
    * Data Handling Steps: Set Labware Barcode (discussed later).
  * Populates the Sample Tracking Database.

## Load Smart Step

<figure><img src="../../.gitbook/assets/image (861).png" alt=""><figcaption></figcaption></figure>

* Scans carrier positions at every index.
* Some manual recovery is allowed:
  * Repeat scan (check for reversed tube).
  * Exclude removes sequence position.
  * Manual barcode entry is possible.

## Walk-away Mode

* Avoids prompts, allowing the user to walk away.
* May miss turned tubes.

## Transport Read Barcode

* Ensure autoload position is collision-free (watch for tall carriers!).
* Return value has the barcode available immediately.
* Same format for CO-RE Grippers or iSwap/IPG.

## The Data

* In the underlying database, there is a correlation between an object and a barcode string.
* Objects can be referenced indirectly through sequences or directly, depending on the step.
* Barcode handling differs depending on object types:
  * **Plate Carriers**: Barcodes are not visible in sequence data but set directly by their LabwareID.
  * **Tube Carriers**: Barcodes are accessible through sequences via LabwareID.
  * **Tube Barcodes**: Accessible through sequences by PositionID.
  * **Plate Tubes (bottom labeled)**: Accessible through PositionID (requires secondary device and DB value setting).

## Barcode Data and Transporting

* Sample tracking monitors the flow of barcode information and volumes.
* Barcodes cannot be set or accessed for objects that haven't been loaded by the system (pipetted, transported, or passed through load dialog/device).
* Once a barcode is obtained for an object, it follows that object within the database.

## HSLAppsLib::GetLabwareBarcode

* **Purpose**: Retrieves the string representing the barcode value at the current sequence location.
* **Parameters**: Instrument reference, sequence (loaded), and level.
* **Usage**: Loop iterating over the loaded sequence, get the barcode, store observed string into an array, and increment sequence using `HSLAppsLib::SequenceIncrement`.

## Data Handling::Set Labware Barcode

* **Purpose**: Sets a barcode value for a specified object (opposite of `GetLabwareBarcode`).
* **Parameters**:
  * Option 1: Set by Labware ID/Position ID (Strings).
  * Option 2: Set by sequence position (sequence object and position integer).

## Example: Filling Applications

* If a bulk product is dispensed to barcoded tubes and tracking is required:
  * Barcode text file may provide sufficient outgoing information.
  * Generate mapping files for more detailed information on barcodes and volumes.

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

## SequenceGetLabwareID / GetPositionID

* When an array of loaded barcodes is created, the index where a barcode is found correlates to the position in the loaded sequence.
* Extract LabwareID and PositionID from the loaded sequence to build a processing sequence.

## Turning a Barcode into a Sequence

* Lookup the barcode in the array of barcodes.
* Set the current sequence position based on where the barcode is found.
* Use `SequenceGetLabwareID` and `SequenceGetPositionID` in the `SequenceAdd` function to build a new sequence.
* Processing sequences only added when both source and destination barcodes are found.

## Example Workflow

1. Load a sample tube rack and scan the tube barcodes.
2. Store the barcodes from the database in an array of loaded barcodes.
3. Store the barcodes from the worklist into an array.
4. Use `HSLAppsLib::ArrayLookup` to find the index of each worklist barcode in the array of loaded barcodes.
5. Use the index from the loaded barcodes array to set the current sequence position.
