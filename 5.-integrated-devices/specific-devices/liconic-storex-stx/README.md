# LiCONiC StoreX STX

## StoreX Instruments

The StoreX Series is the first compact Climate Storage with Integrated Handling that covers the whole range of climates in laboratory applications. The StoreX Series not only covers a wide temperature range, it also offers storage and processes from ultra-dry to extreme humidity. A variety of gas options are available.&#x20;

The modular mechanical design in combination with extremely simple commands eases the integration of StoreX into any environment. A growing number of accessories are available for the StoreX Series. The combination of environmentally controlled _Stor_age and Automatic Plate _Ex_change Capability make StoreX the _Rex_ (Latin: king) of storage in laboratory applications.&#x20;

## LiCONiC StoreX Features

All StoreX units have the same compact dimensions. StoreX has a user front door which allows comfortable and easy access for manual operation. The internal glass door allows visual inspection of the content and operation of the system without disturbing the internal climate. Removable stackers make the use of the StoreX even simpler and more efficient. Stackers are available for all common plate types.

<figure><img src="../../../.gitbook/assets/image (5).png" alt=""><figcaption></figcaption></figure>

## The StoreX 40 Handler

Inside the StoreX climate chamber there is a handling system that allows random transport of plates. Plates can be moved internally as well as transferred to and from the environment. Access times are short and the internal climate is kept stable even for short time periods between accesses.

<figure><img src="../../../.gitbook/assets/image (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

A Handler (4) is used for vertical transport as well as loading and unloading of samples. The Handler consists of a Vertical Positioning Drive (40), a Turn Drive (42) and a Shovel Drive (43). The Handler has a number of vertical positions which are determined by the number of stacker levels and the loading or unloading level.&#x20;

A Stepper motor is used for vertical positioning of the Handler. All vertical positions are defined by a z-Initiator (15) and the software z-Offset (DM20). The level height is determined by the number of steps of height. The actual travel path to a certain stacker level is calculated by multiplying the level (DM5) by the pitch (DM21) and then adding the z-Offset (DM20). The z-positions of the Transfer Station are stored in Data Memories (DM22, DM24).&#x20;

The Handler is not only used for vertical transport of the samples, it is also used to pick and place plates in the stackers and to get from, or put plates on the Transfer Station. The pick / place and get / put actions are vertical movements with the extended shovel. Beware of the difference in vertical travel for pick / place movement (DM21), get movement (DM26) and put movement (DM28).&#x20;

The Turn Drive is used to face the Shovel towards the Transfer Station or towards the desired stacker. The Turn Drive may be positioned at three turn positions. The position at the left stacker is stored in Data Memory DM80, the turn position at the right in Data Memory DM81 and the turn position at the Transfer Station is stored in Data Memory DM82.&#x20;

The radial Shovel motion is between two hard stops. Force and speed of this drive is controlled by the hardware of the controller card. Speed and force can be adjusted by authorized service personnel.&#x20;

The correct sequence of motions is monitored by initiators, by detecting the end-positions of motions. Initiators are foreseen for Shovel-In (11) and Shovel-Out Position (12) and Turn Save Range (13).&#x20;

For save operation, Gate-Open and Gate-Close Positions are detected. The Gate may only be closed when the Turn Save Initiator is active indicating the Handler is turned in.&#x20;

The Transfer Station is the location where the samples are taken by or put on by the StoreX and the surrounding system. The Transfer Station acts as the common loading / unloading position of the StoreX and the surrounding system. There are several different types of Transfer Stations. This will allow simple integration of the StoreX toany existing system.&#x20;

## The StoreX Carrousel Handler

Inside the StoreX climate chamber of higher capacity instruments there is a handling system that includes a positionable carrousel thus allowing random access and transport of plates. Plates can be moved internally as well as transferred to and from the environment. Access times are short and the internal climate is kept stable even for short time periods between accesses.

<figure><img src="../../../.gitbook/assets/image (2) (1) (1).png" alt=""><figcaption></figcaption></figure>

A Handler is used for vertical transport as well as loading and unloading of samples. The Handler consists of a Vertical Positioning Drive, a Turn Drive and a Shovel Drive an a Rotating Drive. The Handler has a number of vertical positions which are determined by the number of stacker levels and the loading or unloading level.

## N-Way Decontamination

This feature is a combination of Liconel and the Steam Injection option. Since full chambers of copper or Liconel are rather expensive, this option may be a cost-effective contamination prevention solution.&#x20;

N-Way uses Liconel alloy in critical section of the chamber where cleaning is not easily possible. Additional to that the Steam Injection is included. The advantage of the Steam Injection is to provide sterile humidity and no water pond at the bottom of the unit.&#x20;



{% file src="../../../.gitbook/assets/STX_V0713-2.pdf" %}

