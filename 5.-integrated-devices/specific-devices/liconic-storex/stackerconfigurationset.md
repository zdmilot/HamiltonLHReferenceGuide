# StackerConfigurationSet

## Description

This function is used to set the stacker pitch for all of the stackers in the device.

This function must be used prior to any of the following functions: [InventoryScan](chm://c6eee35ebc6f05b6562520699a23e565/topics/InventoryScan.html), [BarcodeRead](chm://c6eee35ebc6f05b6562520699a23e565/topics/BarcodeRead.html), [PlateImport](chm://c6eee35ebc6f05b6562520699a23e565/topics/PlateImport.html) and [PlateExport](chm://c6eee35ebc6f05b6562520699a23e565/topics/PlateExport.html)

It is possible to define a different type of stacker for each position.

The default pitch settings are done for a STX44 with cassettes with a pitch of 23 and a capacity of 22 plates (MTP).

## Syntax

StackerConfigurationSet (variable i\_intModuleIDStore, variable i\_intStacker, variable i\_intPitch, variable i\_intCapacity)

## Arguments

| argument                  | value             | description                                                                                                                                                                                                                        |
| ------------------------- | ----------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| i\_intModuleIDStore \[in] | integer \[0..3]   | Unique identifier for the Liconic StoreX device as returned by function [Initialize](chm://c6eee35ebc6f05b6562520699a23e565/topics/Initialize.html).                                                                               |
| i\_intStacker \[in]       | integer \[1..100] | Number of the stacker to set the values for.                                                                                                                                                                                       |
| i\_intPitch \[in]         | integer \[1..999] | <p>Stacker pitch according to the table shown below (Pitch).</p><p>You may use the predefined pitch values of Liconic_Store_X::Cassettes::Length_XXXX> for standard stackers. XXXX is the length in mm.</p>                        |
| i\_intCapacity \[in]      | integer \[1..200] | <p>Stacker capacity according to the tables shown below (# Plates per cassette).</p><p>You may use the predefined capacity values of Liconic_Store_X::Cassettes::Length_XXXX> for standard stackers. XXXX is the length in mm.</p> |

## Table of available stackers

| Maximum plate height                                     | Pitch    | # Plates per cassette |         |    |     |
| -------------------------------------------------------- | -------- | --------------------- | ------- | -- | --- |
| 505 mm                                                   | 645 mm\* | 1250 mm\*             | 1710 mm |    |     |
| 6 mm                                                     | 12 mm    | 42                    | -       | -  | -   |
| 7 mm                                                     | 13 mm    | 38                    | -       | -  | -   |
| 8 mm                                                     | 14 mm    | 36                    | -       | -  | -   |
| 9 mm                                                     | 15 mm    | 33                    | -       | -  | -   |
| 10 mm                                                    | 16 mm    | 31                    | -       | -  | -   |
| 11 mm                                                    | 17 mm    | 30                    | 38      | -  | 100 |
| 12 mm                                                    | 18 mm    | 28                    | -       | 69 | 95  |
| 13 mm                                                    | 19 mm    | 26                    | -       | 65 | 90  |
| 14 mm                                                    | 20 mm    | 25                    | -       | 62 | 85  |
| 15 mm                                                    | 21 mm    | 24                    | 30      | 59 | 81  |
| 16 mm                                                    | 22 mm    | 23                    | 29      | 57 | 77  |
| 17 mm                                                    | 23 mm    | 22                    | 28      | 54 | 74  |
| 18 mm                                                    | 24 mm    | 21                    | 27      | 52 | 71  |
| 19 mm                                                    | 25 mm    | 20                    | 26      | 50 | 68  |
| 20 mm                                                    | 26 mm    | 19                    | -       | 48 | 65  |
| 21 mm                                                    | 27 mm    | -                     | 24      | 46 | 63  |
| 22 mm                                                    | 28 mm    | 18                    | 23      | 44 | 61  |
| 23 mm                                                    | 29 mm    | -                     | 22      | 43 | 59  |
| 24 mm                                                    | 30 mm    | 17                    | 21      | 41 | 57  |
| 25 mm                                                    | 31 mm    | 16                    | 20      | 40 | 55  |
| 26 mm                                                    | 32 mm    | -                     | -       | 39 | 53  |
| 27 mm                                                    | 33 mm    | 15                    | 19      | 37 | 51  |
| 28 mm                                                    | 34 mm    | -                     | -       | 36 | 50  |
| 29 mm                                                    | 35 mm    | -                     | -       | 35 | 48  |
| 30 mm                                                    | 36 mm    | 14                    | 18      | 34 | 47  |
| 31 mm                                                    | 37 mm    | -                     | -       | -  | 46  |
| 32 mm                                                    | 38 mm    | 13                    | 17      | 33 | 45  |
| 33 mm                                                    | 39 mm    | -                     | -       | 32 | 43  |
| 34 mm                                                    | 40 mm    | -                     | 16      | 31 | 42  |
| 35 mm                                                    | 41 mm    | -                     | -       | 30 | 41  |
| 36 mm                                                    | 42 mm    | 12                    | 15      | -  | 40  |
| 37 mm                                                    | 43 mm    | -                     | -       | 29 | -   |
| 38 mm                                                    | 44 mm    | -                     | -       | 28 | -   |
| 39 mm                                                    | 45 mm    | -                     | -       | -  | 38  |
| 40 mm                                                    | 46 mm    | 11                    | 14      | 27 | 37  |
| 41 mm                                                    | 47 mm    | -                     | -       | -  | 36  |
| 42 mm                                                    | 48 mm    | -                     | -       | 26 | 35  |
| 44 mm                                                    | 50 mm    | 10                    | 13      | 25 | 34  |
| 45 mm                                                    | 51 mm    | -                     | -       | -  | 33  |
| 46 mm                                                    | 52 mm    | -                     | -       | 24 | -   |
| 47 mm                                                    | 53 mm    | -                     | -       | -  | 32  |
| 48 mm                                                    | 54 mm    | -                     | 12      | 23 | -   |
| 49 mm                                                    | 55 mm    | -                     | -       | -  | 31  |
| 51 mm                                                    | 57 mm    | 9                     | 11      | 22 | 30  |
| 53 mm                                                    | 59 mm    | -                     | -       | 21 | 29  |
| 55 mm                                                    | 61 mm    | -                     | -       | -  | 28  |
| 56 mm                                                    | 62 mm    | -                     | -       | 20 | -   |
| 57 mm                                                    | 63 mm    | 8                     | -       | -  | 27  |
| 58 mm                                                    | 64 mm    | -                     | 10      | -  | -   |
| 59 mm                                                    | 65 mm    | -                     | -       | -  | 26  |
| 62 mm                                                    | 68 mm    | -                     | -       | -  | 25  |
| 65 mm                                                    | 71 mm    | -                     | -       | -  | 24  |
| 66 mm                                                    | 72 mm    | 7                     | 9       | -  | -   |
| 68 mm                                                    | 74 mm    | -                     | -       | -  | 23  |
| 71 mm                                                    | 77 mm    | -                     | -       | -  | 22  |
| 74 mm                                                    | 80 mm    | -                     | 8       | -  | -   |
| 75 mm                                                    | 81 mm    | -                     | -       | -  | 21  |
| 78 mm                                                    | 84 mm    | 6                     | -       | -  | -   |
| 79 mm                                                    | 85 mm    | -                     | -       | -  | 20  |
| 87 mm                                                    | 93 mm    | -                     | 7       | -  | -   |
| 95 mm                                                    | 101 mm   | 5                     | -       | -  | -   |
| 101 mm                                                   | 107 mm   | -                     | 6       | -  | -   |
| 112 mm                                                   | 106 mm   | -                     | -       | -  | 16  |
| 120 mm                                                   | 126 mm   | 4                     | -       | -  | -   |
| 123 mm                                                   | 129 mm   | -                     | 5       | -  | -   |
| 128 mm                                                   | 122 mm   | -                     | -       | -  | 14  |
| 148 mm                                                   | 142 mm   | -                     | -       | -  | 12  |
| 155 mm                                                   | 161 mm   | -                     | 4       | -  | -   |
| 162 mm                                                   | 168 mm   | 3                     | -       | -  | -   |
| 209 mm                                                   | 215 mm   | -                     | 3       | -  | -   |
| \* can only be used with STX500 or STX 1000 bi-carousels |          |                       |         |    |     |

\
