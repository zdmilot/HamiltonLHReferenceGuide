# StackerConfigurationGet

## Description

This function is used to retrieve the stacker configuration of the Liconic StoreX device.

Use function StackerConfigurationSet to set the stacker configuration.

## Syntax

StackerConfigurationGet (variable i\_intModuleIDStore,

variable& o\_intNumberOfStackers, variable& o\_arrIntNumberOfLevels\[])

## Arguments

| **argument**                   | **value**        | **description**                                                                          |
| ------------------------------ | ---------------- | ---------------------------------------------------------------------------------------- |
| i\_intModuleIDStore \[in]      | integer \[0..3]  | Unique identifier for the Liconic StoreX device as returned by function Initialize.      |
| o\_intNumberOfStackers \[out]  | integer          | Number of stackers available in the device.                                              |
| o\_arrIntNumberOfLevels \[out] | array of integer | Array of size _o\_intNumberOfStackers_ containing the number of levels for each stacker. |
