# ESP Docs
 
## ESP Dashboard
 
Data Upload application including installed and custom parser. 
 
Oracle APEX application to interface and provide workflow to ESP Indicators contributions help to streamline data to Stock Assessments.


**Agency**: NOAA (Alaska)

**NOAA**: Kalei, Eren, Shannon

**PSMFC**: Matt, Bob

**PM**: Camille

**Development**: Frank


## Highlights

- Keep Database Design Agile
- Authentication Required
- Interactive Grid & Data Upload
- Data Manager User
 
It’s a reorganization of the existing tool and addresses issues like: quick access to main functionalities from admin perspective, also introduces/renames the concept of “Super Admin”, which has access to all modules and application settings, and invite other users with existing account in PSMFC.
 
 
## Roles
 
- **Super Admin**: access to all modules
- **Admin**: must assign modules
- **Contributor**: must assign modules

 
## To-Do:
 
- Update User Guide
- Add SARA Interactive Grid under Administration
- Fix Email Notifications: upload, indicator summary, delete, comments and approval
- Fix email URL
- Ensure email logic is based on environment
- Complete Email Notifications section
 
 
## Overall
 
Contributor and Admin log in and they can upload, view data and approve.
 
- Don’t display anything if we have N/A or missing year just don’t display anything for the series.
- Copy and past defect in Indicator Summary for AKFIN Source indicators
- 12:00 AM (30 min): Prepare demo & testing for Shannon and Kalei


## Contributor Dashboard
 
 
## Admin Dashboard
 
 
## Management
 
 
## Notes
 
The tendency shows the tool is nothing but a collaboration concept with two roles: admin and contributors whom might used one or different templates for the data, templates available based on role: ESP template (v1, v2, v2.1, v3, etc..), SARA (v1.0, v2), ESR (coming soon).
 
** Collaboration with other regions (ex: Northeast): The super admin creates a module, this would allow the data be isolated from other modules otherwise can be segmented within the module utilizing the Intended ESP.
 
Scenario 1. Northeast also wants to collaborate and use the tool to bring together their indicators, they can create their Intended ESP which later can be used to group the Indicators that will be assign to the contributors.
 
Scenario 2. Northeast wants to create their module which could also result in a different webservice or webservice endpoint since the data would be isolated from the module level.
 
In both scenarios BYOD 3.0 provides coverage.
 
 
**VERY IMPORTANT**:
 
The different modules must used the same database model and potential enhancements to support extra complexities.
 
- Use module table: User Modules
 
 
## Functionalities
 
- **CRUD Operations**: Source Target, Comments, Lookup Tables (Modules, Data Sources, Databases, Filetypes…)
- **Source Target Workflow**: Create a Source Target, Submission & Store Files, Parse File (Templates), Validate Data, Error Handling, Approval, Rejection, Removal
- **Email Notification**: Handles queuing and send email notifications, also handles email scheduling.
 
- Parser Package: supports parsing different template files to the database.
- Email Package: supports email scheduling for different groups.
 
- Schedule Notification: send email at specific time, select a list of users, include template, last year upload, user guide.
- Create Email Subject, Email Body, Email Footer, Sender, Receiver, Template, 
 
- Create ESP Procedure: allows admin create ESP and necessary database objects to function
 
- CREATE_ESP_TABLES process
 
- Create SARA Procedure: allows admin create SARA and necessary database objects to function
 
 
## Super Admin Pages
 
- **Dashboard**
 
- **super_admin_metrics_v**: needs definition (Ask: metrics across all modules)

- **Management**


## Contributor Pages
 
- **Dashboard**
 
- **contributor_metrics_v**: sources badge list
- **contributor_targets_v**: return list of indicators assigned to user sorted by priority, time
- **contributor_targets_archived_v**: return list of indicators retired that was contributed by user
 
 
## Administrator Pages
 
- **Dashboard**


- **admin_metrics_v**: sources badge list
- **admin_recent_actions_v**: 
 
- **Create Indicator**


## Webservice Actions


- **Webservice Logs**
- **Update Webservice**


## Management
 
- Modify Indicator Metadata and/or e CT Assignee
 
- Archive Indicator (Retire)
 
- Indicator Page
 
- Upload Indicator
 
- Indicator Metadata (admin version)
 
- Submission Review
 
- Comment History
 
- Approve Indicator
 
- Remove Indicator
 
- Administration
 
- Webservice Actions
 
- **Target Page**
 
- **submissions_by_target_v**: return list of submission by indicators
- **collections**: display data [time series comparison, indicator data, indicator summary]
 
- **Submission Page**
 
- Indicator Metadata
- Submission Review
- Comment History
- Remove Indicator
