---
description: How to create and configure system layouts in Venus.
---

# Creating the Deck Layout

To create or modify system layouts in a predefined method, access the System Deck Editor within the Hamilton Method Editor while the method is open. Navigate to this by selecting **View -> System Deck** from the menu.

<figure><img src="../../.gitbook/assets/image (358).png" alt=""><figcaption></figcaption></figure>

This will bring you to the Layout Editor:

<figure><img src="../../.gitbook/assets/image (359).png" alt=""><figcaption></figcaption></figure>

## Creating a New System Deck <a href="#creating-a-new-system-deck" id="creating-a-new-system-deck"></a>

There are several methods to create a new system deck layout:

#### 1. Using an Existing Layout or Template <a href="#id-1.-using-an-existing-layout-or-template" id="id-1.-using-an-existing-layout-or-template"></a>

Select an existing layout or template from the dropdown list to create a new system deck. The dropdown shows files located in the default directories. You can also use the "Browse..." button to locate files in other directories.

#### 2. Using an Instrument <a href="#id-2.-using-an-instrument" id="id-2.-using-an-instrument"></a>

Create a new system deck by selecting a registered instrument from the dropdown list.

#### 3. Creating an Empty Deck <a href="#id-3.-creating-an-empty-deck" id="id-3.-creating-an-empty-deck"></a>

You can also create an empty system deck with no devices.

#### 4. Importing P'X5 Configuration <a href="#id-4.-importing-px5-configuration" id="id-4.-importing-px5-configuration"></a>

Import a configuration created and exported using Perspectix P'X5. The system will check for compatible instruments and devices before generating the new system deck.

### Adding a Deck Position <a href="#adding-a-deck-position" id="adding-a-deck-position"></a>

Deck positions can be added anywhere within the instrument deck space.

* **Name:** Assign a name to the deck position.
* **Location:** If the position coordinates are known, enter them manually.
* **Move Probe:** Use the "Move Probe" button to have the probe assign the position coordinates automatically.

### System Deck Options <a href="#system-deck-options" id="system-deck-options"></a>

Use this menu to customize the visualization and behavior of the System Deck.

#### View Options <a href="#view-options" id="view-options"></a>

* **Show Labware Tool Tips:** Display labware information via tooltips (available in 2D mode).
* **Show Labware Names:** Display labware names (only in 2D view). Use tooltips in 3D view modes.
  * **Labware Text Size:** Adjust the text size of labware names.
* **Use System 3D View:** Render the system in 3D.
* **Use Instrument 3D Views:** Render instruments in 3D. The sequence view mode remains in 2D.
* **Advanced 3D View Options:** Open a sub-menu to adjust 3D quality and appearance settings.

### Deck Layers <a href="#deck-layers" id="deck-layers"></a>

![](https://zacharys-organization-2.gitbook.io/\~gitbook/image?url=https%3A%2F%2F290267149-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252FL1EbG69WzgF8VGhKqqtE%252Fuploads%252FwZoI7iX7rYeqMx8LWACA%252Fimage.png%3Falt%3Dmedia%26token%3D7986a237-f952-4b29-afef-88529a1579bc\&width=768\&dpr=4\&quality=100\&sign=69bbbf5\&sv=1)

#### Deck Layers List <a href="#deck-layers-list" id="deck-layers-list"></a>

This displays all deck layers for the current instrument deck. Checkboxes next to each layer allow you to toggle their visibility.

#### Using Deck Layers <a href="#using-deck-layers" id="using-deck-layers"></a>

Access all layer management functions through the context menu in the Layers panel.

* **Active Layer:** The currently selected layer. New labware or sequences are assigned here.
* **Show/Hide Layer:** Toggle the visibility of a layer. Hidden layers and their contents will not be drawn, listed, or available for operations. The active layer cannot be hidden.
* **Add Layer:** Create a new layer with a specified name.
* **Rename Layer:** Change a layer’s name (must be unique).
* **Delete Layer:** Delete a layer. Labware and sequences assigned solely to this layer will also be deleted.
* **Show All Layers:** Make all layers visible.
* **Hide All Layers:** Hide all layers except the active one.

## Labware <a href="#labware" id="labware"></a>

Follow the naming convention used for default labware when naming new labware definitions. Include a prefix of the manufacturer and a brief description of the labware. For example, a Falcon branded 96-well flat bottom plate would be named “Fal\_96FlatBottom”. More detailed info like the part number should go in the description field in the labware definition.

#### Labware Category Tree <a href="#labware-category-tree" id="labware-category-tree"></a>

Displays a categorized view of available labware. Unassigned labware can be accessed via the "Browse..." button.

#### Labware Category List <a href="#labware-category-list" id="labware-category-list"></a>

Shows labware assigned to the selected category. If no optional name is set, the file name is shown.

#### Searching for Labware <a href="#searching-for-labware" id="searching-for-labware"></a>

Enter keywords to search for labware. Results are displayed in the list, and categories are automatically opened for selected labware.

#### Labware Preview <a href="#labware-preview" id="labware-preview"></a>

A preview of the selected labware is displayed on the right side, with a description and image if available.

#### Adding Labware <a href="#adding-labware" id="adding-labware"></a>

Drag labware to the desired deck position. You can also copy labware already placed on the deck.

* **Generate Default Deck Sequence:** Automatically create a default sequence for new labware.
* **Include Cover:** Optionally add a cover if available.

### Labware Editing on the Instrument View <a href="#labware-editing-on-the-instrument-view" id="labware-editing-on-the-instrument-view"></a>

Right-click on labware to access the following options:

| Option               | Description                                        |
| -------------------- | -------------------------------------------------- |
| Properties           | View and assign labware properties                 |
| Adjust Location      | Fine-tune the labware’s position                   |
| Copy/Paste           | Duplicate or move labware                          |
| Delete               | Remove labware from the deck                       |
| Add Default Sequence | Create a default sequence for labware              |
| Add to Stack         | Add additional labware of the same type to a stack |
| Reduce Stack         | Remove one item from the stack                     |
| Layer Linking        | Manage the layer associated with the labware       |
| Add Deck Position    | Add a new position to the deck                     |
| Add Resource         | Add a resource (Dynamic Scheduler required)        |
| Edit Resources       | Edit resources (Dynamic Scheduler required)        |
| Bring to Front       | Move the labware to the foreground (2D view only)  |
| Send to Back         | Move the labware to the background (2D view only)  |
| Select Labware       | Highlight the labware (3D view only)               |

### Adjusting Labware Location <a href="#adjusting-labware-location" id="adjusting-labware-location"></a>

You can adjust the labware position using fixed or flexible deck positions. A rotational factor can also be applied. If the position is known, coordinates can be entered manually.

* **Move Probe:** Use the probe’s coordinates to automatically assign position coordinates.
