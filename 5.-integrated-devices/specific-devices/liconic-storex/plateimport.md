# PlateImport

## Description

This function is used to transport a plate from the transfer position to a position inside the StoreX device.

For security reasons, this command checks the existence of a plate on the transfer position as well as the existence of a plate at the target position.

This behavior may be changed using function OptionSet.

## Syntax

PlateImport (variable i\_intModuleIDStore,

variable i\_intStacker, variable i\_intLevel)

## Arguments

| **argument**              | **value**         | **description**                                                                                                                                                                                      |
| ------------------------- | ----------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| i\_intModuleIDStore \[in] | integer \[0..3]   | Unique identifier for the Liconic StoreX device as returned by function Initialize.                                                                                                                  |
| i\_intStacker \[in]       | integer \[1..100] | <p>Number of the stacker the plate shall be imported to.</p><p>Check the current store configuration using function StackerConfigurationGet for the number of stackers available!</p>                |
| i\_intLevel \[in]         | integer \[1..200] | <p>Number of the level inside the stacker the plate shall be imported to.</p><p>Check the current store configuration using function StackerConfigurationGet for the number of levels available!</p> |
