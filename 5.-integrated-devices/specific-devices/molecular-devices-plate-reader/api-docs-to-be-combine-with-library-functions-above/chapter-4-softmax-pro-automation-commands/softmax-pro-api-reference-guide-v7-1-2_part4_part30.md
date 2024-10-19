# softmax pro api reference guide v7 1 2\_Part4\_Part30

AutomationObject.InstrumentStatusChanged -= InstrumentStatus;\
AutomationObject.Dispose();\
}\
}\
private void Error( object sender,\
SoftMaxPro.AutomationClient.SMPAutomationClient.ErrorEventArgs e)\
{\
Results.AppendResult("Error: Command ID = " + e.QueueID.ToString() + " - " + e.Error); }\
private void InstrumentStatus( object sender,\
SoftMaxPro.AutomationClient.SMPAutomationClient.InstrumentStatusEventArgs e)\
{\
Results.AppendResult("Status changed to " + e.Status);\
}

OpenDrawer

OpenDrawer()\
CloseDrawer(String drawerType)\
OpenDrawer(Int32 xPosition, Int32 yPosition, Bool locked)

Purpose\
The OpenDrawer commands open a drawer on the instrument. This command opens the plate drawer for most instruments.

| <img src="../../../../../.gitbook/assets/0 (24).png" alt="" data-size="original"> | Note: For instruments with temperature control, the plate drawer cannot open when the incubator is on. See SetTemperature on page 91. |
| --------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------- |

Parameters for the FlexStation 3\
The OpenDrawer drawerType parameter is recognized by the FlexStation 3 only. This parameter is ignored and can be omitted for all other instruments.

drawerType

Type: String

Must be one of the following:

• “Assay Plate Drawer” \[default]

• "Compound Plate Drawer”

• “Tips Drawer”

These values are not case sensitive.

| <img src="../../../../../.gitbook/assets/1 (21).png" alt="" data-size="original"> | Note: The drawerType parameter is required for the FlexStation 3. The assay plate drawer opens if you omit this parameter. |
| --------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------- |

Parameters for Other Instruments\
The OpenDrawer xPosition, yPosition, and locked parameters are recognized by the FilterMax™F3 Multi-Mode Microplate Reader, FilterMax F5™Multi-Mode Microplate Reader, SpectraMax® i3 Multi-Mode Platform, SpectraMax® i3x Multi-Mode Detection Platform, and SpectraMax® Paradigm® Multi-Mode Microplate Reader only. These parameters are ignored and can be omitted for all other instruments.

xPosition

Type: Int32

This parameter defines the left-right offset for the position of the open plate drawer.

![](<../../../../../.gitbook/assets/2 (11).png>) Range for the SpectraMax i3 and SpectraMax i3x: 0 to 2900

![](<../../../../../.gitbook/assets/3 (13).png>) Range for the SpectraMax Paradigm: 0 to 2950

![](<../../../../../.gitbook/assets/4 (12).png>) Range for the FilterMax F3 and FilterMax F5: 0 to 2950 yPosition

Type: Int32

This parameter defines the front-rear offset for the position of the open plate drawer.

![](<../../../../../.gitbook/assets/5 (11).png>) Range for the SpectraMax i3 and SpectraMax i3x: 5200 to 6900

![](<../../../../../.gitbook/assets/6 (8).png>) Range for the SpectraMax Paradigm: 5200 to 6900

![](<../../../../../.gitbook/assets/7 (5).png>) Range for the FilterMax F3 and FilterMax F5: 5200 to 6900 locked

Type: Bool

When this parameter is true, the plate is held in a fixed position to allow operations such as dispensing.

Example\
This example describes how to open the plate drawer.

int mStatusID;\
public void Main()\
{\
AutomationObject.Initialize("localhost");\
AutomationObject.CommandCompleted+= CommandCompleted;\
AutomationObject.OpenDrawer();\
mStatusID = AutomationObject.GetDrawerStatus();\
Results.AppendResult("Status Command ID = " + mStatusID .ToString() );\
}\
private void CommandCompleted( object sender,\
SoftMaxPro.AutomationClient.SMPAutomationClient.CommandStatusEventArg e)\
{\
Results.AppendResult("Command complete Command ID = " + e.QueueID.ToString() ); if( mStatusID== e.QueueID )\
{\
Results.AppendResult( "Result: " +e.StringResult);\
}
