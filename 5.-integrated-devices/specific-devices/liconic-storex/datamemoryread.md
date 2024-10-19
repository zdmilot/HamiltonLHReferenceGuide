# DataMemoryRead

## Description

This function is used to retrieve the current value of a data element of a Liconic StoreX device.

Data elements are values stored into the internal memory of the device - they are used to control the device and its behavior.

## Syntax

DataMemoryRead (variable i\_intModuleIDStore,

variable i\_strAddress, variable& o\_strValue)

## Arguments

| **argument**              | **value**       | **description**                                                                                                           |
| ------------------------- | --------------- | ------------------------------------------------------------------------------------------------------------------------- |
| i\_intModuleIDStore \[in] | integer \[0..3] | Unique identifier for the Liconic StoreX device as returned by function Initialize.                                       |
| i\_strAddress \[in]       | string          | <p>Address of the data element to retrieve.</p><p>See the device documentation for details on the existing addresses.</p> |
| o\_strValue \[out]        | string          | Current value of the data element.                                                                                        |
