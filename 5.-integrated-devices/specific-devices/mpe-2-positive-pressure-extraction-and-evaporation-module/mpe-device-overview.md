# \[MPE]² Device Overview

## Control Box

The Control Box connects the \[MPE]² to the power supply and controlling computer. It also connects to the liquid waste and to the laboratory air supply to operate a pump via a Filter/Regulator Unit.

<figure><img src="../../../.gitbook/assets/image (4) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

Additional modules, like the Evaporator and Reagent Fill Modules, require an additional Accessory Control Module Extension (ACME) to integrate with the \[MPE]². The ACME connects to the Control Box to communicate with the Logistics Module.

<figure><img src="../../../.gitbook/assets/image (5) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>



The Control Box manages the air flow into the Logistics Module. The \[MPE]² has been tested with compressed air and nitrogen with pressure ranging from 1 to 120 psi. There is a pressure drop of approximately 20% from the input at the Control Box to the Manifold in the Logistics Module. For example, an input pressure of 100 psi at the Control Box translates to a pressure of 80 psi at the manifold. The \[MPE]² has sensors that read pressure; an input pressure below 80 psi will generate an error.

## Logistics Module

The Logistics Module is where the \[MPE]² processes samples. This component can operate as a benchtop device or as an integration with a liquid handling system. Refer to section 4.2 for instructions on integrating the Logistics Module with different Hamilton platforms.

<figure><img src="../../../.gitbook/assets/image (6) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>



## Dual Elevator System

The \[MPE]² Logistics Module uses a dual elevator system to handle and process samples. The top elevator stage indicated in Figure 3–3 transports and seals labware (or the Evaporator Module) to the air manifold. The bottom elevator stage, located directly below the top stage in Figure 3–3, works in conjunction with the top elevator stage to transport liquid to a collection bottle. The bottom stage is connected to a pump in the Control Box, which works with a vacuum trap to capture the liquid as it moves toward the waste bottle. The bottom elevator stage also transports collection plates used during elution steps.

<figure><img src="../../../.gitbook/assets/image (7) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>



Both the top and bottom elevator stages can be forced to release labware using the manual release buttons on top of the Logistics Module. This function is useful in the event of unrecoverable errors that occur while labware is being processed within the \[MPE]².&#x20;



## Manifold

The manifold is where pressure is applied to labware via an air pump. It is designed to distribute air pressure equally across all plate wells, and make sure that wells that are processed more quickly do not affect other wells. Manifolds are tested to ensure that a CV of 2% is achieved across the plate.&#x20;

Different manifolds are available for 96-well, 48-well, and 24-well formats. The manifolds can be removed and switched to process different plate sizes. The 48- and 24-well manifolds can be used with tube adapters to process samples tubes. Refer to section 4.8 for instructions on installing manifolds.

<figure><img src="../../../.gitbook/assets/image (8) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

## Evaporator Module

The Evaporator Module can be used in conjunction with the Logistics Module to evaporate solvents. Unlike the Logistics Module, the Evaporator Module does not have a fixed deck position when integrated – the instrument’s gripper must place the Evaporator Module on a filter plate adapter on the Logistics Module when it is used. Depending on the solvent and evaporation parameters, the Evaporator Module can evaporate solvents in 2-20 minutes.

<figure><img src="../../../.gitbook/assets/image (11) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

<table data-header-hidden><thead><tr><th width="145"></th><th></th></tr></thead><tbody><tr><td><img src="../../../.gitbook/assets/image (9) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" data-size="original"></td><td><p>WARNING</p><p>The air exhaust must be connected to the laboratory ventilation system and routed out of the building to avoid creation of harmful aerosols. The [MPE]² has ports available to connect to a fume hood or ventilation system, but it is the responsibility of the laboratory to provide them.</p></td></tr></tbody></table>

The Evaporator Module works with a gas heater integrated with the Logistics Module. Instead of a filter plate, the Evaporator Module is loaded onto the dual elevator. The needles on the Evaporator module are heated, evaporating liquid in the wells of the plate below.

<figure><img src="../../../.gitbook/assets/image (12) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

<table data-header-hidden><thead><tr><th width="145"></th><th></th></tr></thead><tbody><tr><td><img src="../../../.gitbook/assets/image (10) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" data-size="original"></td><td><p>WARNING</p><p>Do not touch the Evaporator Module or gas heater when it is in use.</p></td></tr></tbody></table>



## Reagent Fill Module

The Reagent Fill Module integrates with the dual elevator on the Logistics Module to distribute reagents to labware. The pump can distribute 1 mL of liquid across a 96-well plate in 50 seconds using a reagent manifold, and is able to connect to 17 reagent bottles when using valve extensions. The manifold can dispense 50-2000 μL per well.

<figure><img src="../../../.gitbook/assets/image (13) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

The reagent tubes must be flushed with deionized water between dispenses. Liquid waste is pumped to a waste bottle.

The reagent bottles can be housed in Hamilton bottle racks. Each bottle rack holds two reagent bottles. The bottle racks are equipped with load cells that connect to the ACME to tell when a reagent bottle is empty.&#x20;

<figure><img src="../../../.gitbook/assets/image (14) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>
