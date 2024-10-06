---
description: Sudha Gollapudi
---

# Liquid Class Development

In the world of laboratory automation, the devil is in the details—especially when it comes to liquid handling. While we’ve covered the basics of [liquid class principles](https://theautomatedlab.com/article.html?content=liquid-classes), understanding these concepts is just the beginning. Applying that knowledge effectively to automated assay development requires a thoughtful and proactive approach to liquid class development.

Before incorporating a liquid class into a protocol, it’s essential to go through an iterative process of testing and optimization. This starts with understanding the unique physical properties of each liquid and translating them into specific pipetting behaviors for your liquid handler. By carefully adjusting parameters and testing your changes, you can refine a liquid class that minimizes pipetting variability and enhances assay accuracy.

Once the liquid class is optimized, it must then be validated using dye-based testing to confirm accuracy and precision, as well as cross-contamination tests.

Proper development and optimization are crucial steps to prevent issues before they arise in your protocols. However, even with careful preparation, challenges can still occur during biological sample testing. When you encounter inconsistencies or unexpected variability in your assay results, applying these testing principles could be useful for troubleshooting and identifying the root cause. Whether you’re addressing problems with dispensing accuracy, precision, or contamination, understanding how to test and validate a liquid class will help you achieve reliable, consistent performance in your automated workflows.

Let’s take a look at how we prepare for robust and reliable liquid class development.

![](https://theautomatedlab.com/assets/images/content/flowchart-lc-development.png)

#### Preparing for Liquid Class Development

Liquid classes translate the unique physical properties of a liquid (viscosity, surface tension, density) into mechanical pipetting behaviors (velocity, acceleration). It’s important to understand these material properties before fine-tuning your liquid handler’s liquid class settings.

**Develop a **_**Feel**_** for Liquid Behavior**

Use a manual pipette to pipette the liquid with multiple tip sizes and pipetting techniques. This hands-on approach gives you a sense of how the liquid behaves—whether it sticks to the pipette tip, how it responds when you pipette quickly or slowly, or if it tends to drip.

These observations will prepare you to optimize parameters like aspiration speed, dispense speed, blowout volume, or tip pre-wetting when you move to automated testing.

**Determine Liquid Density at Relevant Temperatures**

![A simplified chart of the liquid densities of water, glycerin, and ethanol by temperature.](https://theautomatedlab.com/assets/images/content/chart-density.png)

Before performing weight-based (gravimetric) testing, gather information about the liquid’s density at the temperature range at which the liquid will be handled. For example, if your reagent will be pipetted after being stored on-deck at 4°C, the liquid class should be developed and tested using reagents at that same temperature. Use this information to back-calculate the volume of liquid dispensed into your plate.

Understanding how temperature affects the liquid’s density ensures that your liquid class is tailored to the specific conditions of your assay. For example, many enzyme used for NGS library preparation contain a small quantity of glycerol to prevent freezing. These reagents need to be stored at 4°C before use and behave differently at room temperature.

**Create Your Liquid Class**

When defining your liquid class parameters, it’s most effective to start by copying a default liquid class that closely matches your liquid’s composition at the target volume range. Most liquid handling systems come with predefined liquid classes for common liquids like water, ethanol, or DMSO.

Start by selecting the default liquid class that is closest to your needs, perform a test dispense, and then make modifications based on your observations of the liquid’s behavior. This approach can save time and provide a good starting point for further optimization.

**Choose the Optimal Tips for Your Application**

Selecting the appropriate pipette tips for your application is critical for accurate liquid handling. Low-retention tips are great for viscous liquids, while filtered tips may be necessary for handling biological samples to prevent cross-contamination. Ensure that the tips are compatible with the specific liquid being dispensed.

**Mimic Real-World Conditions with the Right Labware**

When testing your liquid class, use the same labware (e.g. plates, tubes, reservoirs) that will be used in your automated assay. This ensures that the test conditions closely mimic the real-world scenario, which is necessary for accurate validation.

**Finalize Performance Criteria**

Determine the accuracy, precision, and %CV metrics that the liquid class needs to meet during the validation process. This should be shaped by the capabilities of the liquid handler as well as the sensitivity of the assay step.

Additionally, verify that your liquid handler is calibrated and maintained properly. Even the best liquid class won’t perform well on a poorly calibrated instrument.

#### Time to Test

Finally, it's time to test, adjust, and repeat. In the [next article](https://theautomatedlab.com/article.html?content=liquid-classes-2) we'll explore different techniques for qualitative and quantitative liquid class testing.

***

Source: [https://theautomatedlab.com/article.html?content=category-basics](https://theautomatedlab.com/article.html?content=category-basics)
