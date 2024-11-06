# Error Expected Labware not Present - QCG Error

I would recommend making sure the tabs on your QCG aren’t bent (see attached). The grip height/width are parameters in the transport steps so make sure that you are gripping the plate in position that cause the flap to move and also that you are not gripping too tightly.

&#x20;

There is a firmware command to turn off the cLLD detection for the QCG. You only have to run it once and it will keep the detection off. Include the quotes and it is case sensitive.

Command: “####”

Parameter: “A1AMBLbl0”

&#x20;

The default value for the sensitivity is 100 “A1AMBLbl100” You can try increasing the sensitivity (maximum is 1000) however this issue is usually due to the tabs being bent or debris in the QCG holes. You can clean out the QCG with a compressed air cannister.
