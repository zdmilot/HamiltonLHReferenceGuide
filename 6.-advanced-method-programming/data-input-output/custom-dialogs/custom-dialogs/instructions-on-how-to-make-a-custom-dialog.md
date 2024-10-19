---
icon: dev
---

# Instructions on How to Make a Custom Dialog

Drag the Custom Dialog over from the toolbox within venus\
![](<../../../../.gitbook/assets/image (3) (1) (1).png>)\


[![image](https://labautomation.io/uploads/default/optimized/2X/9/9f58b64f4c3b99fed50b1e67b364acc59d367bda\_2\_690x412.png)](https://labautomation.io/uploads/default/original/2X/9/9f58b64f4c3b99fed50b1e67b364acc59d367bda.png)



then it will ask you to choose a template



here is where you choose the template

<figure><img src="../../../../.gitbook/assets/image (2) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

This is what the first dialog looks like (run config/selection)

\


[![image](https://labautomation.io/uploads/default/optimized/2X/6/665115f61fc057f12732552e66731fd035b090b1\_2\_690x422.png)](https://labautomation.io/uploads/default/original/2X/6/665115f61fc057f12732552e66731fd035b090b1.png)\
Drop down menu with options, and the selected option is outputted as a variable/index and is used in the following assignment command for the string temp value.\
[![image](https://labautomation.io/uploads/default/original/2X/0/0776226fa00b0bc7c37ddf34b5284196f4fb3df1.png)](https://labautomation.io/uploads/default/original/2X/0/0776226fa00b0bc7c37ddf34b5284196f4fb3df1.png)

Deck loading dialog:\
s



s

[![image](https://labautomation.io/uploads/default/optimized/2X/9/9a84476e0a256ed08303790c1f57c6d84f999e7c\_2\_690x401.png)](https://labautomation.io/uploads/default/original/2X/9/9a84476e0a256ed08303790c1f57c6d84f999e7c.png)

string temp value is inputted into the image name. Must have images loaded/added to the image selection. Note that large image files can crash the Hamilton method editor.\


[![image](https://labautomation.io/uploads/default/original/2X/c/c2c525460a30ae87e9250dde8f218e552da9d746.png)](https://labautomation.io/uploads/default/original/2X/c/c2c525460a30ae87e9250dde8f218e552da9d746.png)

\
![image](https://labautomation.io/uploads/default/original/2X/5/5dae553a758bd82842771bcf543d5e5920ce90b6.png)



***





In this example we are making a simple loading instructions custom dialog… using cropped screenshots from the deck editor in a VENUS method.

1. Step 1: Resize your workspace to accommodate the desired elements.\
   ![](<../../../../.gitbook/assets/image (53).png>)\

2. Step 2: Add and resize an image element to be used for the deck layout. Rename its Control ID to Deck.\
   ![](<../../../../.gitbook/assets/image (54).png>)
3. Step 3: Add and Resize an image element to be used for the labware. Rename its Control ID to Deck\_Detail\_Image.\
   ![](<../../../../.gitbook/assets/image (55).png>)
4. Step 4: Add and Resize button elements.\
   ![](<../../../../.gitbook/assets/image (56).png>)
5. Step 5: Select your deck layout image (adding it to the Pictures list using the + button), then add additional image elements to use as “Mouse enter/Mouse leave” points at each labware position. Rename their Control IDs starting with the reservoir to Reagent, Plate, and Tips respectively.\
   ![](<../../../../.gitbook/assets/image (57).png>)
6.  Step 6: Select the Reagent element, then create Events under the “Mouse Enter” and “Mouse Leave” Triggers.

    **Mouse Enter** has two events: one to make the image visible, one to change which image is displayed using the Deck\_Detail\_Image element. \
    **Mouse Leave** has one event: to make the Deck\_Detail\_Image element invisible.\
    ![](<../../../../.gitbook/assets/image (58).png>)
7. Step 7: Update pictures for image elements as desired. Continue by adding Events for the Plate and Tips elements. Remember to update the picture displayed for each one, and ensure appropriate designations of the “visible” event actions.\
   ![](<../../../../.gitbook/assets/image (59).png>)
8. Step 8: Set your Return/Close values for the two buttons, and bind the variable to the Dialog\_Value (so it stores the Return/Close value when the dialog is closed).\
   ![](<../../../../.gitbook/assets/image (60).png>)
9. Step 9: Set the Deck\_Detail\_Image element to be invisible by default (under Properties and Appearance). Perform any other aesthetic modifications you want.\
   ![](<../../../../.gitbook/assets/image (61).png>)
