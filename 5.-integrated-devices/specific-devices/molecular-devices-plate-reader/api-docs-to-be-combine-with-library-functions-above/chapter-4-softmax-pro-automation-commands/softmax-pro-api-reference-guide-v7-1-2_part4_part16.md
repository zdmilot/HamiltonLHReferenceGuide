# GetGroupNameAssignments

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

