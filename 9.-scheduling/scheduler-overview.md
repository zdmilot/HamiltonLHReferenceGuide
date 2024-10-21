# Scheduler Overview

* Scheduler is flexible, and can accommodate for variable timings, either from user selections or events at run time (reloads, errors, etc.)
* Allows for more concise methods
  * Scripting for one or a set of functions within a document
  * Do not have to script all possible outcomes as in a multiplate example
  * Increasing throughput could be done by adjusting the deck, not changing the script
* Methods adapted for scheduler (i.e. Single Plate process) allow the scheduler to find parallel processes for multiple instances
* Scalable – instead of programming for a plate, could program for batches, or parts of processes&#x20;

&#x20;

<figure><img src="../.gitbook/assets/image (25).png" alt=""><figcaption></figcaption></figure>

## Examples:

### Single Plate Assay

A particular method has six distinct functions (example durations listed):

1. Send a plate from deck  HHS (60s)
2. Preincubate (wait) for the plate to warm (120s)
3. Start a reaction with the 96MPH (60s)
4. Incubate the reaction (300s)
5. Stop the reaction with the 96MPH (60s)
6.  Return the plate from the HHSdeck (60s)\


    <figure><img src="../.gitbook/assets/image (24).png" alt=""><figcaption></figcaption></figure>

* A single plate will take (sum of times) 11 minutes to complete
* Without scheduler, the method would run serially, with reloads between runs as needed by the operator:
  * 2 plates = 22min
  * 3 plates = 33min, etc.&#x20;

### Multi-Plate Assay

Can be created by recognizing parallel capable processes

* Parallel processes do NOT share resources
* Simple assays could use timers/sequences/loops/conditionals for parallel tasks
* Could use parallel functions (Fork\&Join or Parallel Process)
* These approaches are fine for predictable assay timings
* See Venus II Advanced Module #4 for additional information

| <img src="../.gitbook/assets/image (23).png" alt="" data-size="original"> | <p>Example of parallel process functions “ping-ponging” a resource (MLSTAR), timers omitted for clarity</p><p></p><p><strong>Time on an HHS</strong> is the independent resource for each thread</p> |
| ------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |

