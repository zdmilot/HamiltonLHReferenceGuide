# Appendix B: Exporting File Details

Whether you save the export as a .txt or .xls, the information is presented as tab-separated values. This topic describes the basic information that is included in a .txt or .xls file export format.

For a copy of the SoftMax Pro .xml schema, contact Molecular Devices.

The first line of an export file defines the number of sections (or "Blocks") that are in the export with the following format:

![](<../../../.gitbook/assets/1 (22).png>) ##BLOCKS= _n_

where _n_ is the number of sections that are in the export file.

The software exports the sections you select to export in the sequence that they display in the document.

Each section displays the following:

![](<../../../.gitbook/assets/2 (23).png>) Header line

The header line displays the section type: Note, Plate, or Group, and the title of the section you define in the document. Plate sections header lines contain additional information.

![](<../../../.gitbook/assets/3 (24).png>) Data lines

The data lines follow the header line and contain the text or data from the section. The layout and format of the data lines depend on the section type, export type, read mode, and read type.

![](<../../../.gitbook/assets/4 (21).png>) End line

The end line of each section is displays the text: **\~End**

The final line of an export file contains a single field with the original name of the export file,and the date and time the file was last saved.
