# Using Templates

*   “Templates” offer a framework for commonly used method parts. This shortens the programming time immensely since the programmer does not have to start from scratch. Templates and sub- method libraries within a method are treated similarly.

    A “Templates” or “Toolbox Templates” Tab is available. This is where the existing templates can be found.

    \


    ![image](../../.gitbook/assets/Image\_435.jpg)

    \


    ![Originalbild anzeigen](../../.gitbook/assets/Image\_436.gif)

    NOTE

    Templates are not part of the basic installation of VENUS Software. They have to be added after the installation of VENUS Software.

    \


    1.  #### ‌Including Templates‌

        \


        Templates have to be stored in the folder C:\Program files\HAMILTON\Library\Templates (the non-bold sections of the path may differ if a different language is in use).

        \


        ![Originalbild anzeigen](../../.gitbook/assets/Image\_437.gif)

        NOTE

        For the availability of templates, please consult a local Hamilton Representative.
    2.  #### ‌Using Templates‌

        \


        After the templates have been copied to the …/HAMILTON/Library/Templates folder, they will now be visible in the “Templates” or “Toolbox Templates” Tab found in the Toolbox on the left side of the window when opening/creating a method.

        To use a template, drag it from the toolbox onto the method.

        \


        ![image](../../.gitbook/assets/Image\_438.jpg)

        \


        [If a template is using parameters, the parameter window opens and can be filled (this is very similar to the use of sub-methods / sub-method libraries). Refer to ](Using\_Templates.md#bookmark199)[Section 9.1 Sub-Methods ](Using\_Templates.md#bookmark199)and[ ](Using\_Templates.md#bookmark199)Sub-Method Libraries.

        The example below shows the parameter window of the serial dilution template, where the instrument, sequences, volumes and the concentration have to be defined.

        \


        ![image](../../.gitbook/assets/Image\_439.gif)

        \


        After entering all necessary parameters and closing the window, the system will generate a “Sub- method” Tab in the method editor (see below) and include the sub-method steps to the new sub- method.

        \


        ![image](../../.gitbook/assets/Image\_440.gif)

        \


        If the template is fulfilling all requirements, no further changes are necessary. Finish the method programming.
    3.  #### ‌Changing Templates‌

        \


        There are two ways to change a template:

        * Change an added template (in a method locally)
        * Change the template’s source file

        \


        Change an added Template (in a method locally)

        If the templates steps need modification, just click on the Template’s Tab in the method. This switches to the e.g. SerialDilution96\_1 steps. Here, all necessary changes can be made to completely fulfill all the requirements. For example, an aspiration of a sample can be modified with a mix step.

        \


        ![Originalbild anzeigen](../../.gitbook/assets/Image\_441.gif)

        NOTE

        Changes made in the method under the Template’s Tab are only valid for the particular template.

        \


        It is also possible to add the same template several times into the same method. This could be the case when e.g. two serial dilutions with different steps are needed in the same method. The templates include an index as a suffix (see below) as an indicator so that each template can be adapted according to the customer’s needs.

        \


        ![image](../../.gitbook/assets/Image\_442.png)

        \


        Change a Template’s source file

        If a template should be changed to reduce the adaption work in every method, open the original Template file in the C:\Program Files\HAMILTON\Library\Templates folder. This folder is where the original Template files are stored. The Templates can be opened and modified from here. After applying the necessary changes, save the new version and open up a method to include the new version.

        \


        ![Originalbild anzeigen](../../.gitbook/assets/Image\_443.gif)

        NOTE

        To change a template globally, please open the file located in the C:\Program Files\HAMILTON\Library\Templates folder and change the original template. All following includes will then contain the changes made on the template.

        Changing an original template file will have no effect on the previously included templates. Only the newly added templates will contain the changes made in the original file.
*   ### ‌Programming Templates‌

    \


    There are different ways to create a template.

    1.  The easiest one is through the “File  New  Template Library” Menu.

        \


        ![image](../../.gitbook/assets/Image\_444.jpg)

        \

    2. Save the new template with a relevant name. Confirm with \[Save].

    \


    ![image](../../.gitbook/assets/Image\_445.jpg)

    \
