# Custom Excel Formulas

You can write custom formulas for use in a SoftMax Pro Excel workflow. You should add additional custom formulas to the SoftMax Pro Excel Visual Basic module called SMPWorkflow. See CellFormat Statement on page 30.

**ElapsedTime Custom Formula**

This custom formula writes a column of elapsed time values, in seconds, between successive instrument reads. This assists in plotting a graph of data collected from instrument reads over time. The ElapsedTime custom formula is provided with the SoftMax Pro Excel workflows.

### Dependency

The date/time of each read must be recorded in the Excel Worksheet.

### Usage

\=ElapsedTime(Base Date Cell, Date Column) where:

![](<../../../../../.gitbook/assets/0 (8).png>) Base Date Cell is the Excel worksheet cell that contains start date/time against which all other dates are compared.

![](<../../../../../.gitbook/assets/1 (11).png>) Date Column is the column that contains the dates to compare against the Base Date. The Date Column must be in quotation marks, for example, “C” for column C of the worksheet.

### ElapsedTime Example

This example describes how to use the ElapsedTime custom formula to write the elapsed time between runs in Column B of the Sheet1 worksheet.

![](<../../../../../.gitbook/assets/2 (4).jpeg>)

The output written to Excel appears in the following figure.

![](<../../../../../.gitbook/assets/3 (1).jpeg>)

### Visual Basic Code

Function ElapsedTime(ByVal startDate As Date, ByVal compareDateCol As String) As Long Dim compareDateColIndex As Long

compareDateColIndex = ColumnLetterToNumber(compareDateCol) Cells(ActiveCell.row, compareDateColIndex).NumberFormat = "dd/mm/yy"

Dim compareDate As Date

compareDate = Cells(ActiveCell.row, compareDateColIndex) ElapsedTime = DateDiff("s", startDate, compareDate)

End Function
