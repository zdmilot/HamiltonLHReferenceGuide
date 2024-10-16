# StartSoftMaxPro

## Description

This function is used to start the SoftMax Pro Software.

### Syntax

```
StartSoftMaxPro(i_strFullFilePath
                i_blnGxP)
```

### Arguments

\[in] i\_strFullFilePathFully qualified path name of the software.\[in] i\_blnGxPASWGLOBAL::BOOL::TRUE if the GxP version of the software is used. this will suppress the Log On dialog that requires manual entry of user ID and password. The function [Logon](chm://03ca6a293f9ae28bd0f386a42dcd2a1a/topics/Logon.html) should be used to log the user on.

Note:

Fully qualified path name (standard edition):\
"C:\Program Files (x86)\Molecular Devices\SoftMax Pro 7.0\SoftMaxProApp.exe"

Gxp:\
"C:\Program Files (x86)\Molecular Devices\SoftMax Pro 7.0 GxP\SoftMaxProApp.exe"
