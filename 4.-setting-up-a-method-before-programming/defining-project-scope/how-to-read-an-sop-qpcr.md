---
description: Madeline Wolf
---

# How To Read An SOP: qPCR

An email arrives in your inbox from your favorite colleague in your lab. Subject line: Can we automate this? 🙏

The email is empty except for a single attachment. It’s a link to your lab’s preferred [qPCR SOP](https://github.com/RobertsLab/resources/blob/master/protocols/qpcr.md). No context provided. Terrible communication skills, but hey—they’re still you’re favorite colleague.

Let’s take a look at that SOP!

A _standard operating procedure_ is a document of step-by-step instructions for executing a workflow within a certain context. Lots of detailed language that may or may not mean much to you, but it’s your job to get a sense for whether this process can be automated, and what risks or tradeoffs will need to be discussed.

We can start at the top with the reagents to get a sense for any highly sensitive materials we’ll have to be mindful of.

qPCR Standard Operating Protocol (SOP)1

**Reagents:**

* SsoFast EvaGreen Supermix ([BioRad: 172-5203](https://github.com/sr320/LabDocs/blob/master/protocols/Commercial\_Protocols/BioRad\_Sso\_Fast\_EvaGreen\_Supermix.pdf))
* Primer working stocks (10uM)
* DNase-free H2O (NanoPure H2O)

#### Reagents

I’m seeing a proprietary reagent, primers, and water. Water is a great thing to see—it’s relatively cheap, stable at room temperature, and very easy to work with from a liquid handling standpoint.

Primers are more sensitive. They are a solution of short, single-stranded DNA strands (ssDNA). ssDNA is less stable than double-stranded DNA (dsDNA), but the short fragment length of primers makes them less fragile. Stock solutions should probably be stored in the -20°C freezer and keep working aliquots in the 4°C fridge to avoid freeze-thaw damage to the primers.

Let’s look at the manufacturer’s documentation for this proprietary reagent.

SsoFast EvaGreen Supermix2

**Storage and Stability**

SsoFast EvaGreen supermix is stable for 12 months when stored in a constant temperature freezer at -20°C, protected from light. For convenience, it may be stored at 2-8°C for up to 6 months. Repeated freezing and thawing of the supermix is not recommended.

**Kit Contents**

SsoFast EvaGreen supermix is a 2x concentrated, ready-to-use reaction cocktail containing all components, except primers and template, for real-time quantitative PCR(qPCR). The mixture has been optimized to deliver maximum PCR efficiency, sensitivity, and robust fluorescent signal using fast or conventional cycling protocols for dye-based detection in qPCR. Highly specific amplification is crucial for successful qPCR, since EvaGreen dye binds to and detects any dsDNA generated during amplification. The antibody-mediated hot-start feature employed by the Sso7d-fusion polymerase sequesters enzymatic activity prior to the initial PCR denaturation step. Upon heat activation, the antibodies denature irreversibly, releasing the fully active DNA polymerase. This enables specific and efficient primer extension with the convenience of room temperature reaction assembly.

Looks like this is a handy dandy pre-made mixture of all of the other ingredients we need to make qPCR work. It contains enzymes, which tells me we need to be mindful of temperature stability. It also contains a dye, which means I need to check for whether this reagent is degraded by light exposure. I’m not seeing anything about light sensitivity in the manufacturer’s documentation, but we should double check with the operator.

Finally, I see that the enzymes in this mixture are heat-activated. Enzymes are protein catalysts for chemical reactions. Chemical reactions are generally inhibited at colder temperatures, but at room temperature the reaction may trickle along, chewing up samples and messing up the reagent ratios. That means we need to be considerate of minimizing the time between addition of enzymes to a sample and running the qPCR method.

This particular polymerase enzyme needs to be heat-activated; it won’t work properly until the reagent has been heated as part of the qPCR method. This gives us more flexibility, but we still want to avoid long wait times in the middle of this process.

qPCR Standard Operating Protocol (SOP)1

**Personal Protective Equipment (PPE):**

* Gloves

**Equipment:**

* Pipettes (10 - 1000uL)
* Filtered pipette tips
* White PCR plates, non-skirted, low profile ([USA Scientific: 1402-9590](http://www.usascientific.com/non-skirted-96-well-PCR-plate-low-profile-white.aspx))
* Optically clear strip caps ([USA Scientific: 1400-3800](http://www.usascientific.com/8-capstrip-0.2ml-tubes-flat-top.aspx))
* Sterile 1.7mL snap-cap microfuge tubes ([Genesee: 22-281S](https://geneseesci.com/shop-online/product-details/?product=22-281S))
* Real-time PCR machine
* ice

#### Equipment

Glancing at the equipment (and consumables) list, it looks like this process is mostly going to involve simple liquid transfers and a qPCR method. A centrifuge isn’t listed here, but I suspect there will be a spin-down step prior to the qPCR method. A spin-down is a quick, low intensity centrifugation step that ensures that any lingering droplets have been pulled down to the bottom of the well. This habit is so routine in the lab that it often gets left off instructions. I generally assume a spin-down step should come after each liquid handling script, but we can confirm with the operators if it isn’t specified in the SOP.

#### Labware

I’m also seeing some non-ideal labware. The “White PCR plate” is [SBS-format](https://www.slas.org/SLAS/assets/File/public/standards/ANSI\_SLAS\_4-2004\_WellPositions.pdf) , but does not have a skirt. That means we will need an adaptor to ensure that the plate can be seated on a liquid handler deck or handled by a robot.

Ideally, we would use automation-friendly skirted plates, but that type of infrastructural decision will depend on the goals and resources of this lab. Are we planning to scale up and operationalize this workflow? Or just trying to make this process a little easier on the rare occasions that it is needed? Automation demands infrastructural consideration, but ultimately you’ll have to work within your lab’s priorities and limitations.

We also need to consider the compatibility of this plate type with the qPCR machine we plan to use. It looks like the qPCR input plate needs white wells and an optically-clear cap or seal. Let’s make sure we confirm that with the operators before we get to process validation—the wrong labware type could mess up our data.

I’m also seeing snap-cap microfuge tubes. I suspect this will be for mastermix preparation, in which case it shouldn’t be a big deal if we need to change this to a different type of labware.

qPCR Standard Operating Protocol (SOP)1

**Procedure**

Total Time: \~ 2.0 - 4.0hrs

Cost/sample: \~ $0.42

1. Read the [manufacturer's protocol.](https://github.com/sr320/LabDocs/blob/master/protocols/Commercial\_Protocols/BioRad\_Sso\_Fast\_EvaGreen\_Supermix.pdf)
2. Read _this_ protocol.
3. Verify sufficient quantities of reagents and samples before beginning.
4. Wear clean gloves.
5. Prepare master mix. Be sure to make a master mix volume that will accommodate the following: all of your samples, two water (i.e. no template controls; NTC) samples, plus an extra 10% to accommodate pipetting errors. A single reaction is shown below:

| Component                    | Volume (uL) | Final Concentration                                          |
| ---------------------------- | ----------- | ------------------------------------------------------------ |
| 2x SsoFast EvaGreen Supermix | 10          | 1x                                                           |
| Reverse Primer (10uM)        | 0.5uL       | 0.2uM                                                        |
| Reverse Primer (10uM)        | 0.5uL       | 0.2uM                                                        |
| Water                        | Variable    | Use to bring reaction volume up to 20uL (including template) |

#### Procedure

Here we have some key information about what needs to end up in each well. Note that there are a couple variables left up to the operator, specifically the volume of sample and water that will go into the solution.

This tells me that I need to talk to the operator to understand their needs for this workflow. Is it always used the same way with the same sample volumes? Or do these volumes change from run to run? In fact, do these volumes change from sample to sample? Would the operator prefer the flexibility to change any or all of these volumes for each sample in a plate?

qPCR Standard Operating Protocol (SOP)1

6. Distribute appropriate amount of master mix (volume of master mix + template = 20uL) to white PCR plate.
7. Add template.
8. Cap with optical PCR caps.

Mastermix and sample are added to a new PCR plate, which then needs to be sealed with an optical cap or seal. Caps can be a bit of a pain in an automation context, so I would advocate for automated plate sealing if we’re aiming for an end-to-end solution.

qPCR Standard Operating Protocol (SOP)1

9. Spin plate for 1min @ 3000g.

See, what did I tell you about the spin-down steps!

qPCR Standard Operating Protocol (SOP)1

10. Put plate in real-time PCR machine.
11. Recommended cycling parameters (40 cycles) are listed below. They may need to be changed to accommodate your specific primers/samples. See manufacturer's protocol for recommendations.

    Step 1 - 98C 2mins \
    Step 2 - 98C 5secs \
    Step 3 - 60C 5secs\
    Step 4 - Plate read \
    Step 5 - Got to Step 2 39 more times\
    Step 6 - Melt curve 65C - 95C, increment 0.5C, wait 2secs, plate read.

And then all we have to do is get the sealed plate into a qPCR machine and execute the correct qPCR method. Seems easy enough! Let me jot down my understanding of the process so far.

![Flowchart diagram illustrating the functional steps in this SOP. Start with the mastermix recipe and addition of mastermix to the qPCR plate. Next the sample is added to the qPCR plate. The plate is then sealed with optical tape, spun down in a centrifuge, and processed on a qPCR machine.](https://theautomatedlab.com/assets/images/content/sop-qpcr.png)

#### Approach

The answer to our colleague’s question is yes, we could automate this. The real question to follow up on is what prompted the automation request and how can we resolve the root cause.

The pipetting steps in this workflow are quick and uncomplicated. If our colleague only needs to process one 96-well plate per day, automation probably won’t be faster than the current manual workflow. However, it could still improve process quality or help streamline this workflow within a broader context.

Since this process is amenable to a few automation approaches, let’s sketch out some options that we can present to our colleague for consideration. Once we communicate some of the possibilities and tradeoffs, we can start to have a real conversation about next steps.

**Semi-Automated**

Most of the work in this process is liquid handling, so the MVP (minimum viable product) is to move the pipetting steps onto a liquid handler and keep the remaining steps manual. Assuming we already have a liquid handler on site, this approach is cheap and easy to implement.

We could consider using a multi-dispenser to dispense mastermix into each well of a plate. If we can find a multi-dispenser with an appropriate degree of precision and repeatability, we could use it to prepare qPCR plates with mastermix, then use a liquid handler or multi-channel pipette to transfer template into the qPCR plate. Of course, when a user has to context-switch between multiple automation devices, we risk over-complicating the workflow.

We should also consider the number of qPCR devices available to us. If we prepare 8 qPCR input plates in bulk, but can only run one at a time, we can expect performance to decrease as our plates sit at room temperature. This appears to be an exceptionally fast qPCR method, taking roughly 10 minutes of processing time per plate. This gives us a little more flexibility with timing, but we probably don’t want enzymes mingling with samples for more than 30 minutes, even with the hot-start polymerase.

**Fully Automated**

This process is a suitable candidate for end-to-end automation. After we figure out the liquid handling strategy, the remaining steps are straightforwardly automation-friendly: ambient or cold storage, plate transport, plate sealing and peeling, centrifugation, and an automation-friendly qPCR machine. There are plenty of details to work out, but it’s not worth figuring out until we talk to our colleague about their process improvement goals and what resources are available for this project.

#### What's Next?

That's a lot of information on a quick pass of the SOP! But, there's plenty more to unpack. In[Part 2](https://theautomatedlab.com/article.html?content=sop-qpcr-2) we'll follow up with our colleage and start focusing in on the key process decisions that need to be made.

#### Acknowledgements

Thank you to University of Washington’s [Roberts Lab](https://faculty.washington.edu/sr320/) for sharing your [open source lab handbook](https://robertslab.github.io/resources/) and making this SOP available for analysis. We’re grateful for your commitment to open knowledge sharing.

1White, Sam. “qPCR Standard Operating Protocol (SOP).” _GitHub_, Roberts Lab, University of Washington, 3 Nov. 2020, github.com/RobertsLab/resources/blob/master/protocols/qpcr.md.

2 Bio-Rad Laboratories, Inc. “SsoFast EvaGreen Supermix” GitHub, Roberts Lab, University of Washington, 17 Jun. 2017, github.com/sr320/LabDocs/blob/master/protocols/Commercial\_Protocols/BioRad\_Sso\_Fast\_EvaGreen\_Supermix.pdf.\
\
Last we left off, our colleague had sent us an SOP document for a qPCR workflow, asking whether we thought it was automatable. We gave it a first pass and determined that yes, there are a few ways we could automate this process. You can read this initial assessment in detail in [Part 1.](https://theautomatedlab.com/article.html?content=sop-qpcr-1)

Let’s have a chat with our colleague and see if we can triage their needs, and establish some goals and requirements if we plan to move forward with an automation project.

#### Stakeholder Triage

When we talk to our colleague, we need to make sure we ask about the problem behind our colleague’s request as well as the constraints on the solution. We’re ultimately looking fora _reasonable solution_ to the _right problem_.

Let’s have a chat with our colleague.

**“Why do you want this process automated?”**

“It’s a huge pain to run. We have to consolidate samples from a few different plates, and there’s always one or two batches that arrive late. It’s a tricky process and it almost never gets started before 5pm, so someone ends up staying late.”

**“Why does the process feel tricky?”**

“Consolidating samples from multiple plates means triple-checking that each sample is pipetted into the right place. And batches aren’t always in even sets of 8, so it’s surprisingly easy to mess up, especially at the end of the day.”

**“What labware do you use for this process?”**

“Samples are received in either strip tubes or 96-well deepwell plates. We use 5 mL microtubes for the mastermix and run qPCR on 96-well white PCR plates.”

**“Would you be open to changing the input labware?”**

“Probably yes, but I’ll have to check with the team to confirm. Can I ask why? It’ll be annoying to change our process without a good reason.”

**“Understandable! Not all labware is equally automation-friendly, so there’s a chance that the best solution will require different inputs.”**

“Okay, let’s talk about it more if it becomes an issue.”

**“Why do you need to stay late to run qPCR? Can you wait until the next day?”**

“If we wait until the next day, we throw off the whole schedule for the week. The workflow after qPCR takes a full 8 hours to run because of some long incubation steps, so even if we run qPCR first thing in the morning someone will end up working late.”

**“Why do samples come in at different times if they all need to be processed together?”**

“We receive samples from multiple teams for different projects, but we prefer to batch our work in order to save on reagents and time. Of course, we can’t delay forever because everyone has deadlines to meet.”

**“It sounds like sample consolidation is the biggest pain point in your current workflow. Would you agree that we should prioritize improving this step? Or are there other paint points we should address?”**

“I think you’re right about focusing on sample consolidation.”

**“Is there a particular timeline you’re hoping we can meet? And are you expecting to purchase new equipment for this process?”**

“We’re expecting an uptick in requests next month, so if it’s possible to have a solution before then that would be appreciated. We don’t have any budget for new equipment at the moment.”

From this quick conversation, we have learned that our colleague is looking for a solution that doesn’t require purchasing new equipment.

We’ve also learned more about the context around qPCR that makes it a pain point for our colleague. qPCR itself isn’t capacity constrained, but it has become a bottleneck because of it’s relationship to the processes that come before and after.

In fact, there is one particular step in preparation for qPCR that is causing our colleague the most trouble: sample consolidation. It’s important that we prioritize this step when we propose a solution.

#### Equipment Inventory

* 1 [liquid handler](https://theautomatedlab.com/article.html?content=liquid-handling-basics) with a 96-well stamping head, an independent 8-channel head, and 16 deck positions
* 1 [liquid handler](https://theautomatedlab.com/article.html?content=liquid-handling-basics) with a 96-well stamping head and 9 deck positions
* 1 [acoustic liquid handler](https://theautomatedlab.com/article.html?content=liquid-handling-basics)
* 1 multi-dispenser
* 1 automated plate sealer with foil seals
* 1 automation-friendly centrifuge
* 2 automation-friendly thermal cyclers
* 1 [SCARA robot arm](https://theautomatedlab.com/article.html?content=lab-robots) (broken)
* 1 qPCR machine (not automation friendly)

That’s a lot to work with—surely we can come up with a high-impact, low-cost solution for our colleague. Let’s take some time to put together a proposal and discuss in the next edition of [How to Read an SOP](https://theautomatedlab.com/article.html?content=category-how-to-read-an-sop).
