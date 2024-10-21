# GetFormulaResult

Int32 GetformulaResult(String results)\
The GetFormulaResult command returns the result from a formula. This command requires the name of the formula, name of either the Note section or the Group section, and the name of the experiment. If you do not specify the experiment name, it searches from the first experiment in the document.

| <img src="../../../../../.gitbook/assets/0 (16) (1).png" alt="" data-size="original"> | Note: The returned value is the calculated value for the formula, not the formula string. |
| ------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- |

Parameters\
results

Type: String

fully qualified formula name, including section and experiment identifiers

Example: formulaName@sectionName@experimentName

Returns\
This function returns the command ID used to retrieve the data that the CommandCompleted Event returns.

Data Returned Through the CommandCompleted Event

Type: String

Calculated value for the formula

Example\
This example describes how to get information from a Note section. If the Note section does not have a field titled Summary1, the command fails.

int mID;\
int bAutomix;\
System.Collections.Generic.Dictionary\<int, string> commandResultFormatter = new System.Collections.Generic.Dictionary\<int, string>();\
public void Main()\
{\
string now = System.DateTime.Now.ToString();\
Results.AppendResult(now);\
AutomationObject.Initialize("localhost");\
AutomationObject.ErrorReport += Error;\
AutomationObject.CommandCompleted += CommandCompleted;\
AutomationObject.SelectSection("Notes1");\
mID = AutomationObject.GetFormulaResult("Summary1");\
commandResultFormatter.Add(mID, "Formula Result of Summary1 :- {0}");

AutomationObject.SelectSection("Notes1");\
mID = AutomationObject.GetFormulaResult("Summary2");\
commandResultFormatter.Add(mID, "Formula Result of Summary2 :- {0}");\
}\
private void Error( object sender,\
SoftMaxPro.AutomationClient.SMPAutomationClient.ErrorEventArgs e)\
{\
Results.AppendResult("Error: Command ID = " + e.QueueID.ToString() + " - " + e.Error); }\
private void CommandCompleted( object sender,\
SoftMaxPro.AutomationClient.SMPAutomationClient.CommandStatusEventArg e)\
{\
Results.AppendResult("Command complete Command ID = " + e.QueueID.ToString() ); if( !string.IsNullOrEmpty(e.StringResult) )\
{\
if(commandResultFormatter.ContainsKey(e.QueueID))\
Results.AppendResult(string.Format(commandResultFormatter\[e.QueueID],\
e.StringResult));\
else\
Results.AppendResult(e.StringResult);\
}\
if( e.QueueEmpty)\
{\
Results.AppendResult("Queue empty - disconnecting events");\
AutomationObject.ErrorReport -= Error;\
AutomationObject.CommandCompleted -= CommandCompleted;\
AutomationObject.Dispose();\
}\
}
