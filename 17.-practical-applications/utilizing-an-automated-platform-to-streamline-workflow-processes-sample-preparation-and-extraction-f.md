# Utilizing an Automated Platform to Streamline Workflow Processes: Sample Preparation and Extraction for Definitive Drug Testing on the Hamilton Microlab STAR

### Abstract

This work aims to provide a practical and broadly applicable, automated SPE strategy for the accurate and reproducible quantification of drugs of abuse and pain management drugs from urine samples in support of clinical research in forensic toxicology. A previously validated method was transferred to the Hamilton Microlab STAR which performed all sample pretreatment in addition to the full SPE procedure. These automation strategies simplify and streamline the sample preparation workflow, maximize productivity, and reduce risk of human error, while ensuring peak analytical performance.

#### Benefits

* Automation of repetitive tasks
* Reduces risk of manual error
* Robust and reproducible method for SPE
* Frees up scientist time to perform other tasks

### Introduction

Liquid chromatography coupled with mass spectrometry (LC-MS/MS) is now a common technique for rapid analysis of multiple compounds in a single acquisition. However, despite advances in instrumental analysis, sample preparation can be a rate limiting step and a source of errors in the overall bioanalysis workflow.1Driven by analytical sensitivity, selectivity, and robustness requirements for LC-MS/MS bioanalysis, the choice of sample preparation techniques commonly include simple dilution, protein precipitation (PPT), liquid-liquid extraction (LLE), supported liquid extraction (SLE), and solid-phase extraction (SPE). Development, optimization, and implementation of these methods, especially for larger analyte panels, can prove to be time consuming and difficult to transfer between scientists and laboratories. Employing fully automated devices such as the Hamilton Microlab STAR frees up the analyst to concentrate on other tasks by streamlining the sample preparation process. Perhaps more important is the possibility of reducing human errors such as mis-spikes, internal standard addition errors, inconsistencies in technique, and sample transfer errors.2-5 In turn this improves analytical method reproducibility and consistency.&#x20;

This work aims to provide a practical and broadly applicable, automated SPE strategy for the accurate and reproducible quantification of drugs of abuse and pain management drugs from urine samples in support of clinical research in forensic toxicology. A previously validated method was transferred to the Hamilton Microlab STAR which performed all sample pretreatment in addition to the full SPE procedure.6 These automation strategies simplify and streamline the sample preparation workflow, maximize productivity, and reduce risk of human error, while ensuring peak analytical performance.

### Experimental

All standards were obtained from Cerilliant (Round Rock, TX) and Cayman Chemical (Ann Arbor, MI). A mixed stock solution was prepared in methanol at concentrations of 2, 10, and 25 µg/mL, depending upon the analyte. Stable isotope labeled standards were used as internal standards (IS). The IS stock solution was prepared in methanol at a concentration of 1 µg/mL.6 Samples were prepared by diluting stock solutions into pooled, blank urine. &#x20;

#### Sample Extraction

All calibration standards and quality control samples were prepared manually in pooled blank urine prior to solid-phase extraction. The Hamilton Microlab STAR deck layout and accessories used for this extraction process are shown in Figure 1. The extraction process was also carried out manually to compare accuracy and precision across the four QC levels. For pretreatment, the STAR liquid handler adds 100 µL of IS in hydrolysis buffer followed by 100 µL of urine into individual wells of the Oasis MCX µElution Plate and aspirates to mix the samples. After incubation, the STAR adds 200 µL of 4% H3PO4 and aspirates to mix. The samples are loaded onto the sorbent bed under vacuum on the STAR deck and subsequently washed with 200 µL of 20% MeOH in H2O. The sorbent is dried under high vacuum. The samples are eluted with 2 x 25 µL of 50:50 ACN:MeOH containing 5% strong ammonia solution (28-30%). All samples are diluted with 150 µL of 97:2:1 H2O:ACN:formic acid and mixed on the heater-shaker for 3 minutes prior to removal for analysis on LC-MS/MS. A detailed visual of the workflow process can be seen in Figure 2. The entire automated SPE process explained in detail above comes as a readily available script that can be easily implemented to any Hamilton Microlab STAR or STARlet configuration.

![A representation of the layout for Hamilton Microlab STAR with accessories](https://www.waters.com/content/dam/waters/en/app-notes/2020/720006984/720006984en-f1.jpg.82.2048.resize/img.jpg)Figure 1. A representation of the layout for Hamilton Microlab STAR with accessories.![The workflow for the addition of internal standard, incubation, and entire SPE process](https://www.waters.com/content/dam/waters/en/app-notes/2020/720006984/720006984en-f2.jpg.82.2048.resize/img.jpg)Figure 2. The workflow for the addition of internal standard, incubation, and entire SPE process.

#### LC-MS/MS Conditions

| LC system:        | ACQUITY UPLC I-Class (FTN)                                                     |
| ----------------- | ------------------------------------------------------------------------------ |
| Detection:        | Xevo TQ-S micro ESI+                                                           |
| Column:           | ACQUITY UPLC BEH C18, 1.7 μm, 2.1 x 100 mm (p/n: 186002352)                    |
| Temp.:            | 40 °C                                                                          |
| Sample temp.:     | 10 °C                                                                          |
| Injection volume: | 5 µL                                                                           |
| Mobile phases:    | <p>A: 0.1% formic acid in water </p><p>B: 0.1% formic acid in acetonitrile</p> |
| Purge solvent:    | 50% methanol in H2O                                                            |
| Wash solvent:     | 25:25:25:25 MeOH:H2O:IPA:ACN                                                   |
|                   |                                                                                |

#### Gradient:

| Time (min) | Flow (mL/min)  | %MPA | %MPB |
| ---------- | -------------- | ---- | ---- |
| 0.00       | 0.6            | 98   | 2    |
| 3.33       | 0.6            | 33   | 67   |
| 3.50       | 0.6            | 10   | 90   |
| 3.60       | 0.6            | 98   | 2    |
| 4.00       | 0.6            | 98   | 2    |

#### MS Conditions

| Capillary:            | 1.0 kV    |
| --------------------- | --------- |
| Desolvation temp.:    | 500 °C    |
| Cone gas flow:        | 150 L/Hr  |
| Desolvation gas flow: | 1000 L/Hr |

The following parameters were optimized for specific compounds: Acquisition range, cone voltage, MRM transitions, and collision energy. These parameters can be found in Appendix 1 of Waters application note [720006187EN](https://www.waters.com/waters/library.htm?cid=511436\&lid=134965859).

#### Data Management

| Hamilton control software:    | Venus 3       |
| ----------------------------- | ------------- |
| Instrument control software:  | MassLynx v4.2 |
| Quantification software:      | TargetLynx    |

### Results and Discussion

#### Quantitative Analysis

Prior to quantitative analysis, an analyte recovery experiment was conducted for comparison on a manual platform against the Hamilton Microlab STAR to prove robustness of the validated method on an automated platform. The recovery results were comparable between the two platforms deeming the use of automation for sample extraction to be as effective as manual extraction.

Pooled urine samples were extracted in three batches on three different days. A seven-point calibration curve was extracted in duplicate and quality control samples at four different concentrations were extracted in replicates of six. For most compounds, quality control samples were prepared at 15, 75, 250, and 750 ng/mL, with compounds in the lower concentration range at 3, 15, 50, and 150 ng/mL, and compounds in the higher concentration range at 37.5, 187.5, 625, and 1875 ng/mL. The calibration ranges for each compound can be found in Table 1 of Waters application note [720006187EN](https://www.waters.com/waters/library.htm?cid=511436\&lid=134965859). The acceptance criteria for each individual calibrator was within ±15% of target values, except for the lowest point at 20%. Acceptance criteria for quality control samples was within 15% except for the lowest QC at 20%. These are in line with SWGTOX guidelines7 and FDA bioanalytical method validation requirements.8 A summary of inter-day results across the three batches can be seen in Appendix 1. All compounds met the criteria above and %RSDs for most compounds were less than 5%. A summary of intra-day results for batch #3 can be seen in Appendix 2. All compounds (except for 7-aminoclonazepam 117%, buprenorphine 131%, diazepam 116%) met criteria with %RSDs for most compounds less than 5%. All compounds had R2 values of greater than 0.99.

#### Comparative Analysis

All individual samples were extracted twice for every batch. One aliquot of each calibrator and quality control sample was processed using the Hamilton Microlab STAR, and one aliquot of each calibrator and quality control sample was processed manually. The purpose of this was to prove the reliability of the automated platform to perform an extraction that will give accuracy and precision within the expected range of acceptance criteria. The results for QC 2 across the three batches for manual versus automated sample preparation is shown in Figure 3. When comparing manual versus automated sample extraction, the results are comparable if not better for accuracy and %RSD for individual compounds on the STAR.&#x20;

![The comparison of accuracies and %error](https://www.waters.com/content/dam/waters/en/app-notes/2020/720006984/720006984en-f3.jpg.82.2048.resize/img.jpg)Figure 3. The comparison of accuracies and %error for QC2 between the manual and automated platform.

### Conclusion

To address the issue of the rate limiting step that is sample preparation, the use of the Hamilton Microlab STAR to automate the pretreatment and subsequent extraction process of a large panel of drugs of abuse and pain management drugs in urine proved most effective. The solution offers a simple and fast SPE process for a comprehensive panel of toxicological compounds. A ready-made script, in combination with a previously validated SPE and analytical method enables rapid implementation of the entire process. This fully automated sample preparation approach provides robust and reproducible quantitative performance with R2 values greater than 0.99, QC accuracies between 85-115% (80-120% for low QC) for all compounds, and %RSDs under 10% for most compounds. Analyst associated errors, such as analyst inconsistency, sample transfer, IS additions, and labelling errors, are effectively minimized. Accurate quantification was achieved using a simple yet robust fully automated sample preparation and SPE protocol.

### References

1. _Chapter 5 Automation Tools and Strategies for Bioanalysis_, in _Progress in Pharmaceutical and Biomedical Analysis_, David A. Wells, Editor 2003, _Elsevier_. p. 135-197.
2. Lehmann, S.; _et al_. Determination of 74 New Psychoactive Substances in Serum Using Automated In-line Solid-Phase Extraction-Liquid Chromatography-Tandem Mass Spectrometry_._ _J. Chromatogr. B._ 2017, _1064_, 124-138.
3. Wei, D.; _et al_. Online and Automated Sample Extraction. _Bioanalysis_ 2015, _7_ (17), 2227-2233.
4. Zheng, N.; Jiang, H.; Zeng, J. Current Advances and Strategies Towards Fully Automated Sample Preparation for Regulated LC–MS/MS Bioanalysis. _Bioanalysis_ 2014, _6_ (18), 2441-2459.
5. Ramírez Fernández, M.d.M.; _et al_., Validation of an Automated Solid-Phase Extraction Method for the Analysis of 23 Opioids, Cocaine, and Metabolites in Urine with Ultra-Performance Liquid Chromatography–Tandem Mass Spectrometry. _Journal of Analytical Toxicology_ 2014, _38_ (5), 280-288.
6. Danaceau, J. P.; Freeto, S. M.; Calton, L. J. A Comprehensive Method for the Analysis of Pain Management Drugs and Drugs of Abuse Incorporating Simplified, Rapid Mixed-Mode SPE with UPLC-MS/MS for Forensic Toxicology. Waters Application Note, [720006187EN](https://www.waters.com/waters/library.htm?cid=511436\&lid=134965859), 2019.
7. Scientific Working Group for Forensic Toxicology (SWGTOX) – Recommendations of the Research, Development, Testing, and Evaluation Committee._\*_ _Journal of Analytical Toxicology_ 2013, _37_ (3), 187-191.
8. Bansal, S.; DeStefano, A. Key Elements of Bioanalytical Method Validation for Small Molecules. _The_ _AAPS Journal_ 2007, _9_ (1), E109-E114.

#### Appendix 1

![Summary of inter-day results](https://www.waters.com/content/dam/waters/en/app-notes/2020/720006984/720006984en-t1.jpg.82.2048.resize/img.jpg)Summary of inter-day results providing mean accuracies for the four QC levels across all three batches.

#### Appendix 2

![Summary of intra-day results](https://www.waters.com/content/dam/waters/en/app-notes/2020/720006984/720006984en-t2.jpg.82.2048.resize/img.jpg)Summary of intra-day results providing mean accuracies across all four QC levels between the three batches.

### Featured Products

* [Xevo TQ-S micro Triple Quadrupole Mass Spectrometry](https://www.waters.com/134798856)
* [ACQUITY UPLC I-Class PLUS System](https://www.waters.com/134613317)
* [MassLynx MS Software](https://www.waters.com/513662)
* [TargetLynx](https://www.waters.com/513791)
