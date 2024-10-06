---
description: Madeline Wolf
---

# Liquid Class Principles

#### What is a liquid class?

Anyone tasked with moving small volumes of liquid from one place to another knows that a pipette is only as accurate as its operator’s technique. Fluid dynamics at the microliter scale impact the performance of every liquid transfer. Humans learn the nuances of pipetting technique by adjusting their fine motor movements to achieve accurate liquid transfers. Robots, however, must be provided with explicit pipetting instructions parametrized based on the physical properties of each liquid. We call this set of instructions a _liquid class_.

![](https://theautomatedlab.com/assets/images/content/poor-pipetting.png)

Just as poor pipetting technique can ruin an assay or damage a pipette, poorly optimized liquid classes can make or break automated pipetting by increasing process variability and reducing accuracy. Use of the wrong liquid class may create bubbles in your sample, droplets on your instrument deck, and can even flood or contaminate your liquid handler’s hardware, increasing process variability and reducing accuracy.

Read on for an explanation of the core liquid class concepts you’ll need to learn as you master the art of liquid class development.

#### Liquid Handling Mechanisms

[Liquid handling mechanisms](https://theautomatedlab.com/article.html?content=liquid-handling-basics) are surprisingly diverse! _Displacement pipetting liquid handlers_ tend to steal the show, but any device that aspirates or dispenses fluid implements liquid classes in some form.

_Acoustic liquid handlers_ like Beckman’s [Echo series](https://www.beckman.com/liquid-handlers/echo-650-series) use sound waves to drive droplets between plates for a no-contact liquid transfer. This mechanic offers a high degree of precision and automatic liquid type compensation, but is limited in its range of function and liquid type compatibility.

_Peristaltic pump-based dispensers_ use motor rotation to drive liquid from a single stock reservoir into the destination plate. Liquid class settings on peristaltic pump dispensers are generally limited to controlling dispense speed and acceleration, as well as dispense height.

| Dispense Mechanism         | Displacement Pipetting                                                  | Acoustic Transfer                                          | Peristaltic Pump                                |
| -------------------------- | ----------------------------------------------------------------------- | ---------------------------------------------------------- | ----------------------------------------------- |
| Dispense Considerations    | Wide range of functionality;  must be optimized for liquid and function | Highly accurate nL-scale transfers;  limited functionality | Bulk dispense only; limited degree of precision |
| Liquid Class Customization | Extensive                                                               | Limited                                                    | Limited                                         |

![](https://theautomatedlab.com/assets/images/content/air-gap-diagram.png)

#### Liquid Types

For the purpose of liquid handling, there are three essential _liquid types_: Water, Solvent, and Viscous.

“Water” can include any reagent that has a high water content, [strong cohesion](https://www.usgs.gov/special-topics/water-science-school/science/adhesion-and-cohesion-water), and low viscosity. This liquid type tends to have default or moderate liquid class settings, and tends to be easier to optimize.

“Solvent” includes organic solvents such as ethanol or DMSO, and are defined by their [volatility](https://www.chemicool.com/definition/volatile.html). Solvent liquid class properties may be similar to Water liquid classes in pipetting speed and acceleration, but may require small trailing air gaps and slow arm movements to prevent droplets from forming. It may also be necessary to reduce aspiration speed in order to prevent vapors from building up in the tip. Solvent volatilization pushes corrosive vapors into the liquid handling channels while pushing fluid out of the tips.

The “Viscous” liquid type is by far the most frustrating (vicious, even) to develop around. Highly viscous liquids require slow pipetting acceleration and deceleration, and demand tip-specific optimization. A clean viscous dispense from a 1000 uL tip may cause aspiration bubbles or flooding in a 50 uL tip. A slow dispense speed and leading air gap blowout can be used to minimize transfer loss, while a post-dispense air gap can be used to prevent droplets from forming on the way to tip ejection.

| Parameters       | Water      | Solvent  | Viscous       |               |
| ---------------- | ---------- | -------- | ------------- | ------------- |
| Aspiration       | Velocity   | Fast     | Fast/Moderate | Slow/Moderate |
| Acceleration     | Fast       | Moderate | Slow          |               |
| Deceleration     | Fast       | Fast     | Slow          |               |
| Delay            | Short      | Short    | Long          |               |
| Dispense         | Velocity   | Fast     | Fast          | Slow/Moderate |
| Acceleration     | Fast       | Fast     | Slow          |               |
| Deceleration     | Fast       | Fast     | Slow          |               |
| Delay            | Short      | Short    | Long          |               |
| Trailing Air Gap | None       | Small    | None          |               |
| Leading Air Gap  | None/Small | Small    | Moderate      |               |

![](https://theautomatedlab.com/assets/images/content/pipette-function.png)

#### Liquid Transfer Functions

The essential liquid transfer functions are the “wet” and “free” dispenses. In a wet dispense, the pipette tip makes contact with the liquid in the destination well during dispense.  With a free dispense, the dispensed liquid free-falls into the well.

Wet dispenses are ideal for improving dispense accuracy and minimizing transfer loss. A lower dispense velocity is used because the transfer is driven by liquid cohesion rather than pipetting force. This provides the additional benefit of reducing aerosol and bubble risk.

Free dispenses, or sterile dispense, can be essential for enabling multi-dispensing or repeat transfer from the same set of tips. Free dispenses require faster pipetting velocity and deceleration to drive liquid out of the pipette tip, and may benefit from a blowout of the leading air gap. For Water and Solvent liquid types, free dispense can be a good option for minimizing contamination risk or dispensing into dry plates. Free dispense of Viscous liquid types is inherently challenging, and will likely result in transfer loss, droplets, or bubbles.

| Parameters      | Wet Dispense                    | Free Dispense             |      |
| --------------- | ------------------------------- | ------------------------- | ---- |
| Dispense Height | Submerged, or on liquid surface | Maximum height of labware |      |
| Dispense        | Velocity                        | Moderate                  | Fast |
| Acceleration    | Moderate                        | Moderate                  |      |
| Deceleration    | Moderate                        | Fast                      |      |
| Leading Air Gap | None                            | Moderate                  |      |

There’s a secret third category of essential liquid handling functions: the pipette-mix. A mix liquid class aspirates and dispenses multiple times within a single well. This agitates the well’s contents in order to homogenize them.

Since transfer quality is less of a consideration for mix classes, they may be shared across multiple liquid types. Instead of optimizing for dispense accuracy, a mix class should be optimized based on the vigor of the mix in relation to the size of the tip.

#### When To Develop A Liquid Class

Many liquid handlers will provide a set of default liquid classes. These defaults _should_ be sufficient for transferring water-like reagents from point A to point B. If “Viscous” and “Solvent” liquid classes are provided, they should work with moderately viscous or moderately volatile liquids, respectively. Using existing liquid classes for new applications makes it easier to maintain an instrument and to support large instrument fleets.  However, some cases will require new liquid class development.

Dripping, bubbles, and inconsistent dispense volumes are some of the warning signs that a new liquid class might be needed. Before developing a new liquid class, consider whether the new liquid type has similar properties to other reagents you work with. Is it viscous, like glycerin or PEG?  Is it volatile and prone to dripping like ethanol?  Is it runny and cohesive like water?  If not, you will need to develop a new liquid class to support this new liquid type.

Perhaps your liquid transfer quality is excellent, but your process demands a specialized pipetting technique. Your script may require a tip-touch to draw lingering droplets into the well. Or, you may need to aspirate without disturbing pelleted cells. If the desired pipetting function + liquid type combination is not available in an existing liquid class, then it’s time to develop a new one.

#### How Instrument Software Influences Development

Each liquid handler’s control software exposes different liquid class parameters for liquid class optimization. Tecan’s _Fluent Control_ gives the developer command-level control over the pipetting mechanics of each liquid class and tip type. By contrast, Tecan’s _EVOWare_ exposes a subset of aspiration and dispense parameters grouped by volume range. The former enables a high degree of customization, while the latter is approachable and in many cases equally effective. When developing a new liquid class, consider the tools and level of detail that are available to you, and plan your development timeline accordingly.

#### Getting Started With Liquid Class Development

1. Consult your liquid handler’s user guide to find the specific liquid class features that come with your device and software suite.
2. Consider the liquid type and pipetting function you want to achieve, and how these guidelines translate into the numerical or categorical parameters available to you.
3. Don’t develop! If an existing liquid class can be used instead, you can stop here.
4. Create a new liquid class with a name that reflects a liquid type and functional purpose, and copy over the settings from a similar liquid class. Modify the settings incrementally.
5.  Apply settings, test on your liquid handler, and repeat. Before releasing a new liquid class, confirm that it works with all compatible liquid types across its intended volume range.

    _Editor’s note: more information on testing and volume verification techniques to come!_

***

Source: [https://theautomatedlab.com/article.html?content=liquid-classes](https://theautomatedlab.com/article.html?content=liquid-classes)
