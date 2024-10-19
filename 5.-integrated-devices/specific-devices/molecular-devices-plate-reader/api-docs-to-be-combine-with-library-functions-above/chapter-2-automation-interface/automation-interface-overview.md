# Automation Interface Overview

You use the automation interface to control the SoftMax Pro Software. To use the automation interface to connect to the SoftMax Pro Software, call the Initialize() function. After the automation interface initializes, the SoftMax Pro Software enters automation mode. Automation mode disables the SoftMax Pro Software user interface to prevent user input.

To end automation mode from the automation interface, call Dispose() or click Terminate from the SoftMax Pro Software user interface.

After initialization completes, hook up the events for the application to monitor. You should disconnect events when the CommandCompleted event indicates that the command queue is empty.

Commands in the automation interface return a command ID and the command IDs are maintained in a command queue. Each command ID is stored and then used to obtain command results when the command completes. An application obtains the results of a command by subscribing to the CommandCompleted event and matching the command ID in the event with the one that returns when the command is sent.

![](../../../../../.gitbook/assets/4.jpeg)

You should consider the following published events when you design and write an automation application. See Events on page 97.

![](<../../../../../.gitbook/assets/5 (1) (1).png>) **ErrorReport Event** - When the automation server detects an error, an Error event is published, followed by a CommandComplete event. All commands in the automation server command queue are flushed.

![](<../../../../../.gitbook/assets/6 (1) (1).png>) **InstrumentStatus Event** - When the instrument changes state, for example from Idle to Busy, an InstrumentStatus event is published.

To create an environment for C# and Visual Basic .NET clients, see Creating Projects With Visual Studio on page 12.
