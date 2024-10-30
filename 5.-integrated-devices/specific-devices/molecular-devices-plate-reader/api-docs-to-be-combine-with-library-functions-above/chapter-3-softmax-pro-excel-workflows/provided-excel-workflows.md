# Provided Excel Workflows

After you install the Add-In, you can run or edit the provided Excel workflows that the SoftMax Pro Software installs in the same folder as the Add-In files.

C:\Program Files (x86)\Molecular Devices\SoftMax Pro n.n Automation SDK\ExcelAddIn\Examples The Excel workflow files have the .xlsm file extension.

![](<../../../../../.gitbook/assets/6 (1) (1) (1) (1) (1) (1).png>)

**Note:** Save a copy of the workflow before you run or edit a provided Excel workflow.

**Excel Workflow Layouts**

Each Excel workflow must be contained in one workbook. This includes the provided workflows and the workflows you customize.

The provided workflows are color coded for readability. The color coding does not affect the execution of workflow. See Workflow Statement Types on page 26.

**Provided Workflow Statement Type Color Codes**

| **Workflow Statement Type**      | **Color Code** |
| -------------------------------- | -------------- |
| Initialization Statements        | Orange         |
| Automation Command Statements    | Yellow         |
| Worksheet Formatting Statements  | Green          |
| Workflow Flow Control Statements | Gray           |
| Free-Format Statement Arguments  | Pink           |

**SMPWorkflow Worksheet Features**

Each statement in the workflow is on a single row that starts in column B and can continue in the columns to the right with parameters or formatting information. Workflow Loop Control statements start in column A.

After you click Execute, the first statement is read and executed. See Running Excel Workflows on page 23.

![](<../../../../../.gitbook/assets/7 (1) (1) (1) (1) (1) (1).png>) The first blank column in the statement row indicates the end of the statement and then the next statement in the following row executes.

![](<../../../../../.gitbook/assets/8 (3).png>) The first blank row indicates the end of the workflow.

This document contains the list of valid instrument names to prevent mismatches in the format of the name of the instrument. You should copy and paste name into the workflow. See SetReader on page 87.
