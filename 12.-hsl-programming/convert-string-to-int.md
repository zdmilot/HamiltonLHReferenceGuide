# Convert String to Int

[Lab Automation Forums](https://labautomation.io/)

## [Convert String to Int](https://labautomation.io/t/convert-string-to-int/547)

[Hamilton (Venus)](https://labautomation.io/c/hamilton-venus/7)[Stefan](https://labautomation.io/u/Stefan) October 10, 2022, 3:34am1

Hi,

How do I convert a string e.g. “50” to an integer in Venus? I’m trying to use the SBS centrifuge in simulation mode by passing a string like “1200, 1400, 1200” for the array variables. I have a string tokenize function that can split the string by the commas but I don’t know how to convert from that to an int.

The trace output doesn’t register any errors but I can see that my integer arrays aren’t getting passed as input parameters.

```auto
2022-10-09 23:32:44> LIBRARY: Hamilton Centrifuge : Centrifuge - start;  i_strLabel = GSK_Centrifuge, i_blnCloseCoverAtEnd = 1, i_intPresentPosition = 2, i_intDirection = 0, i_intDecelleration = 1200
2022-10-09 23:32:44> LIBRARY: Hamilton Centrifuge : Centrifuge ==> _SendFirmwareCommand - progress;  i_strCommand [NodeMS], i_strParameter [zo084000zu01200]
2022-10-09 23:32:44> LIBRARY: Hamilton Centrifuge : Centrifuge ==> _SendFirmwareCommand - progress;  Command successful: er00 / No Error
2022-10-09 23:32:44> LIBRARY: Hamilton Centrifuge : Centrifuge ==> _PresentPosition ==> _SendFirmwareCommand - progress;  i_strCommand [NodeMP], i_strParameter [zp01]
2022-10-09 23:32:44> LIBRARY: Hamilton Centrifuge : Centrifuge ==> _PresentPosition ==> _SendFirmwareCommand - progress;  Command successful: er00 / No Error
2022-10-09 23:32:44> LIBRARY: Hamilton Centrifuge : Centrifuge ==> _CoverClose ==> _SendFirmwareCommand - progress;  i_strCommand [NodeMC], i_strParameter []
2022-10-09 23:32:44> LIBRARY: Hamilton Centrifuge : Centrifuge ==> _CoverClose ==> _SendFirmwareCommand - progress;  Command successful: er00 / No Error
```

EDIT: Solved, it’s in HSLAppsLib::StrConvertToNumber

[EricSindelar\_Hamilton](https://labautomation.io/u/EricSindelar\_Hamilton) October 10, 2022, 2:15pm2

Hi Stefan,

The HSL Core library that is part of the HSL Extensions installer also includes a ConvertToInteger function. The HSL String library command StrIVal performs a similar function.

\-Eric

[WilliamCham\_Hamilton](https://labautomation.io/u/WilliamCham\_Hamilton) October 10, 2022, 3:19pm3

Hello [@Stefan](https://labautomation.io/u/stefan),

While we have multiple libraries with some of these conversions, the HSL String Library contains all of our data type conversion functions:

* **StrAsciiToStr**: Converts ASCII integer value to a String
* **StrFStr**: Converts a Float to a String
* **StrFStrEx**: Converts a Float to a String with the option for language specific decimal symbol and number of significant figures
* **StrFVal**: Converts a String to a Float
* **StrHexIStr**: Converts an Integer into a Hexadecimal Character String
* **StrIStr**: Converts an Integer into a String
* **StrIVal**: Converts a String into an Integer
* **StrStrToAscii**: Converts a String character into an ASCII integer value

As a note, VECTOR does not have CHAR or BOOL data types. CHAR are just STR and BOOL are just INT.

\~William

5 Likes[bdunk17](https://labautomation.io/u/bdunk17) January 6, 2023, 3:33am4

Looks like my C++ skills might finally pay off on this project. I have a couple questions.

Does HSL offer any std equivalent libraries that provide the user dynamic/associative containers?

Does the static keyword assign a variable to a constant memory location?

1 Like[NickHealy\_Hamilton](https://labautomation.io/u/NickHealy\_Hamilton) January 6, 2023, 9:57pm5

[@bdunk17](https://labautomation.io/u/bdunk17) - I am not 100% sure on either, so I have relayed your questions internally for further comment.

In the meantime, if you wouldn’t mind elaborating just a bit on the context or intent I may be able to provide additional info for you. Thanks.

\-Nick

[NickHealy\_Hamilton](https://labautomation.io/u/NickHealy\_Hamilton) January 9, 2023, 6:45pm6![](https://labautomation.io/letter\_avatar\_proxy/v4/letter/b/bb73d2/48.png) bdunk17:

> Does HSL offer any std equivalent libraries that provide the user dynamic/associative containers?

As far as I am aware, that type of data structure is specific to C++. HSL, while it is it’s own proprietary programming language, is most comparable to C# (though that certainly doesn’t mean they are interchangeable).

It seems that the data structure accessible through VENUS/HSL most equivalent to your query may be a dictionary, which can store an indefinite number of parameter pairs. VENUS does require that when using a dictionary, that the variant type used for the keys be conserved within the dictionary.

I use these for various purposes, via the Dictionary library of HSLExtensions (found in this [link](https://download.hamiltonsupport.com/wl/?id=x4h9EWHa4fvXuWnMSqAWYy7wWbUseHLt) from the VENUS library downloads post).

Further discussion adjacent to this topic and VENUS data structures can be found in this [post](https://forums.pylabrobot.org/t/2d-arrays/852) which may be of interest.

![](https://labautomation.io/letter\_avatar\_proxy/v4/letter/b/bb73d2/48.png) bdunk17:

> Does the static keyword assign a variable to a constant memory location?

If you are referring to the HSL keyword used when declaring static variables, objects or functions, that actually doesn’t have any bearing on their memory allocation. In HSL, ‘static’ dictates that the object or function will not be exported and/or visible outside of the HSL file (library) in which it is declared and used, and is essentially kept local.

When using method editor to create SMT libraries, this is the same as designating the function visibility as ‘Exported’, so that methods and libraries which include that library can access the function for use at the various levels the library is called.

[![image](https://labautomation.io/uploads/default/optimized/1X/e70cb52e4594b0b1d8e36e244934e2ac5e10c574\_2\_690x94.png)image932×128 26.3 KB](https://labautomation.io/uploads/default/original/1X/e70cb52e4594b0b1d8e36e244934e2ac5e10c574.png)

In VENUS, variable memory allocation is static.

Hope this helps.

\-Nick

1 Like

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
