# Locking the Cover

[Lab Automation Forums](https://labautomation.io/)

## [Cover Staying Locked During Custom Dialogue - Hamilton STAR](https://labautomation.io/t/cover-staying-locked-during-custom-dialogue-hamilton-star/2860)

[Hamilton (Venus)](https://labautomation.io/c/hamilton-venus/7)[HamiltonUser](https://labautomation.io/u/HamiltonUser) January 29, 2024, 8:33pm1

Title basically says it all, it used to be the case that while a method was paused during a custom user dialogue interface, the cover would unlock allowing you to lift it and add tips/replace reagents/add plates etc.

Is this a new feature with VENUS 6 that intentionally prevents the lid from unlocking? If not, does anyone know how I might go about re-enabling this feature?

[EricSindelar\_Hamilton](https://labautomation.io/u/EricSindelar\_Hamilton) January 29, 2024, 8:49pm2

To my knowledge, nothing has changed with VENUS 6 regarding the front cover functionality. The recommendation has been to use the single-step Lock/Unlock the Front Cover to unlock right before the dialog and to lock afterward.

See below for more info on enabling automatic locking of front cover:

Open the VENUS Method Editor and go to the Menu → Tools → System Configuration Editor. Select ML\_STAR and go to the Instrument configuration section. For the automatic locking of front cover, select Enabled as shown below:

[![image](https://labautomation.io/uploads/default/original/2X/1/1bd1df1d6ea2abf51ce0a1c90382ea9cd975f03d.png)image1278×694 32.8 KB](https://labautomation.io/uploads/default/original/2X/1/1bd1df1d6ea2abf51ce0a1c90382ea9cd975f03d.png)

​In the VENUS method editor, there is a command to Lock/Unlock the Front Cover (Single Step). ​In general, it is recommended to add a Front Cover Lock command at the start of the method, set it to Unlock just before any user output to allow an operator to access the deck, and then immediately set to Lock after.

3 Likes[Yass](https://labautomation.io/u/Yass) January 31, 2024, 7:01pm3

Hi,

With the Venus 6 launcher we noticed a lot of issues related to security. Hamilton local application engineer has advised us to use the lagacy run control and it works a lot better.\
You can try it on your side it can be changed in the parameters.

Regards

[EricSindelar\_Hamilton](https://labautomation.io/u/EricSindelar\_Hamilton) January 31, 2024, 7:07pm4

Can you please provide some more details on the issues you were experiencing?

Using the new VENUS 6 UI or the legacy run control should not impact the front cover monitoring functionality.

[HamiltonUser](https://labautomation.io/u/HamiltonUser) February 7, 2024, 9:33pm5

Thanks, Eric. I will use the single steps to lock/unlock the cover moving forward.

1 Like

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
