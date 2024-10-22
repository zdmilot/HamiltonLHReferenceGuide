# Step Return Format

**“BLOCK” return Format**

* Blocks are consistent **groups** of information for the step – starting with a **left bracket \[**, then delineated by commas
* Analogous to **lines in a file**, multiple blocks may be present, and will be consistent in data returned
* An **Error Flag** will often precede the data blocks (0= No error, 1=Error)

**\[Num,MainErr,SlaveErr,RecoveryBtnId,StepData,LabwareName,LabwarePos**

| **Num**           | Step dependent information (e.g. the channel number, a loading position etc.) à Check the step’s **help menu**                                                                                   |
| ----------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **MainErr**       | Main error code which occurred on instrument. See **appendix** at the end of this document                                                                                                       |
| **SlaveErr**      | Detailed error code of dependent slave (e.g. auto load, washer etc.) See **appendix** at the end of this document for example Channel errors                                                     |
| **RecoveryBtnId** | Recovery which has been used to handle this error (operator selection, or automated error recovery selection)                                                                                    |
| **StepData**      | <p>Step depended information, e.g. the barcode read, the volume aspirated etc.</p><p>The meaning and data type for this information should be found in the step’s <strong>help menu</strong></p> |
| **LabwareName**   | Labware name of used labware                                                                                                                                                                     |
| **LabwarePos**    | Position within a Labware. Sequence tools would call this the **Position ID**, but within a block, “Position” has an alternate meaning, so we refer to it as **Labware Pos**                     |

