# Shell

<figure><img src="../../.gitbook/assets/image (3) (1) (1).png" alt=""><figcaption></figcaption></figure>

The shell command option in **Venus** allows an app specialist to run an additional command such as a batch file, cmd file, or an external exe from within a method. If there is something you can think of that you can do with the Windows command prompt that **Venus** doesn’t natively allow, **Shell Command** is your path.

| <p>You have the option to run the command in sequence or serial, so you’ll need to decide if the method should wait until the external command is finished before it continues.</p><p>This command executes a definable application.</p> | <img src="https://sp-ao.shortpixel.ai/client/to_auto,q_lossless,ret_img,w_278,h_255/https://raverobot.com/wp-content/uploads/2018/11/ShellCommand-1.jpg" alt="A shell command pointing to an external .bat file which 
will run in serial in the current method" data-size="original"> |
| ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |





***

## **Program:**

Defines the file name of an executable program.

For the location of the file to be used, click on the browse button on the right of the **Program** field. This will display an Open dialog box.

### _**Format:**_

* String constant
* Entry from the given list
* New variable name
* New array element reference

### _**Note:**_

* When the path is manually entered via keyboard, double backslashes ('\\') instead of single backslashes ('') must be used!

### _**Examples:**_

* `"C:\\Bin\\MyProgram.exe"`
* `"C:\\MyBatches\\DoSomething.bat"`

***

## **Examples of Shell Commands Utility in Venus:**

* Copying a file from a template.
* Mapping a network drive.
* Deleting a temporary file.
* Making a call to a notification service.
* Data Logging.

***

## **Window style:**

Defines the window style to be used.

### _**Window styles:**_

| **Hide**      | Hides the window and activates another window.                         |
| ------------- | ---------------------------------------------------------------------- |
| **Normal**    | Activates the window and displays it in its current size and position. |
| **Minimized** | Activates the window and displays it as a minimized window.            |
| **Maximized** | Activates the window and displays it as a maximized window.            |

***

### **Concurrency:**

Defines the execution mode.

#### _**Execution mode:**_

| **Serial**   | Starts execution of the specified program and waits until this program is terminated (execution of running method is blocked until shell program is finished).                                                        |
| ------------ | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Parallel** | After starting the specified program, method execution is continued immediately in parallel to the shell program. The **event** specified in this mode can be used later to wait until the shell program is finished. |

***

### **Event handle:** (optional)

Defines an Event Identifier if the shell program is started in parallel to method execution (see **concurrency** above).

This identifier can be used later within an Event: Wait for command to wait until the corresponding shell program is finished.

***

### **Bind exit code to:** (optional)

Defines a variable to retrieve the termination status (exit code) of the executable program.

If the execution mode is set to 'Parallel' the exit code is available after the program has terminated.
