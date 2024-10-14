# Using the Shell to Execute a Method

## Passing Parameters to HxRun.exe in Hamilton VENUS

If you're looking to set up automated testing of a method using **HxRun.exe** in Hamilton VENUS, one common challenge is finding a way to pass parameters or arguments to the method so that you can bypass user dialog prompts, such as selecting a worklist. Below is a summary of the discussion and solutions shared by community members on how to tackle this problem.

#### Challenge: Passing Parameters to a Method

In Hamilton VENUS, the **HxRun.exe** executable is commonly used to start a method from the command line. However, there is no direct support for passing custom arguments or parameters to a method without using external tools. This makes it difficult to automate tasks like selecting a worklist without displaying a dialog box to the user.

#### Solutions and Workarounds

**1. Using a Parameter File**

One solution, as suggested by **EricSindelar\_Hamilton**, is to create a **parameter file** in a designated location. This file could contain the necessary information, such as the file path of the worklist, which the method would read at the beginning of its execution.

* **Step-by-Step Approach**:
  1. Create a text file (e.g., `worklist.txt`) in a specified directory.
  2. Inside the method, use the **HSLFileDirectory** library or standard file commands to read the contents of this file and store the path of the worklist.
  3. The method can then proceed without requiring a user to manually select the worklist.
  4. Optionally, delete or move the parameter file after reading it to prevent reuse.

This approach allows automation without requiring interaction from the user, making it ideal for automated testing scenarios.

**2. Handling Multiple Worklists**

If you need to handle multiple worklists, you can either:

* Name the parameter file consistently (overwriting it as needed).
* Use the **GetFileNames** or **GetNewestFileName** functions from the **HSLFileDirectory** library to dynamically pick the appropriate worklist from a folder.

This would allow you to iterate over worklists during automated testing, but you would need an external process to manage which worklist has been used during each run.

**3. Utilizing Scheduler Software**

While VENUS has a built-in **Scheduler** tool, it is primarily designed for scheduling methods from a workflow rather than passing parameters from the command line. However, **VENUS Scheduler** can pass parameters within the workflow itself, which may be useful in more complex workflows.

* **VENUS Scheduler** and **TADM** (Test and Diagnostics Module) are included in VENUS 5, allowing additional functionality without separate software installation.

**4. Custom Logic for Test Mode**

Another approach, especially for regulated environments where files are stored in protected locations, is to build a "test mode" into the method itself. You could:

* Create a **test folder** that is used exclusively during automated tests.
* Modify the method logic to check if it's running in "test mode" and pull worklists from this designated folder.

This setup allows you to keep operational worklists separate while running tests on unique files.

#### Limitations and Considerations

1. **No Direct CLI Support**: As discussed by **DanHartman\_Hamilton**, Hamilton VENUS does not natively support passing custom arguments from the command line (via **HxRun.exe**) to a method. Instead, external methods such as parameter files or databases must be used.
2. **Using Submethods**: Parameters can be passed to submethods, as indicated in the **Vector Unit Test Framework**, but not directly to methods. This could be useful in some testing scenarios if you’re testing specific submethod logic.
3. **External Scripting (PyHamilton)**: While some community members suggested using **PyHamilton**, which allows passing parameters more flexibly in Python, Gareth confirmed that this wasn't an option for his specific projects. However, if you have flexibility with tools, PyHamilton offers a straightforward way to automate testing with parameters.





***

[Lab Automation Forums](https://labautomation.io/)

## [Passing parameters to HxRun.exe](https://labautomation.io/t/passing-parameters-to-hxrun-exe/349)

[Hamilton (Venus)](https://labautomation.io/c/hamilton-venus/7)[Gareth](https://labautomation.io/u/Gareth) September 13, 2022, 10:42am

> I’d like to use HxRun to setup some automated testing of a method. Normally, we show a custom dialog for a user to select a file, which is then processed etc.
>
> I understand that we can start run control from the command line via HxRun.exe, but is there a way to pass parameters/arguments to the method, so I can select the file automatically and not show the dialog? I don’t need help with handling the logic once I get the parameter, I just need help with the passing of parameters into the method.
>
> Thanks in advance.



[EricSindelar\_Hamilton](https://labautomation.io/u/EricSindelar\_Hamilton) September 13, 2022, 2:06pm4

> You can have a dedicated location for the parameter file and then the method just reads the file at the beginning to get the info. The method could delete or move the file after it is read in. It would require another process to download or overwrite the parameter file in the designated folder.
>
> Otherwise, scheduler software can pass parameters to a method from a workflow, but you’d still need to select the parameter file from the workflow.



[smohler](https://labautomation.io/u/smohler) September 13, 2022, 3:14pm

> @gwp tried using the `FileDirectoryLibrary` to loop over a large set of example worklist but the library function `GetFilesInDirectory` didn’t work. I kept getting an invalid class string error even though I followed the docs on the input types.



[EricSindelar\_Hamilton](https://labautomation.io/u/EricSindelar\_Hamilton) September 13, 2022, 3:19pm

> You’ll need to run the installer which I uploaded [here](https://download.hamiltonsupport.com/wl/?id=V1UIcLqX4nCtxbzxlY7n1qP1nLmzvhy0). But that is what I was alluding to - so long as you put the file in a designated location you can either give it the same name (overwriting as needed) or use commands such as the GetFilesInDirectory from the HSLFileDirectory library to get the file name, then you don’t need a user prompt in your method.



[Gareth](https://labautomation.io/u/Gareth) September 13, 2022, 3:24pm11

> Unfortunately we can’t use logic like that, namely because we need unique worklists that are generated externally and are saved with unique names to a specific network location (and for regulated areas this folder has special perms), and we can’t iterate through all files in a directory because we need to keep all worklists in the same folder, even those already run. The way we have it is as we need it. Just I’d like to be able to send arguments into the method that can override that. I guess I could have “test mode” that looks at a special folder for testing, but as 1 run = 1 worklist, I’d need an external way to keep track of what worklists have been run for this test session. Calling it in a bash script for e.g. with an argument for which worklist to use would be much simpler and cleaner. I guess it’s just not an option without the scheduler software.



[EricSindelar\_Hamilton](https://labautomation.io/u/EricSindelar\_Hamilton) September 13, 2022, 3:26pm12

> Sorry, I should also point out that the Directory.hsl library in the HSL Extensions also has commands to GetFileNames, GetNewestFileName, etc. which you could also use instead of overwriting or moving files.



[smohler](https://labautomation.io/u/smohler) September 13, 2022, 3:48pm

> [![Screen Shot 2022-09-13 at 11.46.27 AM](https://labautomation.io/uploads/default/optimized/1X/fda8946e63ce7aab4f706c8e6573fe78a71a93a3\_2\_690x276.png)](https://labautomation.io/uploads/default/original/1X/fda8946e63ce7aab4f706c8e6573fe78a71a93a3.png)\
> [@EricSindelar\_Hamilton](https://labautomation.io/u/ericsindelar\_hamilton) found an error in the docs that holding me up me up. It needs to be **“\*.txt”**\* instead of **“.txt”** for the filter command.[DanHartman\_Hamilton](https://labautomation.io/u/DanHartman\_Hamilton) September 13, 2022, 3:55pm14
>
> While it isn’t possible to directly pass a parameter to a method by way of the Executor class, the parameter file Eric mentioned at the start achieves the same thing. The file could be as simple as a text file sitting in a designated location (i.e. “HAMILTON\Parameter Files”) that only has one line of information, that being the file path of the worklist for the run. When the method starts, it opens this file and reads in the one line to be stored in your worklist variable, then everything proceeds as normal.
>
> The added functionality you need is something to change the name of the worklist in the parameter file. This could be as simple as a user opening and changing the worklist file path manually, or using a different software tool to change it automatically. Your automated setup would need a way to change the file path either way, however in this case it needs to handle writing to a file instead of passing the information as a method parameter.
>
> We use this technique when working with third-party integration software to send/receive information between the integration software and VENUS during runtime.



[WilliamCham\_Hamilton](https://labautomation.io/u/WilliamCham\_Hamilton) September 13, 2022, 4:28pm

> Hi all,
>
> Just to add to Dan’s response, yes, it would likely require some kind of a “Developer Mode” switch within your Method or at the very least a “GetSimulationMode” condition, to determine whether to use the user input or the “parameter file.” As for editing the value of the file, at least in a Windows environment it’s pretty straightforward writing a line to a text file, and the Method can delete the file if needed after reading it.
>
> Just to clarify on Scheduler, a Scheduled Method can accept parameters, but only from a Workflow, which is an alternate “Method” file type that uses specific steps to call out and execute Methods in the scheduled environment. Having Scheduler would not allow you to call a Method directly from a command line or script with specific parameters and would still result in the same situation as previously encountered: At some point, that input needs to be retrieved somehow (user dialog, flat file, database, etc.).
>
> As a side note, I would also recommend using HSLExtensions over any specific File/Directory libraries we had previously as long as the function needed exists in it, as HSLExtensions doesn’t require a DLL to be registered to function, while most of the others do.
>
> \~William



[Stefan](https://labautomation.io/u/Stefan) September 13, 2022, 5:01pm

> Im happy to show how to do this (or any other unique method request) in PyHamilton, passing parameters to a method can be accomplished fairly easily in a lot of forms. [@Gareth](https://labautomation.io/u/gareth) if you want to send a message with some brief details of your method I can post an example that very simply elucidates how to implement this.



[Martin](https://labautomation.io/u/Martin) September 13, 2022, 5:38pm

> For me it sounds like [@Gareth](https://labautomation.io/u/gareth) just needs the parameters for the command line to start a method with HxRun.exe immediately (without loading the file within HxRun and hit the start button).\
> This can already be done in Venus 4.5, e.g. with a desktop shortcut or command line using
>
> “C:\Program Files (x86)\Hamilton\Bin\Hxrun.exe” " -
>
> parameters can be\
> \-t meaning that HxRun terminates after the run\
> there are more, but I dont have them in mind. Will look it up tomorrow. One is to run HxRun minimized, maybe you need a parameter to immediately start. Will let you know tomorrow.
>
> Since you talked about testing: There is a Unit Test tool to test Hamilton submethods. It is called Vector Unittest Framework. Maybe it is just what you are currently setting up.



[bowlineknot](https://labautomation.io/u/bowlineknot) September 13, 2022, 6:41pm

> Oh, that’s super interesting that there’s a unit test tool. Do you have more information on the Vector Unit test Framework?



[smohler](https://labautomation.io/u/smohler) September 13, 2022, 6:43pm

> Good lord this would be the dream right. But you cannot pass a parameter to a method from the cli. Man if you could though and if they updated the cli to allow parameter passing you could set up a git commit process so when people commit changes you could auto run and catch any stdout errors.
>
> I guess this would mean though you’d need to beable to install VENUS in some sort of docker container thought and run in a headless mode.&#x20;
>
> Just spit balling now



[Gareth](https://labautomation.io/u/Gareth) September 14, 2022, 9:12am

> I know about the /t /r arguments, this is more about passing custom arguments to the method rather than those few to the run control.
>
> I too am interested in the unit test tool. Would you be able to upload it/have more info?



[Gareth](https://labautomation.io/u/Gareth) September 14, 2022, 9:13am

> I was expecting you to suggest pyhamilton. However for lots of reasons we can’t use it (at least for the current projects). Stuff like this is easy in python in general, but we need to stick to venus.



[Martin](https://labautomation.io/u/Martin) September 14, 2022, 2:43pm

> Well, as far as I know, custom arguments cannot be used as input for methods, only for submethods. Thats what the Vector Unittest Framework covers.
>
> Unfortunately, I do not have the installer which is needed. Maybe [@EricSindelar\_Hamilton](https://labautomation.io/u/ericsindelar\_hamilton) or [@WilliamCham\_Hamilton](https://labautomation.io/u/williamcham\_hamilton) can help out?



[EricSindelar\_Hamilton](https://labautomation.io/u/EricSindelar\_Hamilton) September 14, 2022, 3:14pm

> I do not have a library or method called Vector Unit Test Framework. I will reach out to my colleagues to try and find out more.



[Pete](https://labautomation.io/u/Pete) September 14, 2022, 9:04pm

> What is the relationship between Venus and Venus Scheduler? Is the Scheduler a separate application, a component of venus, etc.?



[EricSindelar\_Hamilton](https://labautomation.io/u/EricSindelar\_Hamilton) September 14, 2022, 9:19pm

> VENUS Scheduler, like TADM, is a component of VENUS. My understanding is that the installers actually just unlock those functions within VENUS. So, they aren’t separate applications. With VENUS five, these installers are included along with the base software.



