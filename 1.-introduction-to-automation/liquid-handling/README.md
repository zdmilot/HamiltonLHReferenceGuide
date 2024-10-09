---
description: Madeline Wolf
---

# Liquid Handling

I often joke that the main function of life science companies is to move small volumes of liquid from one place to another. Add a reagent to a sample. Incubate or shake or spin down. Add another reagent and repeat.

Is that vastly oversimplifying the centuries of scientific achievement that made an arsenal of molecular biology techniques routine? Yes. But it is often the automation engineer’s job to generalize, so here we are.

Liquid Handlers are the robots designed to automate that transferring of liquid from one place to another. Each liquid handler model has its own strengths, weaknesses, and quirks, but the basic construction is this: a pipetting end effector attached to a [cartesian robot](https://theautomatedlab.com/article.html?content=lab-robots), all bolted to a deck that is designed to help the robot locate and interact with labware. The choices made in designing each of these elements define the capabilities of a liquid handler.

<figure><img src="../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" width="351"><figcaption></figcaption></figure>

#### Pipetting Heads

The end effector of a pipetting robot is often called a “head”. It’s often possible to configure a particular vendor’s liquid handler with different heads much like a scientist may choose between different multichannel pipettes. We generally see two categories of pipetting heads: “stamping” heads and independent channel heads.



**Stamping Heads**



![](https://theautomatedlab.com/assets/images/content/stamp-96.png)

“Stamping” head configurations generally match popular microplate formats: 96 or 384 channels aligned in SBS format for ultra-efficient execution of pipetting steps across an entire plate. Each channel on the head acts in tandem with the others—aspirating or dispensing the same volume at the same time, powered by a central mechanism.

Stamping heads get their name from their function: they act like a rubber stamp, picking up samples from one plate and putting them down in another, in the same layout. This is quite useful if a plate contains 96 unique patient samples that need to be kept in order. It’s also useful for moving stock reagents from a reservoir to another plate; each channel is carrying the same contents. They provide speed and throughput but reduce flexibility—a common tradeoff in the world of automation.





**Independent Channel Heads**

![](https://theautomatedlab.com/assets/images/content/independent-8.png)



To get flexibility, you need a head with independently operating channels. These are often configured with 8 channels in a line, like a traditional multi-channel pipette. The key feature is the ability of these channels to pipette different volumes, and for each channel to move independently along the z-axis. Each channel can be programmed to aspirate different volumes at different times. This enables variety in the volumes pipetted across a plate, but also enables re-arraying of samples.

Sample re-array is a mandatory feature for many lab processes. Perhaps you need to consolidate and normalize patient samples from multiple tubes into a single microplate at different volumes. Or, sample order needs to be randomized across a plate to control against plate-edge effects. Or perhaps you have to add indexed primers to particular samples based on any number of experiment requirements. Each of these requires the flexibility of a human holding a single-channel pipette, but can still be automated using independent channel heads.

The tradeoff here is flexibility over throughput; 96 or 384 transfers with an independent channel head can be quite slow. In fact, an experienced lab tech is almost certainly faster in a head-to-head race. However, don’t let that dissuade you from automating a process—the benefits of automation are more complex than the speed of any particular task.

**Hybrids and Other Specialty Heads**

Though the previous categories cover the majority of liquid handler options on the market, there is a growing collection of devices and device heads that break this mold. There are stamping heads that can [pipette different volume with each tip](https://dynamicdevices.com/technology/#volume-verified-pipetting-technology), as well as liquid handlers designed to [swap heads on the fly](https://www.tecan.com/fluent-automated-workstation#features-benefits) and a dozen other technologies and application-specific end effectors.

#### Liquid Handler Decks

The importance of a good liquid handler deck often goes unappreciated. The deck is both the physical grid to which labware can be aligned, and the virtual landscape that guides the behavior of the liquid handler.

![](https://theautomatedlab.com/assets/images/content/deck.png)

One of the biggest challenges in lab automation is the interface between human and robot work. It’s easy to tell a human what to do, knowing that they will intuitively understand how to set up their workspace and execute within it—or ask questions if critical information is missing from the instructions. It’s also straightforward to program a robot—it’ll do exactly what you tell it to do, for better and worse.

When an intuitively-driven human hands off work to a program-executing robot, there must be guardrails that ensure that the human leaves their outputs exactly where the robot expects its inputs.

With liquid handlers, errors are often caused by a lack of these guardrails: A rushed scientist places their destination plate in the wrong deck position, causing the liquid handler to dispense samples directly onto its deck. Or worse, the edge of a microplate catches the edge of a deck’s carrier, resulting in a millimeter of misalignment and the heartbreaking crunch of pipette tips against a microplate.

The liquid handler’s deck is this interaction point, and the invisible engineering behind it can set a team up for success or failure for years to come. The physical design of the deck positions or carriers can be designed for user-proof interaction. The liquid handler can also provide secondary checks through sensors, barcode scanning, or user checkpoints. These are not strictly necessary features, but your resident automation engineer should be aware of the risks associated with a particular user interaction point, and aim to mitigate them.

#### Alternative Liquid Handling Technologies

So far we’ve talked about the traditional liquid handler framework in which a cartesian robot maneuvers a pipetting head around the deck. However, there are a few other liquid handling technologies worth mentioning.

**Acoustic Liquid Handlers**

Acoustic liquid handling technology is true science fiction, made only more impressive by how well it works. Acoustic liquid handlers use targeted sound waves to launch nanoliter-scale droplets of liquid from the source plate directly into the destination plate, one well at a time. The use cases can be limited—particularly viscous or chunky samples can be incompatible with the technology, and the liquid transfer speed can become frustratingly slow once transfer volumes reach microliter scale. These devices also require specialty, acoustic-friendly (read: expensive) labware to function. Caveats aside, they are incredible devices when used appropriately—particularly in genomics and drug discovery labs.

**Multi-Dispensers**

Multi-dispensers or bulk dispensers aren’t typically considered liquid handlers, but they are worth acknowledging given their value in automated lab workflows. Rather than aspirating from a source plate and dispensing into a destination plate, multi-dispensers dispense directly from an on-instrument stock bottle. This is a fantastic way to fill plates or reservoirs with stock reagents. Depending on the mechanism and configuration of the particular multi-dispenser, almost any reagent can be hooked up as a stock solution. However, dispensing mechanisms tend to have high dead volumes, and care must be taken to protect temperature-sensitive or light-sensitive reagents while they sit out in a stock bottle.

**Plate Washers**

Plate washers overlap significantly with multi-dispensers, with some plate washers being multi-dispensers and vice versa. Plate washers are designed to add and remove any number of washing buffers or other reagents to samples in a microplate in order to clean the target material of contaminants. This type of work shows up across a broad range of applications, and so the specific configurations and features of each plate washer model can vary drastically. Plate washers generally have a mechanism for removing liquid from a plate as well as adding stock reagents to a plate.

***

Source: [https://theautomatedlab.com/article.html?content=liquid-handling-basics](https://theautomatedlab.com/article.html?content=liquid-handling-basics)
