# Sequences

1.
   1.  Sequences Definition

       VENUS Software uses sequences for pipetting, transport, tip handling etc.

       A sequence is a list that specifies the order of execution. A sequence contains three columns:

       Index - column that identifies each sequence position.

       Labware ID - specifies the labware on which the position is defined (e.g. Plate) Position ID - container on which the sequence position is defined (e.g. Well A1) Refer to the example shown below.

       ![image](../../.gitbook/assets/Image\_336.gif)

       HAM\_DW\_12\_ml\_0001

Example:

\


![image](../../.gitbook/assets/Image\_337.gif)

Almost every action of an instrument needs two sequences: a source and a target sequence. This is true for pipetting from an aspirate to a dispense sequence, when transporting labware from the getPlate sequence to the placePlate sequence, when coupling tips from the pickup sequence and ejecting it to the waste sequence etc.

Pointers:

Every sequence (such as the ones shown below) has three pointers which may change during a run:

* Current position (which is the _next available_ position in the sequence)
* End position (the _last position_ to be used)
*   Total number of elements (the overall length of the sequence)

    Consider this Example:

    \


    ![sequence](../../.gitbook/assets/Image\_338.gif)

    1 2 3 4 5 6 7 8 9 10 11 12

    ![image](../../.gitbook/assets/Image\_339.png) ![image](../../.gitbook/assets/Image\_340.png) ![image](../../.gitbook/assets/Image\_341.png)

    Current Position End Position Total Elements

    \


    Within the method, all three pointers may be modified or requested through the appropriate functions.

    | A default sequence is created automatically when plates or tube racks are placed on the deck. The sorting of these sequences is depending on the selected stamp tool. |
    | --------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
    | <p><br></p><p>Having for instance, the stamp tool for the CO-RE 96 Probe Head activated, the default sequence will be optimized to be processed with this head.</p>   |

    \


    ![image](../../.gitbook/assets/Image\_342.jpg)

    ![image](../../.gitbook/assets/Image\_343.png)

    Cos\_384\_Sq\_0001

Custom sequences can be defined graphically in two ways:

1. By clicking on each appropriate well on the plate or tube rack
2.  By using the rubber band zoom

    In both ways, the current selected “Stamp Tool” is used to sort the added position.

    \


    Example:

    On the STAR, an action to aspirate samples from tubes and dispense into microplates in a manner that will be free of contamination – in which case disposable tips will be preferred.

    The example describes such a method:

    \


    Method: 1. Pick up Tips

    1. Aspirate from Samples
    2. Dispense to Plates
    3. Eject to Waste

\


![image](../../.gitbook/assets/Image\_344.png)

Sample Carrier Tip Carrier Plate Carrier

Tracks

Samples

\


Tips

\


Plates

\


Waste

Definitions

* A Method describes operations on sequences.
* A Deck Layout describes the physical positions of labware on the instrument deck.
* A Labware item describes the geometry of parts which can be dealt with as a whole, such as the wells of a Microplate, or which can be combined on the deck, such as a carrier holding several plates.
* A Sequence describes the order in which labware positions are to be processed on the instrument’s deck.

\


Advantage of Using Sequences

The advantage of working with sequences is the unrivalled flexibility.

[As described in the ](Sequences.md#bookmark128)[Section 5.3 System Deck](Sequences.md#bookmark128), VENUS Software obtains the coordinates of the pipetting spots out of sequences.

In an example of a 96-well Microplate and the 8-Pipetting Channel STAR, the default pipetting order is:

\


| <p>1st pipetting: 2nd pipetting: 3rd pipetting: 4th pipetting:</p><p>…</p> | <p>A1; B1; C1; D1; E1; F1; G1; H1 ( = column 1) A2; B2; C2; D2; E2; F2; G2; H2 ( = column 2) A3; B3; C3; D3; E3; F3; G3; H3 ( = column 3) A4; B4; C4; D4; E4; F4; G4; H4 ( = column 4)</p><p>…</p> |
| -------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |

![MTP](../../.gitbook/assets/Image\_345.jpg)

[Because labware is represented by a sequence (refer to ](Sequences.md#bookmark129)Section 5.4 Sequences) there is the ability to change the order of the pipetting steps, for example:

* Excluding of complete columns or single wells
* Sorting the pipetting spots by the characteristics of the: x-/y- coordinates, Position ID, etc.

Another advantage of the sequence philosophy is the possibility of merging several sequences like in the case of reformatting four 96-well Microplates to one 384-well Microplate.

Now all of the pipetting spots of the 96-well plates are merged into one sequence.

Only one pipetting step is now needed because of merging the 96-well Microplates to one source sequence.

\


![image](../../.gitbook/assets/Image\_346.jpg)

The programming of the reformatting steps then becomes much easier. Within only one pipetting step, all wells of the four 96-well Microplates can be transferred to the 384-well Microplate.

\


1.
