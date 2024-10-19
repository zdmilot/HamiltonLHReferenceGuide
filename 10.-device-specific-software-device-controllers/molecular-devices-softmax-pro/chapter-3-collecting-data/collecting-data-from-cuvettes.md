# Collecting Data From Cuvettes

Two types of data collection are possible when you use a cuvette: a reference read and a sample read.

You can start a read after you define the acquisition settings. It is not necessary to define groups and assign cuvettes in the Template Editor dialog first, but you can use the Template Editor to create the required number of cuvettes in the section. As an alternative, you can create a small number of cuvettes one at a time with the ![](<../../../.gitbook/assets/0 (4) (1) (1).jpeg>) New Cuvette Set icon in the Navigation Tree.

Instrument settings must be the same for all cuvettes in a Cuvette Set section.

Cuvette Set sections have a limit of 96 cuvettes. If you reach this limit, create a new Cuvette Set section.

### Sample Read

If you select more than one cuvette, the software starts with the left-most selected cuvette that does not contain sample read data.

To do a sample read:

1. In the Navigation Tree, select a cuvette in the Cuvette Set section.
2. Click ![](<../../../.gitbook/assets/1 (4) (1).jpeg>) **Read** on the Home tab or below the Settings Information area. The Read button changes to ![](<../../../.gitbook/assets/2 (3) (1) (1).jpeg>) **Stop**, to terminate a read.

### Reference Read

You can take a reference read either on air or you can use a cuvette that contains the buffer of your sample.

The reference can be read before or after you read samples.

If you do not take a reference read in a Cuvette Set section before samples were read and you then read a reference, the following occurs:

![](<../../../.gitbook/assets/3 (4) (1) (1) (1).png>) The software applies the reference read to all cuvettes in the Cuvette Set section if it is the first reference read.

![](<../../../.gitbook/assets/4 (4) (1) (1) (1).png>) In subsequent reference reads, if you select one or more cuvettes, the software selectively replaces the reference read for the cuvettes you select.

![](<../../../.gitbook/assets/5 (3) (1) (1) (1).png>) The time and date of the read displays under each cuvette in the section.

![](<../../../.gitbook/assets/6 (4) (1) (1).png>) The software applies the reference to new cuvettes you subsequently create in the section.

You can have more than one reference per Cuvette Set section. To do a reference read:

1. Select the cuvettes in the Cuvette Set section.
2. Place the correct reference in the cuvette port.
3. Click ![](<../../../.gitbook/assets/7 (2).jpeg>) **Ref**.

The time and date stamp of the reference for the cuvettes you select changes.

the new reference read.

The software applies the reference read to all cuvettes in the Cuvette Set section, unless you select specific cuvettes. The reference value does not display. To see the reference value, use one of the following procedures.

### Procedure 1:

1. Create a cuvette in the Cuvette Set section and Ref on air (empty cuvette port).
2. Read a cuvette that contains the blanking solution.

If you want to have both reference and read values available, do the following:

1. Create a Cuvette Set section with up to the maximum of 96 cuvettes.
2. Define a template blank in the Cuvette Set section.
3. Place buffer in the cuvette and click ![](<../../../.gitbook/assets/0 (3) (1) (1).jpeg>) **Read**.
4. Click ![](<../../../.gitbook/assets/1 (3) (1).jpeg>) **Read** again to read the remaining samples.

The software subtracts the optical density of the cuvette you designate as the template blank from the optical density of all the other cuvettes in the Cuvette Set section.

### Procedure 2:

1. Create a Cuvette Set section with up to the maximum of 96 cuvettes.
2. Reference and read the cuvette.
3. Create a template with the applicable groups.
4. Create a column in each Group table with the formula !wellprereadLm1.

If you have a multiple wavelength read and you want to see the reference at each wavelength, create more columns with the formula !wellprereadLmx where **x** is 2, 3, or 4, corresponding to the wavelength for which you want to see a reference.

The OD/RFU/RLU with the reference subtracted displays in the Values column. The referencevalue for each sample displays in the custom column you create.
