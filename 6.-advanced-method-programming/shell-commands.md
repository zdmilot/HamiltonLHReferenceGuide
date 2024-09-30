# Shell Commands

<figure><img src="https://sp-ao.shortpixel.ai/client/to_auto,q_lossless,ret_img,w_278,h_255/https://raverobot.com/wp-content/uploads/2018/11/ShellCommand-1.jpg" alt="" height="255" width="278"><figcaption><p>A shell command pointing to an external .bat file which will run in serial in the current method</p></figcaption></figure>

The shell command option in Venus allows for an app specialist to run an additional command such as a batch file, cmd file, or an external exe from within a method.&#x20;

If there is something you can think of that you can do with the Windows command prompt that Venus doesn’t natively allow, Shell Command is your path.

You have the options for running the command in sequence or serial so you’ll need to decide if the method should wait until the external command is finished before it continues.

This command executes a definable application.&#x20;

<table data-header-hidden><thead><tr><th width="124"></th><th></th></tr></thead><tbody><tr><td>Program:</td><td><p>Defines the file name of an executable program.</p><p>For the location of the file to be used, click on the browse button on the right of the Program field. This will display an Open dialog box.</p><p><strong>Format:</strong></p><ul><li>String constant</li><li>Entry from the given list</li><li>New variable name</li><li>New array element reference</li></ul><p><strong>Note:</strong></p><ul><li>When the path is manually entered via keyboard, double back slashes ('\\') instead of single back slashes ('\') must be used!</li></ul><p><strong>Examples:</strong></p><ul><li>"C:\\Bin\\MyProgram.exe"</li><li>"C:\\MyBatches\\DoSomething.bat"</li></ul></td></tr><tr><td>Window style:</td><td><p>Defines the window style to be used.</p><p><strong>Window styles:</strong></p><table data-header-hidden><thead><tr><th></th><th></th></tr></thead><tbody><tr><td>Hide</td><td>Hides the window and activates another window.</td></tr><tr><td>Normal</td><td>Activates the window and displays it in its current size and position.</td></tr><tr><td>Minimized</td><td>Activates the window and displays it as a minimized window.</td></tr><tr><td>Maximized</td><td>Activates the window and displays it as a maximized window.</td></tr></tbody></table></td></tr><tr><td>Hide</td><td>Hides the window and activates another window.</td></tr><tr><td>Normal</td><td>Activates the window and displays it in its current size and position.</td></tr><tr><td>Minimized</td><td>Activates the window and displays it as a minimized window.</td></tr><tr><td>Maximized</td><td>Activates the window and displays it as a maximized window.</td></tr><tr><td>Concurrency:</td><td><p>Defines the execution mode.</p><p><strong>Execution mode:</strong></p><table data-header-hidden><thead><tr><th></th><th></th></tr></thead><tbody><tr><td>Serial</td><td>Starts execution of the specified program and waits until this program is terminated (execution of running method is blocked until shell program is finished).</td></tr><tr><td>Parallel</td><td>After starting the specified program, method execution is continued immediately in parallel to the shell program. The event specified in this mode (see below) can be used later to wait until shell program is finished.</td></tr></tbody></table></td></tr><tr><td>Serial</td><td>Starts execution of the specified program and waits until this program is terminated (execution of running method is blocked until shell program is finished).</td></tr><tr><td>Parallel</td><td>After starting the specified program, method execution is continued immediately in parallel to the shell program. The event specified in this mode (see below) can be used later to wait until shell program is finished.</td></tr><tr><td><p>Event handle:</p><p>(optional)</p></td><td><p>Defines an Event Identifier if the shell program is started in parallel to method execution (see concurrency above).</p><p>This identifier can be used later within an Event: Wait for command to wait until the corresponding shell program is finished.</p></td></tr><tr><td><p>Bind exit code to:</p><p>(optional)</p></td><td><p>Defines a variable to retrieve the termination status (exit code) of the executable program.</p><p>If the execution mode is set to 'Parallel' the exit code is available after the program has terminated.</p></td></tr></tbody></table>



## Examples:

A few examples of Windows commands you can run from within Venus:&#x20;

* Copying a file from a template.
* Mapping a network drive.
* Deleting a temporary file.
* Making a call to a notification service.
* Data Logging.



