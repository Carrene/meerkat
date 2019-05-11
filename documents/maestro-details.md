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
 - Target
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
#### Upcoming Nuggets
-- Comming Soon --
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
#### Newly Assigned
User has not yet submitted estimate & The Phase before the User's assigned phase status is anything other than 'Complete' or 'Done'
##### Columns:
- ID
- Name
- Tempo
- Type
- Project
- Priority
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
- Phase
- Status
- Start
- Target
- Hours worked
- Load Resource
##### Resource columns:
- Resource
- Status
- Start
- Target
- Hours Worked
- Load
## Modules & Functions
### Nugget Sub Modules
#### Details:
Fields:
- Name (1-128 char)(required)
- Type (dropdown select: bug, feature)(required)
- Project (dropdown select: all available projects)(required)
- Status (dropdown select: To Do, In Progress, Complete, Done, On Hold)(required)
- Priority (dropdown select: low, medium, high)(required)
- Target (calendar)
- Tags (dropdown select: all available tags)(optional)
- Related Nuggets (dropdown select: all available nuggets)(optional)
- Description (0-8192 char)(optional)

Functions: 
- F1 - New Nugget:
	(What) Button to create a new nugget and provides empty fields in Details
	sub-tab in order for a new nugget to be described
	(How) clicking the ‘New’ button
	(Default) depending on the module/view
- F2 - Save:
	(What) Save button that saves any edits made to the fields in detail tab
	(How) clicking on ‘Save’ button
	(Default) Inactive

#### Media:
‘Media’ consists of Attachments & Links. It contains all of the attachments posted in the chat, as well as the links posted in the chat

Attachments:
- File Name: name of the uploaded file
- Date: date the file was uploaded
- User: user that uploaded the file

Links: 
- Link: the next string of the link itself
- Date: date the link was posted
- User: user that posted the link

Functions:
- F1 - Filter:
 (What) Filter function to filter by type, date, user
	(How)
	(Default) inactive

### Audit Log:
audit log of every saved change recorded on the selected nugget

Views: Grid View

Grid Columns:
- Event: attribute that was changed
- New: new value of the attribute
- Old: old value of the attribute
- User: User that made the change
- Date: DTS of the change made

Functions: 
- F1 - Filter:
 (What) Filter function to filter by field changed, date, user
	(How)
	(Default) inactive
- F2 - Sort: 
	(What) Ascending/Descending sort based on the column clicked
	(How) By clicking the column header
	(Default) sort order = date descending (newest events at the top)
