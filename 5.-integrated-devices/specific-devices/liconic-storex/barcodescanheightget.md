# BarcodeScanHeightGet

## Description

This function is used to retrieve the current barcode scan height of the device.

Use function BarcodeScanHeightSet to set the height.

## Syntax

BarcodeScanHeightGet (variable i\_intModuleIDStore,

variable& o\_intScanHeight)

## Arguments

| **argument**              | **value**       | **description**                                                                     |
| ------------------------- | --------------- | ----------------------------------------------------------------------------------- |
| i\_intModuleIDStore \[in] | integer \[0..3] | Unique identifier for the Liconic StoreX device as returned by function Initialize. |
| o\_intScanHeight \[out]   | integer         | Barcode scan height in increments. Higher numbers mean higher scan levels.          |
