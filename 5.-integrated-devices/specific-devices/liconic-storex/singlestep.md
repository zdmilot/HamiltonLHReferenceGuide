# SingleStep

## Description

This function is used to execute single steps on the Liconic StoreX device.

These single steps are helpful for error cases where it is necessary to execute single movements to get out of a blocking situation (i.e. a plate on the shovel from a previous error condition).

The movements are execute in a very raw format (without sensor supervision) and should therefore not be used for routine work !.

### Syntax

```
SingleStep (variable i_intModuleIDStore,
            variable i_intStep,
            variable i_intStacker,
            variable i_intLevel)
```

### Arguments

| argument                  | value             | description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| ------------------------- | ----------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| i\_intModuleIDStore \[in] | integer \[0..3]   | Unique identifier for the Liconic StoreX device as returned by function [Initialize](chm://c6eee35ebc6f05b6562520699a23e565/topics/Initialize.html).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| i\_intStep \[out]         | integer \[1..4]   | <p>Single step to execute. Set to one of the following predefined constants:<br><br></p><table><thead><tr><th>constant</th><th>value</th><th>description</th></tr></thead><tbody><tr><td>Liconic_Store_X::SingleStep::PlateIn</td><td>1</td><td>Pick plate from transfer station to plate handler shovel.</td></tr><tr><td>Liconic_Store_X::SingleStep::PlateOut</td><td>2</td><td>Place plate from plate handler shovel to transfer station.</td></tr><tr><td>Liconic_Store_X::SingleStep::PlaceToStacker</td><td>3</td><td>Place plate from plate handler shovel to selected level of selected stacker.</td></tr><tr><td>Liconic_Store_X::SingleStep::PickFromStacker</td><td>4</td><td>Pick plate from selected level of selected stacker to plate handler shovel.</td></tr></tbody></table> |
| i\_intStacker \[in]       | integer \[1..100] | Number of the stacker to use.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| i\_intLevel \[in]         | integer \[1..200] | Number of the level to use.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |

\
