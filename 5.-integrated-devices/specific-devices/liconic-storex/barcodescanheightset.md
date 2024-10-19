# BarcodeScanHeightSet

## Description

This function is used to set the barcode scan height of the device.

Changing the scan height might be helpful in case the barcode of DeepWell plates has to be read and the barcode is located at the upper edge of the plate.

The scan height is the height that the handler moves above the plate pickup height to scan the barcode of a plate in function BarcodeRead or InventoryScan (in case barcode reading is enabled).

If the change in scan height is not sufficient (barcodes are located in different heights), it might be needed to enable barcode scan using function OptionSet.

## Syntax

BarcodeScanHeightSet (variable i\_intModuleIDStore,

variable& o\_intScanHeight)

## Arguments

| **argument**              | **value**                   | **description**                                                                     |
| ------------------------- | --------------------------- | ----------------------------------------------------------------------------------- |
| i\_intModuleIDStore \[in] | integer \[0..3]             | Unique identifier for the Liconic StoreX device as returned by function Initialize. |
| i\_intScanHeight \[in]    | integer\&nbps; \[100..1000] | Barcode scan height in increments. Higher numbers mean higher scan levels.          |

