---
icon: dev
---

# Using a variable inside a Custom Dialog

[Lab Automation Forums](https://labautomation.io/)

## [Using a variable inside a Custom Dialog?](https://labautomation.io/t/using-a-variable-inside-a-custom-dialog/4384)

[Hamilton (Venus)](https://labautomation.io/c/hamilton-venus/7)[NFred](https://labautomation.io/u/NFred) August 21, 2024, 7:10am1

Hi. I am building a multi-plate normalization protocol, and my vision is to first ask the user how many plates we are working with, and after that looping over a Custom Dialog prompt to ask for each plate’s input file.

So how can I accomplish something like “Please choose the input file for \[intNumberOfPlates]”? On each iteration changing the displayed number to match with which number plate we are currently choosing. The help file for the Custom Dialogs in quite sparse.

Also having a bit of a hard time wrapping my mind around how to go from there: should I make a new Sequence into which the samples from each plate get added to? I’m thinking of having a maximum of 96 samples at first.

Thanks!

[mnewsom](https://labautomation.io/u/mnewsom) August 21, 2024, 2:02pm2

First part is pretty simple.

For a dialog that prompts the user for a number of plates you could set something up like this:\


[![image](https://labautomation.io/uploads/default/optimized/2X/e/e35af167724ec91b10ca3f5c8deba879433b79c9\_2\_690x459.png)](https://labautomation.io/uploads/default/original/2X/e/e35af167724ec91b10ca3f5c8deba879433b79c9.png)

The initial value is retrieved from int\_maxPlate and then the dialog box replaces that value with whatever is chosen. So this snippet would show 5 when the method is run, then if you traced it out after it would be whatever is set in the numerical value.

Then in the second dialog box you mentioned, you could set it up in a loop as such:

![image](https://labautomation.io/uploads/default/original/2X/9/9d77a9e51c569f6f7eb6e8df3f0c53649d48475d.png)\
The Str library allows you to concatenate a message together which is passed in to the text box within the dialog itself:\


[![image](https://labautomation.io/uploads/default/original/2X/7/790ac0ed0cee5e5ce0e69a6ced83a6c829bf6088.png)image1003×453 33.2 KB](https://labautomation.io/uploads/default/original/2X/7/790ac0ed0cee5e5ce0e69a6ced83a6c829bf6088.png)\
and gets updated with whatever the loop counter says each time it’s run:

![image](https://labautomation.io/uploads/default/original/2X/2/2f0a128256b31c04b5251b0a172fc65264e0788b.png)

For the second part, I would probably just make one sequence (e.g. seq\_dispense) and one volume array (arr\_fltDestVol). If you’re going from a reservoir with a buffer, the aspirate sequence is already handled. If you’re cherry picking from a source to a destination, the aspirate portion would probably come from a file, so you’d have to add that in.

Basically, once the user puts in their file, it will go through it and add the pieces to the dispense sequence and the volume array. Then they’re prompted for the next file and it processes through that until you hit the max plates they defined.

This method assumes you have positions on deck with IDs of “SamplePlate1” “SamplePlate2”… and so on until your max setup.

[![image](https://labautomation.io/uploads/default/optimized/2X/9/9cfa843cae801571e3073c2c1c981ccd7c773a81\_2\_479x500.png)image738×770 53.6 KB](https://labautomation.io/uploads/default/original/2X/9/9cfa843cae801571e3073c2c1c981ccd7c773a81.png)

Hope this is clear! The file stuff is just a skeleton example and there’s no pipetting steps included here.

5 Likes[NFred](https://labautomation.io/u/NFred) August 22, 2024, 5:47am3

Thanks so much [@mnewsom](https://labautomation.io/u/mnewsom) ! ![:raised\_hands:](https://labautomation.io/images/emoji/twitter/raised\_hands.png?v=12) I will dig into this today.

1 Like[NFred](https://labautomation.io/u/NFred) August 22, 2024, 10:45am4

I got the first part in order but the use of variable sequences feels a bit cryptic to me. How do I “connect” a variable sequence to an actual deck “labware” sequence?

Thanks again ![:slight\_smile:](https://labautomation.io/images/emoji/twitter/slight\_smile.png?v=12)

[mnewsom](https://labautomation.io/u/mnewsom) August 22, 2024, 1:21pm5

That’s part of the labware ID component.

In my layout for this, I would have something like the following:

[![image](https://labautomation.io/uploads/default/optimized/2X/5/5d33278fde264dec3948f5f5f8ac3b80db06b06f\_2\_688x500.png)image1095×795 48.3 KB](https://labautomation.io/uploads/default/original/2X/5/5d33278fde264dec3948f5f5f8ac3b80db06b06f.png)

where the SamplePlate# is the labware id for each of the plates that are possible to dispense to. The loop on that first bit, where it’s concatenating the loopCounter1 variable to the str\_destPlateName which gives you a string (str\_plateID) that you can use as the labware id.

Every time it goes through it adds the new loop counter to the end of that so you end up with a string that references\
SamplePlate1\
SamplePlate2\
and so on. These labware IDs must match what’s in your layout. As you build the sequence (SeqAdd function), it takes the result from the concatenation (str\_plateID) and the position it reads from the file (file1\_dest\_well) and adds it to the sequence which in this case is just called seq\_dispense.

The final seq\_dispense would look something like\
**Labware** - **Position**\
SamplePlate1 - A1\
SamplePlate1 - B1\
SamplePlate2 - A1\
SamplePlate2 - B1\
SamplePlate3 - A1

Using this would look something like:

[![image](https://labautomation.io/uploads/default/original/2X/a/aa9a351e64181725a22a759866ad3ecf283bb7b8.png)image736×424 29.5 KB](https://labautomation.io/uploads/default/original/2X/a/aa9a351e64181725a22a759866ad3ecf283bb7b8.png)

This assumes you’re aspirating from a buffer trough with the sequence defined in the layout (which is why we’re not incrementing that sequence - manual counting) and you’re incrementing the seq\_dispense in the dispense step (automatic counting). Then the volume is taken from the array you made when reading the file and that array index is incremented with every loop at the end.

Note: I didn’t simulate this so there may be errors&#x20;

1 Like[NFred](https://labautomation.io/u/NFred) August 23, 2024, 5:58am6

Thanks so much again&#x20;

