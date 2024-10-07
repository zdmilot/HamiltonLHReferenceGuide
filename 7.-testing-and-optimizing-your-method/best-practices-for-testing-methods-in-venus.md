---
description: Testing workflows before production runs.
icon: dev
---

# Best Practices for Testing Methods in Venus

1. Use enable/disable steps to test methods peicewise
2. Run the simulator as much as possible before running using tips.
3.
   1. \*\* important\*\* disable device integration commands when using simulation mode as most devices will still receive the commands and think that the run is actually happening which could lead to device issues, failures, or even break the device
4. Do iterative water runs
5.
   1. Make sure plates and labware have liquid in them where it would be present in a normal run
6. Utilize user output as break statements to halt the program at certain points to test
7. Utilize python code or pseudo code to work through tough workflows if needed
8. Ensure that volumes for pipetting and reachability has been checked, Venus only checks syntax and does not check for any possible run errors during runtime- this will save you a lot of time where you might have something happen in the middle or end of your test run
9. Be cautious about reusing tips durring testing. It is very easy to accidentally forget to blow out the tip/dry it fully before using which may lead to liquid aspiration into the pipetting channel which is extremely important to avoid&#x20;
10. Make sure plates and samples are positioned properly for that portion of the run
11. Make sure carriers are fully positioned and pushed in where needed
12. Make sure that no materials are left on the auto load or in the way of any moving parts
13. Make sure to check tip waste throughout testing as this might be a wasteful process, although limiting the amount of waste durring development by utilizing simulations and reusing tips wherever possible is good practice&#x20;

\
