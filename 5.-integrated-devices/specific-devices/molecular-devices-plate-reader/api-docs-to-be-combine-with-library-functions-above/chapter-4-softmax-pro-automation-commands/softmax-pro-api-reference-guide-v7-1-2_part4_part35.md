# softmax pro api reference guide v7 1 2\_Part4\_Part35

AutomationObject.ErrorReport -= Error;\
AutomationObject.CommandCompleted -= CommandCompleted;\
AutomationObject.Dispose();\
}\
}\
private void Error( object sender,\
SoftMaxPro.AutomationClient.SMPAutomationClient.ErrorEventArgs e)\
{\
Results.AppendResult("Error: Command ID = " + e.QueueID.ToString() + " - " + e.Error); }

SelectSection

Int32 SelectSection(String sectionName)\
Int32 SelectSection(Int32 sectionNumber)\
The SelectSection commands select a section by name or by the order of the section within an experiment. SelectSection using the System.String parameter is useful for multi-plate protocols or to select Group tables to copy.

Parameters\
sectionName\
Type: String

The name of the section.

Either the name of a section within an experiment or a fully qualified section name, including section and experiment identifiers

Examples: sectionName or sectionName@experimentName sectionNumber

Type: Int32

The order number of the section.

Example\
This example describes how to select a section using the System.String parameter.

int mStatusID;\
public void Main()\
{\
AutomationObject.Initialize("localhost");\
AutomationObject.CommandCompleted += CommandCompleted; AutomationObject.ErrorReport += Error;\
AutomationObject.NewExperiment();\
mStatusID = AutomationObject.SelectSection("Pleate1@Exp02"); AutomationObject.NewExperiment();\
mStatusID = AutomationObject.SelectSection(2);\
AutomationObject.AppendTitle("\_&&^^\*\*%%\$$##@@");
