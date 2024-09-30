---
description: Adding and managing pipetting, mixing, and other steps in the action editor.
---

# Activity Action Editor

The command **Action Editor** or **Activity Editor** from **View** menu on Steps Editor activates the Activity/Action Editor.

The command **Replace Actions with Activities** from **Method** menu on Steps Editor is used to change from Action Editor to Activity Editor.

The command **Replace Activities with Actions** from **Method** menu on Steps Editor is used to change from Activity Editor to Action Editor.

&#x20;

## Activity Editor

The Activity Editor is a graphical editor, containing activity symbols, start and end symbol and connections. Activity symbols can be free positioned in the editor window. Directed connections are added between activity symbols. The activity symbols are connected in the order as they appear in the steps editor. The activities in the steps editor and in the activity editor are synchronized. Adding an activity symbol generates an activity step in the steps editor and adding an activity step in the steps editor adds an activity symbol in the activity editor.&#x20;

The toolbox contains the resources defined in the system deck. Drag and drop a resource to the activity editor creates an activity that uses this resource. The activity symbol is configured with Select Activity Type property page, Activity Resources property page, Activity Data property page, and Advanced Activity Data dialog box of the Activity wizard. The activity step may also be configured with the Activity dialog box.

### Start Symbol, End Symbol

The start symbol indicates the start of the method and the end symbol indicates the end of the method. The start symbol is the predecessor of the first activity. The symbols are connected direct or indirect with activity links and activity symbols.

### Activity Symbol

Activity symbols represent activities in the method. The activity diagram shows the activities in the order as they appear in the ‘Method’ in the steps editor. The symbol is labeled with the activity name. The image displayed is the image of the first resource for this activity. The image of the resource is defined in the system deck. The following table shows the commands/actions on an activity symbol:

| Command             | How to execute command and description                                                                                                                                                                                                                                                                                                                                                                                    |
| ------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Move Symbol.        | Moving the symbol with the mouse, by clicking left mouse button an dragging mouse. Moving the selected symbol with the arrow keys. When a symbol is moved, the edges of this symbol are also moved.                                                                                                                                                                                                                       |
| Reposition Activity | Drag and Drop the Activity over an activity link. The insert cursor shows the insert position for the activity if it is dropped. Holding down the CTRL key saves the insert cursor position but the activity symbol can be moved to a free place.                                                                                                                                                                         |
| Delete.             | The activity is deleted. The steps of the activity are disabled (not deleted), with two exceptions: The Activity Wait step and the Abort step are also deleted.                                                                                                                                                                                                                                                           |
| Add Activity        | <p>Drag and Drop a resource from the toolbox.</p><p>To append the activity at the end of the method, drop it on a free place.</p><p>To insert the activity between other activities, move the activity over an activity link. A cursor is displayed that shows the insert position for the activity. Holding down the CTRL key saves the insert cursor position but the activity symbol can be moved to a free place.</p> |
| Properties          | Selecting Properties on the context menu, or Properties from the Edit menu, or a double-click. This command displays the Activity wizard for the selected activity symbol.                                                                                                                                                                                                                                                |
| Go to Activity      | The command opens the steps editor and displays the associated activity step.                                                                                                                                                                                                                                                                                                                                             |

&#x20;

&#x20;

### Resources in Toolbox

The toolbox contains the resources defined in the system deck. The resources are displayed with the display Name and with an image. The toolbox provides on its context menu a command to add, edit, and delete resources on the system deck. The toolbox provides drag and drop of a resource item to the activity editor.

&#x20;

### Toolbox Context Menu:

| Command       | How to execute command and description                                          |
| ------------- | ------------------------------------------------------------------------------- |
| Add Resource… | Opens the dialog box to add a resource to the system deck (and to the toolbox). |
| Edit…         | Opens the dialog box to edit the resource that is selected in toolbox.          |
| Delete        | Removes the selected resource from system deck (and from toolbox).              |

&#x20;

&#x20;

### Activity Link:

An activity link is a line with an arrow drawn between an ancestor activity symbol and a predecessor activity symbol to indicate a relationship. The line represents a directed connection between the predecessor and the ancestor activity. The activity link displays an image, if steps exist between the two activities.

&#x20;

## Action Editor

The Action Editor is similar to the activity editor. It is used to arrange actions (activities in Activity Editor) from Start to End. Actions are created by drag and drop activities from toolbox. The actions and the action steps in the steps editor are synchronized.

The toolbox contains the activities for the instruments in the system deck. Drag and drop an activity to the action editor creates an action.
