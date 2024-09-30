# Dispense on the Fly sequence error

Depending the used mode different checks will be made to validate the sequence used.

&#x20;

**On 'Dispense on the fly mode' (0) Complete plate:**

| **Error**                     | **Description**                                                                                         | **Recovery**                                                                                                                       |
| ----------------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------- |
| Wrong count of channels       | Odd number of channels activated (greater than 1)                                                       | The count of used channel must be 1 or a multiple of 2. Note: On 5ml Channel maximum 4                                             |
| Too many channels activated   | Y distance of activated channels is greater than the distance between the wells on the same X position. | Count of activated channels must be smaller or equal than the well distance. ((ChnCount-1)\* channel y distance) <= well distance. |
| Not enough sequence positions | The given sequence remains not enough positions.                                                        | Make sure that the given sequence contains unused positions for each well of used plate.                                           |

&#x20;

&#x20;

**On 'Dispense on the fly mode' (1) Sequence order:**

| **Error**                   | **Description**                                                       | **Recovery**                                                         |
| --------------------------- | --------------------------------------------------------------------- | -------------------------------------------------------------------- |
| Shoots cannot be calculated | Count of used sequence positions cannot be divided without remainder. | Use a sequence which contains a position for each channel and shoot. |

&#x20;

&#x20;

&#x20;

**Both mode:**

| **Error**                   | **Description**                                      | **Recovery**                                                                              |
| --------------------------- | ---------------------------------------------------- | ----------------------------------------------------------------------------------------- |
| Different count of channels | Channel pattern used does not fit to given sequence. | Make sure that the used 'Channel pattern' matches to the sorting order of given sequence. |
| Sorted in a wrong Y offset  | The sequence is sorted with a wrong Y offset.        | Sort the sequence with the same offset than the Y delta between the used channel.         |
| Wrong 'serpentine' sort     | Sequence is not sorted in serpentine manner.         | Correct the sequence sort (use the stamp tool)                                            |
| To many positions           | The sequence contains more the 1536 positions.       | Split the sequence and define more than one Dispense on the Fly step.                     |

&#x20;
