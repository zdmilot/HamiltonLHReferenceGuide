# Device Library

The device library offers a set of commands to collect labware and device details.

<table><thead><tr><th width="278">Command</th><th width="102">Icon</th><th>Action Performed</th></tr></thead><tbody><tr><td>DevAddContainerTo Rack</td><td><img src="../../.gitbook/assets/image (573).png" alt="" data-size="original"></td><td>Replaces a container on a rectangular pre-loaded rack.</td></tr><tr><td>DevAddLabware</td><td><img src="../../.gitbook/assets/image (574).png" alt="" data-size="original"></td><td>Adds given labware to Deck Layout using deck coordinates.</td></tr><tr><td>DevAddLabware ToTemplate</td><td><img src="../../.gitbook/assets/image (575).png" alt="" data-size="original"></td><td>Adds given labware to deck site on named template.</td></tr><tr><td>DevAddPreloaded Labware</td><td><img src="../../.gitbook/assets/image (576).png" alt="" data-size="original"></td><td>Adds given labware including any preloaded labware to Deck Layout using deck coordinates.</td></tr><tr><td>DevAddSequence</td><td><img src="../../.gitbook/assets/image (577).png" alt="" data-size="original"></td><td>Adds a sequence to the collection holding the editable sequences of the device.</td></tr><tr><td>DevAddSequence2</td><td><img src="../../.gitbook/assets/image (578).png" alt="" data-size="original"></td><td>Adds a sequence to the collection holding the editable sequences of the device.</td></tr><tr><td>DevCompute ContainerVolume</td><td><img src="../../.gitbook/assets/image (579).png" alt="" data-size="original"></td><td>Calculates the volume in ml for the container at the given position and the given internal height. The function does NOT support connected containers.</td></tr><tr><td>DevCompute ContainerVolume2</td><td><img src="../../.gitbook/assets/image (580).png" alt="" data-size="original"></td><td>Calculates the volume in ml for the container at the given position and the given internal height. The function supports connected containers.</td></tr><tr><td>DevCopyReset Sequence</td><td><img src="../../.gitbook/assets/image (581).png" alt="" data-size="original"></td><td><p>Reloads a copy of the original deck sequence with the name sequenceName from the Deck Layout file into the sequence object sequenceObj. All indexes, limits and positions are re-initialized. The sequence must exist.</p><p>The original deck sequence remains unchanged.</p></td></tr><tr><td>DevEditSequences</td><td><img src="../../.gitbook/assets/image (507).png" alt="" data-size="original"></td><td><p>Displays the “Edit Sequence” Dialog which shows the Deck Layout with all the sequence positions of the sequences set by the DevAddSequence() or the DevAddSequence2() functions.</p><p>The “Edit Sequence” Dialog allows it to enabled / disabled sequence positions on the Deck Layout in a graphical manner by using the mouse.</p></td></tr><tr><td>DevEditSequences2</td><td><img src="../../.gitbook/assets/image (508).png" alt="" data-size="original"></td><td><p>Displays the “Edit Sequence” Dialog which shows the Deck Layout with all the sequence positions of the sequences set by the DevAddSequence() or the DevAddSequence2() functions.</p><p>The “Edit Sequence” Dialog allows it to enabled / disabled sequence positions on the Deck Layout in a graphical manner by using the mouse.</p></td></tr><tr><td>DevGetBarcodeData</td><td><img src="../../.gitbook/assets/image (509).png" alt="" data-size="original"></td><td><p>Gets the barcode mask for the instance of labware at</p><p>a position.</p></td></tr><tr><td>DevGetBarcodeData2</td><td><img src="../../.gitbook/assets/image (510).png" alt="" data-size="original"></td><td>Gets the barcode masks for the instances of labware at positions.</td></tr><tr><td>DevGetBarcodeData3</td><td><img src="../../.gitbook/assets/image (512).png" alt="" data-size="original"></td><td>Gets the barcode masks for the instances of labware at positions.</td></tr><tr><td>DevGetCfgValueWith Key</td><td><img src="../../.gitbook/assets/image (513).png" alt="" data-size="original"></td><td>Returns the configuration value for the instrument mapped to a given key (integer, float, or string).</td></tr><tr><td>DevGetDeckLayoutFile Name</td><td><img src="../../.gitbook/assets/image (514).png" alt="" data-size="original"></td><td>Returns the absolute Deck Layout file name (string; may be empty for a device without Deck Layout).</td></tr><tr><td>DevGetInstrument Name</td><td><img src="../../.gitbook/assets/image (515).png" alt="" data-size="original"></td><td>Returns the property value for a property key of a labware.</td></tr><tr><td>DevGetLabwareData</td><td><img src="../../.gitbook/assets/image (523).png" alt="" data-size="original"></td><td>Obtains the position of the given labware item from the Deck Layout using deck coordinates.</td></tr><tr><td>DevGetLabware Position</td><td><img src="../../.gitbook/assets/image (524).png" alt="" data-size="original"></td><td>Obtains the position of the given labware item from the Deck Layout using deck coordinates.</td></tr><tr><td>DevGetLabware Positionex</td><td><img src="../../.gitbook/assets/image (525).png" alt="" data-size="original"></td><td>Obtains the position of the given labware item from the Deck Layout using deck coordinates.</td></tr><tr><td>DevGetLabware Positionex2</td><td><img src="../../.gitbook/assets/image (526).png" alt="" data-size="original"></td><td>Obtains the position information of the given labware item from the Deck Layout using deck coordinates.</td></tr><tr><td>DevGetPosition LabwareNameAt</td><td><img src="../../.gitbook/assets/image (527).png" alt="" data-size="original"></td><td>Retrieves the template site with associated labware name or labware name with associated position name at a given index, retrieved during a previous call to the function Get Positions Labware Names.</td></tr><tr><td>DevGetPosition LabwareNames</td><td><img src="../../.gitbook/assets/image (528).png" alt="" data-size="original"></td><td>Retrieves template sites with associated labware names or labware names with associated position names of all positions on the given labware which are referenced by the specified sequence.</td></tr><tr><td>DevGetReleaseVersion</td><td><img src="../../.gitbook/assets/image (529).png" alt="" data-size="original"></td><td><p>Returns the release version for the instrument,</p><p>e.g. 3.0.0.630 (string).</p></td></tr><tr><td>DevGetSequence</td><td><img src="../../.gitbook/assets/image (530).png" alt="" data-size="original"></td><td>Gets a copy of the deck sequence with the name sequenceName.</td></tr><tr><td>DevGetSequenceRef</td><td><img src="../../.gitbook/assets/image (531).png" alt="" data-size="original"></td><td>Gets a reference to the deck sequence with the name seqId.</td></tr><tr><td>DevGetTemplate LabwareNameAt</td><td><img src="../../.gitbook/assets/image (532).png" alt="" data-size="original"></td><td>Returns the labware name with associated template name at a given index.</td></tr><tr><td>DevGetTemplateLabware Names</td><td><img src="../../.gitbook/assets/image (533).png" alt="" data-size="original"></td><td>Queries labware names with associated template name.</td></tr><tr><td>DevIsValidLabwareFor CurrentDeck-Layout</td><td><img src="../../.gitbook/assets/image (534).png" alt="" data-size="original"></td><td>Checks whether the given labware is valid for the current Deck Layout.</td></tr><tr><td>DevPause</td><td><img src="../../.gitbook/assets/image (535).png" alt="" data-size="original"></td><td>Suspends the program execution at the current position.</td></tr><tr><td>DevRemoveLabware</td><td><img src="../../.gitbook/assets/image (522).png" alt="" data-size="original"></td><td>Removes given labware from the deck.</td></tr><tr><td>DevRemoveLabware FromTemplate</td><td><img src="../../.gitbook/assets/image (521).png" alt="" data-size="original"></td><td>Removes given labware from named template.</td></tr><tr><td>DevRemoveSequences</td><td><img src="../../.gitbook/assets/image (520).png" alt="" data-size="original"></td><td>Removes all sequences from the collection holding the editable sequences of the device.</td></tr><tr><td>DevResetSequence</td><td><img src="../../.gitbook/assets/image (519).png" alt="" data-size="original"></td><td>Reloads the original deck sequence with the name seqId from the Deck Layout file, all indexes, limits and positions are re-initialized. The sequence must exist.</td></tr><tr><td>DevSetBarcodeData</td><td><img src="../../.gitbook/assets/image (518).png" alt="" data-size="original"></td><td><p>Sets the barcode mask for the instance of labware at</p><p>a position.</p></td></tr><tr><td>DevSetBarcodeData2</td><td><img src="../../.gitbook/assets/image (517).png" alt="" data-size="original"></td><td>Sets the barcode masks for the instances of labware at positions.</td></tr><tr><td>DevSetBarcodeData3</td><td><img src="../../.gitbook/assets/image (516).png" alt="" data-size="original"></td><td>Sets the barcode masks for the instances of labware at positions.</td></tr></tbody></table>