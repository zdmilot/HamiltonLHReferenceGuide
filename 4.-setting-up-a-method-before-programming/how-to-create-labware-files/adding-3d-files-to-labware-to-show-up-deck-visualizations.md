---
icon: dev
---

# Adding 3D files to labware to show up deck visualizations

Blender ( [blender.org - Home of the Blender project - Free and Open 3D Creation Software 10](https://www.blender.org/)) would work. It offers the option to save in .x format. If you haven’t worked with blender before, it can be quite challenging. In that case you could use your favorite CAD program, import the file to Blender and just save it as .x file (if your favorite CAD program doesn’t support this option).\
\
specifically Blender 2.8 and earlier which has the ability to export to .x files; I believe in later versions it was removed. It’s still possible to download earlier versions; I kept my 2.8 version in a virtual machine to avoid any issues with the latest version.\
\
Generally speaking, for the 3D models, you’d need to create a model using a third-party software such as Blender, export to .x format and set it in the labware definition. Check out [this thread 14](https://forums.pylabrobot.org/t/creating-custom-3d-models/1481)for more info.

For the image, you can set this to a .png or .jpg. There are a lot of images found throughout the Hamilton\Labware directory or you can create your own. Keep the file size in mind - I don’t know what the limit is off-hand, but I would recommend keeping it around the size of the other images found in the directory (\~100 to 200 KB).

When you use the Labware Assistant tool, it creates the .x model for the carrier for you, but it does not create an image.

[![image](https://labautomation.io/uploads/default/original/1X/574debfd00377a4850d2269ac34fc6f642431819.png)](https://labautomation.io/uploads/default/original/1X/574debfd00377a4850d2269ac34fc6f642431819.png)
