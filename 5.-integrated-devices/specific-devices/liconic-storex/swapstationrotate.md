# SwapStationRotate

| **constant**                                  | **value** | **description**          |
| --------------------------------------------- | --------- | ------------------------ |
| Liconic\_Store\_X::SwapStation::POSITION\_0   | 0         | Normal position (0°).    |
| Liconic\_Store\_X::SwapStation::POSITION\_180 | 1         | Rotated position (180°). |

## Description

This function is used to rotate the swap station of the Liconic StoreX device.

This function may only be used with a device that has a swap station !

## Syntax

SwapStationRotate (variable i\_intModuleIDStore,

variable i\_intPosition)

## Arguments

| **argument**              | **value**       | **description**                                                                           |
| ------------------------- | --------------- | ----------------------------------------------------------------------------------------- |
| i\_intModuleIDStore \[in] | integer \[0..3] | Unique identifier for the Liconic StoreX device as returned by function Initialize.       |
| i\_intPosition \[in]      | integer \[0..1] | Position to rotate the swap station to. Set to one of the following predefined constants: |
