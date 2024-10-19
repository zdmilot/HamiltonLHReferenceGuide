# softmax pro api reference guide v7 1 2\_Part4\_Part16

GetGroupNameAssignments\
Int32 GetGroupNameAssignments\
The GetGroupNameAssignment command returns the group name assignments of a Plate section.

Parameters\
None\
Returns\
The function returns the command ID used to retrieve the data that the CommandCompleted Event returns.

Data Returned Through the CommandCompleted Event\
Return Type: String\
Returns a tab-delimited list of group names assigned to wells for all the wells in the plate.

Wells without a group assignment return as blank.

GetInstrumentStatus\
Int32 GetInstrumentStatus\
The GetInstrumentStatus command returns the instrument status.

Parameters\
None\
Returns\
The function returns the command ID used to retrieve the data that the CommandCompleted Event returns.

Data Returned Through the CommandCompleted Event Return Type: String\
For the possible values, see InstrumentStatusChanged on page 98.
