# ExportAs Script

int mStatusID ; public void Main()

{

AutomationObject.Initialize("localhost"); AutomationObject.ErrorReport += Error; AutomationObject.CommandCompleted += CommandCompleted; AutomationObject.SelectSection("Plate1"); AutomationObject.SetReader("Offline", "SPECTRAmax M2"); AutomationObject.SetSimulationMode(true); AutomationObject.StartRead();

mStatusID = AutomationObject.ExportAs("C:\\\Automation\_Test\\\Results\\\test.xml", SoftMaxPro.AutomationClient.SMPAutomationClient.ExportAsFormat.XML );

Results.AppendResult("Status Command ID = " + mStatusID .ToString() ); mStatusID = AutomationObject.ExportAs("C:\\\Automation\_Test\\\Results\\\Plate.txt",

SoftMaxPro.AutomationClient.SMPAutomationClient.ExportAsFormat.PLATE ); Results.AppendResult("Status Command ID = " + mStatusID .ToString() );

mStatusID = AutomationObject.ExportAs("C:\\\Automation\_Test\\\Results\\\COLUMNS.txt", SoftMaxPro.AutomationClient.SMPAutomationClient.ExportAsFormat.TIME); Results.AppendResult("Status Command ID = " + mStatusID .ToString() );

}

private void Error( object sender, SoftMaxPro.AutomationClient.SMPAutomationClient.ErrorEventArgs e)

{

Results.AppendResult("Error: Command ID = " + e.QueueID.ToString() + " - " + e.Error);

}

private void CommandCompleted( object sender, SoftMaxPro.AutomationClient.SMPAutomationClient.CommandStatusEventArg e)

{

Results.AppendResult("Command complete Command ID = " + e.QueueID.ToString() ); if( mStatusID == e.QueueID )

{

Results.AppendResult(e.StringResult);

}

if( e.QueueEmpty)

{

Results.AppendResult("Queue empty - disconnecting events"); AutomationObject.ErrorReport -= Error; AutomationObject.CommandCompleted -= CommandCompleted; AutomationObject.Dispose();

}

}
