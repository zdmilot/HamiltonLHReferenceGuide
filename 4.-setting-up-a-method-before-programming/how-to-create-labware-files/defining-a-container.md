# Defining a Container

The following section illustrates the procedures for defining a labware using the example of a rectangular rack. The first step of each labware definition is to describe the geometry of a single container. The second step is by putting several containers together which creates an overall labware (e.g. tube).\


<figure><img src="../../.gitbook/assets/image (108) (1) (1) (1) (1).png" alt=""><figcaption><p>All measurements are from the inside bottom of container</p></figcaption></figure>



A completed container can then be used in a rack definition.

1. Select “File -> New -> Container“ from the Labware Editor Menu.
2. Define the container as a round-bottomed tube with an outer diameter of 10 mm, with a total container length of 75 mm and a material thickness of 0.5 mm.
3. Indicate the number of container segments as “2” because the tube has a cylindrical segment and a round-bottomed segment.
4.  Remember that the Base Point for all further references is the inside bottom point.\


    <figure><img src="../../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" width="375"><figcaption></figcaption></figure>
5.  Set the clearance height at 80 mm (75 mm for the container length plus additional 5 mm for the traveling); measured from the container inner base (Base Point). The clearance height is the height at which the pipetting arm can pass over the container without touching it.\


    <figure><img src="../../.gitbook/assets/image (3) (1) (1) (1) (1) (1) (1) (1).png" alt="" width="188"><figcaption></figcaption></figure>
6. Set the maximum pipetting height (minimum height above tube bottom) counted from the container bottom to 4 mm. This allows the tip to go down to a position of 4 mm above the tube bottom (this gives the “Dead Volume”).
7. Click the checkbox for Liquid Level Detection, to mark it.
8.  With the assumption that the last 7 mm will not contain any liquid and with some additional LLD space (here 2.5 mm) the liquid seeking height is 70 mm.\
    \
    An information will be prompted when an unexpected LLD is found.

    <figure><img src="../../.gitbook/assets/image (4) (1) (1) (1) (1) (1) (1) (1).png" alt="" width="375"><figcaption></figcaption></figure>
9. Set the “touch-off at bottom height” to 0 mm.
10. “Touch-off at bottom height” is the position of the tip when dispensing with “touch off” into an empty container.
11. If a side touch dispensing on the container is not wanted, leave the “wick side of container” checkbox unmarked.\
    ![](<../../.gitbook/assets/image (5) (1) (1) (1) (1) (1) (1).png>)\
    \
    A **Side Touch Dispense** is a special dispense mode to prevent droplets on the tips end.\

12. The tip will move in the center of the container to the specific touch off height. From there, a Right move is performed. Then, the liquid will be dispensed and the tip or needle moves up and away.\
    \


    <figure><img src="../../.gitbook/assets/image (6) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>
13. To perform a side touch dispense with the ML STAR, the values for the touch off height and the right move must be specified. Mark the checkbox “wick side of container” to display the dialog for setting the values as shown below.\
    ![](<../../.gitbook/assets/image (7) (1) (1) (1) (1) (1).png>)\

14. Click \[Next >] to continue.
15. The “Container Segment Definition” Screen shown below appears.\


    <figure><img src="../../.gitbook/assets/image (111) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>


16. Select “Cylinder” as a shape for the upper segment (Segment 1).\
    \
    ![](<../../.gitbook/assets/image (9) (1) (1) (1) (1) (1).png>)
17. Supply values for the inner diameter (10 mm) and the segment height (20 mm).
18. Now, Click on the “Segment 2” Tab. The tab should appear as follows.
19. Select the \[Rounded base segment] Radio Button.
20. Supply values for the upper internal diameter (10 mm) and the segment height (12 mm).\
    ![](<../../.gitbook/assets/image (10) (1) (1) (1) (1).png>)
21. Click \[Next >]. The screen presented below will appear.
22. Unmark the “Use front distance for all” Box. Supply a value for the right move and one for the touch off height. Please make sure that the values are correct, otherwise it can result to a mechanical crash.\
    ![](<../../.gitbook/assets/image (11) (1) (1) (1) (1).png>)
23. Either calculate or measure these values before testing on a real instrument. An example on how to measure the values is being illustrated below.\


    <figure><img src="../../.gitbook/assets/image (12) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>
24. Click \[Finish] to complete the container definition.
25. Select the “![](<../../.gitbook/assets/image (13) (1) (1) (1) (1).png>)” Icon from the Toolbar to save the newly defined container or select “File  Save as” from the File Menu. Enter a name for the container (e.g. “MyContainer”.\[ctr]) and click \[Save].

\


