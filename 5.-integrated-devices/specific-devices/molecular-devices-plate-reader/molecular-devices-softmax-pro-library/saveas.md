# SaveAs

## Description

This is function is used to save the current document as a data file or a protocol file.

Note Define the file type for the saved file by the file extension in the path statement. Use the \*.sda extension for data files and \*.spr for protocol files. If you are using the SoftMax Pro GxP Software, use the \*.sdax extension for data files and \*.sprx for protocol files.

Warning If a file with the same name already exists, the SoftMax Pro Software automatically overwrites the file with no warning. The SoftMax Pro GxP Software does not allow overwriting existing files, and generates an error message if an overwrite is attempted.

### Syntax

```
SaveAs(i_strFullFilePath)
```

### Arguments

\[in] i\_strFullFilePathFully qualified path and name of file to be saved, including the file extension.
