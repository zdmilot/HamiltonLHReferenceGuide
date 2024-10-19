# ShakerStop

## Description

This function is used to stop the shaker of a StoreX device.

Not all devices support shaking !

Use function ShakerSpeedsGet to retrieve the currently set speed(s), function ShakerSpeedsSet to set the speed(s) and function ShakerStart to start shaking.

## Syntax

ShakerStop (variable i\_intModuleIDStore)

## Arguments

| **argument**              | **value**       | **description**                                                                     |
| ------------------------- | --------------- | ----------------------------------------------------------------------------------- |
| i\_intModuleIDStore \[in] | integer \[0..3] | Unique identifier for the Liconic StoreX device as returned by function Initialize. |
