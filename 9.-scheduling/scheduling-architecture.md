# Scheduling Architecture

## Pieces of the scheduling Puzzle

<figure><img src="../.gitbook/assets/image (62).png" alt=""><figcaption></figcaption></figure>

### Higher Level Organization

* Remove non-activity steps from a method ![](<../.gitbook/assets/image (79).png>)
* Create methods with fewer, related activities
* Use a workflow document to control the order of tasks instead of using a method to control the order of activities
* Allows scheduler to run other tasks, or add delays between the smaller task functions (if allowed)
* Must pass Resource units between tasks for consistent use

<figure><img src="../.gitbook/assets/image (80).png" alt=""><figcaption></figcaption></figure>

### Workflows

| <ul><li>Unique to scheduler</li><li>Higher level document than a Task</li><li>Allows logic (loops, conditionals) to drive method selection and task activation</li><li><p>Allows fine tuning of the schedule</p><ul><li>Task activation conditions</li><li>Eases information passing between tasks (parameters on selected methods)</li></ul></li><li>Programmer control of resource units</li><li>Fills parameters for methods that require them</li></ul><p><img src="../.gitbook/assets/image (63).png" alt=""></p> | <img src="../.gitbook/assets/image (64).png" alt="" data-size="original"> |
| ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------- |

