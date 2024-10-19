# DataMemoryWrite

## Description

This function is used to set a new value for a data element of a Liconic StoreX device.

Data elements are values stored into the internal memory of the device - they are used to control the device and its behavior.

Setting values may have an instant influence on the behavior of the device and may damage it !

## Syntax

DataMemoryWrite (variable i\_intModuleIDStore,

variable i\_strAddress, variable i\_strValue)

## Arguments

| **argument**              | **value**       | **description**                                                                                                           |
| ------------------------- | --------------- | ------------------------------------------------------------------------------------------------------------------------- |
| i\_intModuleIDStore \[in] | integer \[0..3] | Unique identifier for the Liconic StoreX device as returned by function Initialize.                                       |
| i\_strAddress \[in]       | string          | <p>Address of the data element to retrieve.</p><p>See the device documentation for details on the existing addresses.</p> |
| i\_strValue \[in]         | string          | <p>New value for the data element.</p><p>See the device documentation for details on the value range.</p>                 |
