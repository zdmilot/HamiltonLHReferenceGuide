---
description: >-
  Some users wish to launch a particular method from a desktop icon or from a VB
  method.
---

# Starting HxRun from the command line

Below are the formats you can use to do this.  For example, use these examples as a guide to changing the Properties of your HxRun icon.



To launch the Run Control and open Method1:

&#x20;    "C:\Program Files\Hamilton\Bin\HxRun.exe” Method1.med

To launch the Run Control, open Method1, and start the method:

&#x20;    "C:\Program Files\Hamilton\Bin\HxRun.exe” Method1.med /r

&#x20;

To launch the Run Control, open Method1, start the method, and then terminate (close) the Run Control when the method is complete:

&#x20;    "C:\Program Files\Hamilton\Bin\HxRun.exe” Method1.med /t

&#x20;

If your method is not in the Methods directory but in some other location, include the path with the method name, like this:

"C:\Program Files\HAMILTON\Bin\HxRun.exe" "C:\Program                 Files\HAMILTON\Methods\Demo\Method1.med" /t
