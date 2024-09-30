# CO-RE 96 Head pattern mode limitations

CO-RE 96 Head steps can be used with different tip pattern modes.

&#x20;

The tip pattern chosen must correspond to the physical labware.

&#x20;

The sort of labware differs between CO-RE 96 Head Tip Pick Up and the other CO-RE 96 Head steps. For CO-RE 96 Head Tip Pick Up only one sort of labware is correct, for the other CO-RE 96 Head steps a multiple of sort direction is allowed.

&#x20;

_**Important:** Do not use tip racks with a border if you select any other mode besides (0) All !_

&#x20;

Depending on the pattern mode selected, the corresponding deck positions around the current tip rack must be left free (see pictures below).

&#x20;

|                                   | This area must be free (Width of CO-RE 96 Head) |
| --------------------------------- | ----------------------------------------------- |
| This area must be free (5 tracks) |                                                 |

&#x20;

&#x20;

| This area must be free (Width of CO-RE 96 Head) |                                   |
| ----------------------------------------------- | --------------------------------- |
|                                                 | This area must be free (5 tracks) |

&#x20;

&#x20;

#### CO-RE 96 Head pattern mode: (0) All

&#x20;

_Restrictions / Notes_

* Labware sort: 96 (or a multiple of 96) positions in a raster of x = 9mm and y = 9 mm
* Used sequence position: 96

&#x20;

| Used head pattern | Sequence sort for **CO-RE 96 Head Tip Pick Up**                                      | Sequence sort for other **CO-RE 96 Head steps**                                      |
| ----------------- | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ |
|                   |   **Sort:** Row - or column - sorted starting on a corner.       **Free area:** none |   **Sort:** Row - or column - sorted starting on a corner.       **Free area:** none |

&#x20;

&#x20;

#### CO-RE 96 Head pattern mode: (1) One channel

&#x20;

_Restrictions / Notes_

* Labware positions in a raster of x = 9mm and y = 9 mm
* Used sequence position: 1

&#x20;

| Selected head pattern | Sequence sort for **CO-RE 96 Head Tip Pick Up**                                                                          | Sequence sort for other **CO-RE 96 Head steps**                                                             |
| --------------------- | ------------------------------------------------------------------------------------------------------------------------ | ----------------------------------------------------------------------------------------------------------- |
|                       |   **Sort:** Row - or column - sorted starting on corner A1 of labware.       **Free area:** Left and rear of labware.    |   **Sort:** Row - or column - sorted starting on a corner.       **Free area:** Left and rear of labware.   |
|                       |   **Sort:** Row - or column - sorted starting on corner H1 of labware.       **Free area:** Left and front of labware.   |   **Sort:** Row - or column - sorted starting on a corner.       **Free area:** Left and front of labware.  |
|                       |   **Sort:** Row - or column - sorted starting on corner H12 of labware.       **Free area:** Right and front of labware. |   **Sort:** Row - or column - sorted starting on a corner.       **Free area:** Right and front of labware. |
|                       |   **Sort:** Row - or column - sorted starting on corner A12 of labware.       **Free area:** Right and rear of labware.  |   **Sort:** Row - or column - sorted starting on a corner.       **Free area:** Right and rear of labware.  |

&#x20;

&#x20;

#### CO-RE 96 Head pattern mode: (2) Row(s)

&#x20;

_Restrictions / Notes_

* Labware positions in a raster of x = 9mm and y = 9 mm
* Used sequence positions: n x 12 ( n = number of activated rows. A row is activated if at least one channel is selected )

&#x20;

| Selected head pattern | Sequence sort for **CO-RE 96 Head Tip Pick Up**                                                        | Sequence sort for other **CO-RE 96 Head steps**                                                   |
| --------------------- | ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------- |
|                       |   **Sort:** Row sorted starting on corner A1 or A12 of labware.       **Free area:** Rear of labware.  |   **Sort:** Row - or column - sorted starting on a corner.       **Free area:** Rear of labware.  |
|                       |   **Sort:** Row sorted starting on corner H1 or H12 of labware.       **Free area:** Front of labware. |   **Sort:** Row - or column - sorted starting on a corner.       **Free area:** Front of labware. |

&#x20;

&#x20;

#### CO-RE 96 Head pattern mode: (3) Column(s)

&#x20;

_Restrictions / Notes_

* Labware positions in a raster of x = 9mm and y = 9 mm
* Used sequence positions: n x 8 ( n = number of activated columns. A column is activated if at least one channel is selected )

&#x20;

| Selected head pattern | Sequence sort for **CO-RE 96 Head Tip Pick Up**                                                            | Sequence sort for other **CO-RE 96 Head steps**                                                   |
| --------------------- | ---------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------- |
|                       |   **Sort:** Column sorted starting on corner A1 or H1 of labware.       **Free area:** Left of labware.    |   **Sort:** Row - or column - sorted starting on a corner.       **Free area:** Left of labware.  |
|                       |   **Sort:** Column sorted starting on corner A12 or H12 of labware.       **Free area:** Right of labware. |   **Sort:** Row - or column - sorted starting on a corner.       **Free area:** Right of labware. |

&#x20;

&#x20;

[_k_](https://www.helpndoc.com/step-by-step-guides/how-to-convert-a-word-docx-file-to-an-epub-or-kindle-ebook/)
