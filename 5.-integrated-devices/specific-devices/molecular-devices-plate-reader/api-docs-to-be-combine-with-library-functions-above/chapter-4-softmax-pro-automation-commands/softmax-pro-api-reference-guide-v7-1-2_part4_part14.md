# GetDrawerStatus

Int32 GetDrawerStatus()\
Int32 GetDrawerStatus(String drawerType)\
The GetDrawerStatus command returns the state of the drawer on the instrument. This command returns the state of the plate drawer for most instruments.

Parameters\
The GetDrawerStatus parameters are recognized by the FlexStation 3 only. The parameters are ignored and can be omitted for all other instruments.

drawerType

Type: String

Must be one of the following:

• “Assay Plate Drawer” \[default]

• "Compound Plate Drawer”

• “Tips Drawer”\
These values are not case sensitive.

| <img src="../../../../../.gitbook/assets/0 (15) (1).png" alt="" data-size="original"> | Note: The drawerType parameter is required for the FlexStation 3. The status of the assay plate drawer is returned if you omit this parameter. |
| ------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------- |

Returns\
This function returns the command ID used to retrieve the following from the CommandCompleted Event.

Return type: String\
Returns the status of the drawer.

The return string is one of following properties:

![](<../../../../../.gitbook/assets/1 (18).png>) SMPAutomationClient.DrawerStatus.OPENED = The drawer is open

![](<../../../../../.gitbook/assets/2 (9) (1).png>) SMPAutomationClient.DrawerStatus.CLOSED = The drawer is closed

Example\
This example describes how to determine if each drawer on a FlexStation 3 is open or closed. All other instruments do not require this parameter.

int mStatusID;\
public void Main()\
{\
AutomationObject.Initialize("localhost");\
AutomationObject.CommandCompleted += CommandCompleted;\
AutomationObject.ErrorReport += Error;\
mStatusID = AutomationObject.GetDrawerStatus("Assay Plate Drawer"); cStatusID = AutomationObject.GetDrawerStatus("Compound Plate Drawer"); tStatusID = AutomationObject.GetDrawerStatus("Tips Drawer");\
Results.AppendResult("Status Command ID = " + mStatusID .ToString());

}\
private void Error(object sender,\
SoftMaxPro.AutomationClient.SMPAutomationClient.ErrorEventArgs e)\
{\
Results.AppendResult("Error: Command ID = " + e.QueueID.ToString() + " - " + e.Error); }\
private void CommandCompleted(object sender,\
SoftMaxPro.AutomationClient.SMPAutomationClient.CommandStatusEventArg e)\
{\
Results.AppendResult("Command complete Command ID = " + e.QueueID.ToString() ); if( mStatusID== e.QueueID )\
{\
Results.AppendResult( "Assay Plate Drawer Status: " +e.StringResult);\
}\
if( e.QueueEmpty)\
{\
Results.AppendResult("Queue empty - disconnecting events");\
AutomationObject.CommandCompleted -= CommandCompleted;\
AutomationObject.ErrorReport -= Error;\
AutomationObject.Dispose();\
}\
Results.AppendResult("Command complete Command ID = " + e.QueueID.ToString() ); if( cStatusID== e.QueueID )\
{\
Results.AppendResult( "Compound Plate Drawer Status: " +e.StringResult);\
}\
if( e.QueueEmpty)\
{\
Results.AppendResult("Queue empty - disconnecting events");\
AutomationObject.CommandCompleted -= CommandCompleted;\
AutomationObject.ErrorReport -= Error;\
AutomationObject.Dispose();\
}\
Results.AppendResult("Command complete Command ID = " + e.QueueID.ToString() ); if( tStatusID== e.QueueID )\
{\
Results.AppendResult( "Tips Drawer Status: " +e.StringResult);\
}\
if( e.QueueEmpty)\
{\
Results.AppendResult("Queue empty - disconnecting events");\
AutomationObject.CommandCompleted -= CommandCompleted;

AutomationObject.ErrorReport -= Error;\
AutomationObject.Dispose();\
}\
}
