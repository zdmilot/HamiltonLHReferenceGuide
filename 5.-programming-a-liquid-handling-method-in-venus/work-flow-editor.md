---
description: How to structure workflows for simple to complex methods.
---

# Work Flow Editor

The workflow editor is used to create and edit workflow files. A workflow consists of four files with the extensions WFL, HSL, STP, SUB.

## The workflow editor window

The workflow editor window is divided into two sections, Advanced Workflow Steps and Graphical Window. A section is opened if clicking on the section's button (section's title). The currently opened section is closed.

## Advanced Workflow Steps

This sections can be used to execute steps before the workflow (defined in the graphical window) is activated. This section contains the Method Editor Window and provides it's functionality and the toolbox contains steps from instruments, smart steps and libraries. Note: Programming a more sophisticated workflow may be done in this section using the Scheduler Smart Steps.

## Graphical Window

The graphical workflow editor window is used to create a workflow by drag Selected Methods from the toolbox to the graphical window and create Tasks.  A task is displayed as a rectangular symbol with the task name. Activation Links connect Tasks with lines. A workflow is a graph with the Start symbol and tasks as nodes and activation links as directed edges (lines with arrows).

## Start Symbol

The start symbol is always contained in a workflow graphic once. This symbol can not be deleted. Moving the symbol is allowed. The start symbol can be the ancestor of tasks. This is expressed with an activation link from the start symbol to the task symbol. Such an activation link does per default activate the task when the workflow starts running. The start symbol does not have properties.

## Task

A task is a symbol in the workflow graphic. The symbol is labeled with the task name. The following table shows the commands/actions on a task symbol:

| Command                   | How to execute command and description                                                                                                                                                                                                                                                                                                                                     |
| ------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Move Symbol.              | Moving the symbol with the mouse, by clicking left mouse button an dragging mouse. Moving the selected symbol with the arrow keys.When a symbol is moved, the edges of this symbol are also moved.                                                                                                                                                                         |
| Cut, Copy, Paste, Delete. | <p>Standard behavior. Data is transfered to the clipboard.</p><p>Note: Copy does also add a picture of the selection, that can be pasted in a word processing application.</p>                                                                                                                                                                                             |
| Add Task                  | Drag and Drop a selected method from the toolbox.                                                                                                                                                                                                                                                                                                                          |
| Task Properties           | Selecting Properties on the context menu, or Properties from the Edit menu, or a double-click. This command displays the Task Properties dialog box for the selected task                                                                                                                                                                                                  |
| Check of tasks            | <p>The editor checks if a task is valid after each change.</p><p>The check includes:</p><ul><li>Task has an predecessor, either a task or the start symbol.</li><li>An activation link must point to the task.</li></ul><p>If the check is negative, an error message is displayed on the tooltip of the task and the task is marked (Displayed in a different color).</p> |

&#x20;

&#x20;

## Task Activation Link

A task activation link is a directed edge that connects two tasks.

A task activation link is displayed as a sequence of line segments with an arrow at the target end. No label is displayed. The properties of the task activation link are displayed on a tooltip&#x20;

To add a Task Activation Link, choose the Add Activation Link command on the Edit menu or on the Context menu. Click on the Start symbol or on the predecessor Task, then click on the target task.

To modify the properties of the Task Activation Link, select the link and choose the Properties command on the Edit menu or double click the activation link. (See Task Activation dialog box and Task Activation at specified Time dialog box).

&#x20;

## Check of Task Activation Link

The editor checks if all task activation links are valid after a change. The check includes:

* A task activation link must have a predecessor task (or Start Symbol) and a target task.
* Cycles are not allowed. That is: The target task must not point to the predecessor task, neither direct (same task is target and origin) nor indirect (target task has a link to predecessor task).
* All tasks must be directly or indirectly connected with Task Activation Link's to the Start Symbol.
