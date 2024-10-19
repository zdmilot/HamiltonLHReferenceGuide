# Terminate

## Description

This function is used to terminate the connection to Liconic StoreX device and the appropriate barcode scanner.

## Syntax

Terminate (variable i\_intModuleIDStore, variable i\_intModuleIDScanner)

## Arguments

| **argument**                | **value**         | **description**                                                                      |
| --------------------------- | ----------------- | ------------------------------------------------------------------------------------ |
| i\_intModuleIDStore \[in]   | integer \[0..3]   | Unique identifier for the Liconic StoreX device as returned by function Initialize.  |
| i\_intModuleIDScanner \[in] | integer \[0..160] | Unique identifier for the barcode scanner device as returned by function Initialize. |
