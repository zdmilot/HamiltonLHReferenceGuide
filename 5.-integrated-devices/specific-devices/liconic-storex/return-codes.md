# Return Codes

## Description

All functions use the following return codes:

| **constant**           | **value**    | **description**                       |
| ---------------------- | ------------ | ------------------------------------- |
| ASWGLOBAL::BOOL::TRUE  | hslTrue (1)  | The function returned successfully.   |
| ASWGLOBAL::BOOL::FALSE | hslFalse (0) | The function returned unsuccessfully. |

If a function failed with return code ASWGLOBAL::BOOL::FALSE, check the trace file for a brief description of the error.
