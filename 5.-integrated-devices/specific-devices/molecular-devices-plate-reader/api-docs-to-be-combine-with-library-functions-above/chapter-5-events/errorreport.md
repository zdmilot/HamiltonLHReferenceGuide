# ErrorReport

event EventHandler(object sender, SoftMaxPro.Automation.SMPAutomationclient.ErrorEventArgs) ErrorReport

The ErrorReport events generate a client callback when an error condition occurs.

**ErrorEventArgs Properties**

| **Name** | **Type** | **Description**                      |
| -------- | -------- | ------------------------------------ |
| Error    | String   | A description of the error           |
| QueueId  | Int32    | The id of the command with the error |

### Error Event Related Processing

When an Error event generates, it is followed by a CommandComplete event for the command that caused the error.

All commands waiting in the Automation server command queue are deleted so that the Automation client can control which commands are executed when an error is reported.

### Example

public void Main()

{

AutomationObject.Initialize(); AutomationObject.ErrorReport += Error; AutomationObject.CloseDrawer(); AutomationObject.SetShake(true); AutomationObject.OpenDrawer();

}

private void Error( object sender, SoftMaxPro.AutomationClient.SMPAutomationClient.ErrorEventArgs e)

{

Results.AppendResult("Error: Command ID = " + e.QueueID.ToString() + " - " + e.Error);

}
