# SoftMax Pro Automation Sample Application



The SoftMax Pro Automation Sample Application allows you to prototype and test code. The SoftMax Pro Automation Sample Application binds the automation interface to a Microsoft scripting control.

![](<../../../../../.gitbook/assets/0 (1) (1) (1) (1) (1) (1) (1) (1) (1).png>)

![](<../../../../../.gitbook/assets/1 (1) (1) (1) (1) (1) (1) (1) (1).png>)

**Note:** The SoftMax Pro Automation Sample Application is not intended for use in an actual laboratory or research environment.

Execute the SoftMax Pro Automation Sample Application shortcut from the Windows Start menu to display the Scripting Window dialog.

The Scripting Window dialog allows you view the interface commands and to load, run, and save scripts. Errors display in the Compiler Errors area and output information for the script display in the Result area.

To prototype sample code, the SoftMax Pro Automation Sample Application scripting engine creates the object instance for the automation component, called AutomationObject, behind the scenes. In the script, you can use this object to access all automation commands and events to monitor. If you transfer the code to a stand-alone application, you must add the code to create the automation object instance.

The SoftMax Pro Automation Sample Application includes a Result object that allows you to append text data. You can use this to monitor the execution of commands and the progress in the command queue.

After you prototype the programming code in the Script area in the Scripting Window dialog, you can use the code to create a stand-alone robotic/automation application that directly controls the SoftMax Pro Software.

### Creating Projects With Visual Studio

The automation interface allows you to use your preferred programming language to develop custom applications and create new projects with Visual Studio.

1. Select the relevant template (for example, Windows Form Application, WPF Application, or Console Application).
2. Add a reference to each of the following assemblies: ![](<../../../../../.gitbook/assets/2 (1) (1) (1) (1) (1) (1) (1) (1) (1).png>) SoftMax Pro AutomationClient.dll

![](<../../../../../.gitbook/assets/3 (1) (1) (1) (1) (1) (1) (1) (1).png>) SoftMaxPro.AutomationInterface.dll ![](<../../../../../.gitbook/assets/4 (1) (1) (1) (1) (1) (1) (1).png>) SoftMaxPro.AutomationExtensions.dll

The default installation places these assembles in the following path: C:\Program Files (x86)\Molecular Devices\SoftMax Pro n.n Automation SDK

![](<../../../../../.gitbook/assets/5 (1) (1) (1) (1) (1) (1).png>)

**Note:** The SoftMax Pro Automation Sample Application does not display the assembly because the assembly loads dynamically at run time and is injected into the scripting interface. You must reference the assembly for normal application development.

### Sample Source Code and Applications

Sample automation scripts and the command example scripts that this guide describe are included as a part of the SoftMax Pro Automation API installation package. The default software installation places the samples scripts in the following location:

C:\Program Files (x86)\Molecular Devices\SoftMax Pro n.n Automation SDK\Scripts You can use the sample application to load, view, and run the script examples.

### Example

This example of a basic code structure includes a call to Initialize(), a subscription to an event, and a Dispose() call to terminate the connection. These examples assume that you use the SoftMax Pro Automation Sample application.

// An instrument must be connected to SoftMax Pro

// before running this code

int lastCommandId = -999; bool connected = false;

public void Main()

{

// Initialize the interface

connected = AutomationObject.Initialize();

if ( connected )

{

// Hook up the CommandCompleted event AutomationObject.CommandCompleted+= CommandCompleted;

// Open the reader drawer

lastCommandId = AutomationObject.OpenDrawer();

}

}

private void CommandCompleted( object sender, SoftMaxPro.AutomationClient.SMPAutomationClient.CommandStatusEventArg e)

{

// report on the command being completed

Results.AppendResult("Command complete Command ID = " + e.QueueID.ToString() );

// Disconnect from the automation server if( lastCommandId == e.QueueID )

{

Results.AppendResult("Command execution complete, disconnecting from server"); AutomationObject.CommandCompleted -= CommandCompleted; AutomationObject.Dispose();

}

}

This generates the following output:

Command complete Command ID = 0Command execution complete, disconnecting from server

### C\#

This example is similar logic written in C#.

private int lastCommandId = -999;

private bool connected = false; private SMPAutomationClient client;

public void OpenDrawerExample()

{

// Create an instance of the automation client client = new SMPAutomationClient();

// Initialize the interface connected = client.Initialize();

if (connected)

{

// Hook up the CommandCompleted event client.CommandCompleted += CommandCompleted;

// Open the reader drawer lastCommandId = client.OpenDrawer();

}

}

private void CommandCompleted(object sender, SMPAutomationClient.CommandStatusEventArg e)

{

// report on the command being completed

Console.WriteLine("Command complete Command ID = " + e.QueueID.ToString());

// Disconnect from the automation server if (lastCommandId == e.QueueID)

{

Console.WriteLine("Command execution complete, disconnecting from server"); client.CommandCompleted -= CommandCompleted;

client.Dispose();

}

}

### Visual Basic .NET

This example is similar logic written in Visual Basic .NET.

Imports System.Threading

Imports SoftMaxPro.AutomationClient Module OpenDrawerExample

Dim lastCommandId = -999

Dim client As SMPAutomationClient

Sub Main()

REM Create an instance of the automation client client = New SMPAutomationClient

REM Initialize the interface

Dim connected = client.Initialize()

If (connected) Then

REM Hook up the CommandCompleted event

AddHandler client.CommandCompleted, AddressOf CommandCompleted

REM Open the reader drawer WaitForCommandCompletion(client.OpenDrawer())

REM Disconnect from the automation server

Console.WriteLine("Command execution complete, disconnecting from server") RemoveHandler client.CommandCompleted, AddressOf CommandCompleted client.Dispose()

End If End Sub

Private Sub CommandCompleted(ByVal sender As Object, \_ ByVal e As SMPAutomationClient.CommandStatusEventArg)

Console.WriteLine("Command complete Command ID = " + e.QueueID.ToString()) lastCommandId = e.QueueID

End Sub

Private Sub WaitForCommandCompletion(ByVal commandId As Integer) While commandId > lastCommandId

Thread.Sleep(10) End While

End Sub End Module

### Get() Functions

Commands that return information, that you prefix with Get..., like GetVersion() or GetNumberPlateSections(), are queued like other commands. The command returns information by way of the CommandStatusEventArgs class in the CommandCompleted event.

### The CommandStatusEventArg class

public class CommandStatusEventArg : EventArgs

{

public CommandStatusEventArg( int queueID, bool queueEmpty, int commandID, int intResult, String stringResult)

{

QueueID = queueID; QueueEmpty = queueEmpty; CommandID = commandID; IntResult = intResult; StringResult = stringResult;

}

public int QueueID; public bool QueueEmpty; public int CommandID; public int IntResult;

public String StringResult;

}

### Functions That Return Information

This example demonstrates how to use functions that return information.

int mStatusID;

public void Main()

{

AutomationObject.Initialize(); AutomationObject.CommandCompleted+= CommandCompleted;

mStatusID = AutomationObject.GetVersion(); Results.AppendResult("Status Command ID = " + mStatusID .ToString() );

}

private void CommandCompleted( object sender, SoftMaxPro.AutomationClient.SMPAutomationClient.CommandStatusEventArg e)

{

Results.AppendResult("Command complete Command ID = " + e.QueueID.ToString() );

if( mStatusID== e.QueueID )

{

Results.AppendResult( "Result: " +e.StringResult);

}

if( e.QueueEmpty)

{

Results.AppendResult("Queue empty - disconnecting events"); AutomationObject.CommandCompleted -= CommandCompleted; AutomationObject.Dispose();

}

}
