---
icon: dev
---

# Intermittent Custom Dialog crashing method

[Lab Automation Forums](https://labautomation.io/)

## [Intermittent Custom Dialog crashing method](https://labautomation.io/t/intermittent-custom-dialog-crashing-method/3200)

[Andre](https://labautomation.io/u/Andre) March 16, 2024, 2:36pm1

Hi everyone-

We recently upgrade to new Dell Optiplex 5000 desktop PC (64bit, 8gb ram, I7) , and getting strange method aborting at custom dialog calls. It seems intermittent, since it runs fine initially but if have to call custom dialog (with custom image) more than 3x then it aborts method and crashes method editor.

I suspect there is a memory leak, but same exact method works perfectly on older dell computer with same memory size. I am puzzled…

I am running Venus 4 (4.5) and error happens on both while running method manager and direct from method editor.

Has anyone seen this problem before? Thanks in advance!!!

[Kastronaut](https://labautomation.io/u/Kastronaut) March 16, 2024, 2:55pm2

I have seen upgrading your RAM to 16GB+ and ensuring you have a SSD instead of an HDD mitigates a lot of these aborts/errors. Hoping that helps!

[Andre](https://labautomation.io/u/Andre) March 16, 2024, 3:49pm3

Thank you, I am seriously considering upgrading memory and hard driver at this point.

[WillTurman](https://labautomation.io/u/WillTurman) March 16, 2024, 9:49pm4

How big is your image?

I remember reaching a Run Control memory cap running a long running Scheduler workflow. I’m pretty sure there’s a hot-fix that increases the memory allocation for any given Run Control execution.

In the meantime, do you see the same behavior…

* when you remove the Custom Dialog? Not disable, remove altogether. Copy it into another method in the interim.
* when you replace the images in your Custom Dialog with ones with much smaller file sizes?

[Huajiang](https://labautomation.io/u/Huajiang) March 18, 2024, 8:21am5

Hi [@WillTurman](https://labautomation.io/u/willturman) , we had that problem for long running of scheduler workflow, the memory usage can soon reach about 1G, and it caused many problems. Can you share more information or document about that fix? Thank you.

[Andre](https://labautomation.io/u/Andre) March 18, 2024, 11:15pm6

Hi [@WillTurman](https://labautomation.io/u/willturman) and [@Huajiang](https://labautomation.io/u/huajiang) I have some news about this issue.

Answering Will’s question, images size are 1.57MB, and when I remove them all together problem goes away and when I replace them with smaller image and problem became intermittent.

This is when it dawn on me, HR control is a 32 bit application running on 64 bit system. It can only utilize 2GB of virtual memory(at the most). Further researching a solution to increase virtual memory, I found a patch application (NT core 4GB patch) which let 32 bit application access the additional 2GB of virtual memory and voila, it worked over and over again. This is patch page, [4GB Patch – NTCore](https://ntcore.com/?page\_id=371)

Thank you all for helping!

5 Likes[JBurford](https://labautomation.io/u/JBurford) March 19, 2024, 12:26pm7

[@Andre](https://labautomation.io/u/andre) Ah! A clever solution to a problem I have encountered in the past. I had a similar issue putting “large” images in custom dialog boxes. The work-around I used was compressing the images to <1MB, which did solve the issue. The 4GB Patch seems like a much better fix. Thanks for sharing!

2 Likes

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
