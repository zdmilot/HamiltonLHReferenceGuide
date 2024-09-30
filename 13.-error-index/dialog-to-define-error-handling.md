# Dialog to define error handling

## Error Handling dialog

This dialog lists the errors that can occur during an instrument step and allows use of predefined default error handling or to configure a custom error recovery.

&#x20;

**Error List:**

This table lists all errors of the step.

&#x20;

**Error**

The name of the error.

&#x20;

**🞎 Use default**

If checked the predefined default error handling will be used. If unchecked a custom error recovery can be configured.

&#x20;

**Description**

Shows a short description of the error.

&#x20;

**Error Recovery Settings:**

The error recovery settings show the predefined error handling if _Use default_ is checked; if not checked it allows to configure custom error recovery.

&#x20;

**Timeout**

**Infinite**

If checked, an infinite timeout is used.\
The step error recovery dialog is not closed automatically, user input is required in any case.

&#x20;

**Custom**

Time in seconds to wait for user input before the automatic error handling will be started.\
If timeout is set to 0 (zero) the error recovery will be started immediately (no step error dialog is shown).\
Only enabled if _Infinite Timeout_ is not checked.

&#x20;

**Error Recovery List**

The table shows the error recovery options for the currently selected error in the _Error List_.

&#x20;

**Recovery**

The name of the recovery option.

&#x20;

**🞎 1st Recovery**\
Indicates which error recovery will be executed after timeout has elapsed. Exactly one recovery must be checked as first recovery.\
Only enabled if _Infinite Timeout_ is not checked.

&#x20;

**🞎 2nd Recovery**\
After _First Recovery_ is finished and the same error occurs again, the second recovery will be started after the timeout has elapsed.\
If a second recovery is defined, the count of _Repetitions for the first recovery_ must be set at least to 1 (if set to 0, the system will implicit set the number of _Repetitions_ to 1).\
Only enabled if _Infinite Timeout_ is not checked.

&#x20;

**🞎 Visible**\
If checked, the corresponding button is enabled within step error dialog.

&#x20;

**🞎 Flag Error (Sample Tracker Database)**\
If checked, an error recovery will be tracked on sample tracker database. If not checked, the action state is always set to 'No Error'.

&#x20;

**Description**

Shows a short description of the error recovery option.

&#x20;

**Repetitions for the 1st Recovery**\
Defines the number of repetitions of _First Recovery_ before the _Second Recovery_ will be started.\
Only enabled if _Infinite Timeout_ is not checked.

&#x20;

Note:\
If Repetitions is set to 0 (zero) and no Second Recovery is defined, the First Recovery will be used as many times as necessary. This may lead - depending of set recovery and persistence of error - to an endless loop. It is recommended to use a proper timeout to enable user interaction.

&#x20;

**🞎 Show infinite dialog**

If _Show infinite dialog_ is set as second recovery, the step error dialog is visible with infinite timeout and user interaction becomes necessary.\
Only enabled if _Infinite Timeout_ is not checked.

&#x20;

**Notification Sound**\
File name with path (.wav) to sound which will be played in case of an error. If not set, the error sound as defined for the operating system will be played.\
A sound will only be played if the step error dialog is visible.

&#x20;
