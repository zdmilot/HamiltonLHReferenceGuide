# Excel Visual Basic Components

A Visual Basic module named SMPWorkflow contains logic to initiate the invocation of workflow statements, worksheet formatting logic, and custom Excel formulas. See Custom Excel Formulas on page 45.

The following Visual Basic messages can display:

![](<../../../../../.gitbook/assets/0 (3).png>) The workflow is being validated before execution. ![](<../../../../../.gitbook/assets/1 (4).png>) The workflow is being executed.

![](<../../../../../.gitbook/assets/2 (3).png>) The workflow is paused, with details. ![](<../../../../../.gitbook/assets/3 (4).png>) An error was detected.

Running Excel Workflows

To run a workflow for the first time, you need an open SoftMax Pro Excel workflow that contains no saved data in the worksheet. You must install the Excel Add-In with macros enabled. The SoftMax Pro Software must be running.

Workflows enable you to perform the following operations:

![](<../../../../../.gitbook/assets/4 (3).png>) Executing Continuous Workflows (see below)

![](<../../../../../.gitbook/assets/5 (5).png>) Continuing Discontinuous Workflows, see page 24 ![](<../../../../../.gitbook/assets/6 (3).png>) Canceling Workflows, see page 25

In most workflows, you connect the SoftMax Pro Software to the instrument before you start the workflow. You can have the workflow connect the SoftMax Pro Software to the instrument without user intervention. See Instrument Connectivity on page 47.

### Executing Continuous Workflows

To run the workflow once and save the data in the Excel worksheet:

1. Physically connect the computer to the instrument and power on the instrument.
2. Start the SoftMax Pro Software.
3. Open the Excel workflow to run.
4. In the SMPWorkflow worksheet, click **Execute**.
5. After the workflow completes, save the worksheet.

### Continuing Discontinuous Workflows <a href="#bookmark1" id="bookmark1"></a>

After you execute an Excel workflow to acquire SoftMax Pro Software data, the workflow writes the data to Excel in List Format style and does not overwrite existing data in the worksheets. This allows you to do kinetic reads with variable intervals, such as in a discontinuous workflow. The List Format saves data in separate rows after each read.

1. Physically connect the computer to the instrument and power on the instrument.
2. Start the SoftMax Pro Software.
3. Connect the SoftMax Pro Software to the instrument.
4. Open the Excel workflow to run.
5. In the SMPWorkflow worksheet, click **Execute**.
6. After the workflow completes, save the workbook. The data worksheet has one row of data.
7. Close the workbook.
8. After the correct amount of time passes, open the Excel workflow again.
9. Physically connect the computer to the instrument and power on the instrument.
10. Start the SoftMax Pro Software.
11. Connect the SoftMax Pro Software to the instrument.
12. In the SMPWorkflow worksheet, click **Execute**.
13. After the workflow completes save the workbook. Each worksheet now has an additional row of data.
14. Repeat these step for each additional read.
15. Close the workbook.

### Example Results

When you execute a read once every hour, after the first read the worksheet has one row of data similar to the following:

| **Date/Time**   | **Elapsed Time** | **Temperature** | **A1** | **A2** |
| --------------- | ---------------- | --------------- | ------ | ------ |
| 1/22/2021 18:57 | 0                | 31.5            | 0.30   | 0.21   |

After the second read, the worksheet has two rows of data similar to the following:

| **Date/Time**   | **Elapsed Time** | **Temperature** | **A1** | **A2** |
| --------------- | ---------------- | --------------- | ------ | ------ |
| 1/22/2021 18:57 | 0                | 31.5            | 0.30   | 0.21   |
| 1/22/2021 19:57 | 3600             | 31.5            | 0.31   | 0.25   |

### Canceling Workflows <a href="#bookmark2" id="bookmark2"></a>

When you run an Excel workflow, a message displays in front of the SoftMax Pro Software window, to indicate that the software is in automation mode.

![](../../../../../.gitbook/assets/7.jpeg)

Click **Terminate** to stop the automation mode and regain control of the SoftMax Pro Software. Then close all open dialogs in the Excel workflow.
