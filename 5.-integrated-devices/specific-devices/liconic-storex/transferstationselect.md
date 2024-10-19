# TransferStationSelect

## Description

This function is used to selecte the active transfer station of the Liconic StoreX device.

This function is only valid for devices with 2 transfer stations !

## Syntax

TransferStationSelect (variable i\_intModuleIDStore,

variable i\_intTransferStation)

## Arguments

| **constant**                                        | **value** | **description**        |
| --------------------------------------------------- | --------- | ---------------------- |
| Liconic\_Store\_X::TransferStation::STATION\_IMPORT | 0         | Select import station. |
| Liconic\_Store\_X::TransferStation::STATION\_EXPORT | 1         | Select export station. |

| **argument**                 | **value**       | **description**                                                                     |
| ---------------------------- | --------------- | ----------------------------------------------------------------------------------- |
| i\_intModuleIDStore \[in]    | integer \[0..3] | Unique identifier for the Liconic StoreX device as returned by function Initialize. |
| i\_intTransferStation \[int] | integer \[0..1] | Active transfer station. Set to one of the following predefined constants:          |
