# ShakerSpeedsGet



## Description

This function is used to retrieve the current shaker speed(s) of a Liconic StoreX device with a shaker.

Use function ShakerSpeedsSet to set the speed(s), function ShakerStart to start and function ShakerStop to stop shaking.

## Syntax

ShakerSpeedsGet (variable i\_intModuleIDStore,

variable& o\_arrIntShakerSpeeds)

## Arguments

| **argument**                 | **value**         | **description**                                                                                                                     |
| ---------------------------- | ----------------- | ----------------------------------------------------------------------------------------------------------------------------------- |
| i\_intModuleIDStore \[in]    | integer \[0..3]   | Unique identifier for the Liconic StoreX device as returned by function Initialize.                                                 |
| o\_arrIntShakerSpeeds \[out] | array of integers | <p>Target speed(s) of the device.</p><p>Depending on the value set using function OptionSet, this array contains 1 or 4 values.</p> |
