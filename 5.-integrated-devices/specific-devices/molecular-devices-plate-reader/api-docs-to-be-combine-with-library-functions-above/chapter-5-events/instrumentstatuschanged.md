# InstrumentStatusChanged

event EventHandler(object sender, SoftMaxPro.Automation.SMPAutomationclient.InstrumentStatusEventArgs) InstrumentStatusChanged

The InstrumentStatusChanged events generate a client callback when the status of the connected

instrument changes. **InstrumentStatusEventArgs Property**

| **Name** | **Type** | **Description**                                                                  |
| -------- | -------- | -------------------------------------------------------------------------------- |
| Status   | String   | Provides the new status of the instrument. See the possible values listed below. |

### Returns

The following properties can be used for testing which state has been returned: ![](<../../../../../.gitbook/assets/1 (11).png>) SMPAutomationClient.InstrumentStatus.IDLE

![](<../../../../../.gitbook/assets/2 (10).png>) SMPAutomationClient.InstrumentStatus.INITIALIZING

![](<../../../../../.gitbook/assets/3 (7).png>) SMPAutomationClient.InstrumentStatus.BUSY

![](<../../../../../.gitbook/assets/4 (4).png>) SMPAutomationClient.InstrumentStatus.STOPPING ![](<../../../../../.gitbook/assets/5 (4).png>) SMPAutomationClient.InstrumentStatus.ERROR

![](<../../../../../.gitbook/assets/6 (3).png>) SMPAutomationClient.InstrumentStatus.TIMEOUT ![](<../../../../../.gitbook/assets/7 (3).png>) SMPAutomationClient.InstrumentStatus.OFFLINE

### Example

See Multiple Read and Copy Events Script on page 104
