# EnvironmentSet

## Description

This function is used to set the target environment values for the Liconic StoreX device.

Use function EnvironmentGet to read current or target values.

## Syntax

EnvironmentSet (variable i\_intModuleIDStore,

variable i\_fltTemperature, variable i\_fltHumidity, variable i\_fltCO2, variable i\_fltN2)

## Arguments

| **argument**              | **value**       | **description**                                                                     |
| ------------------------- | --------------- | ----------------------------------------------------------------------------------- |
| i\_intModuleIDStore \[in] | integer \[0..3] | Unique identifier for the Liconic StoreX device as returned by function Initialize. |
| i\_fltTemperature \[in]   | float           | Target temperature in °C.                                                           |
| i\_fltHumidity \[in]      | float           | Target humidity in %rh.                                                             |
| i\_fltCO2 \[in]           | float           | Target CO2 level in % vol.                                                          |
| i\_fltN2 \[in]            | float           | Target N2 level in % vol.                                                           |
