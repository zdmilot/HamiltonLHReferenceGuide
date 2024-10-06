# Liquid Class Validation

![](https://theautomatedlab.com/assets/images/content/flowchart-lc-development.png)

This is part three in a series on liquid classes. View previous articles information on [liquid class principals](https://theautomatedlab.com/article.html?content=liquid-classes) and [liquid class development](https://theautomatedlab.com/article.html?content=liquid-classes-2).

#### Liquid Class Testing Techniques

Objective measurement techniques are critical for elevating your liquid handler's performance. To gather comprehensive data on how well your liquid class is performing, it’s beneficial to perform gravimetric and volumetric checks on each aspiration-dispense step:

**Gravimetric Testing**

1. Start by performing a simple, weight-based measurement. This involves measuring the weight of a plate before and after a dispense in order to determine how much liquid was added to the plate.
2. Back-calculate the liquid volume using liquid density and the measured weight of the plate after dispense to assess the accuracy of your liquid class.
3. The main limitation of gravimetric testing is that it provides only one data point per plate. This can help you determine the average dispense accuracy across an entire plate, but cannot tell you about the quality of any particular dispense.

The [Hamilton LVK](https://www.hamiltoncompany.com/automated-liquid-handling/small-devices/liquid-verification-kit) is a useful tool for performing gravimetric testing of liquid classes on Hamilton liquid handlers.

Advantages: The Hamilton LVK addresses the limitation of gravimetric testing by allowing you to test each individual dispense, providing more granular data. The GUI also allows you to make changes to liquid class parameters easily.

Disadvantages: Setting up the LVK to mimic real assay conditions can take significant time and effort, and comes at an add-on cost. Moreover, it may not be compatible with certain labware, which can limit its use in some setups.

&#x20;_To find out more about this tool, ask our Hamilton chatbot_ [_Vivo_](https://www.notion.so/4c9c81125f9a4bf099b46eb33755355b?pvs=25)_!_

**Volumetric Testing**

1. After performing a gravimetric measurement, spot-check a few wells with a manual pipette. Set the pipette to the target volume to aspirate all the liquid from a well. If there is excess liquid remaining in the well, then the liquid handler is dispensing larger volumes than expected; an air gap at the bottom of the manual pipette tip suggests under-dispensing.
2. You can measure the true dispense volume by setting the pipette volume 5-10uL higher than the target and then slowly lowering the pipette volume until the air gap is eliminated. By comparing the true volume to the expected volume, you can determine the volume error percentage and whether it seems acceptable. See diagram below. NOTE: This can be quite difficult (and inaccurate) for volatile or sticky liquids.
3. Pay close attention to trends in volume differences across the plate, such as increasing volume in each column if the same tips are reused across a plate. This helps identify potential issues like carryover or tip performance variability.

![A simple technique for measuring the dispense volume of a particular well. Use a properly calibrated pipette set to a volume slightly above the expected volume (105uL for a target of 100uL). Aspirate all contents from within a well, being careful to avoid bubbles or droplets within the pipette tip. Slowly lower the pipette volume until there is no air at the bottom of the tip. The number on the pipette is the true dispense volume.](https://theautomatedlab.com/assets/images/content/flowchart-volumetric-test.png)

Conduct these checks using the actual labware from your assays. Perform multiple replicates for each volume to ensure statistical validity. If you notice any deviations, adjust parameters like aspiration speed, dispense speed, or blow-out settings, and repeat the process until you achieve the desired performance. Optimize the liquid class correction curve to further fine-tune dispenses across a volume range.

**Perform Dye-Based Absorbance Testing**

![A dye gradient can be used to measure volume accuracy across a range of dispense volumes.](https://theautomatedlab.com/assets/images/content/flat-bottom-gradient.png)

Once your liquid class passes both the gravimetric and volumetric checks, it’s time to move to dye-based absorbance testing for further validation, especially for sub-10uL transfers.

You can set up a dye test using something as simple as food dye, but tools like the [Artel MVS (Multichannel Verification System)](https://www.aicompanies.com/artel-liquid-handling/mvs-multichannel-verification-system/) are optimized for this function. The Artel MVS is system is robust, traceable, and can be used for volume verification for most liquid handlers and pipettes. You can use the Artel MVS to measure the absorbance of a dye solution dispensed into microplates, allowing you to assess accuracy and precision across multiple pipetting channels simultaneously. However, the Artel MVS has a volume range limitation 0.1uL to 350uL.

1. Using the liquid handler and the liquid class you tested, dispense a known volume of a dye solution (such as a standard dye solution compatible with Artel MVS) into each well and measure the absorbance. By comparing the expected concentration with the measured concentration, you can confirm the liquid handler’s performance.
2. Optimize the liquid class further if the dye tests don’t meet the required performance specifications.

This method allows for high-throughput validation and gives you confidence that your liquid handler is performing correctly, even for low-volume transfers.

**Assess Cross-Contamination Using Fluorescein or Dye**

![A checkerboard plate pattern uses alternating positive and negative controls to test for contamination.](https://theautomatedlab.com/assets/images/content/flat-bottom-checkerboard.png)

When working in applications where cross-contamination is a significant concern—like PCR or qPCR—checking for carryover is critical. A safe and effective way to do this is by using fluorescein, a fluorescent dye that makes it easy to detect even minimal contamination.

To set up a comprehensive cross-contamination test:

1. Prepare a fluorescein solution and perform a checkerboard pattern of dispenses on a microplate. Each well with dye should be surrounded by four wells on each side that are blank.
2. After dispensing, measure the fluorescence in all wells using a fluorescence plate reader. Any detectable fluorescence in wells that should be blank indicates cross-contamination.

This method is highly sensitive and will help you identify contamination issues quickly.

Alternatively, you can use highly concentrated dye to identify potential cross-contamination, and even quantify it using a plate reader.

#### Perform a Reagent Test

Once your liquid class has been tested in isolation, it’s time to see how it performs under real-world assay conditions. Set up a test run using your full assay protocols and observe the overall liquid handling performance. This step ensures that your liquid class is not only theoretically sound but also practically effective. For example, you may not encounter any issues with evaporation during liquid class development, but may see it within the time parameters of your assay run.

#### Document the Development Process for Future Reference

Document the development process, including all test results, parameter settings, and any adjustments made. This serves as a valuable reference for future liquid class development or troubleshooting.

#### Re-Test Periodically

Re-validation is recommended to account for changes in labware, equipment wear and tear, or variations in liquid properties (such as different lots or formulations). If you notice a negative trend in assay controls, re-testing your liquid classes could be helpful.

#### Considerations for Different Validation Needs

It’s important to note that the level of validation needed depends on the application. In some scenarios, approximate pipetted volumes are acceptable, and a thorough validation process may not be necessary. For example, steps such as bead washes or bulk fills in assays often tolerate some variability in pipetting volumes. In these cases, a less stringent validation process may be sufficient, and saves time and money.

#### Don’t Be Afraid!

Testing and validating a liquid class might seem daunting, but it’s crucial to generating reliable, reproducible, and accurate data from automated workflows. With gravimetric, volumetric, and dye-based testing techniques you can develop robust liquid classes that bring your automated lab to the next level. So, take the time to test thoroughly—you’ll save yourself a lot of headaches in the long run!



***

Source: [https://theautomatedlab.com/article.html?content=category-basics](https://theautomatedlab.com/article.html?content=category-basics)
