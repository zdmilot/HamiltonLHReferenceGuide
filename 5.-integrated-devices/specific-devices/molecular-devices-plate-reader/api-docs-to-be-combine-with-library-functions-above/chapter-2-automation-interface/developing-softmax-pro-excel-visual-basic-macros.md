# Developing SoftMax Pro Excel Visual Basic Macros

Visual Basic developers can write Excel Visual Basic macros that access the SoftMax Pro Software through the Automation API. SoftMax Pro Excel macro development requires the installation of the Excel Add-In.

See Installing Excel Add-Ins on page 21.

![](<../../../../../.gitbook/assets/0 (28).png>)

**Note:** Excel Visual Basic macros and Visual Basic .NET are very different software development environments. The development process in this section is significantly different from the Visual Basic

.NET example. See Automation Interface Overview on page 10.

### Accessing the SoftMax Pro Software Automation API

Use a tool called Excel-DNA to access the Excel Visual Basic SoftMax Pro Software automation API. To learn more about Excel-DNA, go to [http://exceldna.codeplex.com/](http://exceldna.codeplex.com/). Excel-DNA allows you to create a wrapper around the SoftMax Pro Software automation interface which results in the following differences.

### Automation Command Names

To invoke an automation command from Excel Visual Basic, prefix the SoftMax Pro Software automation command name with **SMP**.

For example, to invoke the **GetInstrumentStatus** automation API command from Excel Visual Basic, youinvoke **SMPGetInstrumentStatus**.

### Invocation Mechanism

Instead of invoking methods directly as in the Sample Source Code and Applications on page 12 for the **AutomationObject.OpenDrawer()**, commands are passed as arguments to an invocation of **Application.Run**.

For example, **Application.Run "SMPCloseDrawer"**. See SoftMax Pro Excel VBA Example on page 19.

### Synchronous Method Calls

Instead of checking the contents of an event for the result of an automation command, the result returns directly to the Excel Visual Basic statement that issues the command.

For example, **drawerStatus = Application.Run("SMPGetDrawerStatus")**. See SoftMax Pro Excel VBA Example on page 19.

### Error Detection

Two methods are available to Excel Visual Basic for error handling. ![](<../../../../../.gitbook/assets/1 (23).png>) CommandError = Application.Run("SMPHasError")

![](<../../../../../.gitbook/assets/2 (12).png>) ErrorMessage = Application.Run("SMPGetErrorMessage")

See SoftMax Pro Excel VBA Example on page 19.

### Instrument Status

No events are generated. Instead, invoke **SMPGetInstrumentStatus**.

### Command Names

To work within the constraints of the technology in this solution, some Excel Macro Commands do not conform exactly to the SMP prefix mechanism. See Invocation Mechanism on page 18.

![](<../../../../../.gitbook/assets/3 (14).png>) The automation API command SelectSection has two Excel Visual Basic equivalents: ![](<../../../../../.gitbook/assets/4 (13).png>) SMPSelectSectionByName(string sectionName)

![](<../../../../../.gitbook/assets/5 (12).png>) SMPSelectSectionByNumber(int sectionNumber)

![](<../../../../../.gitbook/assets/6 (9).png>) The automation API command Initialize has three Excel Visual Basic equivalents: ![](<../../../../../.gitbook/assets/7 (6).png>) SMPInitialize()

![](<../../../../../.gitbook/assets/8 (4).png>) SMPInitializeByServer(string server)

![](<../../../../../.gitbook/assets/9 (3).png>)SMPInitializeByServerAndPort(string server, int port)

### SoftMax Pro Excel VBA Example

A spreadsheet named VbaMacroExample.xlsm is installed in the SoftMax Pro n.n Automation SDK\ExcelAddIn folder. You should read the notes within the spreadsheet before you execute the Visual Basic macro in the file.

The following is an example of the code for a Visual Basic macro:

Sub AcquireData()

Dim initialized As Boolean Dim disposed As Boolean Dim drawerStatus As String Dim plateData As String Dim commandError As Boolean Dim errorMessage As String

Rem Connect to a running instance of SMP

initialized = Application.Run("SMPInitializeByServer", "localhost")

If initialized Then

Rem For testing purposes turn on the simulator Application.Run "SMPSetSimulationMode", True Rem Execute some sample/example commands Application.Run "SMPCloseDrawer"

drawerStatus = Application.Run("SMPGetDrawerStatus")

Rem Select an initial plate section to make sure we have the experiment selected Application.Run "SMPSelectSectionByName", "Plate1@Expt1"

Rem Check the plate section selection completed correctly, 'HasError' checks the last command executed

commandError = Application.Run("SMPHasError") If commandError Then

Rem An error has occurred

errorMessage = Application.Run("SMPGetErrorMessage") Else

Rem Add a new Plate section

End If

Application.Run "SMPNewPlate"

numberPlateSections = Application.Run("SMPGetNumberPlateSections") Rem Read the plate in the reader

Application.Run "SMPStartRead"

Rem Get the data from the plate

plateData = Application.Run("SMPGetDataCopy") Rem Put the data into Excel

Dim dataArray As Variant

dataArray = Split(plateData, Chr(9)) ActiveWorkbook.Sheets("Sheet1").Select For iRow = 0 To 8

For iCol = 0 To 14

Cells(iRow + 1, iCol + 1) = dataArray(iRow \* 15 + iCol) Next iCol

Next iRow

Rem tidy up

Application.Run "SMPSetSimulationMode", False disposed = Application.Run("SMPDispose")

End If End Sub
