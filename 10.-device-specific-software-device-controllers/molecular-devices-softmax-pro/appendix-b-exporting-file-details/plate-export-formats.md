# Plate Export Formats

The following describes the format of Plate sections you export to a .txt or .xls file. For a copy of the SoftMax Pro .xml schema, contact Molecular Devices.

![](<../../../.gitbook/assets/5 (22).png>) The header line contains the type of section, such as Plate, and the title of the section as defined in the SoftMax Pro Software data file. Plate sections contain more information in the header line. See Plate Header Fields on page 356.

![](<../../../.gitbook/assets/6 (22).png>) The data lines follow the header line and contain the data from the exported section. The layout and format of the data lines are dependent on many factors, such as the sectiontype, export type, read mode, and read type. See Plate Data Lines on page 364.

### Plate Header Fields

The fields in the header line for a Plate section help define the data that is presented in the section. The order and content of the fields are different depending on the read mode you use to collect the data.

**Absorbance Read Mode**

| **Position** | **Name**                           | **Description**                                                                                                                                                                      |
| ------------ | ---------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| 1.           | Section type                       | Contains the type of section such as Plate                                                                                                                                           |
| 2.           | Section name                       | Contains the title of the section as defined in the document                                                                                                                         |
| 3.           | Export version                     | Contains the version of the export application used for this export                                                                                                                  |
| 4.           | Export format                      | Contains Columns output format or Plate output format as defined in the Export dialog                                                                                                |
| 5.           | Read type                          | Contains the read type used for the acquisition, such as Endpoint, Kinetic, Spectrum, or Well Scan                                                                                   |
| 6.           | Read mode                          | Contains the read mode used for the acquisition (Absorbance)                                                                                                                         |
| 7.           | Data type                          | Contains Raw or Reduced to define the type of data in the export file                                                                                                                |
| 8.           | Pre-read                           | <p>Always FALSE</p><p>Pre-read is not a function of SoftMax Pro Software version 6 or newer</p>                                                                                      |
| 9.           | Kinetic points                     | Contains the number of reads done during the acquisition For Endpoint reads the number is 1                                                                                          |
| 10.          | Read time Read pattern             | Contains the read time in seconds for a Kinetic read Contains the scan pattern for a Well Scan read Contains no value (blank) for other read types                                   |
| 11.          | Kinetic interval Well Scan density | <p>Contains the interval between reads in seconds for a Kinetic read</p><p>Contains the scan density for a Well Scan read Contains no value (blank) for other read types</p>         |
| 12.          | Start wavelength                   | Contains the starting wavelength for a Spectrum read Contains no value (blank) for other read types                                                                                  |
| 13.          | End wavelength                     | Contains the ending wavelength for a Spectrum read Contains no value (blank) for other read types                                                                                    |
| 14.          | Wavelength step                    | <p>Contains the wavelength increment or step for a Spectrum read</p><p>Contains no value (blank) for other read types</p>                                                            |
| 15.          | Number of wavelengths              | Contains the number of wavelengths read for the acquisition Contains no value (blank) for Spectrum reads                                                                             |
| 16.          | Wavelengths                        | <p>Contains the wavelengths used for the acquisition</p><p>For multiple-wavelength reads, the values are separated by a space</p><p>Contains no value (blank) for Spectrum reads</p> |

**Absorbance Read Mode (continued)**

| **Position** | **Name**          | **Description**                                                                |
| ------------ | ----------------- | ------------------------------------------------------------------------------ |
| 17.          | First column      | Contains the number of the first column read during the acquisition            |
| 18.          | Number of columns | Contains the number of columns read during the acquisition                     |
| 19.          | Number of wells   | Contains the total number of wells in the plate, such as 96 or 384             |
| 20.          | First row         | Contains a number corresponding with the first row read during the acquisition |
| 21.          | Number of rows    | Contains the number of rows read during the acquisition                        |
| 22.          | Time tags         | Contains time-tag information if the exported data has read- time tags         |

**Fluorescence Intensity and AlphaScreen Read Mode**

| **Position** | **Name**               | **Description**                                                                                                                                    |
| ------------ | ---------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1.           | Section type           | Contains the type of section such as Plate                                                                                                         |
| 2.           | Section name           | Contains the title of the section as defined in the document                                                                                       |
| 3.           | Export version         | Contains the version of the export application used for this export                                                                                |
| 4.           | Export format          | Contains Columns output format or Plate output format as defined in the Export dialog                                                              |
| 5.           | Read type              | Contains the read type used for the acquisition, such as Endpoint, Kinetic, Spectrum, or Well Scan                                                 |
| 6.           | Read mode              | Contains the read mode used for the acquisition, such as Fluorescence or Luminescence                                                              |
| 7.           | Bottom read            | Contains TRUE if read from the bottom of the plate and FALSE if read from the top                                                                  |
| 8.           | Data type              | Contains Raw or Reduced to define the type of data in the export file                                                                              |
| 9.           | Pre-read               | <p>Always FALSE</p><p>Pre-read is not a function of SoftMax Pro Software version 6 or newer</p>                                                    |
| 10.          | Kinetic points         | Contains the number of reads done during the acquisition For Endpoint reads the number is 1                                                        |
| 11.          | Read time Read pattern | Contains the read time in seconds for a Kinetic read Contains the scan pattern for a Well Scan read Contains no value (blank) for other read types |

**Fluorescence Intensity and AlphaScreen Read Mode (continued)**

| **Position** | **Name**                           | **Description**                                                                                                                                                                                                                                                |
| ------------ | ---------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 12.          | Kinetic interval Well Scan density | <p>Contains the interval between reads in seconds for a Kinetic read</p><p>Contains the scan density for a Well Scan read Contains no value (blank) for other read types</p>                                                                                   |
| 13.          | Start wavelength                   | Contains the starting wavelength for a Spectrum read Contains no value (blank) for other read types                                                                                                                                                            |
| 14.          | End wavelength                     | Contains the ending wavelength for a Spectrum read Contains no value (blank) for other read types                                                                                                                                                              |
| 15.          | Wavelength step                    | <p>Contains the wavelength increment or step for a Spectrum read</p><p>Contains no value (blank) for other read types</p>                                                                                                                                      |
| 16.          | Number of wavelengths              | Contains the number of wavelengths read for the acquisition Contains no value (blank) for Spectrum reads                                                                                                                                                       |
| 17.          | Wavelengths                        | <p>Contains the wavelengths used for the acquisition</p><p>For multiple-wavelength reads, the values are separated by a space</p><p>For Fluorescence reads, contains the emission wavelengths Contains no value (blank) for Spectrum reads or Ex/Em sweeps</p> |
| 18.          | First column                       | Contains the number of the first column read during the acquisition                                                                                                                                                                                            |
| 19.          | Number of columns                  | Contains the number of columns read during the acquisition                                                                                                                                                                                                     |
| 20.          | Number of wells                    | Contains the total number of wells in the plate, such as 96 or 384                                                                                                                                                                                             |
| 21.          | Excitation wavelengths             | <p>Contains the excitation wavelengths used for a Fluorescence read</p><p>For multiple-wavelength reads, the values are separated by a space</p><p>Contains no value (blank) for Spectrum reads or Ex/Em sweeps</p>                                            |
| 22.          | Cutoff                             | Contains Manual or Automatic as defined in the Settings dialog                                                                                                                                                                                                 |
| 23.          | Cutoff filters                     | Contains the wavelengths of the cutoff filters with the values separated by a space                                                                                                                                                                            |
| 24.          | Sweep wave                         | Contains Excitation Sweep or Emission Sweep as defined in the Settings dialog                                                                                                                                                                                  |
| 25.          | Sweep fixed wavelength             | Contains the fixed wavelength of an Ex/Em sweep                                                                                                                                                                                                                |

**Fluorescence Intensity and AlphaScreen Read Mode (continued)**

| **Position** | **Name**               | **Description**                                                                                       |
| ------------ | ---------------------- | ----------------------------------------------------------------------------------------------------- |
| 26.          | Reads per well         | Contains the number of times a well is read during a single read                                      |
| 27.          | PMT gain               | Contains Automatic, High, Medium, Low, or Manual as defined in the Settings dialog                    |
| 28.          | Start integration time | Contains the time to start integration for a TRF read. Contains no value (blank) for other read modes |
| 29.          | End integration time   | Contains the time to end integration for a TRF read. Contains no value (blank) for other read modes   |
| 30.          | First row              | Contains a number corresponding with the first row read during the acquisition                        |
| 31.          | Number of rows         | Contains the number of rows read during the acquisition                                               |
| 32.          | Time tags              | Contains time-tag information if the exported data has read- time tags                                |

**Luminescence, Time-Resolved Fluorescence, and Fluorescence Polarization Read Mode**

| **Position** | **Name**               | **Description**                                                                                                                                    |
| ------------ | ---------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1.           | Section type           | Contains the type of section such as Plate                                                                                                         |
| 2.           | Section name           | Contains the title of the section as defined in the document                                                                                       |
| 3.           | Export version         | Contains the version of the export application used for this export                                                                                |
| 4.           | Export format          | Contains Columns output format or Plate output format as defined in the Export dialog                                                              |
| 5.           | Read type              | Contains the read type used for the acquisition, such as Endpoint, Kinetic, Spectrum, or Well Scan                                                 |
| 6.           | Read mode              | Contains the read mode used for the acquisition, such as Luminescence or Time Resolved                                                             |
| 7.           | Data type              | Contains Raw or Reduced to define the type of data in the export file                                                                              |
| 8.           | Pre-read               | <p>Always FALSE</p><p>Pre-read is not a function of SoftMax Pro Software version 6 or newer</p>                                                    |
| 9.           | Kinetic points         | Contains the number of reads done during the acquisition For Endpoint reads the number is 1                                                        |
| 10.          | Read time Read pattern | Contains the read time in seconds for a Kinetic read Contains the scan pattern for a Well Scan read Contains no value (blank) for other read types |

**Luminescence, Time-Resolved Fluorescence, and Fluorescence Polarization Read Mode (continued)**

| **Position** | **Name**                           | **Description**                                                                                                                                                                                                                                                 |
| ------------ | ---------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 11.          | Kinetic interval Well Scan density | <p>Contains the interval between reads in seconds for a Kinetic read</p><p>Contains the scan density for a Well Scan read Contains no value (blank) for other read types</p>                                                                                    |
| 12.          | Start wavelength                   | Contains the starting wavelength for a Spectrum read Contains no value (blank) for other read types                                                                                                                                                             |
| 13.          | End wavelength                     | Contains the ending wavelength for a Spectrum read Contains no value (blank) for other read types                                                                                                                                                               |
| 14.          | Wavelength step                    | <p>Contains the wavelength increment or step for a Spectrum read</p><p>Contains no value (blank) for other read types</p>                                                                                                                                       |
| 15.          | Number of wavelengths              | Contains the number of wavelengths read for the acquisition Contains no value (blank) for Spectrum reads                                                                                                                                                        |
| 16.          | Wavelengths                        | <p>Contains the wavelengths used for the acquisition</p><p>For multiple-wavelength reads, the values are separated by a space</p><p>For Time Resolved reads, contains the emission wavelengths Contains no value (blank) for Spectrum reads or Ex/Em sweeps</p> |
| 17.          | First column                       | Contains the number of the first column read during the acquisition                                                                                                                                                                                             |
| 18.          | Number of columns                  | Contains the number of columns read during the acquisition                                                                                                                                                                                                      |
| 19.          | Number of wells                    | Contains the total number of wells in the plate, such as 96 or 384                                                                                                                                                                                              |
| 20.          | Excitation wavelengths             | <p>Contains the excitation wavelengths used for a Time Resolved read</p><p>For multiple-wavelength reads, the values are separated by a space</p><p>Contains no value (blank) for Spectrum reads or Ex/Em sweeps</p>                                            |
| 21.          | Cutoff                             | Contains Manual or Automatic as defined in the Settings dialog                                                                                                                                                                                                  |
| 22.          | Cutoff filters                     | <p>Contains the wavelengths of the cutoff filters with the values separated by a space</p><p>Contains no value (blank) if no cutoff filter is used</p>                                                                                                          |
| 23.          | Sweep wave                         | Contains Excitation Sweep or Emission Sweep as defined in the Settings dialog                                                                                                                                                                                   |

**Luminescence, Time-Resolved Fluorescence, and Fluorescence Polarization Read Mode (continued)**

| **Position** | **Name**               | **Description**                                                                                                              |
| ------------ | ---------------------- | ---------------------------------------------------------------------------------------------------------------------------- |
| 24.          | Sweep fixed wavelength | Contains the fixed wavelength of an Ex/Em sweep                                                                              |
| 25.          | Reads per well         | Contains the number of times a well is read during a single read                                                             |
| 26.          | PMT gain               | Contains Automatic, High, Medium, Low, or Manual as defined in the Settings dialog                                           |
| 27.          | Start integration time | <p>Contains the time to start integration for a Time Resolved read.</p><p>Contains no value (blank) for other read modes</p> |
| 28.          | End integration time   | <p>Contains the time to end integration for a Time Resolved read.</p><p>Contains no value (blank) for other read modes</p>   |
| 29.          | First row              | Contains a number corresponding with the first row read during the acquisition                                               |
| 30.          | Number of rows         | Contains the number of rows read during the acquisition                                                                      |
| 31.          | Time tags              | Contains time-tag information if the exported data has read- time tags                                                       |

**Imaging Read Mode**

| **Position** | **Name**       | **Description**                                                                                                        |
| ------------ | -------------- | ---------------------------------------------------------------------------------------------------------------------- |
| 1.           | Section type   | Contains the type of section, such as Plate                                                                            |
| 2.           | Section name   | Contains the title of the section as defined in the document                                                           |
| 3.           | Export version | Contains the version of the export application used for this export                                                    |
| 4.           | Export format  | Contains Time Format for Columns output format or Plate Format for Plate output format as defined in the Export dialog |
| 5.           | Read type      | Contains the read type used for the acquisition, such as Endpoint                                                      |
| 6.           | Read mode      | Contains the read mode used for the acquisition, such as Imaging                                                       |
| 7.           | Data type      | Contains Raw or Reduced to define the type of data in the export file                                                  |
| 8.           | Pre-read       | <p>Always FALSE</p><p>Pre-read is not a function of SoftMax Pro Software version 6 or newer</p>                        |

**Imaging Read Mode (continued)**

| **Position** | **Name**              | **Description**                                                                                                                 |
| ------------ | --------------------- | ------------------------------------------------------------------------------------------------------------------------------- |
| 9.           | Kinetic points        | Contains the number of reads done during the acquisition For Endpoint reads the number is 1                                     |
| 10.          | Read time             | Contains no value (blank) for Imaging reads                                                                                     |
| 11.          | Kinetic interval      | Contains no value (blank) for Imaging reads                                                                                     |
| 12.          | Start wavelength      | Contains no value (blank) for Imaging reads                                                                                     |
| 13.          | End wavelength        | Contains no value (blank) for Imaging reads                                                                                     |
| 14.          | Wavelength step       | Contains no value (blank) for Imaging reads                                                                                     |
| 15.          | Number of wavelengths | Contains the number of wavelengths, or channels, read for the acquisition                                                       |
| 16.          | Emission wavelengths  | Contains the emission wavelengths used for the acquisition For multiple-wavelength reads, the values are separated by a space   |
| 17.          | First column          | Contains the number of the first column read during the acquisition                                                             |
| 18.          | Number of columns     | Contains the number of columns read during the acquisition                                                                      |
| 19.          | Number of wells       | Contains the total number of wells in the plate, such as 96 or 384                                                              |
| 20.          | First row             | Contains a number corresponding with the first row read during the acquisition                                                  |
| 21.          | Number of rows        | Contains the number of rows read during the acquisition                                                                         |
| 22.          | Excitation wavelength | Contains the excitation wavelengths used for the acquisition For multiple-wavelength reads, the values are separated by a space |
| 23.          | Analysis type         | Contains the analysis type used, such as Discrete Object Analysis                                                               |
| 24.          | Classification        | Contains On if classification is used and Off if it is not used                                                                 |
| 25.          | Find on               | Contains the emission wavelength used for finding objects or fields                                                             |
| 26.          | Measurement           | Contains the type of measurement selected in the Display Options dialog, such as Cell Count                                     |

### Plate Data Lines <a href="#bookmark2" id="bookmark2"></a>

The data lines immediately follow the header line.

![](<../../../.gitbook/assets/7 (22).png>) The first column shows the time points for a kinetic read, the data points in a well scan read, or the wavelengths in a spectrum read. For endpoint reads, this column is blank.

![](<../../../.gitbook/assets/8 (21).png>) The second column shows the temperature for the read, if you use the incubator for the read. If the incubator is off, the value is zero.

The read data starts in the third column. When both raw and reduced data are exported, the reduced data displays below the raw data.

The format of the data depends on whether the data was exported in column format or plate format.

For column formats, the data displays in a single row. The data for multiple time points for kinetic reads, multiple data points for well scan reads, or multiple wavelengths for spectrum reads is listed in separate rows. For endpoint, kinetic, or well scan reads with multiple wavelengths, the data for each wavelength displays in subsequent rows below the previous wavelength. For imaging reads, the data for each measurement is in a separate row.

<figure><img src="../../../.gitbook/assets/image (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

**Kinetic Data Exported in Column Format**

For plate formats, the data displays in a table to indicate the columns and rows of the plate. The data for multiple time points for kinetic reads, multiple data points for well scan reads, or multiple wavelengths for spectrum reads is listed in separate tables below the previous table. For endpoint, kinetic, or well scan reads with multiple wavelengths, the data for each wavelength displays in separate tables to the right of the previous table. For imaging reads, the data for each measurement is in a separate table to the right of the previous table.

<figure><img src="../../../.gitbook/assets/image (21) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

**Kinetic Data Exported in Plate Format**
