# The TADM Tolerance Band Editor

## **The TADM Tolerance Band Editor**

**Overview**

The TADM Tolerance Band Editor consists of several parts, as shown in its main window.

<figure><img src="../../.gitbook/assets/image (36) (1) (1) (1) (1).png" alt=""><figcaption><p><strong>Fig. 31: TADM Tolerance Band Editor main window</strong></p></figcaption></figure>

1\. Menu toolbar

2\. Filter TADM Curves toolbar

3\. TADM window

4\. Plotting area

The TADM window consists of three tabs (Upper Curve, Lower Curve, TADM Curves). The first two tabs contain the coordinates for the points of the upper and lower tolerance bands respectively. The third tab lists the properties of the displayed TADM curves. The following properties can be viewed: the method name of the run where the TADM curve was recorded, the channel number, pipette date, pipette result (processed/aborted), TADM mode (Recording/Monitoring), and the Curve ID. TADM curves of aborted pipetting steps are displayed in red in the plotting area, while successfully processed ones are displayed in dark blue.

<table data-header-hidden><thead><tr><th width="145"></th><th></th></tr></thead><tbody><tr><td><p></p><p><img src="../../.gitbook/assets/12 (1) (1) (1).jpeg" alt="" data-size="original"></p><p></p></td><td><p><strong>NOTE</strong></p><p><em>The Pipette result “Aborted” can only occur if the run was performed in Monitoring mode.</em></p></td></tr></tbody></table>



Analyzing a large number of TADM curves in an efficient way can be achieved by using the functions available in the “Filter TADM curves” toolbar:

* choose between curves obtained during either recording mode, monitoring mode or both.&#x20;
* choose between processed, aborted, or all curves obtained.
* choose whether curves from all channels or just a specific channel should be displayed.

Obviously, it makes sense to combine these options to limit the number of curves that have to be analyzed – for example: display all curves that were aborted (in monitoring mode) using channel number 5.

## **Menu details**

Below is an overview of all available menus with their options and the corresponding toolbar icons:

Below is an overview of all available menus with their options and the corresponding toolbar icons:

\


| File                                          | Description                                                                                                                                          |
| --------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------- |
| <p><br></p><p>Close &#x26; Apply Changes</p>  | Changes made to the tolerance band (upper and lower limit curves) will be saved and the Tolerance Band Editor will be closed.                        |
| <p><br></p><p>Close &#x26; Cancel Changes</p> | Tolerance band changes will be ignored and the Tolerance Band Editor will be closed. If any changes were made, a cue appears to discard all changes. |

| Edit                                                                                                                                                                                                                                                                                    | Description                                                                                                                                  |
| --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------- |
| <p>Cut Ctrl+X</p><p>Copy Ctrl+C</p><p>Paste Ctrl+V</p><p>Delete Del</p>                                                                                                                                                                                                                 | These options apply to individual tolerance band points, and are only active when either the “Upper curve” or “Lower curve” tab is selected. |
| <p><img src="../../.gitbook/assets/image (37) (1) (1) (1) (1).png" alt="" data-size="original"></p><p>Select</p>                                                                                                                                                                        | When activated, tolerance band points or TADM curves are selectable by clicking on them in the plotting area                                 |
| <p><img src="../../.gitbook/assets/image (38) (1) (1) (1) (1).png" alt="" data-size="original"></p><p>Add Upper Limit Curve Points</p><p><br></p><p><img src="../../.gitbook/assets/image (39) (1) (1) (1) (1).png" alt="" data-size="original"></p><p>Add Lower Limit Curve Points</p> | When activated, clicking in the plotting area adds an upper/lower tolerance band point                                                       |
| <p><img src="../../.gitbook/assets/image (40) (1) (1) (1) (1).png" alt="" data-size="original"></p><p>Delete Limit Curve Points</p>                                                                                                                                                     | When this is activated, clicking on a tolerance band point deletes it                                                                        |
| Delete Limit Curve Point Del                                                                                                                                                                                                                                                            | Deletes a single selected tolerance band point                                                                                               |
| Exclude TADM Curve Ctrl+E                                                                                                                                                                                                                                                               | A selected TADM curve will be excluded (not shown, and not used for guidance curves).                                                        |

| View                                                                                                                                                                                                                                                                                                                                                                                                   | Description                                        |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | -------------------------------------------------- |
| Hand Tool Ctrl+H ![](<../../.gitbook/assets/image (41) (1) (1) (1) (1).png>)                                                                                                                                                                                                                                                                                                                           | Move plotting area.                                |
| <p>Zoom In Tool Ctrl+Shift+I <img src="../../.gitbook/assets/image (42) (1) (1) (1) (1).png" alt=""></p><p>Zoom Out Tool Ctrl+Shift+O <img src="../../.gitbook/assets/image (44) (1) (1) (1) (1).png" alt=""> Zoom In Ctrl+I <img src="../../.gitbook/assets/image (46) (1) (1) (1) (1).png" alt=""></p><p>Zoom Out Ctrl+O <img src="../../.gitbook/assets/image (45) (1) (1) (1) (1).png" alt=""></p> | Zoom into or out of plotting area as desired.      |
| Fit To Window Ctrl+F ![](<../../.gitbook/assets/image (47) (1) (1) (1) (1).png>)                                                                                                                                                                                                                                                                                                                       | Fit all curves to window.                          |
| Guidance Curves                                                                                                                                                                                                                                                                                                                                                                                        | Display guidance curves.                           |
| Excluded TADM Curves                                                                                                                                                                                                                                                                                                                                                                                   | Display excluded TADM curves as dashed lines.      |
| <p><img src="../../.gitbook/assets/image (48) (1) (1) (1) (1).png" alt="" data-size="original"></p><p>TADM Curves...</p>                                                                                                                                                                                                                                                                               | Add or remove TADM curves.                         |
| Guidance Curves Formula...                                                                                                                                                                                                                                                                                                                                                                             | Edit guidance curve parameters.                    |
| <p><img src="../../.gitbook/assets/image (49) (1) (1) (1) (1).png" alt="" data-size="original"></p><p>Line Size</p>                                                                                                                                                                                                                                                                                    | Change size of selected, guidance and limit curves |
| Refresh F5                                                                                                                                                                                                                                                                                                                                                                                             | Refresh plotting area.                             |

Click "Help" in the dialog box of menu item "Guidance Curves Formula..." for the formula behind the guidance curves.

| Window                                                           |                                                       |
| ---------------------------------------------------------------- | ----------------------------------------------------- |
| <p>Upper Limit Curves Ctrl+U</p><p>Lower Limit Curves Ctrl+L</p> | Display upper or lower limit curve points as desired. |
| TADM Curve Properties Ctrl+T                                     | Display TADM curve properties on left side of window. |

| Help        | Description           |
| ----------- | --------------------- |
| Help Topics | View the online help. |

