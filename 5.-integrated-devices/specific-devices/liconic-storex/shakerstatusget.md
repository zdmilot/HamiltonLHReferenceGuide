# ShakerStatusGet

| **constant**           | **value** | **description**        |
| ---------------------- | --------- | ---------------------- |
| ASWGLOBAL::BOOL::FALSE | 0         | Device is not shaking. |
| ASWGLOBAL::BOOL::TRUE  | 1         | Device is shaking.     |

## Description

This function is used to retrieve the current shaker status of the Liconic StoreX device.

## Syntax

ShakerStatusGet (variable i\_intModuleIDStore,

variable& o\_blnShakerEnabled)

## Arguments

| **argument**               | **value**       | **description**                                                                     |
| -------------------------- | --------------- | ----------------------------------------------------------------------------------- |
| i\_intModuleIDStore \[in]  | integer \[0..3] | Unique identifier for the Liconic StoreX device as returned by function Initialize. |
| o\_blnShakerEnabled \[out] | boolean         | Shaker status of the device. One of the following predefined constants:             |
