---
description: How to save, version, and manage your Venus methods.
cover: ../.gitbook/assets/92472.jpg
coverY: -109
---

# Saving and Organizing Methods

The following sections describe the best practices for saving and exporting methods. In general, version control and maintaining backups are the most critical practices.

1. ‌Saving‌
   1.  ‌Folder Structure

       #### Save methods, custom libraries, and labware within their respective Hamilton directory folders. All project-specific files should be grouped in subfolders for each project. Keep files needed for simulation runs and archived drafts of methods in clearly labelled folders within these subfolders.
   2.  ‌Versioning and File Naming

       #### All method and sub-method library names should include a suffix identifying the version using a nomenclature that describes top, middle, and low-level changes.

       | Nomenclature = X.Y.Z (example: 0.2.5) |                                                                                                                                                                                                                                                                                                                                                       |
       | ------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
       | X                                     | <p>Top-level Version Control</p><p>Will require major changes to the method or sub- method library when upgrading from one X rev to another. Little to no similarities to the previous top-level number. Examples: overhaul of the</p><p>entire method structure, addition of new hardware or integrated devices, addition of new workflow steps.</p> |
       | Y                                     | <p>Mid-level Version Control</p><p>May require some changes or parameters corrections but will allow upgrade with easy implementation. Mostly like the previous version with some changes that would require updating the method. Examples: adjustments to the method structure, corrections to entire segments of the method/workflow.</p>           |
       | Z                                     | <p>Low-level Version Control</p><p>Should require no changes or parameter corrections and will be almost identical to the previous version. Examples: typos, variable assignment corrections, volume calculation corrections.</p>                                                                                                                     |

       #### Track all version changes within a sub-method titled “\_VersionHistory” within the method or sub-method library.

       #### Use generic names when possible to make sharing methods easier. The names should describe the project or application the method is for. Avoid using company names for folder, method and labware files. All method names should include a suffix with the version number as detailed above; when a new version is saved, move any old versions to an archive folder.

       #### Follow the naming convention used for default labware when naming new labware definitions. Include a prefix of the manufacturer and a brief description of the labware. For example, a Falcon branded 96-well flat bottom plate would be named “Fal\_96FlatBottom”. More detailed info like the part number should go in the description field in the labware definition.

       #### For larger projects, consider the use of a git repository for sharing and version control of methods and their associated files.
   3.  ‌Installation Folder

       Maintain all materials necessary to recreate the system setup in the default Hamilton installation directory in a subfolder named Hamilton Software and Manuals. Store all installers for the main software, libraries, and drivers in this subfolder. Transfer electronic copies of the manuals and periodically export method files here during development. Adding a shortcut to this folder on the desktop of the computer is helpful for recreating the system setup on another computer.
2.  ‌Exporting‌

    1. Export the method as a \*.pkg file and include the original Hamilton files upon export. Include any dependencies and file paths needed by the method in order for it to run properly when imported.

    <figure><img src="../.gitbook/assets/image (218).png" alt=""><figcaption></figcaption></figure>

    Export methods to local drives before sharing them to shared drives, since exporting directly to shared drives can corrupt files. Certain files such as liquid classes may not be properly exported, so save backups of these files in their respective editors.
