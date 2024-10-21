# CloseDrawer

Int32 CloseDrawer()\
Int32 CloseDrawer(String drawerType)\
The CloseDrawer command closes the drawer you specify on the instrument. This command closes the plate drawer for most instruments.

Parameters\
CloseDrawer parameters are recognized by the FlexStation® 3 Multi-Mode Microplate Reader only. The parameters are ignored and can be omitted for all other instruments.

drawerType\
Type: String\
Must be one of the following strings:\
• “Assay Plate Drawer” \[default]\
• "Compound Plate Drawer”\
• “Tips Drawer”\
These values are not case sensitive.

| <img src="../../../../../.gitbook/assets/1 (14) (1).png" alt="" data-size="original"> | Note: The drawerType parameter is required for the FlexStation 3. If you omit this parameter the assay plate drawer closes. |
| ------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------- |
