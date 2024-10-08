# Method Building Blocks

Programming ML STAR instruments always means creating new or adapting existing methods. A method is a list of instructions for the instrument, appearing as actions, steps, transport steps, loops, user dialogs, etc.

<figure><img src="../../.gitbook/assets/image (44) (1).png" alt=""><figcaption></figcaption></figure>

The user software offers various standard step libraries such as the general steps, the pipetting steps, etc. while the ML STAR instrument software offers different levels of programming.



| <img src="../../.gitbook/assets/image (45) (1).png" alt="" data-size="original"> | **Smart Steps** combine tasks. For example, combining a complete pipetting task with a plate copy, aliquoting, pooling, etc. These commands are best for beginners to get familiar with the system. They incorporate a guided programming wizard, predefined error recoveries and customized recovery strategies. |
| -------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| <img src="../../.gitbook/assets/image (46) (1).png" alt="" data-size="original"> | **Easy Steps** are for pipetting and plate handling. They offer a wider range of settings and possibilities to handle errors than the smart steps. “Easy Steps” Icons have yellow backgrounds.                                                                                                                    |
| <img src="../../.gitbook/assets/image (47) (1).png" alt="" data-size="original"> | **Single Steps** are used when highest flexibility of the system is required. These commands allow even the most complex pipetting and plate handling tasks. Single steps have the suffix “Single Step”.                                                                                                          |

Aside from the standard step libraries, additional libraries for advanced programming are also available.&#x20;

Each method is linked to a System Deck which is an empty environment upon opening. Now, the programmer has to plot the real environment in the software by adding first a ML STAR instrument to the system deck.

<figure><img src="../../.gitbook/assets/image (48) (1).png" alt=""><figcaption></figcaption></figure>

After successfully adding a ML STAR instrument, choose between two different views in the deck editor. The first view is the System Tab which shows an external perspective of the instrument, including 3rd party components.

<figure><img src="../../.gitbook/assets/image (49) (1).png" alt=""><figcaption></figcaption></figure>

The ML\_STAR Tab shows an internal perspective of the instrument which is the deck layout. This is a graphical illustration of the work surface of the ML STAR instrument. It contains all information about the used labware and x/y/z coordinates of the positions

<figure><img src="../../.gitbook/assets/image (50) (1).png" alt=""><figcaption></figcaption></figure>

The ML STAR can be used with various kinds of labware such as: Tubes, Microplates, Reagent Troughs, etc. The software comes with a set of standard labware definitions. Labware is available by clicking the Labware Tab found in the Deck Layout Editor.

<figure><img src="../../.gitbook/assets/image (51) (1).png" alt=""><figcaption></figcaption></figure>

To allow easier access to any kind of labware, use the view selection found on the right side of the labware view window. The deck layout is displayed in 3D and can be rotated to any angle.

<figure><img src="../../.gitbook/assets/image (52) (1).png" alt=""><figcaption></figcaption></figure>

Choose among the different views:

* 3D View <img src="../../.gitbook/assets/image (53) (1).png" alt="" data-size="line">
* Front View<img src="../../.gitbook/assets/image (54) (1).png" alt="" data-size="line">
* Back View <img src="../../.gitbook/assets/image (55) (1).png" alt="" data-size="line">
* Top View <img src="../../.gitbook/assets/image (56) (1).png" alt="" data-size="line">
* Bottom View <img src="../../.gitbook/assets/image (57) (1).png" alt="" data-size="line">
* Left View <img src="../../.gitbook/assets/image (58) (1).png" alt="" data-size="line">
* Right View <img src="../../.gitbook/assets/image (59) (1).png" alt="" data-size="line">

The clipping function will allow cutting off overlaying labware from the labware placed underneath. This makes the creation of, for example, sequences very simple.

<figure><img src="../../.gitbook/assets/image (60) (1).png" alt="" width="20"><figcaption></figcaption></figure>

Please make sure that the deck view has an appropriate size at different z-heights (CVS / BVS), otherwise the clipping slider will not be shown.&#x20;

If a labware of a different or new kind must be defined, the “Labware Editor” helps in defining the new labware.
