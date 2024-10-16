# HSL Update Worklist

<figure><img src="../.gitbook/assets/image (830).png" alt=""><figcaption></figcaption></figure>

The HSL Update Worklist library allows to set the processing status of a job contained in the worklist data of the Vector Database to completed.

&#x20;

The HSL Update Worklist library provides in the namespace UpdateWorklist the following functions:

&#x20;

UpdateJobStatus

&#x20;

Includes:

HSLUpdateWorklist.hs\_

&#x20;

| Function                                                                                                             | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| -------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| <p>UpdateJobStatus(</p><p>variable&#x26; jobName,</p><p>device&#x26; deviceObj</p><p>sequence&#x26; sequenceObj)</p> | <p> </p><p>The UpdateJobStatus function updates the job status to VectorDb_JobState::Processed of all positions contained between positon 1 and (currentPos - 1) in the given sequence which are in the state VectorDb_JobState::Assigned and which are associated to the specified assay name.</p><p>If the current position of the sequence equals to zero, the status of all positions contained between positon 1 and the end position are updated. The positions must still be loaded.</p><p><strong>Arguments:</strong></p><p>jobName [in]</p><p>The job name (string, may be empty).</p><p>deviceObj [in]</p><p>Device containing the positions which status should be updated.</p><p>sequenceObj [in]</p><p>Sequence containing the positions which status should be updated.</p><p><strong>Return:</strong></p><p>The number of jobs updated in the Vector Database table 'Job' (integer).</p><p> </p> |

&#x20;
