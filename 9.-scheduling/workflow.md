# Workflow

## Taking programming to a higher level

### Workflow Set-Up

| <p></p><ul><li><p>Workflow drop down options</p><ul><li>May turn off warning about instrument movement (Workflow Properties)</li></ul></li><li><p>Method -> Instruments and Smart Steps</p><ul><li>Enable Scheduler Steps</li><li>Disable smart steps (can cause excessive memory use)</li></ul></li><li><p>HSLSchedLib</p><ul><li>Many useful scheduler functions</li></ul></li></ul> | <img src="../.gitbook/assets/image (65).png" alt="" data-size="original"> |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------- |

## Building a Workflow

### Select Method

| <ul><li>Found in Scheduler Steps</li><li>Defines a handle to interact with a method</li><li>HSL file name and Method view name may be built from strings</li><li>Method id is the handle name subsequent steps will reference</li><li>Method parameters must be entered if the HSL file requires them</li></ul> | <img src="../.gitbook/assets/image (71).png" alt="" data-size="original"> |
| --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------- |

<figure><img src="../.gitbook/assets/image (72).png" alt=""><figcaption></figcaption></figure>

### Activate Task

| <ul><li>Tasks are created referencing Selected Methods</li><li>Activated tasks are placed in the scheduler “hopper” </li><li>The act of scheduling evaluates all programmer rules and it’s own preferences to determine the schedule of Activated Tasks</li><li>Therefore, the line order that tasks are activated do not impact the schedule </li><li>For example, tasks activated in 1/2/3 order may still schedule 3/2/1 chronological (schedule) order </li></ul>                                                                                                                                                                                                                                                                              | <img src="../.gitbook/assets/image (73).png" alt="" data-size="original"> |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------- |
| <ul><li>Found in Scheduler Steps</li><li>For a given Method ID, provides the scheduler with the rules for when it can be run</li><li><p>Task view name: the name that appears for the task in the Gantt chart </p><ul><li>By default, names would be repeated if step is repeated</li><li>Custom strings useful for uniqueness and for Relations</li></ul></li><li>Bound Task ID: The task ID scheduler creates for this activated task</li><li><p>Activation Criterion:</p><ul><li>Relation and the ID of other tasks are used to make sure that tasks activate in proper order, if needed</li></ul></li><li>Activate at: Set a global time/date – be careful of subsequent activation criterions, can shift remaining schedule</li></ul><p> </p> | <img src="../.gitbook/assets/image (74).png" alt="" data-size="original"> |



## &#x20;Phases

| <p></p><h3>Step Visibility</h3><ul><li>Workflow steps have multiple phases they can exist in</li><li>Set from right click menu</li></ul><h3>Scheduler Only <img src="../.gitbook/assets/image (76).png" alt="" data-size="line"> </h3><ul><li>Only available to run between loading to run control and the before “start” is pressed</li><li>Workflows that are scheduler only are straightforward, can still use UI/GUI’s to determine the schedule</li></ul><h3>Executer Only <img src="../.gitbook/assets/image (77).png" alt="" data-size="line"></h3><ul><li>Only available to run after “start” is pressed</li></ul><h3>Executer And Scheduler <img src="../.gitbook/assets/image (78).png" alt="" data-size="line"></h3><ul><li>Runs in both phases (similar to a Method’s non-activity steps)</li></ul> | <img src="../.gitbook/assets/image (75).png" alt="" data-size="original"> |
| --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------- |



&#x20;

&#x20;
