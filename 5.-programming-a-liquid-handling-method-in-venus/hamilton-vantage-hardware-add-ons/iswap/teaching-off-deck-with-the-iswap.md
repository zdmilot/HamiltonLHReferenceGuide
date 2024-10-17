# Teaching Off Deck with the iSWAP

## Overview

In order to teach off deck positions, the iSWAP must be used as a teaching tool. In teaching mode, the iSWAP is manually guided to a particular location on deck, while holding the labware of interest, and the taught coordinates are saved to the system deck layout. Some off deck locations and system configurations may result in positions that cannot be reached by the iSWAP or are challenging to estimate in order to allow teaching. Errors such as the one below may be seen. This guide is intended to provide instructions on how to address such challenges with teaching off deck positions.\


<figure><img src="../../../.gitbook/assets/image (2) (1).png" alt=""><figcaption></figcaption></figure>

## How to teach off deck sites with the iSWAP

For this example, the system is configured with a device on the left hand side (LHS) of a STAR deck and will require the plate to be transferred with a wide grip.

<figure><img src="../../../.gitbook/assets/image (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

First, it is important to note that one cannot teach a plate site if the starting position is outside of the iSWAP reach, so do not put the plate to be taught too far outside of the system deck layout.

Start the teaching of the target position using the following coordinates and orientation:

<figure><img src="../../../.gitbook/assets/image (2) (1) (1).png" alt=""><figcaption></figcaption></figure>

When teaching the position use the following settings, getting a plate from POS 1 on a standard plate carrier on the deck in wide grip mode:

<figure><img src="../../../.gitbook/assets/image (3) (1).png" alt=""><figcaption></figcaption></figure>

Everything except the grip height should be filled in automatically as seen above so long as the plate is placed in the right location and orientation beforehand (see coordinates above).

However, if you’re starting without a good or “known” position, then you can start by placing a plate somewhere on the deck in positive X and rotating it to the desired orientation, then starting the teaching process and changing all the parameters as follows:

<figure><img src="../../../.gitbook/assets/image (4) (1).png" alt=""><figcaption></figcaption></figure>

* Select the sequence of the source plate you’ll be using to teach with (make sure it’s in a location suitable for the grip orientation)
* Set the grip side (small/skinny or large/wide)
* Set any grip height that is appropriate for your plate. Use 3 to 5mm for standard microtiter plates.
* Set the grip width for the plate dimensions and the opening before access (wide enough to clear the plate without hitting adjacent labware)
* Check the “Complex movement“ box
* Check the “Stretch arm” box
* Set the “Retract distance” to (at least) 139.0mm
* Set the “Labware orientation” to match the final (target) orientation you want the gripper to be in when going to the integration – as you cycle these you will see the image change on the top left to help guide you
* Select Help if needed to review labware orientations
* From there, the teaching should work normally using the Move Probe – Key Control function

## How to create and edit a template file for an off deck plate site

If you want to create or edit a template file that snaps the plate into place, follow the instructions below. The use of a template file allows for reproducible transports even if the plate is moved off of the site and back on. In addition, the use of a template file allows for the rotation of the plate 180 degrees without flipping over A1 throwing off the center point.

For right hand side (RHS) or left hand side (LHS) labware integrations, a template definition must be made to snap into a track (e.g. track 1 or the rightmost track) or the left MPH waste or right MPH tip waste locations. These instructions use the starting labware definition, “LHSIntegrationExample\_Template.tml,” which is a labware definition that snaps to the MPH waste. The starting X/Y/Z values for the site are 0/0/0 to make math easier. See below for the process steps to edit this labware:

* Teach the plate hand off site as described in the prior section and write down the X, Y, and Z coordinates
* Bring a template LHS integration onto your deck and snap it to the MPH waste
* Snap the same type of plate (and in the same orientation) to the site on the LHS integration template you snapped to the MPH
* Determine the X, Y, and Z differences between the template and the taught site
* Change the X, Y, and Z values in the template’s labware definition for the site to correspond to the difference between the plate currently on the template and the taught plate
* Bring the template in again to see if the site now overlaps the taught position – snap a plate to it to make sure it matches (you can change the color of the template to make sure your changes took if needed)

The rotation of the plate on the deck and target location matter. For example, a plate cannot be moved from position 5 of a plate carrier to the off-deck position with A1 in the bottom left or vice versa. Therefore, if the process requires the need to alternate between gripping plates from the back and the front, then two plates/sequences that are rotated 180 degrees from one another are required.

\
