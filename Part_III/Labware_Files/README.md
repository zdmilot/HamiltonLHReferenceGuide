# How to Create Labware Files

If the labware is not pre-defined, custom racks and containers can be defined using the Labware Editor. The custom labware can be used like any other pre-defined labware object from the library. A labware object is a representation of the real physical labware.

To define the new labware:

1.  Select “Tools  Labware  Labware Editor …” in the Method Editor, or the “Define Labware” Icon found on the toolbar:

    \


    ![image](../../.gitbook/assets/Image\_473.png)

    ![labware icon](../../.gitbook/assets/Image\_474.gif)

    Labware Editor

    \

2. The Labware Editor with an empty main window will be activated.
3. To create a new labware, select “File  New“ from the Labware Editor Menu. The sub-menu offers five choices, which are the different types of labware. This will be explained in the succeeding sub-sections.

\


![image](../../.gitbook/assets/Image\_475.jpg)

1.  ### ‌Defining a Labware‌

    \


    The following section illustrates the procedures for defining a labware using the example of a rectangular rack. The first step of each labware definition is to describe the geometry of a single container. The second step is by putting several containers together which creates an overall labware (e.g. tube).

    \


    1.  #### ‌Defining a Container‌

        \


        A completed container can then be used in a rack definition.

        1. Select “File  New  Container“ from the Labware Editor Menu.
        2. Define the container as a round-bottomed tube with an outer diameter of 10 mm, with a total container length of 75 mm and a material thickness of 0.5 mm.
        3. Indicate the number of container segments as “2” because the tube has a cylindrical segment and a round-bottomed segment.
        4.  Remember that the Base Point for all further references is the inside bottom point.

            ![image](../../.gitbook/assets/Image\_476.png)

            10

            \


            Segm. 1

            Base point 75

            Segm. 2

            0.5

            \

        5.  Set the clearance height at 80 mm (75 mm for the container length plus additional 5 mm for the traveling); measured from the container inner base (Base Point). The clearance height is the height at which the pipetting arm can pass over the container without touching it.

            \


            ![image](../../.gitbook/assets/Image\_477.png)

            Clearence height
        6. Set the maximum pipetting height (minimum height above tube bottom) counted from the container bottom to 4 mm. This allows the tip to go down to a position of 4 mm above the tube bottom (this gives the “Dead Volume”).
        7. Click the checkbox for Liquid Level Detection, to mark it.
        8.  With the assumption that the last 7 mm will not contain any liquid and with some additional LLD space (here 2.5 mm) the liquid seeking height is 70 mm.

            An information will be prompted when an unexpected LLD is found.

            \


            ![C:\Users\cweber\Desktop\Capture.PNG](../../.gitbook/assets/Image\_478.gif)

            \

        9. Set the “touch-off at bottom height” to 0 mm.
        10. “Touch-off at bottom height” is the position of the tip when dispensing with “touch off” into an empty container.
        11. If a side touch dispensing on the container is not wanted, leave the “wick side of container” checkbox unmarked.

            \


            ![image](../../.gitbook/assets/Image\_479.jpg)

            \


            A Side Touch Dispense is a special dispense mode to prevent droplets on the tips end.
        12. The tip will move in the center of the container to the specific touch off height. From there, a Right move is performed. Then, the liquid will be dispensed and the tip or needle moves up and away.

            \


            ![image](../../.gitbook/assets/Image\_480.jpg) ![image](../../.gitbook/assets/Image\_481.jpg) ![image](../../.gitbook/assets/Image\_482.jpg) ![image](../../.gitbook/assets/Image\_483.jpg)

            \

        13. To perform a side touch dispense with the ML STAR, the values for the touch off height and the right move must be specified. Mark the checkbox “wick side of container” to display the dialog for setting the values as shown below.

            \


            ![SNAGHTML11b7ee5](../../.gitbook/assets/Image\_484.png)

            \

        14. Click \[Next >] to continue.
        15. The “Container Segment Definition” Screen shown below appears.

            \


            ![image](../../.gitbook/assets/Image\_485.jpg)
        16. Select “Cylinder” as a shape for the upper segment (Segment 1).
        17. Supply values for the inner diameter (10 mm) and the segment height (20 mm).
        18. Now, Click on the “Segment 2” Tab. The tab should appear as follows.
        19. Select the \[Rounded base segment] Radio Button.
        20. Supply values for the upper internal diameter (10 mm) and the segment height (12 mm).

            \


            ![image](../../.gitbook/assets/Image\_486.jpg)

            \

        21. Click \[Next >]. The screen presented below will appear.

            \

        22. Unmark the “Use front distance for all” Box. Supply a value for the right move and one for the touch off height. Please make sure that the values are correct, otherwise it can result to a mechanical crash.

            \


            ![image](../../.gitbook/assets/Image\_487.png)
        23. Either calculate or measure these values before testing on a real instrument. An example on how to measure the values is being illustrated below.

            \


            ![image](../../.gitbook/assets/Image\_488.jpg)

            \

        24. Click \[Finish] to complete the container definition.
        25. Select the “![save icon](../../.gitbook/assets/Image\_489.gif)” Icon from the Toolbar to save the newly defined container or select “File  Save as” from the File Menu. Enter a name for the container (e.g. “MyContainer”.\[ctr]) and click \[Save].

        \

    2.  #### ‌Defining a Rectangular Rack‌

        \


        For ease of use, in defining a rack for the containers, ensure that all racks and containers defined have clear and distinct names.

        \


        ![image](../../.gitbook/assets/Image\_490.jpg)

        \


        1.  Select “New  Rectangular Rack” from the File Menu in the Labware Editor. A series of dialog boxes will appear allowing the programmer to design the rack.

            \


            *   Always choose “Regular rectangular rack” to define or modify rectangular racks and microplates. Choosing “Microplate” requests only a subset of the information relevant for the ML STAR.

                \

            *   If defining the cover is intended, check the “Include cover definition” Option.

                \

            *   Activate one of the “Visible by default” Options.

                \

            * Click the “Background Color” Box to select a background color of preference.
            *   Type a name and a description for the new rack in the corresponding data fields.

                \


                ![image](../../.gitbook/assets/Image\_491.jpg)

                \

        2.  Click \[Next >]. The image shown below will only be included in the wizard settings if the “Include Cover Definition” Box has been ticked in the previous step.

            \

        3. To define the rack cover, specify the following:
           * “Covered Rack Stack Height”, i.e. the stack height if covers without racks are stacked
           * Distance from “Rack base to Cover Base”
           * “Stack Height”, if racks with covers are stacked
           * “Thickness of Cover” (in Z-dimension)
           * Cover “Dimensions” in x, y, and z
           *   A cover name and description and select an icon for the graphical representation of the cover, if one exists

               If the cover shall appear in a labware category, use the “Assign Labware Categories” Tab.

               \


               ![image](../../.gitbook/assets/Image\_492.jpg)

               \

        4. To return to the previous step, simply click on the \[< Back] Button. To proceed click \[Next >]. A dialog for the definition of the rack shape in the x- and y-dimension will prompt.
        5. For the x- and y-axes, click \[Insert Segment], to add the segments where the rack belongs.
        6.  Specify the dimensions of each segment in mm as shown below.

            \


            ![image](../../.gitbook/assets/Image\_493.jpg)
        7.  Click \[OK] on the “Geometry Segment” Screen and click \[Next >] on the “Rack Definition” Wizard.

            \


            ![image](../../.gitbook/assets/Image\_494.jpg)

            \

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
           *   If there is a rack that cannot be stacked, leave a value of 0 mm in the field “Stack height”. Otherwise, measure or calculate the height. The image shown after the dialog box illustrates how to measure the height.

               \


               ![image](../../.gitbook/assets/Image\_495.jpg)

               ![image](../../.gitbook/assets/Image\_496.png) ![image](../../.gitbook/assets/Image\_497.png)

               Clearance height Stack height
           *   Tick “Include Rack Boundary”, to allow the boundaries to be set in one of the next steps.

               \

        10. Click \[Next >], to get the “Rectangular Rack Measurements” Dialog box shown below.
        11. Enter the distance between the holes in:
            * x-direction (distance between the holes), in this example it is set at 9 mm
            *   y-direction (distance between the rows), in this example it is set at 9 mm

                \


                ![image](../../.gitbook/assets/Image\_498.jpg)
        12. Click \[Next >] to proceed to the indexing dialog.

            \


            ![image](../../.gitbook/assets/Image\_499.jpg)

            The default indexing parameters are set as used in the Microplate but with alphanumeric numbering instead of simple indexing. This can be selected or changed, depending on the application.

            \

        13. After specifying the correct settings, click \[Next >]. The dialog for the Boundary Measurements appears.
        14. ‌The dialog below defines the following:
            * Adjacent boundaries of the center of the hole with the lowest (bottom-left-most) x- and y- coordinates,
            *   Width and length of the rack (e.g. the outline of a microplate)

                \


                ![image](../../.gitbook/assets/Image\_500.jpg)

                \

        15. The rack definition has been completed. Since the “Load the Rack with Containers” is checked in step 8, the containers which will be placed in the holes of the rack can be defined too.
        16. Click \[Next >], to continue with the “Container Type” Definition.

            \


            ![image](../../.gitbook/assets/Image\_501.jpg)

            \

        17. In this dialog, either browse the directories for already-defined containers (extension “.ctr”) to fill the new rack with or click \[New] [to define a new container as described in ](./#bookmark212)[Section ](./#bookmark212)10.1.1[ ](./#bookmark212)Defining a Container.
            * Tick the "Rack is regular" Option to add a single container type to all positions in the rack or to add different container types to positions in the rack, deactivate the "Rack is regular" Option and click on the \[Containers with Offset…] Button instead.
            * Tick the “Containers are connected” Setting, if there are virtual containers which are physically in one container. Virtual or Individual containers are required to position each probe or pipetting channel correctly within a single large container and to have the correct follow and volume calculations.
            * Enter the distance from the bottom of the rack to the bottom of the selected container. Remember to add in the thickness of the container bottom for calculations regarding the container’s “reference point”.
        18. To handle the offsets for each container, click \[Containers with Offset]. All the containers with their offsets are listed in a table as presented below.

            \


            ![Originalbild anzeigen](../../.gitbook/assets/Image\_502.gif)

            NOTE

            Update common values first, followed by updating each position through the grid, and the “fine tune” offset values.

            ![image](../../.gitbook/assets/Image\_503.jpg)

            \

        19. Select one or more positions and click on \[Position Properties…]. Note that all selected rows will be updated with the set of values from the table.
            *   Optional container offset (x, y): The default position for any container is the ‘center’ of the container. This will be the calculated coordinate used at runtime (usually by a probe or tip).

                \


                Example: To change the calculated position of a container, provide the offset values of x and y from the actual center of the container. Enter a distance of 3 mm ‘to the right of container center’.

                \


                ![image](../../.gitbook/assets/Image\_504.jpg)

                ![Originalbild anzeigen](../../.gitbook/assets/Image\_505.gif)

                NOTE

                The offset values are per container position only.

                \

        20. Click \[Finish] to see the newly defined rack in the Labware Editor, presented on the next page.
        21. Choose “File  Save” from the File Menu in the Labware Editor or select the corresponding Toolbar Icon to store the new rack under the name “MyRack” (.rck) in the labware directory.

        \


        ![image](../../.gitbook/assets/Image\_506.jpg)

        \


        Fine-Tune Positions

        A fine-tune of the positions of any container can be done. To do so, follow these steps:

        1. Select “Edit  Definition...” in the File Menu of the Labware Editor.
        2. Click through all dialogs boxes until the last by clicking \[Next >].
        3. In the “Container type” Dialog, a table displaying all containers with their corresponding number (defined in the “Indexes” Dialog) and the common base offset will be shown.
        4. [Move each container in any direction: x, y or z (see ](./#bookmark214)[Step 14 for creating a container, ](./#bookmark214)Section[ ](./#bookmark214)10.1.2 Defining a Rectangular Rack).
        5. If everything is correct, click \[OK] to exit and \[Finish] to return to the Labware Editor.
        6. Select “Exit” in the File Menu of the Labware Editor.
        7. Once back in the Deck Layout Editor window, place the newly-designed rack on the deck by clicking the “Labware” Tab, clicking “Browse” and selecting the rack in the file selection box. The rack will be displayed in a graphical representation and can be dragged and dropped onto the deck.
