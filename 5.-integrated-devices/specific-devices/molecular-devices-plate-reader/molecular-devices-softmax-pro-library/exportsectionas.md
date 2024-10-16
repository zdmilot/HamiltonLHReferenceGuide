# ExportSectionAs

## Description

This function is used to Export the currently selected section in the Time, Columns, Plate, or XML format.

### Syntax

```
ExportSectionAs(i_strFullFilePath,
                i_intExportFormat,
                i_blnAppend)
```

### Arguments

\[in] i\_strFullFilePathFully qualified path name of the file.\[in] i\_intExportFormatAn integer that represents an export format. See variables in the namespace 'Molecular\_Devices\_SoftMax\_Pro::ExportFormats':\


* 0 (XML), exports data in an XML file format.
* 1 (PLATE), exports data in a text matrix corresponding to a microplate grid.
* 2 (TIME), exports data in a single column of text for each well.
* 3 (COLUMN), exports data in a single column of text for each well.

\[in] i\_blnAppendASWGLOBAL::BOOL::TRUE to append the data to an existing file.

Warning If append is set to ASWGLOBAL::BOOL::FALSE, the command will overwrite any existing file without warning.

\
\
