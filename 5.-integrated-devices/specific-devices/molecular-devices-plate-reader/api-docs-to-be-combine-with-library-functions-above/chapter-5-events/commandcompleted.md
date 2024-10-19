# CommandCompleted

event EventHandler(object sender, SoftMaxPro.Automation.SMPAutomationclient.CommandStatusEventArgs) CommandCompleted The CommandCompleted event generates a client callback when a command completes.

**CommandStatusEventArgs Properties**

| **Name**     | **Type** | **Description**                                                                                                                 |
| ------------ | -------- | ------------------------------------------------------------------------------------------------------------------------------- |
| DoubleResult | Double   | Returns a double result from a get command, such as GetTemperature()                                                            |
| IntResult    | Int32    | Provides the integer result from a get command, such as GetNumberPlateSections()                                                |
| QueueEmpty   | Boolean  | True indicates the command queue on the server is empty False indicates the command queue on the server still contains commands |
| QueueId      | Int32    | The id of the completed command                                                                                                 |
| StringResult | String   | Provides the string result from a get command, such as GetDrawerStatus()                                                        |

### Example

See Multiple Read and Copy Events Script on page 104.
