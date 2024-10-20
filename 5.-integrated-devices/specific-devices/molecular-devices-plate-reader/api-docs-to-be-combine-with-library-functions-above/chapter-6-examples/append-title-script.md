# Append Title Script

int mAppenTitleID; public void Main()

{

AutomationObject.Initialize("localhost"); AutomationObject.ErrorReport += Error; AutomationObject.CommandCompleted+= CommandCompleted; AutomationObject.SelectSection("Plate01");

mAppenTitleID = AutomationObject.AppendTitle("- YeOld Append");

}

private void Error( object sender, SoftMaxPro.AutomationClient.SMPAutomationClient.ErrorEventArgs e)

{

Results.AppendResult("Error: Command ID = " + e.QueueID.ToString() + " - " + e.Error);

}

private void CommandCompleted( object sender, SoftMaxPro.AutomationClient.SMPAutomationClient.CommandStatusEventArg e)

{

Results.AppendResult("Command complete Command ID = " + e.QueueID.ToString() ); if( mAppenTitleID == e.QueueID )

{

Results.AppendResult(e.StringResult);

}

if( e.QueueEmpty)

{

Results.AppendResult("Queue empty - disconnecting events"); AutomationObject.ErrorReport -= Error; AutomationObject.CommandCompleted -= CommandCompleted; AutomationObject.Dispose();

}

}