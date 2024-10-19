# BarcodeRead

## Description

This function is used to retrieve the barcode of a plate in the device.

If parameter _Liconic\_Store\_X::Option::ExtendedBarcodeReading_ is enabled using function OptionSet, the barcode reading will take some time.

## Syntax

BarcodeRead (variable i\_intModuleIDStore,

variable i\_intModuleIDScanner, variable i\_intStacker, variable i\_intLevel,

variable& o\_strBarcode)

## Arguments

| **argument**                | **value**         | **description**                                                                                                                                       |
| --------------------------- | ----------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------- |
| i\_intModuleIDStore \[in]   | integer \[0..3]   | Unique identifier for the Liconic StoreX device as returned by function Initialize.                                                                   |
| i\_intModuleIDScanner \[in] | integer \[0..160] | Unique identifier for the barcode scanner device as returned by function Initialize.                                                                  |
| i\_intStacker \[in]         | integer \[1..100] | Number of the stacker to use.                                                                                                                         |
| i\_intLevel \[in]           | integer \[1..200] | <p>Level to retrieve barcode for.</p><p>The value will be checked against the capacity of the stacker set using function StackerConfigurationSet.</p> |
| o\_strBarcode \[out]        | string            | <p>Plate barcode.</p><p>A value of 'empty' is returned in case no barcode was read.</p>                                                               |
