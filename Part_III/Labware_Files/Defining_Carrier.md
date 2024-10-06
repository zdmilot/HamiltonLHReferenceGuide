# Defining a Carrier

Carriers are placed onto the ML STAR deck. They have sites for labware, such as plates, troughs or tubes. A carrier files is defined as a template (_.tpl)._

_In the following a carrier that is pre-loaded with flat 96-well Nunc microplates is defined._

\


![Originalbild anzeigen](../../.gitbook/assets/Image\_507.gif)

_NOTE_

_A Tube Carrier in the sense of labware is not a carrier (template). It is a rack which directly fits the track geometry of the Microlab STAR and therefore can directly be loaded onto the instrument deck._

\


_To define a Carrier:_

1.  _Open the Labware Editor and select “File  New  Template”._

    \


    ![image](../../.gitbook/assets/Image\_508.jpg)

    \

2.  _The “Template Definition” Dialog opens._

    \


    ![image](../../.gitbook/assets/Image\_509.jpg)

    *   _The “Width” of the carrier is derived from:_

        \


        ![image](../../.gitbook/assets/Image\_510.png)

        _width \[mm] = # \[track ] ⋅ 22.5 \[_

        _mm track ]_
    * _In the case of a plate carrier which is 6 tracks wide, the result is 136 mm. The length of a ML STAR track is always 497 mm._
    * _Select the “Pre-loaded” Checkbox, to let the carrier be pre-loaded with the microplates. Select a background color of choice._
    * _Type a name and a description for the carrier._
    *   _Select a picture file (if available) for the graphical representation of the carrier in the method editor. Click \[Next >]._

        \


        ![image](../../.gitbook/assets/Image\_511.png)

        _ATTENTION_

        _The clearance height defines – the traverse height at which the pipetting channels can move without collision._

        _Clearance height should not exceed 140mm._

        _Wrong clearance height definitions can lead to serious damages._

        \

3.  _In the next window, the sites hosting the plates have to be defined:_

    \


    ![image](../../.gitbook/assets/Image\_512.jpg)
4. _Select the lines, one after another or several together and click on \[Site Properties…]._
5.  _A new dialog box as shown below opens._

    \


    ![image](../../.gitbook/assets/Image\_513.jpg)
6. _All selected sites will be updated with the values from this dialog._
   * _“Drawing” is only of visual relevance; accept the defaults._
   * _For “Snap to site”, select the lower option for a microplate, because a microplate fits with its bottom onto the plate carrier, to enable a good electrical coupling for capacitance-based LLD._
   * _All plate types should be defined with the same ‘footprint’ of 127 x 86mm. Only this size will snap onto a default carrier._
   * _Click on \[Browse] to search for the corresponding labware to add pre-defined or user- defined labware to the site._
   * _To define a new labware site to be added on the deck, click \[New...]. This starts the “Rectangular Rack Definition” Wizard as described previously._
7. _After filling out all “Site Properties” Fields, click \[OK]._
8. _Save the new carrier within the Labware Editor (e.g. as “MyCarrier” (.tml)). The sketch below illustrates the different “Origin” coordinates and “Dimensions”._
9.  _Click “File  Exit”, to exit the Labware Editor and switch back to the Deck Layout Editor and position the carrier on the deck:_

    _The carrier is now pre-loaded with a plate and the custom rack (sites) on top. The carrier itself without any pre-loaded items can be loaded onto the Deck Layout._

    \


    ![image](../../.gitbook/assets/Image\_514.png)

    _Template_

    \


    \


    _Site origin_

    \


    _Template origin_

    _Length_

    \


    _Site_

    _Site origin y-offset_

    \


    \


    _Width_

    _Site origin x-offset_

    \


    _The decision whether a plate (or tip rack) fits in a site of a carrier is made depending on the length and width of the site: all plates that have the same boundary measures (length 86 mm, width 127 mm) can be placed on the site._
10. _Open the newly defined carrier in the Labware Editor._

    \


    ![image](../../.gitbook/assets/Image\_515.jpg)

    \

11. _Select “Edit  Properties...”. A dialog will prompt._
12. _Click \[Add] to type in the “Labware Specific Properties and Values”._

    \


    ![image](../../.gitbook/assets/Image\_516.png)

    \


    ![image](../../.gitbook/assets/Image\_517.png)

    _Properties of a PLT\_CAR\_L5MD_
13. _A “Properties” Dialog for the racks is also available._

![Originalbild anzeigen](../../.gitbook/assets/Image\_518.gif)

_NOTE_

_Always start with the given settings of a standard carrier and the apply changes in a step by step manner. Do not change the properties names or their spelling. These names are system properties._

