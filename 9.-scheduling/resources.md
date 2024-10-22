# Resources

## Giving Scheduler the information it needs: WHAT’s being used

•       Resources are devices that share identical operations

•       Can be single devices with multiple positions (i.e.. Incubator) or multiple identical devices

•        The total number of tasks that a resource can handle simultaneously is referred to as capacity

&#x20;

| <img src="../.gitbook/assets/image (27) (1).png" alt="" data-size="original">                                                              | <img src="../.gitbook/assets/image (28) (1).png" alt="" data-size="original">                       |
| ------------------------------------------------------------------------------------------------------------------------------------------ | --------------------------------------------------------------------------------------------------- |
| A bank of Heater Shakers has a capacity of 1 per unit. Note – different temperature set points could mean splitting to different resources | The instrument ML\_STAR (or Vantage in VoV) counts as Capacity=1, which includes all arm components |



## Setting

### Deck Layout

*

    <figure><img src="../.gitbook/assets/image (30) (1).png" alt=""><figcaption></figcaption></figure>
* Right click -> Add/Edit Resources

### Resource Properties

<figure><img src="../.gitbook/assets/image (31) (1).png" alt=""><figcaption></figcaption></figure>

* Assign Properties
* Images are useful for method organization
* Mapping Resource Units
  * 1 Capacity = 1 Unit
  * Can be Mapped to a string name, numeric (flt or int), or assigned to a sequence, or left empty
* _Scheduler ensures that unit assignments are maintained between method instances_

&#x20;

## &#x20;Considerations

<figure><img src="../.gitbook/assets/image (33).png" alt=""><figcaption></figcaption></figure>

Keep in mind

* Resources will not be visible, but will appear in a methods Variable's view
* Not all plate locations require a resource – ambient deck positions can be omitted unless timed
* Hidden resources like a hand-off position must also be included – rate limiting for internal capacity access
* Keep capacity as small as possible – excess may lead to poor scheduler performance

&#x20;
