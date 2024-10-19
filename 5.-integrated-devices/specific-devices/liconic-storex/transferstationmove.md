# TransferStationMove

## Description

This function is used to move the plate shovel of the selected transfer station of the Liconic StoreX device.

Use function TransferStationSelect to select the active transfer station.

## Syntax

TransferStationMove (variable i\_intModuleIDStore,

variable i\_intPosition)

## Arguments

| Liconic\_Store\_X::TransferStation::POSITION\_1 | 0 | <p>Move to</p><p>position 1 (extracted).</p> |
| ----------------------------------------------- | - | -------------------------------------------- |
| Liconic\_Store\_X::TransferStation::POSITION\_2 | 1 | <p>Move to</p><p>position 2 (retracted).</p> |

| **argument**              | **value**       | **description**                                                                     |
| ------------------------- | --------------- | ----------------------------------------------------------------------------------- |
| i\_intModuleIDStore \[in] | integer \[0..3] | Unique identifier for the Liconic StoreX device as returned by function Initialize. |
| i\_intPosition \[int]     | integer \[0..1] | Position to move to. One of the following predefined constants:                     |
