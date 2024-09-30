---
description: How to organize sequences and pipetting steps.
---

# Defining Layouts and Labware Sequences

1. **Deck Layouts**:
   * A **deck layout** is the physical setup of the labware and carriers on the robot's deck. It includes the placement of all labware such as tip racks, plates, sample tubes, and reagent carriers.
   * The deck layout tells the robot where all the labware is located spatially. This is crucial for the robot to correctly move between different pieces of labware during method execution.
   * In Challenge 1, a deck layout is created by adding various labware types (e.g., tip carriers, sample tube carriers, reagent tubs) onto the robot's deck, and this layout is saved and used in future challenges.
2. **Labware Positions**:
   * **Labware positions** refer to the specific locations on the deck where each piece of labware is placed. These positions are important because they allow the robot to access the right wells, tips, tubes, etc., based on its program.
   * For example, specific labware types such as "Nunc 96-well plates" or "Deep-well reagent plates" are placed in designated positions on the deck, and these positions are referenced during method execution.
3. **Labware Sequences**:
   * A **labware sequence**, or **sequence** refers to a defined set of labware positions that the robot will interact with in a specific order. It can represent wells on a plate, sample tubes, or any other positions where pipetting or other robotic actions occur.
   * Sequences automate the process of tracking which labware positions the robot will interact with, such as which sample tubes or plate wells to aspirate or dispense into.
   * For example, a sequence could be the first column on four 96-well plates, to be used to automate liquid transfers across those wells.
