# Multiple Read and Copy Events Script

int mCopyID; int read1;

public void Main()

{

string now = System.DateTime.Now.ToString(); Results.AppendResult(now); AutomationObject.Initialize("localhost"); AutomationObject.ErrorReport += Error; AutomationObject.CommandCompleted+= CommandCompleted; AutomationObject.InstrumentStatusChanged += InstrumentStatus; AutomationObject.SetReader("Offline", "SPECTRAmax M2"); AutomationObject.SetSimulationMode(true); AutomationObject.SelectSection("Plate1");

read1 = AutomationObject.StartRead(); Results.AppendResult("Read ID = " + read1.ToString()); read1 = AutomationObject.StartRead(); Results.AppendResult("Read ID = " + read1.ToString()); read1 = AutomationObject.StartRead(); Results.AppendResult("Read ID = " + read1.ToString()); mCopyID = AutomationObject.GetDataCopy();

}

private void Error( object sender, SoftMaxPro.AutomationClient.SMPAutomationClient.ErrorEventArgs e)

{

Results.AppendResult("Error: Command ID = " + e.QueueID.ToString() + " - " + e.Error);

}

private void CommandCompleted( object sender, SoftMaxPro.AutomationClient.SMPAutomationClient.CommandStatusEventArg e)

{

Results.AppendResult("Command complete Command ID = " + e.QueueID.ToString() ); if( read1 == e.QueueID )

{

Results.AppendResult(e.StringResult);

}

if( e.QueueEmpty)

{

Results.AppendResult("Queue empty - disconnecting events"); AutomationObject.ErrorReport -= Error; AutomationObject.CommandCompleted -= CommandCompleted; AutomationObject.InstrumentStatusChanged -= InstrumentStatus;

AutomationObject.Dispose();

}

}
