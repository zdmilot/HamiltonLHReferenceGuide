---
icon: dev
---

# Changing Color Options in Dialog Boxes

[Lab Automation Forums](https://labautomation.io/)

## [Changing Color Options in Dialog Boxes](https://labautomation.io/t/changing-color-options-in-dialog-boxes/2763)

[Hamilton (Venus)](https://labautomation.io/c/hamilton-venus/7)[djunk](https://labautomation.io/u/djunk) January 12, 2024, 7:38pm1

Hi all,

Does anyone know of a way to change the color options developers can choose from for elements in a dialog box? Im imagining there may be a file somewhere with hex codes that Venus uses to present the dropdown list of colors.

[bowlineknot](https://labautomation.io/u/bowlineknot) January 12, 2024, 11:08pm2

Just curious is there a particular reason you want to do this? Match dialog designs to your company colors?

[Venus feature requests](https://labautomation.io/t/venus-feature-requests/248/75)[djunk](https://labautomation.io/u/djunk) January 13, 2024, 12:51am3

Yeah this is the primary reason. Also, this would be nice to allow us to match colors used on other platforms.

[bowlineknot](https://labautomation.io/u/bowlineknot) January 13, 2024, 1:10am4

There might be a Hamilton custom dialog template creator tool. Someone that used to work at my company created a custom dialog template that had our company logo. Makes it easy to replicate custom dialogs across methods.

[DanHartman\_Hamilton](https://labautomation.io/u/DanHartman\_Hamilton) January 15, 2024, 4:13pm5

Hi all,

There is a tool for creating a Custom Dialog Template, which can be downloaded at this [link](https://download.hamiltonsupport.com/wl/?id=hlQvIxADUrkOpe0Vq6lBpswTxzEVfWkf). Note that it is currently incompatible with VENUS 6; I will update this thread when a compatible version is released. Instructions on how to use the Template Creator software are included in the .zip.

The software requires generation of a .xaml file from the Custom Dialog Editor, which can be exported using the Export button along the top of the window:

![image](https://labautomation.io/uploads/default/original/2X/f/fe2d89ef77f27e4afebd1d999e4c4d4b457e58a8.png)

This .xaml file, along with an image file, is used to create a .cdt file which is stored in the Hamilton\Config folder. These .cdt files allow template selection in the first window that pops up when calling a new Custom Dialog step:

![image](https://labautomation.io/uploads/default/original/2X/9/92f2aa13e30681ef992f0a0745715fb07659ac10.png)

Note that the Template Creator tool is not required to be able to use exported .xaml templates, as the files can be imported into new Custom Dialog commands using the Import button along the top of the Custom Dialog Editor window:

![image](https://labautomation.io/uploads/default/original/2X/8/8d866497f728e33ef220229ffa7b17975c363145.png)

Alternatively, the Custom Dialog command can be copied/pasted directly in the Method Editor window as needed.

Thank you,\
Dan

5 Likes[LordNorm](https://labautomation.io/u/LordNorm) February 20, 2024, 6:35pm6

Hi Dan, any idea when this will be available for Venus 6? We’re stuck using the Vector dialog library for our custom dialogs, which is nice but fairly limited in terms of what a user can do within one window, so we’re hoping we can get a version of the custom dialog editor in Venus 6 soon. Thanks!

[DanHartman\_Hamilton](https://labautomation.io/u/DanHartman\_Hamilton) February 21, 2024, 2:14pm7

Hi [@LordNorm](https://labautomation.io/u/lordnorm),

There is currently no timeline for the template software compatibility updates for VENUS 6. That said, this shouldn’t stop you from using Custom Dialogs, as the instructions in my original post work in much the same way as a template does. Whether using the template software or not, a .xaml file will still need to be generated from an originally designed Custom Dialog. The difference is the template software will further create a .cdt file for choosing from the “Select a Template” window, while the raw .xaml can still be imported into a new Custom Dialog window to the same effect.

Thank you,\
Dan

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
