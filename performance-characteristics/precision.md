# Precision

Precision in liquid handling refers to the reproducibility of volume delivery, indicating how closely repeated measurements of the same sample can be made.

{% embed url="https://formulatrix.com/life-science-automation-blog/liquid-handling-for-reproducible-science-post-1-basics-of-accuracy-and-precision/" %}

[**In an earlier post,**](https://formulatrix.com/life-science-automation-blog/a-hybrid-approach-to-liquid-handling/) we discussed that the technology employed by a given liquid handling platform greatly impacts the accuracy and precision of liquid transfer volumes over a given liquid class. In this series of reproducibility related blog posts, we will consider what accuracy and precision mean and how to go about measuring these specifications in a hypothetical use case.

**Volumetric Performance - Accuracy and Precision**

Assuming that the throughput and volume range of a liquid handling platform accommodate each of the liquid handling steps in an application workflow, accuracy and precision exist as the most critical specifications to evaluate when purchasing a system. These specifications will largely impact the reproducibility and trustworthiness of the analytical data generated in the lab!

In the context of liquid handling automation, accuracy can be estimated by calculating the systematic error, which is the difference of the mean of a series of transferred volumes and the target volume that the instrument has been programmed to transfer.

Systematic Error = (Delivered Volume - Target Volume) / Target Volume x 100%

Precision, on the other hand, can be estimated by calculating the random error, which is the standard deviation of a series of transfers under repeatability conditions. Random error is typically expressed as a coefficient of variation (CV), which can be calculated by dividing the standard deviation by the average dispensed volume and converting to a percentage. CVs are the most critical measure of a liquid handler’s volumetric performance, as random errors between transfers often lead to skewed concentration ratios and unknown sample concentrations that can be difficult to account for in analytical data.

Random Error = √ (∑ (Measured Volume - Mean Measured Volume)² / (Number of Replicate Deliveries in Run - 1))

Cv = (Random Error / Mean measured Volume) x 100%

**Measuring Volumetric Performance - Direct vs. Indirect**

Systematic and random error can be measured directly through gravimetric means or indirectly through comparisons of absorption or fluorescence.  Although gravimetric methods offer a direct measurement of a transferred volume, or series of transferred volumes, the amount of time that it takes to achieve a single reading can be time-prohibitive in a laboratory with many liquid handling platforms or complex processes.  Further, as transfer volumes decrease in the context of a given liquid handling workflow, the impact of evaporation on the measured volume can become substantial.  For this reason, transfer volumes under 5 µL cannot be reliably measured through gravimetric approaches.  [**In part 2 of this blog post series, we will look more specifically at the tradeoffs associated with measuring accuracy and precision directly vs. indirectly.**](https://formulatrix.com/life-science-automation-blog/liquid-handling-for-reproducible-science-post-2-setting-up-an-in-house-verification-system/)

**Interpreting Performance Specifications**

When comparing specifications between liquid handling platforms, it is critical to understand that each vendor may have different approaches to validating that an instrument performs to the published specification. Vendors can provide test plans and results that can elucidate the unknown nature of their specifications. [**See this example that outlines very specifically how the volumetric performance of the FORMULATRIX® MANTIS® Liquid Handler was assessed in collaboration with Artel.**](https://formulatrix.com/life-science-automation-blog/assessment-of-the-volumetric-performance-of-the-mantis-liquid-handler-using-the-artel-mvs-multichannel-verification-system/)

The following are some questions that you can ask in order to better understand the legitimacy of published specifications:

* Were delivered volumes measured gravimetrically, fluorescently, or through absorbance based methodologies?
* Were any compensations applied to the raw values provided by the scale, plate reader, or spectrophotometer?
* How many liquid handling instruments were tested, and how many channels on the pipetting module were tested?
* How were specifications averaged between channels and instruments?
* How many different sample types were tested, and if so, which instrumentation parameters were tuned for each sample type?
* Did any single measurements taken during validation fall outside of the published specification?

**When to Verify Volumetric Performance**

During product development, liquid handling manufacturers should extensively test the accuracy and precision of their liquid handling platform under many conditions in order to justify their published specifications.  Further, this information should be accessible to researcher's performing due diligence prior to a making a purchasing decision.

Following installation of a purchased instrument, assessment of volumetric performance is required both at a regular interval and also when developing new automated protocols for target applications. For the utmost reproducibility when working with an air-displacement system, researchers should assess volumetric performance of each target delivery volume for each liquid type gravimetrically or with liquid class specific absorbance readings prior to implementing a given process.

In air-displacement systems, gravimetric or liquid class specific absorbance methods are recommended due to the volumetric difference when transferring fluorescent dye compared to the samples and reagents utilized in the context of a true application.  This requirement can be quite time consuming and expensive, leading many researchers to realize the benefit of positive displacement technology, which performs consistently when transferring liquids of differing viscosities.  When using a positive displacement system, a fluorescent dye can much more reliably indicate the volumetric performance of the system in place of actual target liquids saving labs valuable time and resources.

If you need help translating liquid handling specifications into meaningful implications for your research and laboratory, our friendly Liquid Handling Consultants can help!  Since FORMULATRIX products only manage the reagent dispensing portion of your workflow, we can help you to understand the best solution for your specific application by providing an unbiased take on the traditional sample transfer instruments available in the market.
