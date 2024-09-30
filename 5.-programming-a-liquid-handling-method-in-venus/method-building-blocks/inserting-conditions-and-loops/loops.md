# Loops

## Using Loops

<table data-header-hidden><thead><tr><th width="234"></th><th width="640"></th></tr></thead><tbody><tr><td><br><img src="blob:https://app.gitbook.com/bee01f9f-17dd-4567-bd04-3b5bb1d7447a" alt=""></td><td><ol><li>Add the General Step Loop to your Method and the Loop dialogue window appears</li></ol></td></tr><tr><td><br><img src="blob:https://app.gitbook.com/eeac64f4-7422-474f-9018-b9ad8ea6d7f3" alt=""></td><td><ol start="2"><li>Select the way to Loop, provide any info needed, and click OK</li></ol></td></tr><tr><td><br><img src="blob:https://app.gitbook.com/45c4c288-912b-473e-a97e-32b17171d9b9" alt=""></td><td><ol start="3"><li>An empty Loop-End Loop step combo is added to the Method</li></ol></td></tr><tr><td><br><img src="blob:https://app.gitbook.com/dfa1014d-9a3e-4b41-92e1-d73276f3d7bb" alt=""><br></td><td><ol start="4"><li>Steps added between the Loop and End Loop will be repeated when the Method runs</li></ol></td></tr></tbody></table>





## Four ways to control the looping:

{% tabs %}
{% tab title="Fixed #" %}
Repeat a fixed number of times

***

Loop counter variable created by the Loop step automatically keeps count of the number of iterations.

<figure><img src="../../../.gitbook/assets/image (88).png" alt="" width="177"><figcaption></figcaption></figure>

Loop counter variable = 0 before Loop execution starts,

***

**Example:** Repeat the step 12 times

<figure><img src="blob:https://app.gitbook.com/2b9789cb-3171-4343-b945-6be58dc5ee93" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Logic" %}
Repeat while some logic expression is true

***

To force a Loop to end prematurely, use the Loop Break step. Processing continues with the next step after the End Loop.

<figure><img src="../../../.gitbook/assets/image (89).png" alt=""><figcaption></figcaption></figure>

***

**Example:** Repeat forever or until the step Loop-Break is encountered\


<figure><img src="blob:https://app.gitbook.com/11f3922c-6e6d-419c-a670-133c3e0885d9" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Sequence" %}
Repeat until the controlling & selected sequence has reached its end

***

“Iterate over sequence” =  Repeat the steps inside the loop until the “Controlling” sequence runs out of positions (i.e. reaches it’s End Position)

<figure><img src="blob:https://app.gitbook.com/82592997-0c8a-45d3-8cda-b5f6a70dbdad" alt=""><figcaption></figcaption></figure>

**never** = no change in the current position \
**before loop** = current position set to 1 _before_ Loop step starts\
**after loop** = current position set to 1 _after_ Loop step is finished\
**before & after loop** = current position set to 1 _before & after_ Loop step

<figure><img src="blob:https://app.gitbook.com/fe9368da-a653-44a7-802e-514b93d4c9c6" alt=""><figcaption></figcaption></figure>

***

**Example:** Repeat the pipetting steps until all sequence positions in TargetPlatesX4 are processed\
![](blob:https://app.gitbook.com/8bed9c2a-a37b-4ddc-a4ba-0fe1983f30b0)\

{% endtab %}

{% tab title="File" %}
Repeat until the selected file has reached its end: no more records

&#x20;Read each record from the work list until the end-of-file is reached\
![](blob:https://app.gitbook.com/42267f91-8cac-4cc4-94d3-6f8c1eb17003)
{% endtab %}
{% endtabs %}



## Nested Loops

Loops can contain other Loops.

Nested loops in laboratory liquid handling are used to automate the process of pipetting multiple samples. For example, the outer loop can iterate through a list of reagents, while the inner loop can iterate through a series of test tubes. This ensures that each reagent is added to each

<figure><img src="../../../.gitbook/assets/image (92).png" alt="" width="245"><figcaption></figcaption></figure>

Example: an 8 channel STAR with 300uL tips can Dispense 100uL into 3 wells for each 300uL Aspiration. So it will need to repeat the Aspirate and Dispense steps 4 times to completely fill a 96 well plate (Note: for Part Volume Dispenses, the volume for the first and last dispense will be off)

&#x20;

&#x20;

&#x20;
