# Customized Dialog

## What is the Custom Dialog Step?

The custom dialog step allows creating user dialogs that contain multiple and different input controls such as Drop-Down Lists, Checkboxes, Radio Buttons, Text Input Controls, File Browse Controls, Numeric Input Controls, Pictures, Buttons and Text Blocks. All these controls can be arranged in any desired way.

<figure><img src="../../.gitbook/assets/image (541).png" alt="" width="304"><figcaption></figcaption></figure>

The custom dialog step is located in a separate "Custom Dialog Steps" Tab.

<figure><img src="../../.gitbook/assets/image (542).png" alt=""><figcaption></figcaption></figure>



After a “Drag and Drop” to the method, the selection for templates is shown.

Choose either blank or User Output: 1 Button, User Output: 2 Buttons or User Output: 3 Buttons to start with a predefined dialog that contains already some buttons.

After this selection, the editor starts (In this example: User Output: 2 Buttons)

<figure><img src="../../.gitbook/assets/image (543).png" alt="" width="375"><figcaption></figcaption></figure>

\


### Step 1: Add controls to the custom dialog

Customize the dialog box by adding basic controls and input controls from the toolboxes located on the left of the window. The elements can be added through a simple “Drag and Drop”. It is then possible to arrange the elements added into the dialog. The dialog itself can be adjusted in size.

\


### Step 2: Adjust the Properties of the Added Elements

To make changes on an element, simply select the element and choose ‘Properties’. Depending on the type of the element, the appearance, the behavior, and the font can be adjusted. All elements contain ‘General’ properties that are used to specify the variable binding and containing the handler of the element which is the ControlID. This ID is used to link events to the elements and makes the dialog ‘intelligent’.

\


### Step 3: Add Intelligence to the Custom Dialog

Using the ‘Events’ on the custom dialog can make the dialog intelligent. That means that specified elements of the dialog are only shown if e.g. a checkbox of another element is set. To understand further, see the example to below.

#### Example:

![](<../../.gitbook/assets/image (544).png>)\
\


The details of the ‚Preparation method’ are only visible if the according checkbox is activated. If deactivated, the user cannot make errorous inputs and is not confused by an overloaded dialog.

<figure><img src="../../.gitbook/assets/image (545).png" alt=""><figcaption></figcaption></figure>

\


## Getting Help for the Custom Dialog

Available in the help of the dialog are the explanations about the following:

* how to link variables
* handle events on elements and
* change the behavior at runtime

Simply click on the \[Help] Button on the bottom right corner. This will open the “Custom Dialog Overview”, where a simple click on the desired area will activate the related help section.

<figure><img src="../../.gitbook/assets/image (546).png" alt=""><figcaption></figcaption></figure>
