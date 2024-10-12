# Error Monitoring

Error monitoring in liquid handling systems refers to the process of detecting and addressing errors or anomalies that may occur during automated liquid transfer operations, in contrast to other tasks like pipette calibration or liquid handling protocols.

{% embed url="https://www.hamiltoncompany.com/automated-liquid-handling/everything-you-need-to-know-about-liquid-handling/using-pressure-data-to-address-challenges-of-automated-pipetting" %}

![pressure data affecting automated pipetting accuracy](https://assets-robotics.hamiltoncompany.com/File-Uploads/\_thumbnail/pressure-data-detect-errors.jpg?v=1717444546)

When manual pipetting, a lab technician can see whether or not a pipetting action was successful. But with automated pipetting, there is no user to visually see when the tip is not in the solution, the tip is clogged, or air has been aspirated.\


To an extent, liquid handling instrument manufacturers can control for these situations by tightly mandating the condition of the inputs that a user loads into an instrument. But for many end-users, this places too many limitations on the application or adds too much manual labor.

That’s why next-generation automated liquid handling instruments use integrated pressure sensors inside pipetting channels to allow the instrument to “see” when pipetting actions are successful or not.

This page is part of Hamilton's [Automated Liquid Handling Guide](https://www.hamiltoncompany.com/automated-liquid-handling/everything-you-need-to-know-about-liquid-handling).

![](https://assets-robotics.hamiltoncompany.com/File-Uploads/\_thumbnail/pressure-sensor-01.png?v=1717452569)

### Where is the Pressure Being Monitored?

Hamilton pipetting channels leverage a pressure sensor in the head space between the liquid column and the piston. The pressure data collected can be analyzed and used to predict the success or failure of critical pipetting steps.

### Interpreting Typical Aspirate and Dispense Pressure Data

For a given liquid and a defined pipetting volume, the aspiration and dispense steps will follow a defined and repeatable profile. Once the “success” state is characterized, it is possible to identify deviations that represent pipetting errors.

![](https://assets-robotics.hamiltoncompany.com/File-Uploads/\_thumbnail/ZEUS-Graphs-02.png?v=1717452570)

#### Successful Aspiration Pressure Curve

An aspiration step begins with the pressure at atmospheric levels. As the piston retracts the pressure decreases and liquid is drawn into the pipette tip. When the piston completes its movement the pressure increases and settles at a point below the original atmospheric pressure. This pressure difference is the equilibrium required to retain the liquid in the pipette tip.

![](https://assets-robotics.hamiltoncompany.com/File-Uploads/\_thumbnail/ZEUS-Graphs-03.png?v=1717452576)

#### Successful Dispense Pressure Curve

A dispense step starts at the equilibrium pressure for holding the liquid in the pipette tip. As the piston begins to dispense the pressure increases to push the liquid from the tip. When the piston stops moving the pressure returns to atmospheric which is higher than the equilibrium pressure.

### What Pipetting Errors Can be Detected with Pressure Data?

If the pressure data for a characterized pipetting step deviates from the typical curve, it is a good indication that there was a pipetting error. Common pipetting errors that have been characterized include:

![](https://assets-robotics.hamiltoncompany.com/File-Uploads/\_thumbnail/ZEUS-Graphs-05.png?v=1717452577)

#### Clot Detection

Pressure data can be useful when pipetting solutions with dissolved solids or blood clots that run the risk of blocking the pipette tip. When a clog forms during aspiration the pressure curve will dip well below a typical aspiration. By setting an appropriate clot threshold this error state can be detected.

![](https://assets-robotics.hamiltoncompany.com/File-Uploads/\_thumbnail/ZEUS-Graphs-01.png?v=1717452578)

#### Insufficient Liquid Detection

Pressure data can be used to detect if a vessel runs out of liquid during aspiration. The pressure curve begins normal but when the liquid runs out the pressure curve returns to a pressure that is higher than expected for a successful aspiration. An empty tube threshold can be set to detect this error state.

![](https://assets-robotics.hamiltoncompany.com/File-Uploads/\_thumbnail/ZEUS-Graphs-04.png?v=1717452578)

#### Aspiration of Foam

When pipetting liquids that have a potential to foam, it can be difficult for the liquid level detection to identify the surface of the liquid. This can result in the aspiration of some foam instead of liquid. In this case, you will experience erratic noise in the pressure curve. A threshold can be set on the allowable rate of change to detect when foam has been aspirated.

### Recovering from a Pipetting Error

In many cases, an error during pipetting requires a restart of the pipetting sequence. However, on occasion a pipetting error is so consistent that a recovery strategy can be programmed directly into the pipette channel.

One such case is the accurate pipetting of volatile liquids. Due to some liquids’ high vapor pressure, the pressure in the channel after aspiration increases resulting in drips. Hamilton has leveraged this data to develop automated solutions to mitigating the effects of pipetting volatile liquids.
