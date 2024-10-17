# The TADM Principle

## **TADM curves**

### **Technical aspects**

Figure 3 and Figure 4 explain in detail how the mechanical movement of the plunger influences the flow of liquid inside the tip and the shape of the resulting pressure curve for an aspiration or a dispense step. The lower part of Figure 3 and Figure 4 contain schematic drawings of the situation within the tip at the start, during, and at the end of the pipetting step (Pi = air pressure inside the tip, Ph = hydrostatic pressure inside the tip, pressure).

<figure><img src="../../.gitbook/assets/image (3) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" width="563"><figcaption><p><strong>Fig. 3: TADM curves: Aspiration</strong></p></figcaption></figure>



<figure><img src="../../.gitbook/assets/image (4) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" width="563"><figcaption><p><strong>Fig. 4: TADM curves: Dispense</strong></p></figcaption></figure>



Obviously, the TADM feature would not be feasible if the pressure curves obtained were instrument-, weather- and altitude-dependent. Therefore, the reference point of the pressure curve is zeroed automatically by the software before pipetting commands are executed.

Figure 5 explains at what time the reference point for the pressure curves is zeroed depending on whether an aspiration or a dispense step is programmed. This is important to know if consecutive aspiration or dispensing (aliquoting) steps use the same liquid class and volume.

<figure><img src="../../.gitbook/assets/image (5) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" width="358"><figcaption><p><strong>Fig. 5: Pressure value adjustments for aspiration and dispense steps</strong></p></figcaption></figure>

Because the pressure value is not re-zeroed between consecutive aspiration steps, TADM curves from the different aspiration cycles will be shifted, as can be seen in Figure 6 (left side, 2 aspirations of 400μl each). In other words, the reference point for the start of an aspiration curve will always be the pressure value obtained before the tip was picked up. Since the pressure value is re-zeroed between consecutive dispensing steps, curves as seen in Figure

6 (right side, dispensing 100 μl 8 times) will be obtained, where the curves from all consecutive dispense cycles are not shifted.

<figure><img src="../../.gitbook/assets/image (6) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption><p><strong>Fig. 6: Consecutive aspiration and dispense steps and the resulting TADM curves</strong></p></figcaption></figure>



<table data-header-hidden><thead><tr><th width="145"></th><th></th></tr></thead><tbody><tr><td><p></p><p><img src="../../.gitbook/assets/12 (1).jpeg" alt="" data-size="original"></p><p></p></td><td><p><strong>NOTE</strong></p><p><em>In order to use TADM tolerance bands for an aspiration step such as in Figure 6, different liquid classes have to be used for the individual aspiration steps</em></p></td></tr></tbody></table>





## **Pipetting errors**

By examining the TADM curves of many aspiration or dispense steps, it becomes apparent that curves obtained from a normal, error-free pipetting step are distinctively different from curves from erroneous pipetting steps. These differences are quite obvious and can be used to distinguish between correct and erroneous pipetting steps.

The following two figures show the different types of TADM curves that can be obtained during aspiration and dispense steps respectively. Basically, there are two different types of scenarios that can be detected:

* Pressure above normal
* Pressure below normal

The type of pipetting step (aspiration or dispensing) influences what kind of scenario a specific error produces. For example, a blocked tip will produce pressure below normal during aspiration and pressure above normal during dispensing, while a short sample will produce pressure above normal during aspiration and pressure below normal during dispensing.

<table data-header-hidden><thead><tr><th width="145"></th><th></th></tr></thead><tbody><tr><td><p></p><p><img src="../../.gitbook/assets/12 (1).jpeg" alt="" data-size="original"></p><p></p></td><td><p><strong>NOTE</strong></p><p><em>The vast majority of pipetting errors will be detected during the aspiration step. Foam can behave rather unpredictably and can produce pressure above as well as pressure below normal errors during aspiration and / or dispensing”).</em></p></td></tr></tbody></table>



### **Possible pipetting errors during aspiration**

<figure><img src="../../.gitbook/assets/image (7) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" width="375"><figcaption><p><em>Fig. 7: Typical TADM curves for correct and erroneous aspiration steps</em></p></figcaption></figure>



A pressure value below the normal, error-free aspiration curve means that the pressure decreases because as the plunger continues to move inside the channel, the liquid level inside the tip does not. A pressure signal above the error-free curve signifies that as the Tip blocked (Clot) plunger moves inside the channel, the liquid that enters the tip has less resitance than the reference liquid.

**3.3.2 Possible pipetting errors during dispensing**

<figure><img src="../../.gitbook/assets/image (8) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" width="375"><figcaption><p><strong>Fig. 8: Typical TADM curves for correct and erroneous dispensing steps</strong></p></figcaption></figure>

A pressure value above the error-free dispensing curve means that the pressure increases because as the plunger continues to move inside the channel, the liquid level inside the tip does not. A pressure signal below the error-free curve signifies that as the plunger pushes the air inside the channel, the liquid that leaves the tip has less resitance than the reference liquid.

## **Summary**

Below is a summary table showing the correlation between pipetting errors and the resulting pressure curves during either aspiration or dispensing.

| Pipetting step | Error type         | Pressure curve                                  |
| -------------- | ------------------ | ----------------------------------------------- |
| aspiration     | clot detected      | pressure below normal                           |
|                | no or short sample | pressure above normal                           |
|                | foam               | 'zig-zag' behavior, pressure above/below normal |
|                | leaky system       | pressure above normal                           |

| Pipetting step | Error type        | Pressure curve                                   |
| -------------- | ----------------- | ------------------------------------------------ |
| dispensing     | blocked tip       | pressure above normal                            |
|                | not enough liquid | retarded rise in pressure, pressure below normal |
|                | foam              | 'zig-zag' behavior, pressure above/below normal  |
|                | leaky system      | pressure below normal                            |





## **Step by step using TADM**

**Introduction**

The TADM principle can be used in two different ways:

1. Recording mode: The pressure inside the pipetting channel is **recorded only**.
2. Monitoring mode: The pressure inside the pipetting channel is constantly **recorded and compared** to a predefined tolerance value. If the measured value exceeds the tolerance, the plunger movement stops immediately and the software-dependent error handling is executed.

However, special attention has to be paid to a number of settings that can effectiveness and behavior of TADM (see Figure 9 below).

<figure><img src="../../.gitbook/assets/image (9) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption><p><em>Fig. 9: TADM settings and modes</em></p></figcaption></figure>



<table data-header-hidden><thead><tr><th width="145"></th><th></th></tr></thead><tbody><tr><td><p></p><p><img src="../../.gitbook/assets/image (9) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" data-size="original"></p><p></p></td><td><p><em>ATTENTION</em></p><p><em>If TADM is not enabled for the liquid class, no TADM monitoring will take place for this liquid class even if the TADM mode is set to monitoring.</em></p><p><em>If a tolerance band has not been defined for a specific volume used during</em></p><p><em>pipetting in TADM monitoring mode, the run will be aborted.</em></p></td></tr></tbody></table>

<table data-header-hidden><thead><tr><th width="139"></th><th></th></tr></thead><tbody><tr><td><p></p><p><img src="../../.gitbook/assets/12 (1).jpeg" alt="" data-size="original"></p><p></p></td><td><p><strong>NOTE</strong></p><p><em>The temperature of the liquid can have a significant influence on the pressure</em></p><p><em>curve. It is mandatory that the liquid used for recording the reference pressure curves have the same temperature as the liquid used during routine work.</em></p></td></tr></tbody></table>



## **Methodology**

In order to increase the safety and robustness of the pipetting process, the following guidelines have to be followed for setting TADM tolerance bands.

### **Define the pipetting strategy**

Although setting the TADM tolerance bands is the last stage of application development, the liquid handling process must be defined as early as possible during development, because the implementation of liquid handling in the application may have a huge impact on the method programming.

### **Set up a robust process**

Before the TADM tolerance bands for a specific liquid and volume can be set, a precise and robust pipetting process has to be established. This involves the liquid class (accuracy and precision according to requirements) and the pipetting strategy (surface or jet mode, etc.) itself.

### **Get TADM data**

After the pipetting process has been established, a minimum of 20 curves per channel should be recorded in TADM recording mode in order to collect a significant number of data points. These sample curves provide the basis for setting the TADM tolerance bands – therefore the samples used should be checked carefully for the absence of clots, foam, etc.

### **Set tolerance bands**

After the standard curves have been recorded, the TADM tolerance bands must be set (see Chapter 4.6).

### **Check settings with ’ bad’ samples**

In order to check whether the TADM tolerance bands provide a safe and robust process, a run using stressed samples (foam, clots, etc.) must be performed in TADM monitoring mode.

### **Perform periodic checks**

It is recommended that you verify the usefulness of the TADM tolerance bands in routine operation (about every 3 to 6 months), especially if a lot of pipetting errors occur. This can be a sign that the TADM tolerance bands are set too narrow or are inadequate.

## **Recording of pipetting curves**

### **Instrument settings**

During the development and testing phase, the instrument should be set to “TADM recording mode”. This has to be set in the System Configuration Editor, which can be found under the "Tools" menu from the Method Editor.

The settings for the TADM modes / TADM Upload Modes can be set individually for every pipetting device such as 1000ul channels, 5ml channels and the CO-RE 96 Head.

![Fig. 10: System Configuration Editor: TADM settings](<../../.gitbook/assets/16 (1) (1) (1).png>)

Select your instrument (STAR, STARlet, STARplus) in the left of the window, and then scroll down the right side of the window to the entry "TADM settings". Change "TADM Mode" to "Recording" for the desired pipetting devices. Close the System Configuration Editor and save the changes.

Refer to figure 9 for an explanation of the different settings.

### **Enabling TADM for the liquid class**

To use the TADM feature, the used liquid classes have to be prepared for that. In order to do this, start the Liquid Editor. The "Liquid Classes" window lists all liquid classes available and also shows whether TADM is enabled or disabled for a specific liquid class.

<table data-header-hidden><thead><tr><th width="145"></th><th></th></tr></thead><tbody><tr><td><p></p><p><img src="../../.gitbook/assets/12 (1).jpeg" alt="" data-size="original"></p><p></p></td><td><p><strong>NOTE</strong></p><p><em>All predefined liquid classes supplied by HAMILTON with the installation of the software have TADM disabled and are write-protected.</em></p><p><em>To have the TADM feature enabled, copy the desired predefined liquid class and then enable the TADM feature</em></p></td></tr></tbody></table>



Select the desired predefined liquid class you want to copy and click the right mouse button. Click on ‘Create’

<figure><img src="../../.gitbook/assets/image (10) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption><p><strong>Fig. 11: Copying a predefined liquid class for TADM use</strong></p></figcaption></figure>

A dialog box opens to let you enter the name of the liquids class’ copy:

<figure><img src="../../.gitbook/assets/image (11) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption><p><strong>Fig. 12: Entering a name for the liquid class for TADM use</strong></p></figcaption></figure>



Enter the new name (e.g. with suffix “\_TADM”) and close the dialog by clicking “OK”

The newly created class will be added at the end of the list:

![Fig. 13: The newly created liquid class is added to the list](<../../.gitbook/assets/20 (1) (1).png>)



Now, double click the name of the new liquid class for TADM use. The “Edit Liquid Class” window opens. Set the “TADM” radio button to “Enabled” and close the dialog -> Click “OK”.

<figure><img src="../../.gitbook/assets/image (12) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption><p><strong>Fig. 14: Edit Liquid Class: Enable "TADM"</strong></p></figcaption></figure>



Check if the liquid class’ attribute for “TADM” is “Enabled”. You can also see that the “Origin”

is “User-defined”:

<figure><img src="../../.gitbook/assets/image (13) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption><p><strong>Fig. 15: Liquid class is ready for "TADM"</strong></p></figcaption></figure>



The system is now ready to record TADM curves.



<table data-header-hidden><thead><tr><th width="145"></th><th></th></tr></thead><tbody><tr><td><p></p><p><img src="../../.gitbook/assets/12 (1).jpeg" alt="" data-size="original"></p><p></p></td><td><p><strong>NOTE</strong></p><p><em>The TADM feature 5.1 supports all pipetting channels such as the (old) 300ul channel, the 1000ul channel, the 5ml channel and the CO-RE 96 Head TADM.</em></p><p><em>The CO-RE head 384 does not have individual pressure sensors on each channel and does therefore not support TADM.</em></p></td></tr></tbody></table>



Use the Liquid device selection to make sure the liquid class supports the correct device:

<figure><img src="../../.gitbook/assets/image (14) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption><p><strong>Fig. 16: Liquid device selection</strong></p></figcaption></figure>



## **Preparing the method**

In order to record the reference pressure curves for setting the TADM tolerance bands, the application must have an established pipetting strategy that is both robust and precise. If the method is very large or time consuming to run, smaller methods can be prepared that contain the same pipetting steps like the original method. Original liquids and labware have to be used, and special care has to be taken to make sure that no pipetting errors occur.



## **Analyzing TADM curves**

All pipetting steps of a run are traced and the relevant information like liquid class, pipetting mode (aspiration/dispensing, volume, channel number) is written into a single database.

### **Viewing of TADM Curves**

After running the method in TADM recording mode, the pressure curves obtained can be viewed in the Liquid Editor. Start the liquid editor and double click on the liquid class that is to be analyzed. Select the "TADM Tolerance Bands" tab and then press the "Add from run..." button. All available runs are listed by method name and recording date.

<figure><img src="../../.gitbook/assets/image (15) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption><p><strong>Fig. 17: Select Runs dialog box within the Liquid Editor</strong></p></figcaption></figure>



Select the desired runs by marking the check box and clicking "OK". There are several options and shortcuts available for selecting multiple runs:

| Shortcut | Action                                                                     |
| -------- | -------------------------------------------------------------------------- |
| Shift    | Select all runs between the selected one and the currently highlighted one |
| Ctrl     | Add only the currently highlighted run to the selection                    |
| Ctrl+A   | Select all runs in the list.                                               |
| Ctrl+C   | Check the checkboxes of the selected runs in the list.                     |
| Ctrl+T   | Toggle checkbox state of the selected runs in the list.                    |

<table data-header-hidden><thead><tr><th width="145"></th><th></th></tr></thead><tbody><tr><td><p></p><p><img src="../../.gitbook/assets/12 (1).jpeg" alt="" data-size="original"></p><p></p></td><td><p><strong>NOTE</strong></p><p><em>A maximum of 60 runs can be selected simultaneously.</em></p></td></tr></tbody></table>



After pressing "OK", the selected runs will be searched for the specified liquid class and all aspiration and dispense volumes used will be listed (Figure 18).

<figure><img src="../../.gitbook/assets/image (16) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption><p><strong>Fig. 18: Select a pipetting step to "Open..." the TADM Tolerance Band Editor</strong></p></figcaption></figure>



Selecting a single pipetting step will enable the button "Open...". Double-clicking on a pipetting step, or pressing this button, will open the “TADM Tolerance Band Editor” window (for a detailed account of the editor see chapter 5):

<figure><img src="../../.gitbook/assets/image (17) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption><p><strong>Fig. 19: The TADM Tolerance Band Editor</strong></p></figcaption></figure>



The title bar shows the selected liquid class, the volume and the pipetting mode. The window itself is divided into two frames. The right-hand one shows all curves for the selected volume and pipetting mode; the left-hand part of the window contains detailed information about the individual curves (pipetting time, channel number, TADM mode, etc).

The values are displayed as pressure \[**Pa**scal] over time \[**m**illi**s**econds] curves.

### **Characteristics of TADM curves**

TADM allows the analysis of pipetting steps and the resulting pressure curves in a qualitative way. It can therefore be a very helpful tool to optimize liquid handling.

<div>

<figure><img src="../../.gitbook/assets/image (18) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption><p><strong>Fig. 20a: Uncorrected Aspiration</strong></p></figcaption></figure>

 

<figure><img src="../../.gitbook/assets/image (19) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption><p><strong>Fig. 20b: Optimized Aspiration</strong></p></figcaption></figure>

</div>



The peaks and the fraying of curves observed in Figure 20a (left picture) can be an indication that the liquid class and / or the pipetting steps are not defined in an optimal and robust way, but they can also be characteristic of the liquid used. In the example shown above, the pipetting process was not optimized. An adjustment of the pipetting parameters in the pipetting process resulted in the curves shown in Figure 20b (right picture).

The following example shows typical curves for jet dispense steps.

<figure><img src="../../.gitbook/assets/image (20) (1) (1) (1) (1) (1) (1) (1).png" alt="" width="563"><figcaption><p><strong>Fig. 21: Dispensing process</strong></p></figcaption></figure>

The peak seen in the curves at 100ms in Figure 21 is typical for a dispense step and is not necessarily the result of sub-optimal settings. It actually reflects the dispensing of the transport air and the moment the liquid starts to leave the tip. The same holds true for the apparent fraying of the TADM curves at the end of the dispense step, which is the result of the blow-out volume and the resulting pressure inside the system.

<table data-header-hidden><thead><tr><th width="145"></th><th></th></tr></thead><tbody><tr><td><p></p><p><img src="../../.gitbook/assets/12 (1).jpeg" alt="" data-size="original"></p><p></p></td><td><p><strong>NOTE</strong></p><p><em>A narrow bundle of curves is not an indication that the pipetting process is precise and robust. Moreover, a precise and robust pipetting process does not guarantee closely bundled pressure curves.</em></p><p><em>TADM curves such as in Figure 20a can be - but do not have to be - an indication that the pipetting process is not robust and precise..</em></p></td></tr></tbody></table>



## **Defining the TADM Tolerance Band**

### **Defining the TADM Tolerance Band for single pipetting**

Load a set of TADM curves into the TADM Tolerance Band Editor as shown in Figure 20.

* Choose _Add Upper Limit Curve Points_ from the _Edit_ menu or click on the <img src="../../.gitbook/assets/image (22) (1) (1) (1) (1) (1) (1) (1).png" alt="" data-size="line"> icon

<figure><img src="../../.gitbook/assets/image (21) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption><p>Fig. 22: Upper Limit Curve tolerance band</p></figcaption></figure>

*   It is recommended that you set the first curve point between the 0 and 100 Pascal value (Figure 22). A higher value may be required if wet tips are used for the aspiration (Figure 23). Place the next curve points where the TADM curves change directions. Special attention should be paid to the tolerance band at the beginning and the end of the pipetting step. Here, the tolerance band should follow the actual pressure curve rather closely, while the distance between curves and band should be wider during the remaining phase of the pipetting step tolerance\


    <figure><img src="../../.gitbook/assets/image (23) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption><p><strong>Fig. 23: TADM tolerance bands for an aspiration step</strong></p></figcaption></figure>



* Make sure that the upper TADM tolerance band dips below the broken line shown in Figure 23. This line represents the pressure in the channel at the end of the aspiration step.
* Choose _Add Lower Limit Curve Points_ from the _Edit_ menu or click on the <img src="../../.gitbook/assets/image (22) (1) (1) (1) (1) (1) (1) (1).png" alt="" data-size="line"> icon
* Follow the same rules as mentioned above for setting the lower tolerance band.

A point of the tolerance band can also be deleted <img src="../../.gitbook/assets/image (24) (1) (1) (1) (1) (1) (1) (1).png" alt="" data-size="line"> or moved <img src="../../.gitbook/assets/image (25) (1) (1) (1) (1) (1) (1) (1).png" alt="" data-size="line"> after it has been placed. Zooming in also helps in fine-tuning the placement of the points.

* Choose _Close & apply changes_ under the File menu to save the TADM tolerance bands.

In the Liquid Editor's dialog box "Edit Liquid Class", the status of the selected pipetting step is now displayed as "Band saved". Changing change the status to "Band modified".

<figure><img src="../../.gitbook/assets/image (26) (1) (1) (1) (1) (1) (1) (1).png" alt="" width="291"><figcaption><p><strong>Fig. 24: TADM tolerance bands for a dispense step</strong></p></figcaption></figure>



* The same criteria can be used for applying TADM tolerance bands for dispensing steps (Figure 24), but make sure that the lower TADM tolerance band rises above the broken line. This line represents the pressure in the channel at the end of the dispense step.
* These steps have to be repeated for all liquid classes and volumes used in the method that require TADM.
* After the TADM tolerance bands for all pipetting steps required are defined, press OK and close the liquid editor.

### **Defining the TADM Tolerance Band for Dispense on the Fly**

A special pipetting mode is used in the function _DispenseOnTheFly_. This step does perform a serial dispense of part volumes without stopping the movement in the X-direction.

From this pipetting mode, a different pressure curve results. Please see below the 12 peaks in the dispense curve, representing the on-the-fly-pipetting of 50ul per well with one channel over the row A (A1 – A12) in a 96 well plate.

<figure><img src="../../.gitbook/assets/image (29) (1) (1) (1) (1).png" alt=""><figcaption><p><strong>Fig. 25: Pressure curve for a dispense on the fly step</strong></p></figcaption></figure>

<table data-header-hidden><thead><tr><th width="145"></th><th></th></tr></thead><tbody><tr><td><p></p><p><img src="../../.gitbook/assets/12 (1).jpeg" alt="" data-size="original"></p><p></p></td><td><p><strong>NOTE</strong></p><p><em>It is not necessary to define a tolerance band over all peaks of a dispense-on- the-fly pressure curve. Simply define the upper and lower limitation curve for the first peak, all following peaks will be handled respecting the data defined for peak one.</em></p></td></tr></tbody></table>

<figure><img src="../../.gitbook/assets/image (31) (1) (1) (1) (1).png" alt=""><figcaption><p><strong>Fig. 26: Tolerance band for a dispense on the fly step</strong></p></figcaption></figure>

<table data-header-hidden><thead><tr><th width="145"></th><th></th></tr></thead><tbody><tr><td><p></p><p><img src="../../.gitbook/assets/12 (1).jpeg" alt="" data-size="original"></p><p></p></td><td><p><strong>NOTE</strong></p><p><em>Please make sure the defined upper and lower limitation curve respects the highest peak and the lowest source in the whole curve, although it is defined only for the first peak.</em></p><p><em>Refer to Figure 27, where the highest peak is at the end of the 12 shots.</em></p></td></tr></tbody></table>



<figure><img src="../../.gitbook/assets/image (32) (1) (1) (1) (1).png" alt=""><figcaption><p><strong>Fig. 27: Respect the highest/lowest pressure point for the tolerance band</strong></p></figcaption></figure>



### **General rules for defining the TADM Tolerance Band**

#### **Distance between pressure curve and upper/lower limitation curve**

Take care not to set the TADM tolerance bands too close to the actual TADM curves as seen in Figure 28. While this ensures a safe pipetting process, many TADM errors will occur during pipetting that will result in an unrobust process. This is due to minor variations in the sample liquid (e.g.serum) and the resulting widening of the TADM curve bundle as more and more samples are pipetted (See Figure 29).

<figure><img src="../../.gitbook/assets/image (33) (1) (1) (1) (1).png" alt="" width="375"><figcaption><p><strong>Fig. 28: Inadequate TADM tolerance bands: Bands are set too narrow</strong></p></figcaption></figure>



#### **End position of the upper/lower limitation curve**

The TADM tolerance bands should stop as soon as the pipetting step ends and must not extend further than the actual TADM curves (as seen in Fig 27).

<figure><img src="../../.gitbook/assets/image (34) (1) (1) (1) (1).png" alt=""><figcaption><p><strong>Fig. 29: Inadequate TADM tolerance bands: Bands are much longer than curve</strong></p></figcaption></figure>





## **Interpreting the TADM pressure curves**

In order to check the usefulness of the TADM tolerance bands, perform a run using stressed samples (clots, foam, etc.) in TADM monitoring mode (Figure 30).

<figure><img src="../../.gitbook/assets/image (35) (1) (1) (1) (1).png" alt=""><figcaption><p><strong>Fig. 30: TADM curves obtained from a run using stressed samples</strong></p></figcaption></figure>



## **Working with TADM**

In order to enable TADM, the setting has to be changed within the system configuration editor (Figure 10). Choose between "None", "Error curves only" and "All curves" for the "TADM Upload Mode". In either case TADM will be enabled and each pipetting step will be monitored.

## **The TADM Tolerance Band Editor**

**Overview**

The TADM Tolerance Band Editor consists of several parts, as shown in its main window.

<figure><img src="../../.gitbook/assets/image (36) (1) (1) (1) (1).png" alt=""><figcaption><p><strong>Fig. 31: TADM Tolerance Band Editor main window</strong></p></figcaption></figure>

1\. Menu toolbar

2\. Filter TADM Curves toolbar

3\. TADM window

4\. Plotting area

The TADM window consists of three tabs (Upper Curve, Lower Curve, TADM Curves). The first two tabs contain the coordinates for the points of the upper and lower tolerance bands respectively. The third tab lists the properties of the displayed TADM curves. The following properties can be viewed: the method name of the run where the TADM curve was recorded, the channel number, pipette date, pipette result (processed/aborted), TADM mode (Recording/Monitoring), and the Curve ID. TADM curves of aborted pipetting steps are displayed in red in the plotting area, while successfully processed ones are displayed in dark blue.

<table data-header-hidden><thead><tr><th width="145"></th><th></th></tr></thead><tbody><tr><td><p></p><p><img src="../../.gitbook/assets/12 (1).jpeg" alt="" data-size="original"></p><p></p></td><td><p><strong>NOTE</strong></p><p><em>The Pipette result “Aborted” can only occur if the run was performed in Monitoring mode.</em></p></td></tr></tbody></table>



Analyzing a large number of TADM curves in an efficient way can be achieved by using the functions available in the “Filter TADM curves” toolbar:

* choose between curves obtained during either recording mode, monitoring mode or both.&#x20;
* choose between processed, aborted, or all curves obtained.
* choose whether curves from all channels or just a specific channel should be displayed.

Obviously, it makes sense to combine these options to limit the number of curves that have to be analyzed – for example: display all curves that were aborted (in monitoring mode) using channel number 5.

## **Menu details**

Below is an overview of all available menus with their options and the corresponding toolbar icons:

Below is an overview of all available menus with their options and the corresponding toolbar icons:

\


| File                                          | Description                                                                                                                                          |
| --------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------- |
| <p><br></p><p>Close &#x26; Apply Changes</p>  | Changes made to the tolerance band (upper and lower limit curves) will be saved and the Tolerance Band Editor will be closed.                        |
| <p><br></p><p>Close &#x26; Cancel Changes</p> | Tolerance band changes will be ignored and the Tolerance Band Editor will be closed. If any changes were made, a cue appears to discard all changes. |

| Edit                                                                                                                                                                                                                                                                                    | Description                                                                                                                                  |
| --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------- |
| <p>Cut Ctrl+X</p><p>Copy Ctrl+C</p><p>Paste Ctrl+V</p><p>Delete Del</p>                                                                                                                                                                                                                 | These options apply to individual tolerance band points, and are only active when either the “Upper curve” or “Lower curve” tab is selected. |
| <p><img src="../../.gitbook/assets/image (37) (1) (1) (1) (1).png" alt="" data-size="original"></p><p>Select</p>                                                                                                                                                                        | When activated, tolerance band points or TADM curves are selectable by clicking on them in the plotting area                                 |
| <p><img src="../../.gitbook/assets/image (38) (1) (1) (1) (1).png" alt="" data-size="original"></p><p>Add Upper Limit Curve Points</p><p><br></p><p><img src="../../.gitbook/assets/image (39) (1) (1) (1) (1).png" alt="" data-size="original"></p><p>Add Lower Limit Curve Points</p> | When activated, clicking in the plotting area adds an upper/lower tolerance band point                                                       |
| <p><img src="../../.gitbook/assets/image (40) (1) (1) (1) (1).png" alt="" data-size="original"></p><p>Delete Limit Curve Points</p>                                                                                                                                                     | When this is activated, clicking on a tolerance band point deletes it                                                                        |
| Delete Limit Curve Point Del                                                                                                                                                                                                                                                            | Deletes a single selected tolerance band point                                                                                               |
| Exclude TADM Curve Ctrl+E                                                                                                                                                                                                                                                               | A selected TADM curve will be excluded (not shown, and not used for guidance curves).                                                        |

| View                                                                                                                                                                                                                                                                                                                                                                                                   | Description                                        |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | -------------------------------------------------- |
| Hand Tool Ctrl+H ![](<../../.gitbook/assets/image (41) (1) (1) (1) (1).png>)                                                                                                                                                                                                                                                                                                                           | Move plotting area.                                |
| <p>Zoom In Tool Ctrl+Shift+I <img src="../../.gitbook/assets/image (42) (1) (1) (1) (1).png" alt=""></p><p>Zoom Out Tool Ctrl+Shift+O <img src="../../.gitbook/assets/image (44) (1) (1) (1) (1).png" alt=""> Zoom In Ctrl+I <img src="../../.gitbook/assets/image (46) (1) (1) (1) (1).png" alt=""></p><p>Zoom Out Ctrl+O <img src="../../.gitbook/assets/image (45) (1) (1) (1) (1).png" alt=""></p> | Zoom into or out of plotting area as desired.      |
| Fit To Window Ctrl+F ![](<../../.gitbook/assets/image (47) (1) (1) (1) (1).png>)                                                                                                                                                                                                                                                                                                                       | Fit all curves to window.                          |
| Guidance Curves                                                                                                                                                                                                                                                                                                                                                                                        | Display guidance curves.                           |
| Excluded TADM Curves                                                                                                                                                                                                                                                                                                                                                                                   | Display excluded TADM curves as dashed lines.      |
| <p><img src="../../.gitbook/assets/image (48) (1) (1) (1) (1).png" alt="" data-size="original"></p><p>TADM Curves...</p>                                                                                                                                                                                                                                                                               | Add or remove TADM curves.                         |
| Guidance Curves Formula...                                                                                                                                                                                                                                                                                                                                                                             | Edit guidance curve parameters.                    |
| <p><img src="../../.gitbook/assets/image (49) (1) (1) (1) (1).png" alt="" data-size="original"></p><p>Line Size</p>                                                                                                                                                                                                                                                                                    | Change size of selected, guidance and limit curves |
| Refresh F5                                                                                                                                                                                                                                                                                                                                                                                             | Refresh plotting area.                             |

Click "Help" in the dialog box of menu item "Guidance Curves Formula..." for the formula behind the guidance curves.

| Window                                                           |                                                       |
| ---------------------------------------------------------------- | ----------------------------------------------------- |
| <p>Upper Limit Curves Ctrl+U</p><p>Lower Limit Curves Ctrl+L</p> | Display upper or lower limit curve points as desired. |
| TADM Curve Properties Ctrl+T                                     | Display TADM curve properties on left side of window. |

| Help        | Description           |
| ----------- | --------------------- |
| Help Topics | View the online help. |

