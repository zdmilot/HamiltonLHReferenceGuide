# Wrong configuration file

### Instrument configuration error

The instrument configuration in the configuration file does not match the physical instrument’s configuration or deck definition.

&#x20;

**Depending of error, check following settings:**

* Wrong setting of front cover; expected 1, received 0.\
  Cover locking is activated, cover on Instrument must be set to available.
* Default waste for channel is missing.\
  The default waste for channel is not found on deck.\
  \
  Check 'Labware Data' for a channel tip waste labware which must have the following settings:

| MlStarIsDefaultWasteRack | 1 |
| ------------------------ | - |
| MlStarIsWasteRack        | 1 |

&#x20;

* Default waste for C0-RE 96 Head is missing.\
  The default waste for channel is not found on deck.\
  \
  Check 'Labware Data' for a CO-RE 96 Head tip waste labware which must have the following settings:

| MlStarIsDefaultWasteRack | 1 |
| ------------------------ | - |
| MlStarIsCore96WasteRack  | 1 |

&#x20;

For more information read also Definition of labware properties.

&#x20;

&#x20;

**If one of the following error occurs please call the service technician.**

* Wrong setting of instrument max deck trays; expected X, received Y.\
  The count of max deck tracks doesn't correspond with the count of instrument max deck tracks.
* Wrong setting of max loading trays; expected X, received Y.\
  The count of auto load tracks doesn't correspond with the count of instrument loading tracks.
* Wrong setting of instrument eject position; expected X, received Y.\
  The X value for special movement on tip eject procedure doesn't correspond with the value from instrument.

&#x20;

&#x20;

***

_Created with the Personal Edition of HelpNDoc:_ [_Make Help Documentation a Breeze with a Help Authoring Tool_](https://www.helpauthoringsoftware.com/articles/what-is-a-help-authoring-tool/)
