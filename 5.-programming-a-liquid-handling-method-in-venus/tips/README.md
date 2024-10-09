# Tips

This section discusses essential tip handling topics. Although the process of tip handling is stable and safe, some precautions must be considered when handling with special labware.

VENUS Software offers a tip recognition feature based on the different tip geometries. It is available for both disposables and needles and it is activated during installation by a Service Engineer. This feature increases the ML STAR instrument´s security, especially when different tip types (e.g. low- and standard volume tips) are used. In addition, all tip racks have color-coded labels and are bar-coded to be identified by the Autoload option (if installed).

For distinguishing disposable CO-RE tips, 50µl and CO-RE tips and 300µl, a special library is needed. Please consult a local Hamilton Representative.

<table data-header-hidden><thead><tr><th width="145"></th><th></th></tr></thead><tbody><tr><td><img src="../../.gitbook/assets/image (10) (1) (1) (1) (1) (1).png" alt="" data-size="original"></td><td><p>NOTE</p><p><em>All new or special tip types require additional settings (such as configuration file entries, liquid classes etc.) in the VENUS Software. Please consult a local Hamilton Representative for the implementation data of non-standard tips.</em></p></td></tr></tbody></table>



### Tip Recognition with Different Tip Types on the Same Deck Layout

The tips used in a pipetting procedure must match with the suitable pipetting channel or pipetting head in order to prevent damage to the device. Proper precautions have to be taken when loading tips in order to prevent confusing with the tips or loading wrong tip types.

Whenever possible, use _loading with Autoload_ and make sure that only tip carriers with the suffix …BC… (e.g. TIP\_CAR\_480BC\_ST\_A00) are used. In case of a wrong tip rack, the system, while loading will prompt an error which looks like the image shown below.

![](<../../.gitbook/assets/image (12).png>)\


When using another tip carrier (e.g. the 50 µl tip carrier) switch to the Deck Layout and change the properties MlStarCarBCOrientation to 1 and the MlStarCarNoReadBarcode to 0.

\


<div>

<figure><img src="../../.gitbook/assets/image (13).png" alt=""><figcaption></figcaption></figure>

 

<figure><img src="../../.gitbook/assets/image (14).png" alt=""><figcaption></figcaption></figure>

</div>

\
When _loading manually_, pay extra attention to the tip types which are similar in design and cannot be distinguished by the tip recognition feature. When CO-RE tips, 1-50µl and CO-RE tips, 10-300µl are used on the same Deck Layout, a _special library_ is needed. Please consult a local Hamilton Representative. In addition, check the label of the tip rack. The volume of the tips can be found on the top left corner of the barcode label:

\


<figure><img src="../../.gitbook/assets/image (15).png" alt=""><figcaption></figcaption></figure>

\


When _loading manually_ and there is _no library available_ for distinguishing the different tip types used, _visual inspection_ of the barcode label is the only option. This is the case for Slim Tips, 10- 300µl used in combination with CO-RE Tips, 10-1000µl.

\


<table data-header-hidden><thead><tr><th width="145"></th><th></th></tr></thead><tbody><tr><td><img src="../../.gitbook/assets/image (10) (1) (1) (1) (1) (1).png" alt="" data-size="original"></td><td><p>NOTE</p><p><em>Slim tips and 1000µl tips have the same head sizes therefore it can only be checked through the barcode reader.</em></p></td></tr></tbody></table>

\
