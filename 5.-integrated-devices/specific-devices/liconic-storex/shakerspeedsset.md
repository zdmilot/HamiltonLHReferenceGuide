# ShakerSpeedsSet

## Description

This function is used to set the shaker speed(s) of a Liconic StoreX device with a shaker.

Use function ShakerSpeedsGet to retrieve the currently set speed(s), function ShakerStart to start and function ShakerStop to stop shaking.

## Syntax

ShakerSpeedsSet (variable i\_intModuleIDStore,

variable i\_arrIntShakerSpeeds)

## Arguments

| **argument**                | **value**                   | **description**                                                                                                                            |
| --------------------------- | --------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| i\_intModuleIDStore \[in]   | integer \[0..3]             | Unique identifier for the Liconic StoreX device as returned by function Initialize.                                                        |
| i\_arrIntShakerSpeeds \[in] | array of integers \[1..200] | <p>Target speed(s) for the device.</p><p>Depending on the value set using function OptionSet, this array has to contain 1 or 4 values.</p> |
