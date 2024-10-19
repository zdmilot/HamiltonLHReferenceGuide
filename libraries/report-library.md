# Report Library

The HSL report library provides functions to create report files for labware out of the sample tracking database within a method run (e.g.: a comma separated value result file (.csv) or an AT barcode file).

The “HSLReport” Prefix has been removed for a better overview.

<table><thead><tr><th width="282">Command</th><th width="66">Icon</th><th>Action Performed</th></tr></thead><tbody><tr><td>AddToReportList</td><td><img src="../.gitbook/assets/image (693).png" alt="" data-size="original"></td><td>Adds labware within the given sequence to an internal report list.</td></tr><tr><td>AddToReportListFromLabware</td><td><img src="../.gitbook/assets/image (694).png" alt="" data-size="original"></td><td>Adds labware within the given sequence to an internal report list.</td></tr><tr><td>Create ATBarcode File</td><td><img src="../.gitbook/assets/image (695).png" alt="" data-size="original"></td><td>Executes the Hamilton AT-file filter program HxATFilter in quiet mode, to create the AT barcode file.</td></tr></tbody></table>

\


<table data-header-hidden><thead><tr><th width="145"></th><th></th></tr></thead><tbody><tr><td><img src="../.gitbook/assets/image (10) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" data-size="original"></td><td><p>NOTE</p><p><em>In creating an AT-Barcode file for vials containing more than one barcode (for example sample + reagent were dispensed into this well, both came from containers with a barcode), the last barcode in the pipetting order will be written into the AT-Barcode file.</em></p><p><em>To prevent overwriting, a sample barcode of a reagent barcode (reagent dispensed after the sample) has to be deleted. To do this, set an empty string as a barcode for the container using the SetLabwareBarcode command from the HSLLabwareState library between loading and pipetting.</em></p></td></tr></tbody></table>

\
