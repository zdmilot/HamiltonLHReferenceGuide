# Instrument Connectivity

In most workflows, the user running the SoftMax Pro Software connects the software to the instrument before starting the workflow. This command instructs the workflow to connect to the instrument without user intervention.

To connect to an instrument or to an instrument in Simulator mode, use the following automation commands in the workflow:

![](<../../../../../.gitbook/assets/0 (29).png>) SetReader

![](<../../../../../.gitbook/assets/1 (25).png>) SetSimulationMode

As the automation API requires the name of the instrument be in a very specific format, each model of instrument is included in the supplied example Excel workbooks. When you write or change a workflow, copy and paste the instrument name into place in the workflow. This helps prevent mismatches in the format of the instrument name.

### Connecting to a Real Instrument

The port connected to the instrument should be coded as part of the SetReader command, and the instrument should be taken out of Simulation mode.

![](<../../../../../.gitbook/assets/2 (5).jpeg>) ![](<../../../../../.gitbook/assets/3 (2).jpeg>)

### Using Simulator Mode

The instrument should be set as Offline and the SetSimulation command should say TRUE.

![](<../../../../../.gitbook/assets/4 (2).jpeg>)
