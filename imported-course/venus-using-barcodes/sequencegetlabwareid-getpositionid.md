# SequenceGetLabwareID / GetPositionID

## SequenceGetLabwareID / GetPositionID

<figure><img src="../../.gitbook/assets/image (876).png" alt=""><figcaption></figcaption></figure>

* When an array of loaded barcodes is created, the index where a barcode is found correlates to the position in the loaded sequence.
* Extract LabwareID and PositionID from the loaded sequence to build a processing sequence.

## Turning a Barcode into a Sequence

<figure><img src="../../.gitbook/assets/image (877).png" alt=""><figcaption></figcaption></figure>

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
