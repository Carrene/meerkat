## Maestro Document

### Release(in order)
##### Columns:
 - Name
 - Release Date
 - Release Cutoff
 - Group
 - Projects
 - Manager
##### Detail Fields:
 - Name: short name or summary description of the nugget (1-128 char)
 - Release Date: the official date the release is meant to go live. It informs all stakeholders when the Nuggets/Projects in the release will be released.
 - Release Cutoff: The last day that nuggets/features can be accepted for the release to be ready. Project & Nugget statuses are calculated in relation to release cutoff
 - Group: releases are tied to a certain group, only users that are member of that group may interact with the release. Only projects of the group may be tied to the release.
 - Projects
 - Manager: Release Manager has certain permissions related to release, like edit/save permissions for Release details
 - Description: longer description of the nugget (0-8192 char)

### Project(in order)
##### Columns:
 - Name
 - Tempo(Green = On Time, Yellow = Delayed, Red = At Risk, Blue = Frozen)
 - Status(Queued, Active, On Hold, Done)
 - Workflow
 - Group
 - Release
 - Release Cutoff
 - Current Target: calculated date based on current estimates
 - Manager
##### Detail Fields:
 - Name
 - Release: Associated Release with the project. The Release Cutoff Date is also inherited so that Tempo can be calculated for Projects & Nuggets, and that Release Cutoff can be displayed in the grid for Projects & Nuggets.
 - Workflow: The collection and order of phases that the Projects nuggets will go through. Simple dropdown to select the workflow
 - Group: projects belong to a certain group, only users that are member of that group may interact with the project. Projects can only be associated to a Release of the same group.
 - Project Manager: User selected has special permissions related to project, like edit details, move nuggets
 - Secondary Manager(optional):Same as project manager
 - Description

### Nugget/Unread/Subscribed(in order)
##### Columns:
 - Subscribe: A user can set this flag to subscribe to a Nugget. This is unique per user.
 - ID
 - Name
 - Tempo(Green = On Time, Yellow = Delayed, Red = At Risk, Blue = Frozen)
 - Status
 - Type
 - Phase
 - Days: Number of days a nugget has been sitting in the lead phase.
 - Target
 - Priority
 - Tags
 - Project
 - Updated
 - Updated By: User Name that made the most recent saved change to the Project. This is recorded in Audit Log
 - Created
##### Detail Fields:
 - Name
 - Type: Bug or Feature </br>
 When ‘New Nugget’ is clicked, the default value for Type is Feature. Another way of creating a new Nugget is via reporting a bug by right clicking on a Feature Nugget. In that case, the default is ‘Bug’
 - Project
 - Status(To Do, In Progress, Complete, Done, On Hold) 
 - Priority
 - Tags
 - Related Nuggets: related Nuggets (this is currently referred to as related items in Nutmeg)
 - Description

### Assigned(in order)
Contains a grid that lists all nuggets the user is assigned to as a resource. These assigned nuggets are further sorted into separate ‘buckets’
#### In Progress Nuggets 
User has submitted estimate & WHERE Start Date < Today's Date > Target Date
##### Columns:
- ID
- Name
- Tempo
- Type
- Time Card
- My Start
- My Target
- Hours Worked
- Project
- Priority
- Phase
#### Upcoming Nuggets
User has submitted estimate & WHERE Start Date > Today's Date
##### Columns:
- ID
- Name
- Tempo
- Type
- Starts In
- My Start
- My Target
- Hours Worked
- Project
- Priority
- Phase
#### Need Estimate
User has not yet submitted estimate & When the Phase before the user's assigned phase status was set to 'Complete'
##### Columns:
- ID
- Name
- Tempo
- Type
- Response Time
- Project
- Priority
- Phase
#### Newly Assigned
User has not yet submitted estimate & The Phase before the User's assigned phase status is anything other than 'Complete' or 'Done'
##### Columns:
- ID
- Name
- Tempo
- Type
- Project
- Priority
- Phase
#### Completed/Done
##### Columns:
- ID
- Name
- Tempo
- Type
- My Start
- My Target
- Hours Worked
- Status (Completed / Done)
- Phase
- Project
#### Time Card tab:
##### Estimate:
- Start Date
- Target Date
- Estimate (hrs)
##### Columns:
- Report Date
- Hours
- Notes
#### Assign Tab:
##### Columns:
- Phase: All the Phases in The Workflow of the selected nugget
- Status: To Do: All Resources in that phase status = To Do
In Progress: At least one resource in that phase status = In Progress OR there are no resources that = On Hold and at least one resource =Complete/Done
On Hold: All resources in that phase status = On Hold OR at least one resource in that phase status = ON Hold AND there is no resource in phase with status = In Progress 
Complete: All Resources in that phase have minimum status = Complete 
Done: All resources in that phase have status = Done
- Start
- Target
- Hours worked
- Lead Resource
##### Resource columns:
- Resource: Lists all Resources with the associated skill for the selected phase
- Status: Resources work status 
- Start: Resources Estimated Start Date
- Target: Resources Estimated Target Date
- Hours Worked: Resource Total hours worked/Estimate (h)
- Load: Resource Workload (Light/ Medium / Heavy)

### Good News(in order)
Contains a grid that lists all nuggets the user is assigned to as a resource. These assigned nuggets are further sorted into separate ‘buckets’
#### Backlog (columns)
User has submitted estimate & WHERE Start Date < Today's Date > Target Date
- ID
- Name
- Tempo
- Type
- Batch: Combo box with numbers to assign batch number, in this example the batch numbers would be, 01, 02, 03, 04. It will always go up one based on the batches already existing. 
- Phase: control to switch between backlog and triage. 
- Return to Triage: Date combo box
- Project
- Priority
- Creator

#### Triage (columns)
- ID
- Name
- Tempo
- Type
- Batch
- Phase
- Return to Triage: Date combo box
- Origin: Backlog/New
based on where the nugget is coming from the backlog or if it is a newly created nugget
- Project
- Priority
- Creator

#### Need Approval (columns)
- ID
- Name
- Phase Completed: the phase that was completed by the resources. Since multiple phases can be completed, there can be some duplicates in the main grid.
- Approve: checkbox control to approve the 'Complete' and then save it, which will update it to 'Done'
- Tempo
- Type
- Batch
- Grace Period: timer starting from 48:00 (this is the amount of time the PM has to approve the Completion
- Project
- Priority

#### Hours Reported (columns)
- ID
- Name
- Tempo
- Type
- Mojo
- Project
- Lead Resource
- Priority

### Bad News(in order)
#### Missing Hours (columns)
- ID
- Name
- Tempo
- Type
- Batch
- Project
- Priority
- Phase
#### Missing Estimate (columns)
- ID
- Name
- Tempo
- Type
- Batch
- Grace Period
- Extend
- Project
- Priority
- Phase
#### Expired Triage (columns)
- ID
- Name
- Tempo
- Type
- Batch
- Phase
- Return to Triage
- Grace Period
- Project
- Origin
- Priority
- Creator
