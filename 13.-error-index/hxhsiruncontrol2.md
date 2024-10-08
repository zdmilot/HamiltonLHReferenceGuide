# HxHsIRunControl2

## Error Body:

{% code overflow="wrap" %}
```
An error occurred while running Vector.
The error description is: 
No more positions available in sequence ML_STAR.Nun_96_FI_Lb_0001. (0x28 - 0x2 - 0x80d)
```
{% endcode %}

***

## Cause:

If all positions in a Sequence have been processed and you try to pipette to the same sequence then an error occurs and your Method is aborted.

## Solution:

To avoid this error or to start over from the beginning of a sequence: Use the Sequence: Set Current Position step

<figure><img src="../.gitbook/assets/image (12) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>
