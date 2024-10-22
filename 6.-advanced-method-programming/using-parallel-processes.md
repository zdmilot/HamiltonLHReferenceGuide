---
description: Creating parallel liquid handling workflows for multi-channel operations.
---

# Using Parallel Processes

## What is Parallelization vs Serial

### Serial

* Default method set up – One robot = One resource
* Tasks executed _sequentially_ (SEQUENTIAL Transfer Aliquoting Robot)
* Other example, SERIAL port – command/response/command

### Parallel

* Multiple resources available – devices, instruments, or just program threads
* Multiple ways to handle: ForkJoin, Method Columns, Scheduler
* Key feature is time and resource management!



## Begin/End Parallel

| <p>BEGIN creates new METHOD Column</p><ul><li>Available after line item is called</li><li>Multiple Columns (threads) can be created</li><li><p>Forces open all steps that condense code</p><ul><li>Groups</li><li>Conditionals</li><li>Loops</li></ul></li></ul> | <img src="../.gitbook/assets/image (27).png" alt="" data-size="original"> |
| ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------- |

<figure><img src="../.gitbook/assets/image (28).png" alt=""><figcaption></figcaption></figure>

### &#x20;Events & End Parallel

| <p>Set/Wait for Event</p><ul><li>Event Objects act as “Relay Batons” between threads</li><li>Eliminates conflicts between shared resources</li></ul><p>END Parallel</p><ul><li>Closes the column/Thread</li></ul> | <img src="../.gitbook/assets/image (29).png" alt="" data-size="original"> |
| ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------- |



### Parallel Issues

* If two threads are waiting on a timer, both will be visible in the countdown – neat!
* Beware of Separate threads merging into single sub methods, can cause havoc on local variables
* Task Local variable changes
* Trace file clutter – Multi-line traces (Pipette start :: Complete) can be separated by pages of text
* Waiting on Events that are stalled (timeouts and implications)
* Where Errors occur, Dialog references LINE,COLUMN

&#x20;

&#x20;

## Fork/Join Library

(see [Fork/Join Library](../libraries/fork-join-parallelization/))
