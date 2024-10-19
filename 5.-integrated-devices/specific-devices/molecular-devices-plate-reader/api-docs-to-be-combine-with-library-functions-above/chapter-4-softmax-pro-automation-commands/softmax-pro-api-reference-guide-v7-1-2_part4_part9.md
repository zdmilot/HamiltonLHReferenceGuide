# ExportSectionAs

Int32 ExportSectionAs(String path, ExportAsFormat exportAsFormat, Bool append) The ExportSectionAs command exports an experiment section.

Parameters\
path

Type: String

Fully qualified path name\
exportAsFormat

Type: ExportAsFormat

TIME exports data in a single column of text for each well.

COLUMNS exports data in a single column of text for each well.

PLATE exports data in a text matrix that corresponds to a plate grid.

XML exports data in an XML file format.\
append

Type: Boolean

Specify whether to append the data to an existing file.

If append is set to false, the command overwrites any existing file without warning.
