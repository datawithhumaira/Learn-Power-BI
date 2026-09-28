# Understand Sharing Models in Power BI
 
## Overview
Power BI provides multiple ways to share reports, dashboards, and semantic models while controlling user access and permissions.
 
### Main Sharing Methods
1. Workspace Roles
2. Item-Level Sharing
3. Power BI Apps
4. Org Apps
 
---
 
# 1. Workspace Roles
 
Workspace roles determine what users can do within a Power BI workspace.
 
## Viewer
 
### Permissions
- View reports and dashboards
- Interact with visuals and filters
- Cannot edit content
 
### Key Point
- Row-Level Security (RLS) is enforced only for Viewers.
 
### Example
A manager who only needs to review business reports.
 
---
 
## Contributor
 
### Permissions
- Create reports
- Edit reports
- Delete reports and semantic models
 
### Restrictions
- Cannot manage workspace settings
- Cannot assign roles to users
 
### Example
A data analyst responsible for building reports.
 
---
 
## Member
 
A Member has all Contributor permissions plus additional capabilities.
 
### Permissions
- Add users as Viewer or Contributor
- Publish and unpublish apps
- Change app permissions
 
### Restrictions
- Cannot remove users
- Cannot modify existing role assignments
 
### Example
A team lead managing report distribution.
 
---
 
## Admin
 
### Permissions
- Full workspace control
- Manage permissions
- Assign and remove roles
- Delete workspace
- Configure workspace settings
 
### Example
Workspace owners or IT administrators.
 
---
 
## Important Limitation of Workspace Roles
 
Workspace access is **all-or-nothing**.
 
If a user has access to a workspace, they can access all reports, dashboards, and semantic models inside that workspace.
 
### Analogy
Giving workspace access is like giving someone a key to an entire building rather than a single room.
 
---
 
# 2. Item-Level Sharing
 
Item-level sharing allows you to share specific content rather than the whole workspace.
 
### You Can Share
- Individual reports
- Individual dashboards
 
### User Capabilities
- View content
- Interact with content
- Use filters and slicers
 
### Restrictions
- Cannot edit the shared content
 
---
 
## Security Considerations
 
When a report is shared, users may also gain access to the underlying semantic model.
 
### Row-Level Security (RLS)
 
RLS ensures users can only view data they are authorized to access.
 
### Example
 
A sales report includes:
 
- UAE Sales
- Saudi Sales
- Egypt Sales
 
With RLS:
 
- UAE manager sees only UAE data.
- Saudi manager sees only Saudi data.
 
---
 
## Sharing Options
 
### 1. People in Your Organization
Anyone in the organization can access the content.
 
### 2. People with Existing Access
Only users who already have permission can access the content.
 
### 3. Specific People
Only selected users or groups can access the content.
 
---
 
## Advantage of Item-Level Sharing
 
Item-level sharing overcomes the all-or-nothing limitation of workspace roles.
 
### Example
 
Workspace contains:
- Finance Report
- Sales Report
- HR Report
 
You can share only the Sales Report with an external partner while keeping the other reports private.
 
---
 
# 3. Power BI Apps
 
Power BI Apps allow you to package multiple reports and dashboards into a single application for users.
 
---
 
## Advantages
 
### Easy Distribution
Share one app instead of multiple reports.
 
### Better User Experience
All related content is organized in one place.
 
### Centralized Access
Users access dashboards and reports through a single application.
 
### Controlled Updates
Changes can be tested in the workspace before being published to users.
 
---
 
## Publishing Process
 
1. Develop content in the workspace.
2. Test changes.
3. Publish the app.
4. Users access the finalized version.
 
---
 
## Example
 
A Retail Analytics App may contain:
 
- Sales Dashboard
- Product Performance Report
- Inventory Dashboard
- Regional Sales Analysis
 
Users access everything through one app.
 
---
 
## Limitation
 
- Each workspace can publish only one Workspace App.
- All app content must come from the same workspace.
 
---
 
# 4. Org Apps
 
Org Apps are a newer Microsoft Fabric feature and an alternative to Workspace Apps.
 
---
 
## Advantages
 
### Multiple Apps per Workspace
 
One workspace can publish several apps:
 
- Sales App
- Finance App
- Executive App
 
### More Content Types
 
Org Apps can include:
 
- Reports
- Dashboards
- Notebooks
- Real-Time Dashboards
- Other Fabric Items
 
### Direct Updates
 
Changes can be pushed directly to users without a separate publishing process.
 
---
 
# Workspace Roles vs Item-Level Sharing
 
## Workspace Roles
 
**Best For:** Internal collaboration
 
### Characteristics
- Access to entire workspace
- Easy administration
- Less granular control
 
---
 
## Item-Level Sharing
 
**Best For:** Sharing specific reports securely
 
### Characteristics
- Access to selected reports or dashboards
- Better security
- More granular control
 
---
 
# Exam Tips
 
✅ Viewer is the only workspace role where RLS is enforced.
 
✅ Contributor can create, edit, and delete content.
 
✅ Member can manage app distribution and add users at Contributor level or below.
 
✅ Admin has complete workspace control.
 
✅ Workspace roles provide access to all workspace content.
 
✅ Item-level sharing provides access to specific reports or dashboards.
 
✅ Power BI Apps are used to distribute curated content to large groups.
 
✅ Org Apps allow multiple targeted apps from a single workspace.
 
---
 
# Memory Trick
 
🏢 Workspace Role = Entire Building
 
🚪 Item-Level Sharing = One Room
 
📱 Power BI App = Guided Tour of Multiple Rooms
 
🌐 Org App = Multiple Customized Tours for Different Audiences
 
---
 
# One-Line Summary
 
Use **Workspace Roles** for collaboration, **Item-Level Sharing** for report-specific access, **Power BI Apps** for large-scale distribution, and **Org Apps** when you need multiple targeted apps from the same workspace.

# Create a Power BI App
 
## Overview
 
Power BI Apps allow organizations to distribute reports, dashboards, and other Power BI content to users in a controlled and organized way.
 
### Real-World Example
 
A company has:
 
- Sales Team
- Marketing Team
 
Each team needs access to different reports.
 
Instead of creating multiple workspaces, a single Power BI App can be used with different audiences so that each team sees only the content relevant to them.
 
---
 
# 1. Create a Power BI App
 
Creating a Power BI App involves three main steps.
 
## Step 1: Set Up the App
 
From the workspace:
 
1. Select **Create App**.
2. Enter:
- App Name
- Description
- Theme Color (Optional)
- Support Site Link (Optional)
- Contact Information (Optional)
 
### App-Scoped Copilot (Preview)
 
You can enable **App-Scoped Copilot** during setup.
 
Benefits:
- Ask questions about app reports.
- Generate report summaries.
- Search across app content.
 
### Requirement
 
Fabric Copilot must be enabled at the tenant level.
 
---
 
## Step 2: Add Content
 
Go to the **Content** tab.
 
Select **Add Content** and include:
 
- Dashboards
- Reports
- Other workspace items
 
### Best Practice
 
Arrange content in a logical order so users can easily navigate the app.
 
---
 
## Step 3: Publish the App
 
After setup is complete:
 
1. Click **Publish App**.
2. Power BI generates a shareable link.
3. Distribute the link to users.
 
### Result
 
Users can access all published content through the app.
 
---
 
# 2. Update a Power BI App
 
Updating an app allows you to modify content without immediately impacting users.
 
---
 
## Step 1: Open Workspace
 
Navigate to the workspace.
 
Select the **Edit App** (pencil icon).
 
---
 
## Step 2: Make Changes
 
You can:
 
- Add reports
- Remove reports
- Reorganize content
- Change app settings
 
### Important
 
Changes stay in the workspace and are not visible to users until republished.
 
---
 
## Step 3: Republish
 
Click **Update App**.
 
### Result
 
Users automatically receive the latest version of the app.
 
---
 
# 3. Unpublish a Power BI App
 
If the app is no longer needed:
 
1. Open the workspace.
2. Click **More Options (...)**
3. Select **Unpublish App**
 
---
 
## Impact of Unpublishing
 
### Removed
 
- App access for all users
- User bookmarks
- User comments
- User customizations
 
### Not Removed
 
- Workspace
- Reports
- Dashboards
- Semantic Models
 
The content remains safely stored inside the workspace.
 
---
 
# 4. Audiences in Power BI Apps
 
## What is an Audience?
 
An Audience is a group of users that can see a specific set of content inside a Power BI App.
 
Different audiences can see different reports within the same app.
 
---
 
## Example
 
A company creates one app.
 
### Sales Audience
 
Can see:
- Sales Dashboard
- Revenue Report
- Territory Performance Report
 
### Marketing Audience
 
Can see:
- Campaign Dashboard
- Lead Analysis Report
- Customer Engagement Report
 
### Finance Audience
 
Can see:
- Financial Dashboard
- Profit Analysis Report
 
Each group sees only the content assigned to them.
 
---
 
# Why Use Audiences?
 
## Benefit 1: Better Security
 
Users only see information relevant to their role.
 
---
 
## Benefit 2: Easier Management
 
Instead of creating:
 
- Multiple Apps
- Multiple Workspaces
 
Manage everything from one app.
 
---
 
## Benefit 3: Centralized Administration
 
One app can serve many departments while maintaining separate visibility settings.
 
---
 
# How to Create Audiences
 
## Step 1: Create Audience Group
 
During app creation or editing:
 
1. Open the **Audience** tab.
2. Select **New Audience**.
3. Enter a name.
 
### Examples
 
- Sales
- Marketing
- Finance
- Executives
 
---
 
## Step 2: Customize Content Visibility
 
Use:
 
- Show Icon 👁️
- Hide Icon 🚫
 
to determine which content is visible.
 
### Important
 
Hidden items will not appear for that audience.
 
---
 
## Step 3: Assign Users or Groups
 
In **Manage Audience Access**:
 
Add:
 
- Individual Users
- Security Groups
- Microsoft 365 Groups
 
You can also configure advanced permissions such as:
 
- Sharing content
- Building reports using semantic models
 
---
 
## Step 4: Publish the App
 
Publish or update the app.
 
### Result
 
Each audience sees only the content assigned to them.
 
---
 
# Audience Example
 
## App Content
 
- Sales Dashboard
- Marketing Dashboard
- Finance Dashboard
 
### Sales Audience
 
✅ Sales Dashboard
 
❌ Marketing Dashboard
 
❌ Finance Dashboard
 
---
 
### Marketing Audience
 
✅ Marketing Dashboard
 
❌ Sales Dashboard
 
❌ Finance Dashboard
 
---
 
### Finance Audience
 
✅ Finance Dashboard
 
❌ Sales Dashboard
 
❌ Marketing Dashboard
 
---
 
# Licensing Requirements
 
To Create or Update Apps:
 
You need:
 
- Power BI Pro License
OR
- Power BI Premium Per User (PPU)
 
---
 
# Audience Limits
 
## Maximum Audience Groups
 
Up to **25 audiences** per app.
 
---
 
## Maximum Access Entries
 
Up to **10,000 users and groups combined**.
 
---
 
## Best Practice
 
Use Security Groups instead of individual users.
 
Benefits:
 
- Easier administration
- Better scalability
- Helps stay within limits
 
---
 
# App Viewing Requirements
 
## Scenario 1: Workspace Not in Premium Capacity
 
All users must have:
 
- Power BI Pro
OR
- Power BI PPU
 
to access the app.
 
---
 
## Scenario 2: Workspace in Premium Capacity (F64+)
 
Users without Pro or PPU licenses can:
 
✅ View app content
 
But cannot:
 
❌ Copy reports
 
❌ Create reports from semantic models
 
---
 
# Create vs Update vs Unpublish
 
## Create App
 
Purpose:
- Build a new app
 
Key Action:
- Publish App
 
---
 
## Update App
 
Purpose:
- Modify existing content
 
Key Action:
- Update App
 
---
 
## Unpublish App
 
Purpose:
- Remove app access
 
Key Action:
- Unpublish App
 
---
 
# Exam Tips
 
✅ Create App → Setup → Add Content → Publish.
 
✅ Changes are not visible until **Update App** is selected.
 
✅ Unpublishing removes the app but keeps workspace content.
 
✅ Audiences control who sees specific reports.
 
✅ One app can have up to **25 audience groups**.
 
✅ Apps can support up to **10,000 users/groups**.
 
✅ Security Groups are recommended over individual users.
 
✅ Users without Pro licenses can view apps only when content is in Premium Capacity.
 
---
 
# Memory Trick
 
📦 Power BI App = Package of Reports
 
👥 Audience = Who Can Open Which Reports
 
📝 Create App = Build + Publish
 
🔄 Update App = Edit + Republish
 
🗑️ Unpublish App = Remove Access, Keep Content
 
---
 
# One-Line Summary
 
Use a Power BI App to distribute reports at scale, and use Audiences to ensure each team only sees the content relevant to them while managing everything from a single app.

# Create and Manage Org Apps
 
## Overview
 
Org Apps are a newer way to package and distribute content in Microsoft Fabric.
 
They serve a similar purpose to Power BI Workspace Apps but offer greater flexibility.
 
### Key Advantage
 
Unlike Workspace Apps, a workspace can have **multiple Org Apps**, allowing different teams to receive different sets of content without creating multiple workspaces.
 
---
 
# 1. What Are Org Apps?
 
An Org App is a Microsoft Fabric item that allows content creators to package and share content across an organization.
 
Unlike Workspace Apps:
 
✅ Multiple Org Apps can exist in one workspace.
 
✅ Updates are visible immediately after saving.
 
✅ Users do not need to install the app.
 
✅ Supports more Fabric content types.
 
---
 
## Content Supported in Org Apps
 
An Org App can include:
 
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
 
All created from the same workspace.
 
---
 
# 2. Org Apps vs Workspace Apps
 
## Workspace App
 
### Characteristics
 
- Only one app per workspace
- Requires publishing
- Users must install the app
- Updates are visible only after republishing
 
---
 
## Org App
 
### Characteristics
 
- Multiple apps per workspace
- No publishing required
- Users do not install apps
- Updates appear immediately after saving
 
---
 
# Key Difference
 
## Workspace App
 
Flow:
 
Create → Test → Publish → Users See Changes
 
---
 
## Org App
 
Flow:
 
Create → Save → Users Immediately See Changes
 
---
 
# 3. Benefits of Org Apps
 
## Benefit 1: Multiple Apps per Workspace
 
One workspace can support many teams.
 
### Example
 
Workspace contains data for:
 
- Sales
- Finance
- HR
- Operations
 
Instead of one large app:
 
Create separate Org Apps for each department.
 
---
 
## Benefit 2: Immediate Updates
 
Changes become visible immediately after saving.
 
No extra publish step is required.
 
---
 
## Benefit 3: More Content Types
 
Org Apps support:
 
- Reports
- Notebooks
- Maps
- Real-Time Dashboards
 
Workspace Apps mainly focus on Power BI content.
 
---
 
## Benefit 4: No Installation Required
 
Users receive access through sharing.
 
The Org App automatically appears in:
 
- Home
- Recent
- Item Lists
 
---
 
## Benefit 5: Easier Access Management
 
When sharing reports:
 
Access automatically extends to related semantic models, even when those models exist in another workspace.
 
This reduces manual permission management.
 
---
 
# 4. Prerequisites for Creating Org Apps
 
Before creating an Org App, three requirements must be met.
 
---
 
## Requirement 1: Tenant Setting Enabled
 
A Fabric Administrator must enable:
 
**Users can discover and create org apps**
 
Location:
 
Fabric Admin Portal →
 
Tenant Settings →
 
Users can discover and create org apps
 
---
 
### Administrator Control
 
Admins can:
 
✅ Allow security groups
 
✅ Exclude security groups
 
✅ Control who can create Org Apps
 
---
 
## Requirement 2: Supported Workspace Type
 
The workspace must be one of the following:
 
- Pro
- Fabric Trial
- Premium Capacity
- Fabric Capacity
 
---
 
### Not Supported
 
❌ Standard Free Workspaces
 
---
 
## Requirement 3: Workspace Role
 
Minimum Required Role:
 
✅ Contributor
 
---
 
### Viewer
 
❌ Cannot create Org Apps
 
---
 
### Member/Admin
 
Required for:
 
- Access management changes
- Adding or removing content access
- Permissions administration
 
---
 
# 5. Create an Org App
 
## Step 1: Open Workspace
 
Go to the workspace containing your content.
 
Select:
 
**New → Org App**
 
---
 
## Step 2: Configure App
 
Provide:
 
- App Name
- Theme Colors (Optional)
- Navigation Settings
- Landing Page Experience
 
---
 
## Step 3: Add Content
 
Add the items you want to share.
 
These are called:
 
### Included Items
 
Examples:
 
- Reports
- Dashboards
- Notebooks
- Maps
 
---
 
## Access Behavior
 
When users receive the Org App:
 
They automatically receive:
 
✅ Read access to included items
 
✅ Access to associated semantic models
 
Even if semantic models exist in another workspace.
 
---
 
# 6. Save the Org App
 
After configuration:
 
Click **Save**
 
---
 
## Important
 
There is:
 
❌ No Publish Button
 
Unlike Workspace Apps.
 
---
 
### Result
 
Changes become immediately visible to users who already have access.
 
---
 
# 7. Share the Org App
 
After saving:
 
Select **Share**
 
Add:
 
- Individual Users
- Security Groups
- Microsoft 365 Groups
 
---
 
## Optional Permission
 
### Reshare
 
You can allow users to:
 
✅ Share the Org App with others
 
---
 
# Example
 
Share:
 
Sales Org App
 
With:
 
- Sales Team
- Regional Managers
- Sales Leadership Group
 
---
 
# 8. Audiences in Org Apps
 
## What Is an Audience?
 
An Audience is a defined group of users that sees a specific set of content inside the same Org App.
 
---
 
## Example
 
One Org App contains:
 
- Sales Dashboard
- Finance Dashboard
- HR Dashboard
 
Different audiences see different content.
 
---
 
### Sales Audience
 
✅ Sales Dashboard
 
❌ Finance Dashboard
 
❌ HR Dashboard
 
---
 
### Finance Audience
 
✅ Finance Dashboard
 
❌ Sales Dashboard
 
❌ HR Dashboard
 
---
 
### HR Audience
 
✅ HR Dashboard
 
❌ Sales Dashboard
 
❌ Finance Dashboard
 
---
 
# 9. Manage Audiences
 
Open the Org App Editor.
 
Select:
 
**Manage Audiences**
 
---
 
## Available Actions
 
### Create Audience Groups
 
Examples:
 
- Sales
- Finance
- Executives
- Operations
 
---
 
### Show or Hide Content
 
Use checkboxes to determine:
 
✅ Visible Items
 
❌ Hidden Items
 
for each audience.
 
---
 
### Assign Users
 
Add:
 
- Users
- Security Groups
- Microsoft 365 Groups
 
---
 
### Duplicate Audiences
 
Copy an existing audience configuration.
 
### Example
 
Create:
 
Sales Managers Audience
 
by copying:
 
Sales Audience
 
and making small modifications.
 
---
 
# Advantage Over Workspace Apps
 
Audience management can be performed without entering full edit mode.
 
This reduces the risk of accidentally modifying app content.
 
---
 
# 10. Choosing Between Org Apps and Workspace Apps
 
## Use Workspace Apps When
 
### 1. A Review-and-Publish Process Is Required
 
Workspace Apps are ideal when content must be reviewed, tested, and approved before users can see changes.
 
**Workflow:**
 
Create → Test → Publish → Users See Changes
 
### Example
 
Executive dashboards that require management approval before release.
 
---
 
### 2. You Want a Stable Production Version
 
Changes made in the workspace are not immediately visible to users.
 
This allows developers to:
 
- Test reports
- Fix issues
- Validate data
 
before publishing updates.
 
### Example
 
Monthly financial reports where accuracy is critical.
 
---
 
### 3. Controlled Release of Updates Is Important
 
Organizations can decide exactly when users receive new content.
 
### Example
 
A company releases updated KPI reports only on the first day of each month.
 
---
 
## Use Org Apps When
 
### 1. Multiple Apps Are Needed from One Workspace
 
A single workspace can host multiple Org Apps.
 
### Example
 
One workspace contains:
 
- Sales Content
- Finance Content
- HR Content
 
Create:
 
- Sales Org App
- Finance Org App
- HR Org App
 
without creating multiple workspaces.
 
---
 
### 2. Users Need Instant Updates
 
Changes become visible immediately after saving.
 
**Workflow:**
 
Create → Save → Users See Changes
 
### Example
 
Daily operational dashboards that change frequently.
 
---
 
### 3. You Need More Fabric Content Types
 
Org Apps support:
 
- Power BI Reports
- Paginated Reports
- Notebooks
- Maps
- Real-Time Dashboards
 
### Example
 
A Data Science team sharing notebooks and reports together.
 
---
 
### 4. Users Should Not Install an App
 
Org Apps automatically appear for users once shared.
 
### Example
 
Large organizations where managing app installations would be difficult.
 
---
 
### 5. Teams Need Different Content from the Same Workspace
 
Audience groups make it easy to show different content to different users.
 
### Example
 
Sales Team sees:
 
- Revenue Dashboard
- Territory Report
 
Finance Team sees:
 
- Budget Dashboard
- Cost Analysis Report
 
All from the same Org App.
 
---
 
# Quick Decision Guide
 
## Choose Workspace Apps If:
 
✅ You need a publish/review cycle
 
✅ Changes should not be immediately visible
 
✅ You want controlled release management
 
✅ Content requires approval before distribution
 
---
 
## Choose Org Apps If:
 
✅ You need multiple apps from one workspace
 
✅ Updates should appear instantly
 
✅ You need audience-based visibility
 
✅ You want to include Fabric content like notebooks and real-time dashboards
 
✅ Users should access content without installing apps
 
---
 
# Simple Memory Trick
 
📦 **Workspace App = Draft → Review → Publish**
 
⚡ **Org App = Save → Instantly Available**
 
🏢 **Workspace App = One App per Workspace**
 
🏬 **Org App = Multiple Apps per Workspace**
 
👥 **Org App = Better for Different Teams and Audiences**
 
---
 
# Exam Answer
 
**Workspace Apps** are best when you need a controlled publishing process and a stable production version.
 
**Org Apps** are best when you need multiple apps per workspace, immediate updates, audience-based content visibility, and support for broader Microsoft Fabric content.

# Apply Data Governance Principles
 
## Overview
 
Data Governance ensures that organizational data is:
 
✅ Trusted
 
✅ High Quality
 
✅ Secure
 
✅ Compliant with regulations
 
In Power BI, two important governance practices are:
 
1. Endorse Your Content
2. Apply Sensitivity Labels
 
These features help users identify trusted content and protect sensitive information.
 
---
 
# 1. Endorse Your Content
 
## What Is Content Endorsement?
 
Content endorsement helps users identify reliable and trustworthy Power BI content.
 
When users search through reports, dashboards, and semantic models, endorsements make high-quality content easier to find.
 
---
 
## Why Endorse Content?
 
Organizations often have:
 
- Hundreds of reports
- Multiple dashboards
- Many semantic models
 
Without endorsements, users may not know which content should be trusted.
 
Endorsements provide clear guidance.
 
---
 
# Types of Endorsements
 
Power BI provides two endorsement levels:
 
1. Promotion
2. Certification
 
---
 
# 2. Promotion
 
## What Is Promotion?
 
Promotion allows report owners and workspace contributors to identify content that is valuable and useful for others.
 
Promoted content is recommended for broader organizational use.
 
---
 
## Who Can Promote Content?
 
Users with:
 
✅ Write permissions
 
✅ Workspace member permissions
 
✅ Content owner permissions
 
can promote content.
 
---
 
## Purpose of Promotion
 
Promotion indicates:
 
"This content is useful and recommended."
 
It does not necessarily mean the content has passed formal organizational review.
 
---
 
## Example
 
A Sales Analyst creates a high-quality sales dashboard.
 
The analyst promotes it so other business users can easily find and use it.
 
---
 
## Visual Indicator
 
Promoted content displays a:
 
🏷️ Promotion Badge
 
This badge appears in:
 
- Search Results
- Content Lists
- Semantic Model Searches
 
---
 
# 3. Certification
 
## What Is Certification?
 
Certification is a higher level of endorsement.
 
Certified content is considered:
 
✅ Trusted
 
✅ Approved
 
✅ Authoritative
 
✅ Official
 
---
 
## Who Can Certify Content?
 
Only authorized reviewers designated by Power BI Administrators.
 
Regular users cannot certify content.
 
---
 
## Purpose of Certification
 
Certification indicates:
 
"This content meets organizational quality standards."
 
---
 
## Example
 
The Finance Department has an official revenue dataset.
 
After validation by governance reviewers, it receives certification.
 
All users know that this dataset should be used for official reporting.
 
---
 
## Visual Indicator
 
Certified content displays a:
 
✅ Certification Badge
 
The badge is visible throughout Power BI.
 
---
 
# Promotion vs Certification
 
## Promotion
 
### Meaning
 
Recommended content
 
### Who Approves?
 
Content owner or contributor
 
### Trust Level
 
Medium
 
### Example
 
Helpful team dashboard
 
---
 
## Certification
 
### Meaning
 
Official and authoritative content
 
### Who Approves?
 
Authorized certifier
 
### Trust Level
 
Highest
 
### Example
 
Official financial reporting dataset
 
---
 
# Why Endorse Content?
 
## Benefit 1: Improved Trust
 
Users can quickly identify reliable content.
 
---
 
## Benefit 2: Better Discoverability
 
Endorsed content appears more prominently in searches.
 
---
 
## Benefit 3: Consistent Reporting
 
Everyone uses the same trusted datasets.
 
---
 
## Benefit 4: Faster Report Development
 
Report creators can easily locate certified semantic models.
 
---
 
# Where Are Endorsements Visible?
 
Badges appear in:
 
✅ Power BI Service
 
✅ Search Results
 
✅ Workspace Lists
 
✅ Semantic Model Searches
 
✅ Power BI Desktop
 
---
 
## Example
 
When creating a report:
 
1. Open Power BI Desktop.
2. Connect to a semantic model.
3. Search available datasets.
 
Certified datasets are clearly marked, making them easier to choose.
 
---
 
# 4. Apply Sensitivity Labels
 
## What Are Sensitivity Labels?
 
Sensitivity Labels classify and protect sensitive information.
 
They are powered by:
 
**Microsoft Purview Information Protection**
 
---
 
## Purpose
 
Sensitivity labels help organizations:
 
- Protect confidential data
- Prevent accidental exposure
- Meet compliance requirements
- Guide users on proper data handling
 
---
 
# Common Sensitivity Labels
 
Examples include:
 
### Public
 
Information can be shared freely.
 
---
 
### General
 
Standard business information.
 
---
 
### Confidential
 
Restricted information requiring protection.
 
---
 
### Highly Confidential
 
Highly sensitive business or customer information.
 
---
 
# Example
 
A customer database contains:
 
- Customer Names
- Phone Numbers
- Financial Information
 
Apply:
 
🔒 Highly Confidential
 
to ensure proper protection.
 
---
 
# Applying Sensitivity Labels in Power BI Service
 
## Step 1
 
Open:
 
- Report
- Dashboard
- Semantic Model
- Dataflow
 
---
 
## Step 2
 
Select:
 
**More Options (...)**
 
---
 
## Step 3
 
Open Settings.
 
---
 
## Step 4
 
Choose:
 
**Sensitivity Label**
 
---
 
## Step 5
 
Select an appropriate label.
 
Example:
 
- Confidential
- Highly Confidential
 
---
 
## Result
 
The label becomes visible within Power BI.
 
---
 
# Label Persistence
 
One major advantage is that labels travel with the data.
 
This means protection remains applied after export.
 
---
 
## Supported Exports
 
Labels remain attached when exporting to:
 
- Excel
- PowerPoint
- PDF
 
---
 
## Example
 
A report labeled:
 
🔒 Confidential
 
is exported to Excel.
 
The exported file keeps the Confidential label and associated protection settings.
 
---
 
# Applying Sensitivity Labels in Power BI Desktop
 
Sensitivity labels can also be applied directly to:
 
### .pbix Files
 
---
 
## Steps
 
1. Open Power BI Desktop.
2. Select **Sensitivity** on the toolbar.
3. Choose a label.
4. Save the file.
 
---
 
## Result
 
The label is:
 
✅ Stored in the PBIX file
 
✅ Displayed in the status bar
 
✅ Applied when published
 
---
 
# Publishing a Labeled PBIX File
 
When a labeled PBIX file is published:
 
The associated:
 
- Report
- Semantic Model
 
inherit the same sensitivity label.
 
---
 
Examples:
 
- Views
- Unique Viewers
- Usage Trends
 
---
 
## Performance Metrics
 
Purpose:
 
Measure report responsiveness.
 
Question Answered:
 
"Is the report performing well?"
 
Examples:
 
- Load Time
- Performance Trends
- Browser Performance
 
---
 
# Exam Tips
 
✅ Usage Metrics require Power BI Pro or PPU.
 
✅ Contributor role or higher is required.
 
✅ Viewer role cannot access Usage Metrics.
 
✅ Fabric Admin must enable Usage Metrics.
 
✅ Subscriptions can be scheduled hourly, daily, weekly, or monthly.
 
✅ Subscription emails can include report snapshots and links.
 
✅ Premium Capacity reports can include PDF or PowerPoint attachments.
 
✅ Usage Metrics track views and unique viewers.
 
✅ Performance Metrics help identify slow reports and improve user experience.
 
---
 
# Memory Trick
 
📧 Subscription = "Send Reports Automatically"
 
👀 Views = "How Many Times"
 
👤 Unique Viewers = "How Many People"
 
📈 Usage Metrics = "Is Anyone Using It?"
 
⚡ Performance Metrics = "How Fast Is It?"
 
---
 
# One-Line Summary
 
Use **Subscriptions** to automatically deliver reports and dashboards to users, and use **Usage Metrics and Performance Monitoring** to measure engagement, identify valuable reports, and ensure a fast user experience.
