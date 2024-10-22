# Accessing Barcode Data - Functions and Storage

## HSLAppsLib::GetLabwareBarcode

* **Purpose**: Retrieves the string representing the barcode value at the current sequence location.
* **Parameters**: Instrument reference, sequence (loaded), and level.\
  ![](<../../.gitbook/assets/image (871).png>)
* **Usage**: Loop iterating over the loaded sequence, get the barcode, store observed string into an array, and increment sequence using `HSLAppsLib::SequenceIncrement`.\
  ![](<../../.gitbook/assets/image (873).png>)



## Data Handling::Set Labware Barcode

<figure><img src="../../.gitbook/assets/image (874).png" alt=""><figcaption></figcaption></figure>

* **Purpose**: Sets a barcode value for a specified object (opposite of `GetLabwareBarcode`).
* **Parameters**:
  * Option 1: Set by Labware ID/Position ID (Strings).
  * Option 2: Set by sequence position (sequence object and position integer).

##
