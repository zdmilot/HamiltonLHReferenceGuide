# Activities

## Giving Scheduler the information it needs: WHEN are resources being used

Activities

* Groups of steps that will process uninterrupted
* Whatever resources are not used within an activity are available for parallel tasks
* The scheduler needs to know how long an activity is estimated to take

<figure><img src="../.gitbook/assets/image (34).png" alt=""><figcaption></figcaption></figure>

| The ML\_STAR is not used during Preincubate or Incubate, therefore it is available for **other scheduled tasks** | <img src="../.gitbook/assets/image (35).png" alt="" data-size="original"> |
| ---------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------- |

The ML\_STAR’s schedule requires alternating between activities for Assay\_1 <--> Assay\_2



* Activity Groups may be identified when there is a change in resource usage&#x20;
* Extensive ability within scheduler to granularly control activity dependencies and execution times

<figure><img src="../.gitbook/assets/image (36).png" alt=""><figcaption></figcaption></figure>

## Creating within a Method

### Creating Activities and Setting Properties

* Set from the right click menu
* Activity durations are initially estimated
* Resources are set
* Best practice to consistently color code, as Display Names may be cut off in Schedule View

<div>

<figure><img src="../.gitbook/assets/image (37).png" alt=""><figcaption></figcaption></figure>

 

<figure><img src="../.gitbook/assets/image (38).png" alt=""><figcaption></figcaption></figure>

 

<figure><img src="../.gitbook/assets/image (39).png" alt=""><figcaption></figcaption></figure>

</div>

### Update and Finish Activity

* Accepting the Activity also creates the  End Activity group
* Is executed if the Begin Activity block is cancelled
* Can contain additional Activities that would be scheduled
* If needed, update method steps that were hard coded to reference resource positions
* Activities take on the image of the first resource selected during setup, swap orders to change pictures

<div>

<figure><img src="../.gitbook/assets/image (40).png" alt=""><figcaption></figcaption></figure>

 

<figure><img src="../.gitbook/assets/image (41).png" alt=""><figcaption></figcaption></figure>

</div>

### Advanced Options

1. Resource / Operation / Unit Variable
   1. Get Unit:: Variable provided is filled with the available unit scheduler chooses
   2. Set Unit:: Programmer provides unit variable that must be used
2. Minimum / Maximum Executed Duration&#x20;
   1. If monitored, will cancel a task that is too quick or long during run time
   2. Must not violate duration
3. Pre/Post Activity
   1. Submethods that run in Parallel with main activity Tasks
4. Duration
   1. May set the system to log activity times to DB and use algorithm to supply expected durations from DB data

&#x20;![](<../.gitbook/assets/image (42).png>)
