# Scheduling

## Run Control Order of Operations

### Non Scheduled Method

1. HSL Opened by Run Control
2. HSL Analyzed for errors
3. Wait for operator to press “Go”
4. Execute HSL in line order

<figure><img src="../.gitbook/assets/image (838).png" alt=""><figcaption></figcaption></figure>

### Scheduled Method

1. HSL Opened by Run Control
2. HSL Analyzed for errors
3. Operator prompted for number of tasks (method instances), Operator accepts
4. HSL executed for all non-activity grouped steps, for each instance of the method
5. Schedule generated
   1. _If operator wishes to re-enter number of instances, they may re-analyze to start over_
6. Wait for operator to press “Go”
7. Execute HSL in line order, per schedule and instance
   1. _Steps that are not within an activity are executed again_

## Run Control – Schedule View

### Reviewing the Schedule

* Schedule View shows a Gantt chart indicating when tasks/activities are anticipated to be complete
* Resource View shows what is being used when

&#x20;

<div>

<figure><img src="../.gitbook/assets/image (840).png" alt=""><figcaption></figcaption></figure>

 

<figure><img src="../.gitbook/assets/image (839).png" alt=""><figcaption></figcaption></figure>

</div>

### Checking Scheduler within Method Editor

•       Right click toolbar -> Scheduler

•       Contains the Schedule and Stop Schedule buttons

•       When scheduling, Output -> Scheduler Output replicates Trace view in Run Control

•       Same Operator pop up and potential for instrument movement!

&#x20;![](<../.gitbook/assets/image (16) (1).png>)
