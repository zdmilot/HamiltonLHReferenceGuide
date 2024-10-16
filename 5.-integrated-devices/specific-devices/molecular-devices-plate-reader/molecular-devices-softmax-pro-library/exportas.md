# ExportAs

## Description

This function is used to Export data in the Time, Columns, Plate, or XML format.

Warning The ExportAs command overwrites any existing file without warning.

### Syntax

```
ExportAs(i_strFullFilePath
         i_intExportFormat)
```

### Arguments

\[in] i\_strFullFilePathFully qualified path name of the file.\[in] i\_intExportFormatAn integer that represents an export format. See variables in the namespace 'Molecular\_Devices\_SoftMax\_Pro::ExportFormats':\


* 0 (XML), exports data in an XML file format.
* 1 (PLATE), exports data in a text matrix corresponding to a microplate grid.
* 2 (TIME), exports data in a single column of text for each well.
* 3 (COLUMN), exports data in a single column of text for each well.
