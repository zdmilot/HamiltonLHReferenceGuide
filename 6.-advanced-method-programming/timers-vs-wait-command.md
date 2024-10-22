---
icon: dev
---

# Timers Vs Wait Command

<figure><img src="../.gitbook/assets/image (30).png" alt="" width="359"><figcaption></figcaption></figure>

With Basic Parallelism

* Minimize instrument downtime, maintain process control (activity calculations)
* IF “wait time” activities exceed expected time, actual time captured

&#x20;Assay Relative Time

* Single infinite “RunTimer” at method start
* Error handling, or Activity Logging can reference how far into run event happened

&#x20;

&#x20;

<table data-header-hidden><thead><tr><th width="238"></th><th></th></tr></thead><tbody><tr><td><img src="../.gitbook/assets/image (102) (1) (1) (1) (1) (1).png" alt="" data-size="original"></td><td>Defines and starts a timer. Can use Relative Time, Absolute date and time, and Infinite time</td></tr><tr><td><img src="../.gitbook/assets/image (103) (1) (1) (1) (1) (1).png" alt="" data-size="original"></td><td>Stops the execution of a running method until a previously started timer has elapsed. Never include a wait for an infinite timer in a method, since the Wait for command waits forever and therefore blocks the method's execution!</td></tr><tr><td><img src="../.gitbook/assets/image (105) (1) (1) (1) (1) (1).png" alt="" data-size="original"></td><td>Reads the elapsed time of a previously started timer in seconds</td></tr><tr><td><img src="../.gitbook/assets/image (106) (1) (1) (1) (1) (1).png" alt="" data-size="original"></td><td>Restarts a previously defined timer.</td></tr></tbody></table>

