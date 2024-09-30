# Identify error dialog

## Dialog: Load Carrier - Identify error

Error occurs during a Load Carrier step.

&#x20;

The following recovery action can be performed with this step:

&#x20;

| **Error**                  | **Recovery Button** | **Recovery Description**                                                                                                                                                    |
| -------------------------- | ------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Hardware Error             | Repeat              | The step will be repeated. Needs a user action (on walk away mode too).                                                                                                     |
|                            |                     |                                                                                                                                                                             |
| No Carrier Error           | Repeat              | The step will be repeated.                                                                                                                                                  |
|                            |                     |                                                                                                                                                                             |
| No Carrier Barcode Error   | Repeat              | The step will be repeated. If labware property MlStarBarcodeReadSpeed is not defined or higher than 40 mm/s for the carrier to be loaded, the speed will be set to 40 mm/s. |
|                            | Continue            | The current step will be terminated with no error and the run continues.                                                                                                    |
|                            | Barcode             | An entry dialog, for type in the carrier barcode, will be displayed. If this recovery set as default, the Insert barcode dialog is viewing without timeout.                 |
|                            |                     |                                                                                                                                                                             |
| Wrong Carrier Error        | Repeat              | The step will be repeated.                                                                                                                                                  |
|                            | Continue            | The current step will be terminated with no error and the run continues.                                                                                                    |
| Barcode Not Unique Error   | Continue            | The current step will be terminated with no error and the run continues.                                                                                                    |
|                            | Repeat              | The step will be repeated.                                                                                                                                                  |
| Barcode Already Used Error | Continue            | The current step will be terminated with no error and the run continues.                                                                                                    |
|                            | Repeat              | The step will be repeated.                                                                                                                                                  |
| Delimiter Error            | Continue            | The barcode read is set to empty and the step will continue without error. The empty barcode is tracked with error.                                                         |
|                            | Repeat              | The step will be repeated. This recovery makes only sense if another carrier with a correct barcode will be loaded.                                                         |

&#x20;

All other errors.

&#x20;

For the general use and meaning of the other errors and controls see General Error Dialogs.

For the general use and meaning of the step result string and error ID's see General step result format.

