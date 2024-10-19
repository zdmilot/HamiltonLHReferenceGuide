---
icon: dev
---

# ASW Status Dialog 1.1.4/V6 GUI Issues

[Lab Automation Forums](https://labautomation.io/)

## [ASW Status Dialog 1.1.4/V6 GUI Issues](https://labautomation.io/t/asw-status-dialog-1-1-4-v6-gui-issues/4399)

[Hamilton (Venus) ](https://labautomation.io/c/hamilton-venus/venus-questions/31)[Venus Questions](https://labautomation.io/c/hamilton-venus/venus-questions/31)[labrat](https://labautomation.io/u/labrat) August 22, 2024, 11:29pm1

Hey folks, I’ve got a dialog issue I can’t puzzle out. I’m trying to use the ASW Status Dialog library to update operators during the run, but when I run the method in question with new GUI, I get this abort error with “VENUS execution ended abruptly”, with no info in the trace as to why it aborted:

![Screenshot 2024-08-20 162938](https://labautomation.io/uploads/default/original/2X/7/763bc624b0566b683d2a2e9968e475301dc39cd6.png)

Also, it doesn’t “fully” abort the run; the GUI still shows them as running, despite saying “aborted” on the run control screen. The runs that finished/aborted successfully are iterations with no active status dialog steps.

![image](https://labautomation.io/uploads/default/original/2X/a/a657d3967047d011006360b80ef83b07dcf5b69c.png)

Notes:

* The method/dialog works just fine if I run in the legacy run control
* I was already on the newer/correct version of ASW dialogs for venus 6, aka 1.1.4
* Each attempted use included the appropriate initialize/terminate steps; it’s the initialize step that fails
* Computer is on windows 11
* Venus version 6.0.1.3380
* The step tracker library works just fine (and looks great), but I’d rather not use that library if I can avoid it

What I’ve tried so far, without any change in outcome:

* Uninstall/reinstall ASW Vector Custom Dialogs 1.1.4
* Made a bare-bones test method with nothing else in it
* Exported/imported to another win11/v6 computer, version 6.0.2.3426\
  – This computer is attached to an actual instrument, so I tried both simulated and non-simulated, no dice

If anyone has any thoughts/ideas, I am all ears.

[Custom COM Windows](https://labautomation.io/t/custom-com-windows/4715/2)[BrandonBare\_Hamilton](https://labautomation.io/u/BrandonBare\_Hamilton) August 23, 2024, 1:30am2

Hi [@labrat](https://labautomation.io/u/labrat) ,

Are you using Vector Custom Dialogs to display the status window or the one associated with ASWStandardDialogs? The latter is not compatible with VENUS 6.

Vector Custom Dialogs has the Status window included.

![image](https://labautomation.io/uploads/default/original/2X/f/ffd690866ff00e81be9656262abfb281b11cb9cf.png)

Ensure V1.1.4 is installed (I know you did some uninstall and reinstall so just to be sure). Open up the demo methods that come with the Vector dialogs and run the Status one as a quick check.

**C:\Program Files (x86)\HAMILTON\Methods\Library Demo Methods\VectorCustomDialogs\StatusDialog**

[![image](https://labautomation.io/uploads/default/original/2X/2/28465e2c70a2a80166012cc0588e07db70d446be.png)image792×220 7.69 KB](https://labautomation.io/uploads/default/original/2X/2/28465e2c70a2a80166012cc0588e07db70d446be.png)[![image](https://labautomation.io/uploads/default/optimized/2X/6/690f62e564314bba02fb222614d57ba6e649a15b\_2\_690x365.png)image1920×1017 305 KB](https://labautomation.io/uploads/default/original/2X/6/690f62e564314bba02fb222614d57ba6e649a15b.png)1 Like[labrat](https://labautomation.io/u/labrat) August 23, 2024, 7:29am3

Yeah I was totally trying to use the old one ![:woman\_facepalming:](https://labautomation.io/images/emoji/twitter/woman\_facepalming.png?v=12) I’ve never seen venus 6 abort like that, so it threw me off a bit. Works fine now that I’m using the correct library. I did not remotely clock that the status dialogs weren’t in their own library with 1.1.4, just naively assumed they were both updated with the newer version and did not look into it as closely as I should have. Thanks for your expertise!

Having dug through the demo methods, I’ve got another couple questions: is it possible to change the size of the status dialog and/or force-minimize it? I’ve got a few existing custom dialogs that are on the larger side, and the bottom right corner of the custom dialog is blocking the upper left corner of the status dialog (at least on the monitor I’m testing this on). I saw that some of the other functions allow size parameters, but nothing in status dialogs so I wanted to verify before jumping to the close/reopen after custom dialog route. I do see the “close status dialog” function, but that function doesn’t have anything in the .chm file, and from the demo method it looks like it just fully closes it. Would the best route just be to close it before the custom dialog and reopen it after the dialog is dismissed?

Sidebar question, is the size of the custom dialog box screen-size-percentage driven or is it set to an actual HxW measurement?

[BrandonBare\_Hamilton](https://labautomation.io/u/BrandonBare\_Hamilton) August 23, 2024, 1:53pm4

Hi [@labrat](https://labautomation.io/u/labrat) ,

There isn’t a way to change the size of the Status Window unfortunately, but a minimize/maximize function is a good suggestion that I will share with the team.

My recommendation would be to call the **CloseStatusDialog**, show your dialog, then **ShowStatusDialog**. This will remove the status window so that it doesn’t interfere and then bring it back up. This will clear the status that has been shown so far as a FYI.

According to the help file, the size is based on pixels.

![image](https://labautomation.io/uploads/default/original/2X/a/a7ae3ff8bf299f5489474a3305c417f7b7dacd4a.png)

* [Home](https://labautomation.io/)
* &#x20;
* [Categories](https://labautomation.io/categories)
* &#x20;
* [Guidelines](https://labautomation.io/guidelines)
* &#x20;
* [Terms of Service](https://labautomation.io/tos)
* &#x20;
* [Privacy Policy](https://labautomation.io/privacy)

Powered by [Discourse](https://www.discourse.org/), best viewed with JavaScript enabled
