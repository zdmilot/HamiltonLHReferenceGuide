---
icon: dev
---

# Hamilton Run Control

Hamilton Run Control controls execution of methods and visualizes run progress.

<figure><img src="../../.gitbook/assets/image (10) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

## To Run a Method

**To open the method**

1. On the **File** menu, click **Open**.
2. In the **File Open** dialog box select the method file, change the **file type** with the **Files of type** combo-box if necessary.
3. Click **OK** to close the dialog box.

The method is now loaded and the application either shows a  Run Control Toolbar or a Run Time Control window, depending on the method. The following steps use the **Run Control Toolbar** to run the method. If a **Run Time Control** is visible, refer to it's documentation.

**To start execution**

1. In the **Run Control Toolbar** click the **Start** button.

<table data-header-hidden><thead><tr><th width="145"></th><th></th></tr></thead><tbody><tr><td><img src="../../.gitbook/assets/image (10) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" data-size="original"></td><td><p>NOTE</p><p>Some menu commands will be disabled during method execution.ent to a ML STAR will result in an error message.</p></td></tr></tbody></table>



**To pause execution**

1. In the **Run Control Toolbar** click the **Pause** button.

### Print Traces

**To print traces**

1. On the **File** menu, click **Print Runtime Trace**.
2. In the **Print Trace** dialog box select the trace file and click **Print** button.

### Toolbar

The toolbar is displayed across the top of the application window, below the menu bar. The toolbar provides quick mouse access to many tools used in Hamilton Run Control application.

| <img src="../../.gitbook/assets/Screenshot 2024-10-10 130837.png" alt="" data-size="original">                                      | Close Hamilton Run Control application and return to the parent editor. This button is available only if Hamilton Run Control application was started from an editor. |
| ----------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| <img src="../../.gitbook/assets/image (26) (1) (1) (1) (1) (1).png" alt="" data-size="original">                                    | Open a method file. Hamilton Run Control application displays the Open dialog box, in which you can locate and open the desired file.                                 |
| <img src="../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" data-size="original"> | Opens context sensitive Help window.                                                                                                                                  |



### Run Control Toolbar

Run Time ActiveX control user interface consists of three buttons and a list box. Clicking on Start button initiates method execution. Method execution can be paused by clicking on Pause button. Clicking on Prime button opens the Prime Configuration Dialog. Sample Tracing Display represented by a list box displays the current method execution status.

The Run Control Toolbar provides commands to control the execution of a method:

| Button                                                                        | Effect                                           |
| ----------------------------------------------------------------------------- | ------------------------------------------------ |
| <img src="../../.gitbook/assets/image (734).png" alt="" data-size="original"> | Analyzes the method.                             |
| <img src="../../.gitbook/assets/image (735).png" alt="" data-size="original"> | Starts method execution.                         |
| <img src="../../.gitbook/assets/image (736).png" alt="" data-size="original"> | Pauses method execution.                         |
| <img src="../../.gitbook/assets/image (739).png" alt="" data-size="original"> | Resumes a paused method execution.               |
| <img src="../../.gitbook/assets/image (738).png" alt="" data-size="original"> | Executes the first instrument step and pauses.   |
| <img src="../../.gitbook/assets/image (740).png" alt="" data-size="original"> | Aborts method execution.                         |
| <img src="../../.gitbook/assets/image (733).png" alt="" data-size="original"> | Shows Control Panel dialog boxes of Instruments. |

The last field of the Run Control Toolbar shows the current state of the run control. The field indicates if a method is loading (analyzing), ready to run (idle),  running, or pausing.

<table data-header-hidden><thead><tr><th width="145"></th><th></th></tr></thead><tbody><tr><td><img src="../../.gitbook/assets/image (10) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" data-size="original"></td><td><p>NOTE</p><p>During a run execution, menu and toolbar commands including <strong>Exit</strong> will be disabled.</p></td></tr></tbody></table>

\


## Views

A view is a window that is displayed inside the Hamilton Run Control window (the main window). A view displays information from the run control or from a instrument, e.g. displays trace output or displays the deck layout. A view may have a menu and a toolbar. The view's menu and toolbar are displayed when the view is activated (the user has clicked in the window or uses the window menu).

**Visibility and position**

The user can open or close a view with the Views menu or with the Views toolbar and can move and resize the window of a view like common windows. The Run Control saves the visibility state (is the view open or closed) and the window position. The next time a method is opened, the views are restored.

**Two types of views**

* Run control views
* Instrument views

**Run control views**

The run control views display information offered by a specific run control, e.g. if a HSL method is opened, the  HSL run control views are opened. For example, the following HSL run control views are available:

* Trace view
* Method view
* Variable watch view
* HSL debug view

**Instrument/Deck Layout views**

The instrument views display information specific to the instrument, e.g. the deck layout of that instrument (deck view). The instrument views of all instruments used in a method are opened when the method is loaded.

The deck layout view shows a deck layout that is connected to an instrument.

This view supports the Zoom In  and the Zoom Out command  from the View menu and from the Toolbar.



### Zoom Toolbar / Menus

The Zoom Toolbar (and the zoom menus) provides functionality to zoom the contents of some views.

| **Button**                                                                                                                      | **Effect**                                              |
| ------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------- |
| <img src="../../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" data-size="original"> | Enables the hand tool for moving the content of a view. |
| <img src="../../.gitbook/assets/image (3) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" data-size="original">         | Enables the zoom in tool.                               |
| <img src="../../.gitbook/assets/image (5) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" data-size="original">                 | Enables the zoom out tool.                              |
| <img src="../../.gitbook/assets/image (6) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" data-size="original">                     | Zooms in the current view.                              |
| <img src="../../.gitbook/assets/image (7) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" data-size="original">                     | Zooms out the current view.                             |
| <img src="../../.gitbook/assets/image (8) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" data-size="original">                     | Fits the zoom to show all content of the view.          |
| <img src="../../.gitbook/assets/image (9) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" data-size="original">                     | Resets the zoom to its actual value.                    |

Each view itself defines which buttons are enabled. If a view doesn't support this functionality, all buttons are disabled.

