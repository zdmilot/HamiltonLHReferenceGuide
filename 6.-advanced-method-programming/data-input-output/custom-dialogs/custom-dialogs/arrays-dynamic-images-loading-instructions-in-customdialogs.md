---
icon: dev
---

# Arrays/dynamic images/loading instructions in CustomDialogs

[Lab Automation Forums](https://labautomation.io/)

## [Arrays/dynamic images/loading instructions in CustomDialogs](https://labautomation.io/t/arrays-dynamic-images-loading-instructions-in-customdialogs/3478)

[Hamilton (Venus)](https://labautomation.io/c/hamilton-venus/7)[Not-So-EasyBlood](https://labautomation.io/u/Not-So-EasyBlood) April 18, 2024, 10:05pm1

Hey friends - I’ve got a modified easyBlood method that has a pretty weird target-tube loading setup that is dependent on the source tubes that get loaded. I think it is going to be confusing/annoying for operators, so I want to make a custom dialog box that displays a dynamically-built image of which tubes should be loaded into each carrier. My first thought was to pass it an array of boolean values that would check/uncheck dialog boxes to match the required tube setup, but it doesnt look like you can pass arrays into a dialog box? Anybody have any handy tricks for deck loading instructions like that?

1 Like[luisvillaautomata](https://labautomation.io/u/luisvillaautomata) April 19, 2024, 7:01pm2

Your username is incredible lmaoooo.

2 Likes[mnewsom](https://labautomation.io/u/mnewsom) April 23, 2024, 1:20pm3

Do you have a mock-up of what you’d like to do?

With the custom dialog box you can export, edit the .xaml file, then re-import it. Handy for updating variable names, box names, or fine tuning positions.

exporting dialog:\
![image](https://labautomation.io/uploads/default/original/2X/a/ae8473b61fe9d60573e19ce557325b35a6e9a84e.png)\
editing in notepad++ (or whatever):\


[![image](https://labautomation.io/uploads/default/optimized/2X/9/980d041f231a74c98e1172ba69efb4cf2040c2f8\_2\_345x36.png)image1351×144 15.2 KB](https://labautomation.io/uploads/default/original/2X/9/980d041f231a74c98e1172ba69efb4cf2040c2f8.png)3 Likes[BirdBare](https://labautomation.io/u/BirdBare) April 23, 2024, 7:05pm4

Well hot dog that is cool!

2 Likes

* [Home ](https://labautomation.io/)
* &#x20;
* [Categories ](https://labautomation.io/categories)
* &#x20;
* [Guidelines ](https://labautomation.io/guidelines)
* &#x20;
* [Terms of Service ](https://labautomation.io/tos)
* &#x20;
* [Privacy Policy ](https://labautomation.io/privacy)

Powered by [Discourse](https://www.discourse.org/), best viewed with JavaScript enabled
