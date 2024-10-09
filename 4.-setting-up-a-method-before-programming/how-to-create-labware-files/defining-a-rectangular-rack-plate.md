# Defining a Rectangular Rack (Plate)

The following section illustrates the procedures for defining a labware using the example of a rectangular rack. The first step of each labware definition is to describe the geometry of a single container. The second step is by putting several containers together which creates an overall labware (e.g. tube).\


For ease of use, in defining a rack for the containers, ensure that all racks and containers defined have clear and distinct names.

<figure><img src="../../.gitbook/assets/image (15).png" alt=""><figcaption></figcaption></figure>

1. Select “New -> Rectangular Rack” from the File Menu in the Labware Editor. A series of dialog boxes will appear allowing the programmer to design the rack.
   * Always choose “Regular rectangular rack” to define or modify rectangular racks and microplates. Choosing “Microplate” requests only a subset of the information relevant for the ML STAR.
   * If defining the cover is intended, check the “Include cover definition” Option.
   * Activate one of the “Visible by default” Options.
   * Click the “Background Color” Box to select a background color of preference.
   *   Type a name and a description for the new rack in the corresponding data fields.\
       \


       <figure><img src="../../.gitbook/assets/image (116) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>


2. Click \[Next >]. The image shown below will only be included in the wizard settings if the “Include Cover Definition” Box has been ticked in the previous step.
3.  To define the rack cover, specify the following:

    * “Covered Rack Stack Height”, i.e. the stack height if covers without racks are stacked
    * Distance from “Rack base to Cover Base”
    * “Stack Height”, if racks with covers are stacked
    * “Thickness of Cover” (in Z-dimension)
    * Cover “Dimensions” in x, y, and z
    * A cover name and description and select an icon for the graphical representation of the cover, if one exists

    \
    If the cover shall appear in a labware category, use the “Assign Labware Categories” Tab.\
    \


    <figure><img src="../../.gitbook/assets/image (118) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

    \
    \

4. To return to the previous step, simply click on the \[< Back] Button. To proceed click \[Next >]. A dialog for the definition of the rack shape in the x- and y-dimension will prompt.
5. For the x- and y-axes, click \[Insert Segment], to add the segments where the rack belongs.
6.  Specify the dimensions of each segment in mm as shown below.\


    <figure><img src="../../.gitbook/assets/image (18).png" alt=""><figcaption></figcaption></figure>
7. Click \[OK] on the “Geometry Segment” Screen and click \[Next >] on the “Rack Definition” Wizard.
8. After doing so, a new wizard will display, still requiring values.
9. In this dialog, key in the following:
   * Number of rows (number of containers in y-direction)
   * Number of containers or holes per row (in x-direction)
   * Hole inner diameter for display in the Deck Layout
   * Rack height (total height of the plate)
   * Rack clearance height (clearance from rack base where pipetting channels can travel safely)
   * Stack height (when multiple racks are stacked  height of one rack)
   * Dimensions for clearance height (safe travel height for tips/heads/tools) and stacking height. The difference between these two parameters is shown in the following sketch.
   * Tick “Load Rack with Containers”.
   * Give the overall clearance height of the assembly (here 100 mm).
   *   If there is a rack that cannot be stacked, leave a value of 0 mm in the field “Stack height”. Otherwise, measure or calculate the height. The image shown after the dialog box illustrates how to measure the height.\


       <figure><img src="../../.gitbook/assets/image (122) (1) (1).png" alt=""><figcaption></figcaption></figure>

       \
       ![](<../../.gitbook/assets/image (21).png>)
   * Tick “Include Rack Boundary”, to allow the boundaries to be set in one of the next steps.
10. Click \[Next >], to get the “Rectangular Rack Measurements” Dialog box shown below.
11. Enter the distance between the holes in:
    * x-direction (distance between the holes), in this example it is set at 9 mm
    * y-direction (distance between the rows), in this example it is set at 9 mm\
      ![](<../../.gitbook/assets/image (22).png>)
12. Click \[Next >] to proceed to the indexing dialog.\
    ![](<../../.gitbook/assets/image (23).png>)\
    \
    The default indexing parameters are set as used in the Microplate but with alphanumeric numbering instead of simple indexing. This can be selected or changed, depending on the application.
13. After specifying the correct settings, click \[Next >]. The dialog for the Boundary Measurements appears.
14. The dialog below defines the following:
    * Adjacent boundaries of the center of the hole with the lowest (bottom-left-most) x- and y- coordinates,
    * Width and length of the rack (e.g. the outline of a microplate)\
      \
      ![](<../../.gitbook/assets/image (24).png>)
15. The rack definition has been completed. Since the “Load the Rack with Containers” is checked in step 8, the containers which will be placed in the holes of the rack can be defined too.
16. Click \[Next >], to continue with the “Container Type” Definition.\
    ![](<../../.gitbook/assets/image (25).png>)
17. In this dialog, either browse the directories for already-defined containers (extension “.ctr”) to fill the new rack with or click \[New] to define a new container as described in Section 10.1.1 Defining a Container.
    * Tick the "Rack is regular" Option to add a single container type to all positions in the rack or to add different container types to positions in the rack, deactivate the "Rack is regular" Option and click on the \[Containers with Offset…] Button instead.
    * Tick the “Containers are connected” Setting, if there are virtual containers which are physically in one container. Virtual or Individual containers are required to position each probe or pipetting channel correctly within a single large container and to have the correct follow and volume calculations.
    * Enter the distance from the bottom of the rack to the bottom of the selected container. Remember to add in the thickness of the container bottom for calculations regarding the container’s “reference point”.
18. To handle the offsets for each container, click \[Containers with Offset]. All the containers with their offsets are listed in a table as presented below.\


    <table data-header-hidden><thead><tr><th width="145"></th><th></th></tr></thead><tbody><tr><td><img src="../../.gitbook/assets/image (10) (1) (1) (1) (1) (1) (1) (1).png" alt="" data-size="original"></td><td><p>NOTE</p><p><em>Update common values first, followed by updating each position through the grid, and the “fine tune” offset values.</em></p></td></tr></tbody></table>

    \
    \
    ![](<../../.gitbook/assets/image (27).png>)\

19. Select one or more positions and click on \[Position Properties…]. Note that all selected rows will be updated with the set of values from the table.
    * Optional container offset (x, y): The default position for any container is the ‘center’ of the container. This will be the calculated coordinate used at runtime (usually by a probe or tip).

**Example:** To change the calculated position of a container, provide the offset values of x and y from the actual center of the container. Enter a distance of 3 mm ‘to the right of container center’.

\


<table data-header-hidden><thead><tr><th width="145"></th><th></th></tr></thead><tbody><tr><td><img src="../../.gitbook/assets/image (10) (1) (1) (1) (1) (1) (1) (1).png" alt="" data-size="original"></td><td><p>NOTE</p><p><em>The offset values are per container position only.</em></p></td></tr></tbody></table>



19. Click \[Finish] to see the newly defined rack in the Labware Editor, presented on the next page.
20. Choose “File -> Save” from the File Menu in the Labware Editor or select the corresponding Toolbar Icon to store the new rack under the name “MyRack” (.rck) in the labware directory.

| After completing the definition, click SAVE. A visual representation of the plate is displayed | <img src="../../.gitbook/assets/image (124) (1) (1).png" alt="" data-size="original"> |
| ---------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- |
| <img src="../../.gitbook/assets/image (126) (1) (1).png" alt="" data-size="original">          | Assign one or more Labware Catagories to the new labware and click SAVE once more     |
| <img src="../../.gitbook/assets/image (129) (1) (1).png" alt="" data-size="original">          | <img src="../../.gitbook/assets/image (128) (1) (1).png" alt="" data-size="original"> |



### Fine-Tune Positions

A fine-tune of the positions of any container can be done. To do so, follow these steps:

1. Select “Edit -> Definition...” in the File Menu of the Labware Editor.
2. Click through all dialogs boxes until the last by clicking \[Next >].
3. In the “Container type” Dialog, a table displaying all containers with their corresponding number (defined in the “Indexes” Dialog) and the common base offset will be shown.
4. Move each container in any direction: x, y or z (see Step 14 for creating a container, Section 10.1.2 Defining a Rectangular Rack).
5. If everything is correct, click \[OK] to exit and \[Finish] to return to the Labware Editor.
6. Select “Exit” in the File Menu of the Labware Editor.
7. Once back in the Deck Layout Editor window, place the newly-designed rack on the deck by clicking the “Labware” Tab, clicking “Browse” and selecting the rack in the file selection box. The rack will be displayed in a graphical representation and can be dragged and dropped onto the deck.

