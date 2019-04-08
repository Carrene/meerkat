## Maestro Details

### Release(in order)
#### Columns:
 - Name
 - Release Date
 - Release Cutoff
 - Group
 - Projects
 - Manager
#### Fields:
 - Name: short name or summary description of the nugget (1-128 char)
 - Release Date: the official date the release is meant to go live. It informs all stakeholders when the Nuggets/Projects in the release will be released.
 - Release Cutoff: The last day that nuggets/features can be accepted for the release to be ready. Project & Nugget statuses are calculated in relation to release cutoff
 - Group: releases are tied to a certain group, only users that are member of that group may interact with the release. Only projects of the group may be tied to the release.
 - Projects
 - Manager: Release Manager has certain permissions related to release, like edit/save permissions for Release details
 - Description: longer description of the nugget (0-8192 char)

### Project(in order)
#### Columns:
 - Name
 - Tempo(Green = On Time, Yellow = Delayed, Red = At Risk, Blue = Frozen)
 - Status(Queued, Active, On Hold, Done)
 - Workflow
 - Group
 - Release
 - Release Cutoff
 - Current Target: calculated date based on current estimates
 - Manager
#### Fields:
 - Name
 - Release: Associated Release with the project. The Release Cutoff Date is also inherited so that Tempo can be calculated for Projects & Nuggets, and that Release Cutoff can be displayed in the grid for Projects & Nuggets.
 - Workflow: The collection and order of phases that the Projects nuggets will go through. Simple dropdown to select the workflow
 - Group: projects belong to a certain group, only users that are member of that group may interact with the project. Projects can only be associated to a Release of the same group.
 - Project Manager: User selected has special permissions related to project, like edit details, move nuggets
 - Secondary Manager(optional):Same as project manager
 - Description

### Nugget/Unread/Subscribed(in order)
#### Columns:
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
 #### Fields:
 - Name
 - Type: Bug or Feature </br>
 When ‘New Nugget’ is clicked, the default value for Type is Feature. Another way of creating a new Nugget is via reporting a bug by right clicking on a Feature Nugget. In that case, the default is ‘Bug’
 - Project
 - Status(To Do, In Progress, Complete, Done, On Hold) 
 - Priority
 - Target
 - Tags
 - Related Nuggets: related Nuggets (this is currently referred to as related items in Nutmeg)
 - Description

## Modules & Functions
### Nugget Sub Modules
#### Details:
Name(1-128 char)(required)
