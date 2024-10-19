# HandlerSettingsGet

## Description

This function is used to retrieve the current values for the handler.

Use function OptionSet to set the values.

## Syntax

HandlerSettingsGet (variable i\_intModuleIDStore,

variable& o\_intHandlerOffsetZ,

variable& o\_intHandlerMovementPickPlace)

## Arguments

| **argument**                          | **value**       | **description**                                                                     |
| ------------------------------------- | --------------- | ----------------------------------------------------------------------------------- |
| i\_intModuleIDStore \[in]             | integer \[0..3] | Unique identifier for the Liconic StoreX device as returned by function Initialize. |
| o\_intHandlerOffsetZ \[out]           | integer         | Global handler offset for all z movements in increments.                            |
| o\_intHandlerMovementPickPlace \[out] | integer         | Handler movements in increments for pick\&place operations in the stackers.         |
