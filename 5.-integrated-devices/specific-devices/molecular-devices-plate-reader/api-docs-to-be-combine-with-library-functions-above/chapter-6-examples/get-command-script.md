# Get Command Script

public int AutosaveStateID; public int NumPlateSectionsID; public int DrawerStatusID; public void Main()

{

string now = System.DateTime.Now.ToString(); Results.AppendResult(now); AutomationObject.Initialize("localhost"); AutomationObject.ErrorReport += Error; AutomationObject.CommandCompleted+= CommandCompleted; AutomationObject.CloseDrawer();

AutosaveStateID = AutomationObject.GetAutosaveState(); Results.AppendResult("AutosaveStateID= " + AutosaveStateID.ToString()); NumPlateSectionsID = AutomationObject.GetNumberPlateSections(); Results.AppendResult("NumPlateSectionsID= " + NumPlateSectionsID.ToString()); DrawerStatusID = AutomationObject.GetDrawerStatus(); Results.AppendResult("NumPlateSectionsID= " + DrawerStatusID.ToString());

}

private void Error( object sender, SoftMaxPro.AutomationClient.SMPAutomationClient.ErrorEventArgs e)

{

Results.AppendResult("Error: Command ID = " + e.QueueID.ToString() + " - + e.Error);

}

private void CommandCompleted( object sender, SoftMaxPro.AutomationClient.SMPAutomationClient.CommandStatusEventArg e)

{

Results.AppendResult("Command complete Command ID = " + e.QueueID.ToString() ); if( e.QueueID == AutosaveStateID)

Results.AppendResult("AutosaveState: " + e.IntResult.ToString() ); if( e.QueueID == NumPlateSectionsID ) Results.AppendResult("NumPlateSections: " + e.IntResult.ToString() ); if( e.QueueID == DrawerStatusID ) Results.AppendResult("DrawerStatus: " + e.IntResult.ToString() ); if( e.QueueEmpty)

{

Results.AppendResult("Queue empty - disconnecting events"); AutomationObject.ErrorReport -= Error; AutomationObject.CommandCompleted -= CommandCompleted; AutomationObject.Dispose();

}

}
