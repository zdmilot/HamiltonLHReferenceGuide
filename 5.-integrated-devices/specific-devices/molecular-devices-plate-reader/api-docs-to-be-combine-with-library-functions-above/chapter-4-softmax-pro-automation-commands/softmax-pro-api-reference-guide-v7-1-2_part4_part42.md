# softmax pro api reference guide v7 1 2\_Part4\_Part42

Results.AppendResult("Command complete Command ID = " + e.QueueID.ToString() ); if( mCopyID == e.QueueID )\
{\
Results.AppendResult(e.StringResult);\
}\
if( e.QueueEmpty)\
{\
Results.AppendResult("Queue empty - disconnecting events");\
AutomationObject.ErrorReport -= Error;\
AutomationObject.CommandCompleted -= CommandCompleted;\
AutomationObject.InstrumentStatusChanged -= InstrumentStatus;\
AutomationObject.Dispose();\
}\
}\
private void InstrumentStatus( object sender,\
SoftMaxPro.AutomationClient.SMPAutomationClient.InstrumentStatusEventArgs e) {\
Results.AppendResult("Status changed to " + e.Status);\
}

StopRead

Int32 StopRead()\
The StopRead command stops the read of a Plate section or Cuvette Set section. This command is not queued.

Parameters\
None
