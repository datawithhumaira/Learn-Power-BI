# Power BI Sharing, Apps, Org Apps, and Data Governance
## Introduction
Managing access to reports, dashboards, and datasets is one of the most important responsibilities in Power BI. Organizations need a balance between collaboration, security, governance, and scalability. Power BI provides multiple sharing and distribution options that allow organizations to deliver content to the right audience while maintaining control over permissions and data protection.
In this guide, you'll learn:
- Power BI sharing models and access control
- Workspace Roles and Item-Level Sharing
- Power BI Apps and Audiences
- Org Apps and when to use them
- Data Governance through Endorsements and Sensitivity Labels
- Best practices for secure and scalable content distribution
---
## Overview
Power BI provides four primary methods for sharing and distributing content:
1. **Workspace Roles**
2. **Item-Level Sharing**
3. **Power BI Apps**
4. **Org Apps**
Each method serves a different purpose depending on whether the goal is collaboration, controlled distribution, or broad organizational access.
---
# Understanding Power BI Sharing Models
## Workspace Roles
Workspace roles determine what users can do inside a Power BI workspace.
### Viewer
#### Permissions
- View reports and dashboards
- Interact with visuals and filters
- Consume content without modifying it
#### Important Note
✅ Row-Level Security (RLS) is enforced only for Viewers.
#### Example
A manager who needs access to business reports but should not edit them.
---
### Contributor
#### Permissions
- Create reports
- Edit reports
- Delete reports and semantic models
#### Restrictions
- Cannot manage workspace settings
- Cannot assign workspace roles
#### Example
A data analyst responsible for developing and maintaining reports.
---
### Member
Members inherit all Contributor permissions and gain additional management capabilities.
#### Permissions
- Add users as Viewers or Contributors
- Publish and unpublish Power BI Apps
- Manage app permissions
#### Restrictions
- Cannot remove users
- Cannot modify existing role assignments
#### Example
A team lead responsible for coordinating report distribution.
---
### Admin
#### Permissions
- Full workspace control
- Manage permissions
- Assign and remove roles
- Configure workspace settings
- Delete the workspace
#### Example
Workspace owners and Power BI administrators.
---
### Important Workspace Limitation
Workspace access is **all-or-nothing**.
If a user has access to the workspace, they can access all reports, dashboards, and semantic models contained within it.
#### Memory Trick
🏢 **Workspace Role = Entire Building**
Giving workspace access is like handing someone a key to an entire building instead of a single room.
---
## Item-Level Sharing
Item-level sharing allows specific reports or dashboards to be shared without granting access to the entire workspace.
### Content You Can Share
- Individual Reports
- Individual Dashboards
### User Capabilities
- View content
- Interact with visuals
- Use slicers and filters
### Restriction
- Cannot edit shared content
---
### Security Considerations
When sharing a report, users may also receive access to the underlying semantic model.
---
### Row-Level Security (RLS)
RLS ensures users can only view data they are authorized to access.
#### Example
A sales report contains:
- UAE Sales
- Saudi Sales
- Egypt Sales
With RLS configured:
- UAE Managers only see UAE data
- Saudi Managers only see Saudi data
---
### Sharing Options
#### People in Your Organization
Anyone in the organization can access the content.
#### People with Existing Access
Only users who already have permissions can access the content.
#### Specific People
Only selected users or groups receive access.
---
### Advantages of Item-Level Sharing
Item-level sharing overcomes the workspace all-or-nothing limitation.
#### Example
A workspace contains:
- Finance Report
- Sales Report
- HR Report
You can share only the Sales Report with a business partner while keeping other reports private.
#### Memory Trick
🚪 **Item-Level Sharing = One Room**
---
## Workspace Roles vs Item-Level Sharing
### Workspace Roles
**Best For:** Internal collaboration
#### Characteristics
- Access to entire workspace
- Easier administration
- Less granular security
### Item-Level Sharing
**Best For:** Secure report distribution
#### Characteristics
- Access to selected reports
- Better security
- Granular permissions
---
# Power BI Apps
## What Are Power BI Apps?
Power BI Apps provide a way to package multiple reports and dashboards into a single application experience.
Instead of sharing numerous reports individually, users access all related content from one centralized application.
---
## Benefits of Power BI Apps
### Easy Distribution
Share a single app instead of numerous reports.
### Better User Experience
All content is organized in one place.
### Centralized Access
Users consume reports and dashboards through a unified experience.
### Controlled Updates
Changes can be tested in the workspace before being published to users.
---
## Power BI App Publishing Process
### Step 1: Set Up the App
Provide:
- App Name
- Description
- Theme Color (Optional)
- Support Website (Optional)
- Contact Information (Optional)
### App-Scoped Copilot (Preview)
Optional capabilities include:
- Asking questions about reports
- Generating report summaries
- Searching across app content
**Requirement:** Fabric Copilot must be enabled at the tenant level.
---
### Step 2: Add Content
Include:
- Dashboards
- Reports
- Workspace Items
**Best Practice:** Arrange content logically to improve navigation.
---
### Step 3: Publish the App
1. Select **Publish App**
2. Generate the app link
3. Share the link with users
Users can then access all published content through a single app.
---
## Updating a Power BI App
### Open the Workspace
Select:
**Edit App (Pencil Icon)**
---
### Make Changes
You can:
- Add reports
- Remove reports
- Reorganize content
- Change app settings
### Important
Changes remain invisible to users until the app is republished.
---
### Republish
Select:
**Update App**
Users automatically receive the latest version.
---
## Unpublishing a Power BI App
### Steps
1. Open Workspace
2. Select More Options (...)
3. Choose **Unpublish App**
---
### Removed
- User access
- Bookmarks
- Comments
- Personal customizations
### Not Removed
- Workspace
- Reports
- Dashboards
- Semantic Models
Content remains safely stored within the workspace.
---
# Power BI App Audiences
## What Is an Audience?
An Audience is a group of users that can see specific content within the same Power BI App.
Different audiences can see different reports without requiring separate apps.
---
## Example
### Sales Audience
Can View:
- Sales Dashboard
- Revenue Report
- Territory Performance Report
### Marketing Audience
Can View:
- Campaign Dashboard
- Lead Analysis Report
- Customer Engagement Report
### Finance Audience
Can View:
- Financial Dashboard
- Profit Analysis Report
Each audience only sees content assigned to them.
---
## Benefits of Audiences
### Better Security
Users only see information relevant to their responsibilities.
### Easier Management
One app can serve multiple teams.
### Centralized Administration
No need for multiple workspaces or multiple apps.
---
## Creating Audiences
### Create an Audience Group
Examples:
- Sales
- Marketing
- Finance
- Executives
---
### Configure Content Visibility
Use:
- 👁️ Show
- 🚫 Hide
to determine what each audience can access.
---
### Assign Access
Supported assignments include:
- Individual Users
- Security Groups
- Microsoft 365 Groups
---
### Publish or Update the App
After publishing:
✅ Each audience sees only its assigned content.
---
## Licensing Requirements
### Creating or Updating Apps
Requires:
- Power BI Pro
- Power BI Premium Per User (PPU)
### Limits
- Maximum 25 audiences per app
- Maximum 10,000 users/groups per app
### Best Practice
Use Security Groups instead of individual users.
Benefits:
- Better scalability
- Easier administration
- Simplified access management
---
# Understanding Org Apps
## What Are Org Apps?
Org Apps are a Microsoft Fabric feature that provides greater flexibility than traditional Workspace Apps.
### Key Advantages
✅ Multiple apps per workspace
✅ Immediate updates
✅ No installation required
✅ Supports additional Fabric content types
---
## Supported Content Types
Org Apps can include:
- Power BI Reports
- Paginated Reports
- Fabric Notebooks
- Maps
- Real-Time Dashboards
---
## Example
A single workspace could contain:
### Sales Org App
- Sales Dashboard
- Revenue Report
- Territory Analysis
### Finance Org App
- Profit Dashboard
- Budget Report
- Cost Analysis
### Executive Org App
- KPI Dashboard
- Strategic Metrics
All created from one workspace.
---
# Org Apps vs Workspace Apps
| Feature | Workspace Apps | Org Apps |
|----------|---------------|-----------|
| Apps per Workspace | One | Multiple |
| Publishing Required | Yes | No |
| Installation Required | Yes | No |
| Updates Visible | After Publish | Immediately After Save |
| Content Types | Mostly Power BI | Broader Fabric Content |
---
## Workflow Comparison
### Workspace App
```text
Create → Test → Publish → Users See Changes
```
### Org App
```text
Create → Save → Users Immediately See Changes
```
---
# Creating an Org App
## Prerequisites
### Tenant Setting
A Fabric Administrator must enable:
```text
Users can discover and create org apps
```
---
### Supported Workspace Types
- Pro
- Fabric Trial
- Premium Capacity
- Fabric Capacity
Not Supported:
❌ Standard Free Workspaces
---
### Required Role
Minimum role:
✅ Contributor
Viewer role cannot create Org Apps.
---
## Create an Org App
### Step 1
Navigate to:
```text
Workspace → New → Org App
```
---
### Step 2
Configure:
- App Name
- Theme Colors
- Navigation
- Landing Experience
---
### Step 3
Add Content
Examples:
- Reports
- Dashboards
- Notebooks
- Maps
---
### Step 4
Save
Unlike Workspace Apps:
❌ No Publish Button
Changes become immediately available after saving.
---
# Managing Org App Audiences
Audiences allow different groups to see different content within the same Org App.
Examples:
- Sales Audience
- Finance Audience
- HR Audience
- Executive Audience
Administrators can:
- Create audience groups
- Show or hide content
- Assign users and groups
- Duplicate audience configurations
A major advantage is that audience management can be performed without full edit mode.
---
# Choosing Between Workspace Apps and Org Apps
## Use Workspace Apps When
✅ A review and approval process is required
✅ Changes should not be immediately visible
✅ A stable production version is important
✅ Release timing must be controlled
---
## Use Org Apps When
✅ Multiple apps are needed from one workspace
✅ Users require instant updates
✅ Additional Fabric content must be included
✅ Users should not install apps
✅ Different teams require different content
---
## Quick Decision Guide
### Workspace App
📦 Draft → Review → Publish
### Org App
⚡ Save → Immediately Available
### Workspace App
🏢 One App per Workspace
### Org App
🏬 Multiple Apps per Workspace
---
# Applying Data Governance Principles
## Overview
Data Governance ensures organizational data remains:
- Trusted
- Secure
- High Quality
- Compliant
Two key governance capabilities in Power BI are:
1. Content Endorsement
2. Sensitivity Labels
---
# Endorse Your Content
## What Is Content Endorsement?
Content endorsement helps users identify trusted reports, dashboards, and semantic models.
This improves discoverability and encourages consistent reporting.
---
## Types of Endorsements
### Promotion
Promotion indicates that content is valuable and recommended for broader use.
#### Who Can Promote?
Users with:
- Write Permissions
- Workspace Member Access
- Content Ownership
#### Trust Level
Medium
#### Example
A Sales Analyst promotes a high-quality sales dashboard.
---
### Certification
Certification is the highest level of endorsement.
Certified content is considered:
- Trusted
- Approved
- Authoritative
- Official
#### Who Can Certify?
Only authorized reviewers designated by Power BI Administrators.
#### Trust Level
Highest
#### Example
An officially validated Financial Reporting Dataset.
---
## Promotion vs Certification
### Promotion
- Recommended Content
- Approved by Owner or Contributor
- Medium Trust
### Certification
- Official Organizational Content
- Approved by Authorized Reviewer
- Highest Trust
---
## Benefits of Endorsements
- Improved trust
- Better discoverability
- Consistent reporting
- Faster report development
Badges appear in:
- Power BI Service
- Search Results
- Workspace Lists
- Semantic Model Searches
- Power BI Desktop
---
# Applying Sensitivity Labels
## What Are Sensitivity Labels?
Sensitivity Labels classify and protect sensitive information.
They are powered by:
**Microsoft Purview Information Protection**
---
## Common Labels
### Public
Information can be freely shared.
### General
Standard internal business information.
### Confidential
Restricted business information.
### Highly Confidential
Highly sensitive organizational or customer data.
---
## Applying Labels in Power BI Service
### Step 1
Open:
- Report
- Dashboard
- Semantic Model
- Dataflow
### Step 2
Select:
```text
More Options (...)
```
### Step 3
Open Settings
### Step 4
Select:
```text
Sensitivity Label
```
### Step 5
Choose the appropriate label.
Example:
- Confidential
- Highly Confidential
---
## Label Persistence
Labels remain attached when exported to:
- Excel
- PowerPoint
- PDF
### Example
A report labeled **Confidential** remains confidential when exported to Excel.
---
## Applying Labels in Power BI Desktop
1. Open Power BI Desktop
2. Select **Sensitivity**
3. Choose a label
4. Save the PBIX file
### Result
The label:
- Is stored in the PBIX file
- Appears in the status bar
- Is inherited when published
---
# Exam Tips
✅ Viewer is the only workspace role where RLS is enforced.
✅ Workspace access grants access to all workspace content.
✅ Item-level sharing provides report-specific access.
✅ Contributors can create, edit, and delete content.
✅ Members can manage app distribution.
✅ Admins have full workspace control.
✅ Power BI Apps provide controlled content distribution.
✅ Org Apps support multiple apps per workspace.
✅ Workspace App changes require republishing.
✅ Org App changes become visible immediately after saving.
✅ Promotion indicates recommended content.
✅ Certification identifies officially approved content.
✅ Sensitivity labels stay attached during exports.
✅ Security Groups are preferred over assigning individual users.
---
# Conclusion
Power BI offers multiple sharing and distribution capabilities designed for different business scenarios. Workspace Roles facilitate collaboration, Item-Level Sharing provides granular access control, Power BI Apps support curated content distribution at scale, and Org Apps deliver a flexible modern experience for Microsoft Fabric environments.
To strengthen governance, organizations should leverage content endorsements to promote trusted datasets and use sensitivity labels to protect confidential information. Combined, these features create a secure, scalable, and user-friendly analytics ecosystem that supports both business users and administrators.
