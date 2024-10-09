# Arrays in Steps

Arrays can be used in steps, for example in fields like “Sequence”, “Volume” and “LC”. The existing arrays are listed together with the variables in the drop down list. Once an array has been selected, the \[Array Index Dialog] Button is displayed next to the data field containing the array (see green arrow).\
![](<../../../.gitbook/assets/image (547).png>)



Clicking the button opens the “Array Index Dialog” as shown below.

![](<../../../.gitbook/assets/image (548).png>)\


\


## Use Single Array Value:

Enter the index of the specific array element (a digit or a variable). This selection is disabled when only a series of elements is allowed.

![](<../../../.gitbook/assets/image (549).png>)\




## Use Multiple Array Values:

Enter an array start index, to select a series of array elements. For example in the field of an aspiration step, to set the individual volumes per pipetting channel, starting at a specific index (see picture below).

![](<../../../.gitbook/assets/image (550).png>)\


* Activate automatic array index selection. This function is available for arrays of well-defined functions, where the usage of the array index is specified precisely. For example, a smart step processing some well-defined positions uses an array with all the volumes of the individual positions. In this case, the step needs only the array without index, because the index is, for example, defined by the currently processed position.
