# Labware Properties

Within the labware, some flags and settings (labware properties) are defined to determine handling of the labware elements. Labware properties should not be changed by the user although they are accessible.&#x20;

These properties can be divided up into the following groups:&#x20;

• Information for the handling with the Autoload unit&#x20;

• Information for the accessories like tip handling, waste, etc.&#x20;

• Information to support the reduction of selection during edit time.&#x20;

\


Structure&#x20;

The properties always combine a key name and a value. The key names are case-sensitive. All values are in integers (no decimal points).

To find the following tables, right click an easy step and select “what’s this”. Click “miscellaneous” to expand and finally choose “Definion of labware properties”.

<figure><img src="../../.gitbook/assets/image (179).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (180).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (181).png" alt=""><figcaption></figcaption></figure>

| <p>NOTE </p><p><em>At edit time, the user does not have to define the tip type in the “pick-up tip or needle” Step. The information is taken from this property.</em> </p><p><em>At edit time, the user does not have to define the tip type in the “eject tip or needle” Step.</em> </p><p><em>At edit time, the user can only select sequences out of the list of sequences with underlying racks having these properties.</em> </p><p><em>At edit time in the aspiration or dispense step, the user can only select sequences having underlying racks without these properties out of the sequence list.</em> </p><p><em>Needles can only be ejected into a rack with the property MlStarlsWasteRack and corresponding MLStarTipRack settings.</em> NOTE </p><p><em>There are only two CR wash stations allowed on the same deck.</em> </p><p><em>Each wash station must have a unique identifying number.</em> </p><p><em>At edit time during the wash step, the user can only select sequences with underlying racks having these properties out of the sequence list.</em> </p> |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |

\


## Properties for Temperature Controlled Carrier (TCC)







| <p>NOTE </p><p><em>There are only two TCCs allowed on a deck.</em> </p><p><em>At edit time in the incubator step, the user can only select sequences with underlying racks having these properties out of the sequence list.</em> </p> |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |



| Key                      | Default | Range  | Description                                                             |
| ------------------------ | ------- | ------ | ----------------------------------------------------------------------- |
| MIStarCarIsTemperated    | 0       | 0 or 1 | <p>The carrier can be temperature-controlled<br>1 = TRUE, 0 = FALSE</p> |
| MIStarCarIncubatorNumber | -       | 1 or 2 | Number of temperature incubation stations 1 or 2                        |

| <p>NOTE </p><p><em>If a carrier can be calibrated, all values should be set.</em> </p><p><em>The origin is the zero point of the zero position of the carrier (front, left, down).</em></p><p><img src="../../.gitbook/assets/image (182).png" alt=""> </p><p><em>The calibrate action is executed only if the calibrate property is set.</em></p> |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |

\
