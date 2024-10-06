# Labware

The software comes with a set of definitions for the standard labware items that are most commonly used in laboratories. The carrier name and definition selected must always be identical to the name with which the physical carrier is labeled.

A carrier feature is a varying number of locations for the placement of labware, such as tip racks, microplates, etc.

For the standard carriers and their names, refer directly to the software list which is shown through an image in the next page. The list box displays the available labware names. The selected piece of labware is defined briefly on the right-hand side of the window with its corresponding picture.

The benefits of a plate carrier to the left of Track 1 are:

* Higher deck density, lower reloads
* Work positions available for Multi-Probe Heads
* Labware storage positions available for iSWAP / CO-RE Grips

\


![image](../../.gitbook/assets/Image\_347.jpg)

\


Definition

A labware item describes the geometry of objects which can be dealt with as a whole, such as the wells of a microplate, or which can be combined on the deck, such as a carrier holding several plates.

The ML STAR can be used with all kind of labware such as tubes, microplates, reagent troughs, etc. VENUS Software comes with a set of standard labware definitions.

\


![image](../../.gitbook/assets/Image\_348.jpg)

Pre-loaded Tips and Tube Carriers

In addition to plate and tip carriers, sample carriers can also be placed on the deck. These carriers are pre-loaded with tubes of a specified size (diameter and length). In fact, these carriers are racks (_.rck) in contrast to the other carriers, which are carrier templates (_.tml). The tube carriers are examples of racks which fit directly into the track grids of the ML STAR.

There are also pre-loaded racks and carriers available, for example, a tip carrier equipped with standard tips (TIP\_CAR\_480\_ST\_A00) and more.

\


Naming Convention of the ML STAR Carriers

\


Example: PLT\_CAR\_L5\_AC\_A00

\


![image](../../.gitbook/assets/Image\_349.png) ![image](../../.gitbook/assets/Image\_350.png) ![image](../../.gitbook/assets/Image\_351.png) ![image](../../.gitbook/assets/Image\_352.png)

\


| Type of Carrier                      | Construction  | Orientation | Number of                          | Labware Info                                   | Revision                                                                                                                    |    |                                        |          |
| ------------------------------------ | ------------- | ----------- | ---------------------------------- | ---------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------- | -- | -------------------------------------- | -------- |
| PLT                                  | Plate Carrier | CAR         | Standard Carrier                   | <p>L Landscape</p><p><br></p><p>P Portrait</p> | <p>Plate Positions:</p><p>3</p><p>4</p><p>5</p>                                                                             | AC | <p>Deep Well Plate</p><p>(archive)</p> | A00, A01 |
| <p><br></p>                          | <p><br></p>   | APE         | Application Engineering            | MD                                             | <p>Medium Density (96/384-</p><p>Well)</p>                                                                                  |    |                                        |          |
| <p><br></p>                          | <p><br></p>   | DAT         | <p>Deck</p><p>Adaptor Template</p> | H D                                            | <p>High</p><p>Density (1536-Well)</p>                                                                                       |    |                                        |          |
| <p><br></p>                          | <p><br></p>   | <p><br></p> | <p><br></p>                        | LI                                             | Limbro                                                                                                                      |    |                                        |          |
| <p><br></p>                          | <p><br></p>   | <p><br></p> | <p><br></p>                        | S T                                            | Stack                                                                                                                       |    |                                        |          |
| SMP Sample Carrier                   | CAR Standard  | <p><br></p> | Tubes:                             | 15x75 Tube Size                                | A00, A01                                                                                                                    |    |                                        |          |
| <p>12</p><p>16</p><p>24</p><p>32</p> |               |             |                                    |                                                |                                                                                                                             |    |                                        |          |
| TIP                                  | Tip Carrier   | CAR         | Standard Carrier                   | <p>L Landscape</p><p><br></p><p>P Portrait</p> | <p>1000µl-channel:</p><p>288</p><p>384</p><p>480</p><p>5ml tips:</p><p>72</p><p>96</p><p>120</p><p>384 Head:</p><p>1920</p> | LT | Low Volume 10ul                        | A00, A01 |
| <p><br></p>                          | <p><br></p>   | <p><br></p> | <p><br></p>                        | 50µl                                           | 50µl Tip                                                                                                                    |    |                                        |          |
| <p><br></p>                          | <p><br></p>   | <p><br></p> | <p><br></p>                        | ST                                             | Standard Vol. 300µl                                                                                                         |    |                                        |          |
| <p><br></p>                          | <p><br></p>   | <p><br></p> | <p><br></p>                        | HT                                             | High Volume 1000µl Filter                                                                                                   |    |                                        |          |
| <p><br></p>                          | <p><br></p>   | <p><br></p> | <p><br></p>                        | 5ml T                                          | 5ml Tip Size                                                                                                                |    |                                        |          |
| <p><br></p>                          | <p><br></p>   | <p><br></p> | <p><br></p>                        | BC                                             | Bar-Coded Tip Rack                                                                                                          |    |                                        |          |
| <p><br></p>                          | <p><br></p>   | <p><br></p> | <p><br></p>                        | NT R                                           | Nestable Tip Rack                                                                                                           |    |                                        |          |
| RGT Reagent                          | CAR Standard  | <p><br></p> | Reagent troughs: 3, 4, 5           | R Reagent                                      | A00, A01                                                                                                                    |    |                                        |          |
| CTR Control Carrier                  | <p><br></p>   | <p><br></p> | <p><br></p>                        | C Controls                                     | A00, A01                                                                                                                    |    |                                        |          |
| VER Verification                     | <p><br></p>   | <p><br></p> | <p><br></p>                        | <p><br></p>                                    | A00, A01                                                                                                                    |    |                                        |          |

1.  #### ‌Types of Labware‌

    \


    Containers

    Containers are vessels which hold liquids. They are usually placed in racks. They can also be placed directly onto the carriers, which is the case with reagent containers. An example for containers would be the tubes or the wells of a Microplate.

    The filename has the extension “.ctr”.

    \


    ![Originalbild anzeigen](../../.gitbook/assets/Image\_353.gif)

    NOTE

    Pipetting is only done into containers! Sequences can be created on containers only!

    CO-RE tips and needles are also defined as containers.

    \


    Rectangular Racks and Plates

    Rectangular racks are specialized grids for holding containers (or tips) in row and column order. A Microplate is a rack in this circumstance and the wells represent as containers. The rack is therefore a template describing a discrete number of positions for holding containers (or tips).

    Examples of racks include a tube rack, a Microplate, a microtiter strip, a deep-well plate, and a tip rack.

    The filename has the extension “.rck”.

    Circular Racks

    Circular racks are specialized grids for holding containers in a segment of a circle. The filename has the extension “.crk”.
2.  #### ‌Reference Position‌

    \


    The command dialogs always use the container bottom as a reference position (fixed height, liquid level = 0).

    The x, y, z values of the reference well (usually A1 or #1) stored in the instrument’s system of coordinates are shown in the “Adjust Labware Position” Dialog.

    To access this dialog:

    1. Switch to the System Deck Editor.
    2. Select the labware (Plate, TipRack etc.) to be used.
    3. Right click on the labware item to enter the Context Menu.
    4. Select “Adjust Location”.
    5. The dialog box shown below will appear.

    \


    ![image](../../.gitbook/assets/Image\_354.jpg)
3.  #### ‌Height Parameters‌

    \


    Both the rack and the container have clearance heights. This is the minimal height at which the pipetting channels must pass over the labware so that their movement is not blocked by the labware. The software automatically takes the highest clearance height.

    The maximum pipetting height is the deepest position the tip or needle can be placed inside a well. It is counted from the bottom of the container upwards and determines the dead volume of the container.

    The LLD search height is the height at which the speed of the pipetting channel is reduced to look for the liquid surface.

    \


    ![image](../../.gitbook/assets/Image\_355.png)

    Container

    Rack

    I

    Carrier

    E F B C D A H G

    Z positions of carriers, racks and containers

    Container:

    \


    | A: | Clearance height           |
    | -- | -------------------------- |
    | B: | LLD search height          |
    | C: | Maximum pipetting height   |
    | D: | Container bottom thickness |

    Rectangular Rack:

    \


    | E: | Total calculated clearance height         |
    | -- | ----------------------------------------- |
    | F: | Distance from rack base to container base |

    Carrier (Template):

    \


    | G: | Clearance height                             |
    | -- | -------------------------------------------- |
    | H: | Origin Z (also called “Base Offset”)         |
    | I: | Snap to site of base of rack or to container |

    Regarding the z position, two different cases of rack placement on the deck can be distinguished in the STAR which is controlled by the switch “I” in the sketch above:

    * Snap to base of rack
    * Snap to base of container

    These two cases are described in detail on the next page.

    A “Container-Based” Rack is placed with the container bottom directly on the carrier (e.g. the microplates on a plate carrier):

    \


    ![image](../../.gitbook/assets/Image\_356.png)

    Container

    Rack

    Z 0

    I

    Carrier

    ZDeck = 100mm

    D H

    \


    The reference position Z0 is the lowest position in the well. Here, the reference height is calculated from

    Z0 = Zdeck+Zcarrier+Zthick , Zdeck is fixed at 100mm,

    Zthick (D) is defined in the container labware,

    Zcarrier (H) is defined in the carrier template definition.

    A “Rack-Based” Rack is placed with the frame on the instrument deck (e.g., a tube rack, where Zcarrier (H) = 0, because the tube rack is used directly as a carrier)

    \


    ![image](../../.gitbook/assets/Image\_357.png)

    Container

    Rack

    Z 0

    I

    Carrier

    ZDeck = 100mm

    D H

    \


    The reference position Z0 is the lowest position in the well. The reference height is calculated using: Z0 = Zdeck+Zcarrier+Zbasediff+Zthickness

    Zdeck is a fixed quantity

    Zcarrier (H) is defined in the carrier definition

    Zbasediff (F) is defined in the rectangular rack labware Zthickness (D) is defined in the container labware
