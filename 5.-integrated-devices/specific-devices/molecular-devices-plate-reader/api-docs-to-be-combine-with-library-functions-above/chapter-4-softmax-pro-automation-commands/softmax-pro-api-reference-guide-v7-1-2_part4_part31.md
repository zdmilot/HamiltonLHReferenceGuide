# softmax pro api reference guide v7 1 2\_Part4\_Part31

if( e.QueueEmpty)\
{\
Results.AppendResult("Queue empty - disconnecting events");\
AutomationObject.CommandCompleted -= CommandCompleted;AutomationObject.Dispose(); }\
}

OpenFile

Int32 OpenFile(String pathname)\
The OpenFile command opens a protocol or data document. If the file is not found, the SoftMax Pro application does nothing.

Parameters\
pathname

Type: String

(SoftMax Pro Software - Standard edition) - Fully qualified path to protocol file or protocol name

(SoftMax Pro Software - GxP edition) - Project name / full path / document name

Example\
This example describes how to open a file that exists in the file system.

int mStatusID;\
string mPath="C:\\\Users\\\All Users\\\Application Data\\\Molecular Devices\\\SMP6\\\Default Protocols\\\Basics\\\Spectrum.spr";\
public void Main()\
{\
AutomationObject.Initialize("localhost");\
AutomationObject.CommandCompleted += CommandCompleted;\
AutomationObject.ErrorReport += Error;\
mStatusID = AutomationObject.OpenFile(mPath);\
}\
private void CommandCompleted( object sender,\
SoftMaxPro.AutomationClient.SMPAutomationClient.CommandStatusEventArg e)\
{\
Results.AppendResult("Command complete Command ID = " + e.QueueID.ToString() ); if( mStatusID == e.QueueID )\
{\
Results.AppendResult(e.StringResult);\
}\
if( e.QueueEmpty)\
{\
Results.AppendResult("Queue empty - disconnecting events");\
AutomationObject.ErrorReport -= Error;
