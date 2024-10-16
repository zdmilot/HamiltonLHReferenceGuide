---
icon: dev
---

# How to abort a method on the custom dialog?

[Lab Automation Forums](https://labautomation.io/)

## [How to abort a method on the custom dialog?](https://labautomation.io/t/how-to-abort-a-method-on-the-custom-dialog/1712)

[Hamilton (Venus)](https://labautomation.io/c/hamilton-venus/7)[Nat](https://labautomation.io/u/Nat) June 17, 2023, 7:08pm1

Hi all,

How do you abort a method using the custom dialog? For instance, using the default template, the “cancel” button acts the same as the “ok” button in which the method proceed regardless if you clicked the “cancel” or “ok” button. Tried looking it up in the user manual and Help Topics but to no avail. Below is a screenshot of what I mean. Any help is appreciated.

[![Screen Shot 2023-06-17 at 2.50.34 PM](https://labautomation.io/uploads/default/optimized/1X/c685d99eea3bea9b8ea07f3e3d86c6ba3fccba70\_2\_689x429.jpeg)Screen Shot 2023-06-17 at 2.50.34 PM1268×790 137 KB](https://labautomation.io/uploads/default/original/1X/c685d99eea3bea9b8ea07f3e3d86c6ba3fccba70.jpeg)[Optimize](https://labautomation.io/u/Optimize) June 17, 2023, 7:27pm2

The “Close/return” field set as “(2) Cancel” needs to be handled in the script,

after the “custom dialog” code, you will need to incorporate an If-Then group to handle the “(2) Cancel” response,

![image](https://labautomation.io/uploads/default/original/1X/03e36e081664d71e8d93ad69e3e4e6df510e22f7.png)

i added an example here to force script to abort if the dialog returns the “cancel” selection

1 Like[Nat](https://labautomation.io/u/Nat) June 17, 2023, 8:02pm4

The usage of the If-Then group makes sense for telling the script to abort upon the “(2) Cancel” response but my next question is how do I initialize the left operand variable, in your example, “rtnDialog”, in the button within the custom dialog?

[Optimize](https://labautomation.io/u/Optimize) June 17, 2023, 8:35pm5

create a “new variable”

then in custom dialog script line, set the “return” variable for dialog box to be “rtndialog”

[![image](https://labautomation.io/uploads/default/original/1X/a2b8c22b854dd115716f8d68b918c56d4a09d75e.png)image750×188 13.5 KB](https://labautomation.io/uploads/default/original/1X/a2b8c22b854dd115716f8d68b918c56d4a09d75e.png)1 Like[Nat](https://labautomation.io/u/Nat) June 17, 2023, 8:41pm6

Ah I see now. That answered my question. Thank you so much for the help, greatly appreciated!

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
