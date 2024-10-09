# Dual Arm Programming‌

The VENUS Software is designed to handle tools (e.g. a pipetting tool and a plate handling tool) on different arms. The software monitors each movement of the individual arms of the ML STAR dual arm instruments. If one arm needs priority to pass, the second arm is moved to a safe position first. In this manner, the two arms and the tools on the arms will not crash into each other. The programmer has not to care about sudden collisions in the system.

## VENUS Dynamic Scheduler

For the programming of a dual arm instrument, Hamilton recommends to use the VENUS Dynamic Scheduler software package. This package is not part of the basic VENUS Software.&#x20;

The dynamic scheduler has several advantages and is specially designed for handling complex parallels in an assay. The administration of other devices, such as plate handler, plate washer, reader, etc., is just as easy as the programming of the dual arm configuration.

Compared to the basic VENUS Software, there are advantages of the additional software package (VENUS Dynamic Scheduler), especially the programming of the parallel task. Each arm is defined as a so-called “Resource”. The dynamic scheduler allows defining one resource (arm) as the major and the other as the minor device. The major arm always has the right of way. The dynamic scheduler automatically organizes the optimal use of the resources.

Dual arms also can be programmed by the basic VENUS Software of the ML STAR. Carriers used by both arms should be placed in the middle of the pathway reachable by both arms. If one arm is moving to the common carrier(s), the other arm should not be obstructed in its tasks. Also, the programmer must decide whether the tasks of the two arms work in parallel or not (e.g. one arm must wait until the other has finished its task).
