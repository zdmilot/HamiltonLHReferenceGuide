# Defining a Carrier (Template)

Carriers are placed onto the ML STAR deck. They have sites for labware, such as plates, troughs or tubes. A carrier files is defined as a template (\*.tpl).

In the following a carrier that is pre-loaded with flat 96-well Nunc microplates is defined.

<table data-header-hidden><thead><tr><th width="145"></th><th></th></tr></thead><tbody><tr><td><img src="../../.gitbook/assets/image (10) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" data-size="original"></td><td><p>NOTE</p><p><em>A Tube Carrier in the sense of labware is not a carrier (template). It is a rack which directly fits the track geometry of the Microlab STAR and therefore can directly be loaded onto the instrument deck.</em></p></td></tr></tbody></table>

To define a Carrier:

1.  Open the Labware Editor and select “File -> New -> Template”.\


    <figure><img src="../../.gitbook/assets/image (28) (1).png" alt=""><figcaption></figcaption></figure>
2.  The “Template Definition” Dialog opens.\
    \
    ![](<../../.gitbook/assets/image (31) (1).png>)\


    * The “Width” of the carrier is derived from:\
      $$\text{width} \, [\text{mm}] = \# [\text{track}] \cdot 22.5 \left[ \frac{\text{mm}}{\text{track}} \right]$$
    * In the case of a plate carrier which is 6 tracks wide, the result is 136 mm. The length of a ML STAR track is always 497 mm.
    * Select the “Pre-loaded” Checkbox, to let the carrier be pre-loaded with the microplates. Select a background color of choice.
    * Type a name and a description for the carrier.
    * Select a picture file (if available) for the graphical representation of the carrier in the method editor. Click \[Next >].



    <table data-header-hidden><thead><tr><th width="145"></th><th></th></tr></thead><tbody><tr><td><img src="../../.gitbook/assets/image (9) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" data-size="original"></td><td><p>ATTENTION</p><p><em>The clearance height defines – the traverse height at which the pipetting channels can move without collision.</em></p><p><em>Clearance height should not exceed 140mm.</em></p><p><em>Wrong clearance height definitions can lead to serious damages.</em></p></td></tr></tbody></table>
3.  In the next window, the sites hosting the plates have to be defined:

    <figure><img src="../../.gitbook/assets/image (33) (1).png" alt=""><figcaption></figcaption></figure>
4. Select the lines, one after another or several together and click on \[Site Properties…].
5.  A new dialog box as shown below opens.\


    <figure><img src="../../.gitbook/assets/image (34) (1).png" alt="" width="392"><figcaption></figcaption></figure>
6. All selected sites will be updated with the values from this dialog.
   * “Drawing” is only of visual relevance; accept the defaults.
   * For “Snap to site”, select the lower option for a microplate, because a microplate fits with its bottom onto the plate carrier, to enable a good electrical coupling for capacitance-based LLD.
   * All plate types should be defined with the same ‘footprint’ of 127 x 86mm. Only this size will snap onto a default carrier.
   * Click on \[Browse] to search for the corresponding labware to add pre-defined or user- defined labware to the site.
   * To define a new labware site to be added on the deck, click \[New...]. This starts the “Rectangular Rack Definition” Wizard as described previously.
7. After filling out all “Site Properties” Fields, click \[OK].
8. Save the new carrier within the Labware Editor (e.g. as “MyCarrier” (.tml)). The sketch below illustrates the different “Origin” coordinates and “Dimensions”.
9.  Click “File -> Exit”, to exit the Labware Editor and switch back to the Deck Layout Editor and position the carrier on the deck:\
    \
    The carrier is now pre-loaded with a plate and the custom rack (sites) on top. The carrier itself without any pre-loaded items can be loaded onto the Deck Layout.\
    \
    The decision whether a plate (or tip rack) fits in a site of a carrier is made depending on the length and width of the site: all plates that have the same boundary measures (length 86 mm, width 127 mm) can be placed on the site.

    <figure><img src="../../.gitbook/assets/image (35) (1).png" alt="" width="356"><figcaption></figcaption></figure>
10. Open the newly defined carrier in the Labware Editor.\


    <figure><img src="../../.gitbook/assets/image (36) (1).png" alt="" width="375"><figcaption></figcaption></figure>
11. Select “Edit -> Properties...”. A dialog will prompt.
12. Click \[Add] to type in the “Labware Specific Properties and Values”.\
    ![](<../../.gitbook/assets/image (37) (1).png>)\
    \
    ![](<../../.gitbook/assets/image (39) (1).png>)\
    \


    <table data-header-hidden><thead><tr><th width="145"></th><th></th></tr></thead><tbody><tr><td><img src="../../.gitbook/assets/image (10) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" data-size="original"></td><td><p>NOTE</p><p><em>Always start with the given settings of a standard carrier and the apply changes in a step by step manner. Do not change the properties names or their spelling. These names are system properties.</em></p></td></tr></tbody></table>


13. A “Properties” Dialog for the racks is also available.
