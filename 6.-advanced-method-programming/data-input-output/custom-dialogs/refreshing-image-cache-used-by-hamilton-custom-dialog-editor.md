---
icon: dev
---

# Refreshing image 'cache' used by Hamilton custom dialog editor

[Lab Automation Forums](https://labautomation.io/)

## [Refreshing image 'cache' used by Hamilton custom dialog editor](https://labautomation.io/t/refreshing-image-cache-used-by-hamilton-custom-dialog-editor/2894)

[Hamilton (Venus)](https://labautomation.io/c/hamilton-venus/7)[osand317](https://labautomation.io/u/osand317) February 2, 2024, 10:15pm1

> I often find myself going to update a custom image used in a custom dialog. Replacing the image in Windows explorer with a new image of the same name results in Venus displaying the old image, even though that file no longer exists.
>
> I’m assuming Venus has cached the old image somewhere, is there a way to clear that cache and force it to use the new image? I’d prefer not to have to change the name of the image each time a new version is created.



[bowlineknot](https://labautomation.io/u/bowlineknot) February 2, 2024, 10:42pm2

> In the custom dialog window, select your image. In the right hand panel, select the drop down menu. You have to select + to add your new image, and - to remove the old image. A copy of your photo is added to the custom dialog, so updating your image in windows explorer does nothing to the image in custom dialog.
>
> [![image](https://labautomation.io/uploads/default/optimized/2X/1/154f26ea5ede28e8f4f1bab09b21d3518ebdb283\_2\_690x389.png)](https://labautomation.io/uploads/default/original/2X/1/154f26ea5ede28e8f4f1bab09b21d3518ebdb283.png)
>
>



4 Likes[osand317](https://labautomation.io/u/osand317) February 2, 2024, 11:11pm3

> Just what I was looking for, thanks! Figured it was something simple I was missing. The only additional step I had to do to was save and close the dialog after removing the old images and before adding the new ones.

3 Likes
