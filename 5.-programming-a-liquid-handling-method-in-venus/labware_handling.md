# Loading Labware

There are two options to load labware on the deck: Autoload and manual load. In both cases, always have the needed carriers ready. The following table shows the possible course of action:

| Method contains “Load Carrier” Commands | <p><br></p><p>Autoload Instrument</p>                                                                                                                                                                                          | <p><br></p><p>Manual Load Instrument</p>                                                                       |
| --------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | -------------------------------------------------------------------------------------------------------------- |
| Yes                                     | <p>Run the method.</p><p>Insert carriers in the tracks of the Autoload tray where indicated by LEDs.</p><p>Click “Load” in the dialog.</p><p>Possibility to manipulate sequences.</p><p>Carriers are loaded automatically.</p> | <p>Run the method.</p><p>The instrument will prompt a message to load the carriers manually onto the deck.</p> |
| No                                      | <p>Load the carriers manually into their positions on the deck.</p><p>Run the method.</p>                                                                                                                                      | <p>Load the carriers manually into their positions on the deck.</p><p>Run the method.</p>                      |

\


<table data-header-hidden><thead><tr><th width="145"></th><th></th></tr></thead><tbody><tr><td><img src="../.gitbook/assets/image (10) (1) (1) (1) (1) (1).png" alt="" data-size="original"></td><td><p>NOTE</p><p><em>If no “Load carrier” Commands are specified in the method, no checking of carrier presence is possible</em>.</p></td></tr></tbody></table>



## Autoload

When using the Autoload option, make sure to load the carriers with the appropriate labware first.



With “Load Carrier” Commands in the method:

1. If the “Load Carrier” Commands have been incorporated into the method: start the “Run Screen” as described in the following sections, and run the method.\
   The correct positions for the insertion of carriers will be highlighted by the green LEDs.\

2.  Insert the carriers into the tracks of the Autoload tray until they touch the stop hooks on the far side of the tray.\


    <figure><img src="../.gitbook/assets/image (107).png" alt=""><figcaption><p>These pictures are made from the rear of the instrument. </p></figcaption></figure>
3. Click \[Load] in the dialog.\
   The carriers are loaded onto the deck automatically by the “Load Carrier” Command in the method. At the same time, the barcodes of carriers and labware are read and stored in a file.

<table data-header-hidden><thead><tr><th width="145"></th><th></th></tr></thead><tbody><tr><td><img src="../.gitbook/assets/image (10) (1) (1) (1) (1) (1).png" alt="" data-size="original"></td><td><p>NOTE</p><p><em>If “Sample Tracking” is enabled (in the system configuration editor), the barcodes will be written to the Database.</em></p></td></tr></tbody></table>



Another way for loading is to place the carriers onto the defined positions of the Autoload tray before starting the method. Loading and barcode reading will then be performed without user input.



Without “Load Carrier” Commands in the method

1. If there have been no “Load Carrier” Commands incorporated into the method, the carriers must be loaded manually into the positions on the deck defined in the Deck Layout before the run is started.
2. Make sure that the carriers are inserted completely, until they touch the rear connectors.



## Manual Load

In order to load the ML STAR, fill the carriers with the appropriate labware first.



With “Load Carrier” Commands in the Method

1. If the “Load Carrier” Commands have been incorporated into the method, start the run. The instrument will prompt a message to load the carriers manually onto the deck.
2.  Make sure the carriers are inserted completely, until they lock in the rear snaps. A magnetic sensor checks whether the carriers have been loaded correctly.

    <figure><img src="../.gitbook/assets/image (108).png" alt="" width="563"><figcaption></figcaption></figure>

    \


    Without “Load Carrier” Commands in the Method

    1. If there have been no “Load Carrier” Commands incorporated into the method, load the carriers manually into the positions on the deck defined in the Deck Layout before the run is started.
    2. Make sure that the carriers are inserted completely, until they touch the rear snaps.

    \


## Command Description

The following tables give a brief overview of the available ML STAR-specific loading commands.

{% tabs %}
{% tab title="Single Steps" %}


| Command                 | Icon                                                                       | Action Performed                                                                      |
| ----------------------- | -------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- |
| Load Carrier            | <img src="../.gitbook/assets/image (109).png" alt="" data-size="original"> | Load a carrier on the deck.                                                           |
| Unload Carrier          | <img src="../.gitbook/assets/image (110).png" alt="" data-size="original"> | Unload a carrier from the deck.                                                       |
| Reload carrier          | <img src="../.gitbook/assets/image (111).png" alt="" data-size="original"> | Used to load, unload or reload a carrier.                                             |
| Lock/Unlock Front Cover | <img src="../.gitbook/assets/image (112).png" alt="" data-size="original"> | Locks/unlocks the front cover.                                                        |
| Initialize              | <img src="../.gitbook/assets/image (113).png" alt="" data-size="original"> | Initialize the instrument.                                                            |
| Move Auto Load          | <img src="../.gitbook/assets/image (114).png" alt="" data-size="original"> | Moves the autoload to a selected track number.                                        |
| Calibrate Carrier       | <img src="../.gitbook/assets/image (115).png" alt="" data-size="original"> | Calibrate precise position of a high-density Microplate (1536 wells) before asp/disp. |
{% endtab %}

{% tab title="Smart Steps" %}


| Command               | Icon                                                                       |                                                                                                                                                                                              |
| --------------------- | -------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Advanced Load setting | <img src="../.gitbook/assets/image (116).png" alt="" data-size="original"> | Define other settings than the default of the load steps.                                                                                                                                    |
| Load                  | <img src="../.gitbook/assets/image (117).png" alt="" data-size="original"> | Load carrier on deck.                                                                                                                                                                        |
| Unload                | <img src="../.gitbook/assets/image (118).png" alt="" data-size="original"> | Remove carrier from deck.                                                                                                                                                                    |
| Load and match        | <img src="../.gitbook/assets/image (119).png" alt="" data-size="original"> | Load samples and match loading information with worklist information, to generate data for use in the following process steps. An “Import Worklist” must be performed prior to this command. |
{% endtab %}
{% endtabs %}

