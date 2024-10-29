# EdiPlate96\_custom()

This submethod shows a GUI to select wells in a 96 plate, and returns a sequence sorted A1,B1,C1... with the wells selection.

NOTE: The submethod requires a sequence (i\_OriginalPlateSeq) of the original full plate. This won´t be modified and it´s only used to get the labware ID of the plate.

Parameters:

\- o\_SeqEdit \[out]: Sequence  Returned plate sequence with selected wells

\- i\_OriginalPlateSeq \[in]: Sequence  Sequence of the full 96 plate (won´t be modified)

\- i\_message \[in]: String  Message to show in the GUI

\- fixed\_number \[in]: Integer   If you want the user to select a fixed number of wells, give this variable a value >0. Else give it 0.

\- i\_forbiddenWellsSeq \[in]: Sequence  Sequence with the wells that the user can´t select during the plate edition.

Only positions IDs are used from this sequence, so it can refer to any labware ID. The output edited sequence (o\_SeqEdit) will be related to the labware ID of the original plate sequence (i\_OriginalPlateSeq)

\- i\_preSelectionSeq \[in]: Sequence  Sequence with the wells selected by default.

Only positions IDs are used from this sequence, so it can refer to any labware ID. The output edited sequence (o\_SeqEdit) will be related to the labware ID of the original plate sequence (i\_OriginalPlateSeq)

\- i\_Editable \[in]: Integer  1=wells editable, 0= user can´t modify wells selected.
