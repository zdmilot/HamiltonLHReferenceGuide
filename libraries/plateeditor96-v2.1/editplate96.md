# EditPlate96()

This submethod shows a GUI to select wells in a 96 plate, and returns a sequence sorted A1,B1,C1... with the wells selection.

NOTE: The submethod requires a sequence (i\_OriginalPlateSeq) of the original full plate. This won´t be modified and it´s only used to get the labware ID of the plate.

Parameters:

\- o\_SeqEdit \[out]: Sequence  Returned plate sequence with selected wells

\- i\_OriginalPlateSeq \[in]: Sequence  Sequence of the full 96 plate (won´t be modified)
