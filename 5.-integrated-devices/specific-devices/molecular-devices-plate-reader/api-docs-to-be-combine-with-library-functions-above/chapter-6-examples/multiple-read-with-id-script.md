# Multiple Read With ID Script

public void Main()

{

string now = System.DateTime.Now.ToString(); Results.AppendResult(now); AutomationObject.Initialize("localhost"); AutomationObject.CommandCompleted+= CommandCompleted; AutomationObject.SetReader("Offline", "SPECTRAmax M2"); AutomationObject.SetSimulationMode(true); AutomationObject.SelectSection("Plate1");

int read1 = AutomationObject.StartRead(); Results.AppendResult("Read 1 ID = " + read1.ToString()); int read2 = AutomationObject.StartRead(); Results.AppendResult("Read 2 ID = " + read2.ToString()); int read3 = AutomationObject.StartRead(); Results.AppendResult("Read 3 ID = " + read3.ToString());

}

private void PrintCurrentTime()

{

string now = System.DateTime.Now.ToString(); Results.AppendResult("Read completed at: " + now);

}

private void CommandCompleted( object sender, SoftMaxPro.AutomationClient.SMPAutomationClient.CommandStatusEventArg e)

{

PrintCurrentTime();

Results.AppendResult("Command complete Command ID = " + e.QueueID.ToString() ); if( e.QueueEmpty)

{

Results.AppendResult("Queue empty - disconnecting events"); AutomationObject.CommandCompleted -= CommandCompleted; AutomationObject.Dispose();

}

}
