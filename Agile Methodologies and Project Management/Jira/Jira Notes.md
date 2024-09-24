#  1. Introduction to Jira

   1.1 What is Jira?  
   1.2 History and evolution of the tool  
   1.3 Types of projects supported in Jira  
       1.3.1 Software Projects  
       1.3.2 Business Projects  
       1.3.3 Service Management Projects  
   1.4 Agile methodologies and Jira  
       1.4.1 Scrum  
       1.4.2 Kanban  
## 1.1 What is Jira?
### About Jira
- Launched year: 2002
- Company: Atlassian
- Origin Australian
- Primary purpose: to help developers manage and track bugs. 
## 1.3 Types of Projects Supported in Jira
The types comes with its own set of templates, workflows, and reporting tools tailored to specific needs and are generally classified into three categories: 
- Software Projects,
- Business Projects, 
- Service Management Projects.
### 1.3.1 Software Projects

- follow agile methodologies like Scrum or Kanban
- are built around managing 
	- backlogs, 
	- sprints, 
	- epics, 
	- user stories, 
	- tasks.
Key features include:
- **Backlog management**: For tracking features and bugs.
- **Sprint planning**: To help teams define time-boxed iterations.
- **Version and release tracking**: To manage software releases.
- **Integration with development tools**: Such as Bitbucket, GitHub, and CI/CD pipelines.

### 1.3.2 Business Projects

Business Projects in Jira are designed for non-technical teams that still require structured project management. These projects can be used by HR, marketing, finance, and other business departments to manage workflows that don’t necessarily follow the software development lifecycle.

Key features include:
- **Task management**: For tracking general tasks and deliverables.
- **Simple workflows**: Customizable for different types of business processes like approvals, marketing campaigns, and hiring.
- **Deadline tracking**: To ensure milestones are met.
- **Custom reports and dashboards**: For business performance tracking.

Business Projects are focused on efficiency and communication, helping teams organize their day-to-day operations and maintain visibility into ongoing initiatives.

### 1.3.3 Service Management Projects

Service Management Projects (Jira Service Management) are tailored to IT and operations teams managing service requests, incidents, and problem tickets. They provide features aligned with ITIL (Information Technology Infrastructure Library) best practices, enabling IT teams to offer high-quality service delivery.

Key features include:
- **Service desk portals**: Allowing users to submit tickets for issues or requests.
- **SLA (Service Level Agreements) management**: For ensuring service requests are resolved within agreed timeframes.
- **Incident and problem management**: To track, categorize, and resolve IT issues.
- **Automation**: To streamline request handling and ensure SLAs are met.

These projects are often used in conjunction with tools like Confluence (for knowledge bases) and Opsgenie (for incident response).

## 1.4 Agile Methodologies and Jira
 Allow teams to plan and track workflow with 
- Scrum
- Kanban
- Customizable workflows
Jira provides teams with reporting tools, making it easy report on progress.

### 1.4.1 Scrum

Scrum is an iterative, time-boxed framework used to manage complex software development projects. In Scrum, work is broken down into sprints, which are usually 1-4 week intervals. The goal is to complete a set of tasks during each sprint and deliver a potentially shippable product increment at the end.

In Jira, a **Scrum Board** helps teams visualize their work throughout a sprint:
- **Backlog**: Teams can create, prioritize, and estimate issues (like user stories or bugs) in the backlog.
- **Sprint Planning**: During sprint planning, teams move issues from the backlog to an active sprint.
- **Sprint Execution**: Teams track their progress during the sprint using burndown charts and sprint reports.
- **Sprint Retrospective**: After each sprint, the team reflects on their performance and identifies areas for improvement.

Key Scrum concepts in Jira:
- **Epics**: Larger bodies of work that can be broken down into smaller user stories.
- **User Stories/Tasks**: Short descriptions of features or functionality from the perspective of the user.
- **Burndown Charts**: Used to visualize progress and ensure that the team is on track to complete the sprint.

### 1.4.2 Kanban

Kanban is a lean, continuous flow methodology that helps teams visualize their work and limit the amount of work in progress (WIP) at any given time. Unlike Scrum, Kanban does not use time-boxed iterations (sprints); instead, work is continuously pulled into the workflow as capacity becomes available.

In Jira, a **Kanban Board** represents the workflow and allows teams to visualize tasks as they move through different stages (columns) such as "To Do," "In Progress," and "Done." Teams can manage work-in-progress limits to prevent bottlenecks and ensure smooth task transitions.

Key Kanban concepts in Jira:
- **Continuous Flow**: Work items are pulled as team members have bandwidth.
- **Work-in-Progress Limits**: Limits on how many items can be in each workflow stage at a time.
- **Cumulative Flow Diagrams**: Visual tools to track bottlenecks and understand the state of the flow.

Both Scrum and Kanban boards in Jira can be customized to fit the specific needs of a team, making the tool highly adaptable to different workflows.
# 2. Jira Setup and Configuration

   2.1 Creating a Jira Account  
   2.2 Setting up a new project  
   2.3 Configuring project templates  
       2.3.1 Scrum Template  
       2.3.2 Kanban Template  
       2.3.3 Custom Templates  
   2.4 Project roles and permissions  
       2.4.1 Administrators  
       2.4.2 Developers  
       2.4.3 Project users  This section covers the foundational steps for setting up Jira, from creating an account to configuring your first project. Understanding these core elements will ensure a smooth start when implementing Jira for any team or organization.

## 2.1 Creating a Jira Account

Creating a Jira account is the first step in getting started with the platform. Jira offers both cloud-based and self-hosted (Jira Server/Data Center) versions. 

To create an account in **Jira Cloud**:
- Visit the Atlassian website (www.atlassian.com) and sign up for a Jira Cloud account using an email address. You can also choose to sign in using Google or Microsoft credentials.
- Choose a preferred domain (e.g., `yourteam.atlassian.net`) that your team will use to access Jira.
- Select the type of Jira product you'd like to use (Jira Software, Jira Work Management, or Jira Service Management).
- Once the account is created, you’ll have access to the Jira dashboard where you can begin configuring your workspace.

For **Jira Server/Data Center**:
- Download and install Jira on your server by following Atlassian's documentation.
- After installation, access Jira via a web browser to set up your instance and configure it.

## 2.2 Setting up a New Project

Once your account is created, the next step is setting up a project. A **project** in Jira is essentially a workspace where you can organize and manage all issues related to a specific product, department, or initiative. 

Steps to set up a new project:
1. **Access the Project Creation Page**: From the Jira dashboard, click on "Projects" and then "Create Project."
2. **Choose a Project Type**: Select between Software, Business, or Service Management projects, depending on the team's needs. Each type offers different templates and features.
3. **Select a Template**: Choose from the available templates (Scrum, Kanban, or custom templates) based on the team's workflow (this will be covered in more detail in section 2.3).
4. **Configure Project Details**: Name the project, assign a key (a unique identifier used in issues), and set the project type (Team-managed or Company-managed).
5. **Set Permissions**: Assign roles to users and configure who can access and modify the project. You can select default permission schemes or create custom permissions.

After setting up the project, Jira automatically generates the corresponding board, backlog (for Scrum/Kanban projects), and issue management interfaces.

## 2.3 Configuring Project Templates

Jira provides predefined templates based on common project management methodologies such as Scrum and Kanban. These templates come with built-in workflows, issue types, and reporting tools tailored to each methodology. There is also the option to create custom templates for more specialized workflows.

### 2.3.1 Scrum Template

The **Scrum Template** is ideal for teams that follow the Scrum methodology and work in sprints. This template comes pre-configured with elements that support sprint-based development:

- **Backlog**: A repository of tasks (user stories, bugs, etc.) that the team will work on in future sprints.
- **Sprint Planning**: An interface to plan and start sprints, moving issues from the backlog into the active sprint.
- **Sprint Board**: A visual representation of the team’s sprint, where tasks are moved across columns (To Do, In Progress, Done) as they are completed.
- **Reports**: Built-in reports like Burndown Charts, Velocity Charts, and Sprint Reports to track the team's progress.

Configuring a Scrum project involves defining the sprint length, managing backlog priorities, and adjusting workflows based on how the team operates.

### 2.3.2 Kanban Template

The **Kanban Template** supports continuous workflows, making it ideal for teams that don’t work in defined sprints but instead have ongoing tasks or support work.

Key features of the Kanban template:
- **Kanban Board**: A visual board that displays tasks as they move through the workflow stages (columns such as Backlog, To Do, In Progress, Done).
- **WIP (Work-in-Progress) Limits**: Configurable limits for each column to control the number of tasks that can be in progress at once.
- **Cumulative Flow Diagram**: A report that shows how tasks flow through the board, helping teams identify bottlenecks.

Configuring a Kanban project is more focused on defining appropriate columns and ensuring WIP limits are set to manage workflow efficiently.

### 2.3.3 Custom Templates

Jira also allows you to create **custom templates** for teams that don’t follow traditional Scrum or Kanban frameworks, or who need a more tailored project setup.

Key steps in setting up a custom template:
1. **Define Custom Workflows**: Create workflows that align with the team’s processes, such as multi-step approval processes or complex development pipelines.
2. **Custom Issue Types**: Create new issue types beyond the default (epic, story, task, bug). For example, a legal team might need issue types such as "Contract" or "Review."
3. **Configure Custom Fields**: Add fields specific to the team’s needs, such as due dates, risk levels, or estimated hours.
4. **Custom Boards**: Design your own boards with columns that reflect the stages in your workflow.

## 2.4 Permissions
## 2.4.1 Permission Scopes
There are three scope levels. The Atlassian account scope, the Product scope (Jira, for example) and the product scope.
#### 2.4.1.1. Atlassian account scope
In the Atlassian account, we can create, modify and exclude groups. The main purpose of the groups is to define what level of permissions the the member will be granted to access Atlassian products. Usually, there are more than one group defined to a product. One with administer role and another with just user role.
These groups will also be able to receive Jira global permissions and permissions in the permissions scheme of the projects.
#### 2.4.1.2. Jira Global Level Permissons

| Permission                                                        | Explanation                                                                                                                                                                                                                                  |
| ----------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Administer Jira**                                               | Create and administer projects, issue types, fields, workflows, and schemes for all projects. Users with this permission can perform most administration tasks, except managing users, importing data, and editing system email settings.    |
| **Browse users and groups**                                       | View and select users or groups from the user picker, and share issues. Users with this permission can see the names of all users and groups on your site.                                                                                   |
| **Share dashboards and filters**                                  | Share dashboards and filters with other users.                                                                                                                                                                                               |
| **Manage group filter subscriptions**                             | Create and delete group filter subscriptions.                                                                                                                                                                                                |
| **Make bulk changes**                                             | Modify collections of issues at once. For example, resolve multiple issues in one step.                                                                                                                                                      |
| **Atlassian Home for Jira Cloud project connection issue glance** | Enables the Atlassian Home for Jira Cloud issue glance field in issue sidebars, for connecting a Jira issue to a project overview.                                                                                                           |
| **Create team-managed projects**                                  | Create projects separate from shared configurations and schemes. Team-managed projects don't affect existing projects or shared configurations like workflows, fields, or permissions. Only licensed users can create team-managed projects. |

#### 2.4.1.3 Project Level Permissions

##### a. Premission Schemes

Project permissions in Jira are organized through **Permission Schemes**. **Each** project has **one** scheme that defines all the permission policies for it. **Schemes** can also be **shared** and used by multiple projects. This makes it easier to maintain a consistent permission structure across different projects, as changes to the **shared scheme** will apply to all the projects using it.

The structure is as follows:

**Permission Scheme**: 

A list of all permissions available to be granted. **Each** of these permissions can be granted to one or more of the following five entities: **Roles**, **Groups**, **Users**, **Applications**, and the **Public**, as detailed below:

**Entities:**

- **Roles**
  - One or more project roles.
- **Groups**
  - One or more groups.
  - One or more groups with a specific custom field value set in the its profile.
- **Users**
  - One or more individual users (called ***single user***).
  - Any user who is:
    - The current assignee.
    - Logged in (belongs to the project).
    - The reporter.
    - A user with a specific custom field value set in its profile.
    - The project lead.
    - Registered in the ***Service Project Customer - Portal Access***.
- **Applications**
  - External applications that integrate with Jira.
- **Public**
  - Any user with an Atlassian user account.

You can assign permissions to more than one **entity**.
These following entities require you to select the granted **holder** from a list:

- **Roles**
- **Groups**
- **Individual Users**
- **Applications**
- **Users and groups that have a certain value in a custom field**
##### b. Available Permisions
###### 1. Project Permissions

| Permission              | Explanation                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| ----------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Administer Projects     | Grants users full administrative control over a specific project in Jira. Users with this permission can:<br><br>- **Configure Project Details**: Modify the project's name, description, avatar, and project lead.<br>- **Manage Roles and Permissions**: Create, edit, and assign project roles; configure permission schemes to control what users can do within the project.<br>- **Customize Workflows**: Design and edit the workflows that dictate the life cycle of issues within the project.<br>- **Set Up Screens and Fields**: Customize issue screens by adding or removing fields; configure field behaviors and layouts.<br>- **Manage Issue Types**: Create and modify issue types and their associated schemes to organize different kinds of work.<br>- **Configure Notifications**: Set up notification schemes to control who gets email updates and when.<br>- **Handle Components and Versions**: Organize work by setting up components and fix versions for better project tracking.<br>- **Integrate Add-ons and Plugins**: Install and manage project-specific apps or plugins to enhance functionality.<br>- **Bulk Operations**: Perform bulk changes on issues, such as editing or transitioning multiple issues at once.<br><br>**Note:** This permission is confined to the project it is granted for and does not provide global administrative rights across all projects in Jira. |
| Browse Projects         | Ability to browse projects and the issues within them.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Manage sprints          | Ability to manage sprints.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Service Project Agent   | Allows users to interact with customers and access Jira Service Management features of a project.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| View aggregated data    | Users with this permission will have access to view combined and summarised project data, regardless of their individual permissions. [Learn more.](https://support.atlassian.com/jira-cloud-administration/docs/permissions-for-company-managed-projects/#Permissionsforcompanymanagedprojects-data)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| View Development Tools  | Allows users in a software project to view development-related information on the issue, such as commits, reviews and build information.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| View Read-Only Workflow | Users with this permission may view a read-only version of a workflow.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
###### 2. Issue Permissions

| Permission         | Explanation                                                                                                                                                                            |
| ------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Assignable User    | Users with this permission may be assigned to issues.                                                                                                                                  |
| Assign Issues      | Ability to assign issues to other people.                                                                                                                                              |
| Close Issues       | Ability to close issues. Often useful where your developers resolve issues, and a QA department closes them.                                                                           |
| Create Issues      | Ability to create issues.                                                                                                                                                              |
| Delete Issues      | Ability to delete issues.                                                                                                                                                              |
| Edit Issues        | Ability to edit issues.                                                                                                                                                                |
| Link Issues        | Ability to link issues together and create linked issues. Only useful if issue linking is turned on.                                                                                   |
| Modify Reporter    | Ability to modify the reporter when creating or editing an issue.                                                                                                                      |
| Move Issues        | Ability to move issues between projects or between workflows of the same project (if applicable). Note the user can only move issues to a project they have the create permission for. |
| Resolve Issues     | Ability to resolve and reopen issues. This includes the ability to set a fix version.                                                                                                  |
| Schedule Issues    | Ability to view or edit an issue's due date.                                                                                                                                           |
| Set Issue Security | Ability to set the level of security on an issue so that only people in that security level can see the issue.                                                                         |
| Transition Issues  | Ability to transition issues.                                                                                                                                                          |

###### 3. Voters & Watchers Permissions

| Permission               | Explanation                                          |
| ------------------------ | ---------------------------------------------------- |
| Manage Watchers          | Ability to manage the watchers of an issue.          |
| View Voters and Watchers | Ability to view the voters and watchers of an issue. |

###### 4. Comments Permissions

| Permission          | Explanation                                    |
| ------------------- | ---------------------------------------------- |
| Add Comments        | Ability to comment on issues.                  |
| Delete All Comments | Ability to delete all comments made on issues. |
| Delete Own Comments | Ability to delete own comments made on issues. |
| Edit All Comments   | Ability to edit all comments made on issues.   |
| Edit Own Comments   | Ability to edit own comments made on issues.   |

###### 5. Attachments Permissions

| Permission             | Explanation                                                  |
| ---------------------- | ------------------------------------------------------------ |
| Create Attachments     | Users with this permission may create attachments.           |
| Delete All Attachments | Users with this permission may delete all attachments.       |
| Delete Own Attachments | Users with this permission may delete their own attachments. |

###### 6. Time Tracking Permissions

| Permission          | Explanation                                    |
| ------------------- | ---------------------------------------------- |
| Delete All Worklogs | Ability to delete all worklogs made on issues. |
| Delete Own Worklogs | Ability to delete own worklogs made on issues. |
| Edit All Worklogs   | Ability to edit all worklogs made on issues.   |
### 2.4.3 Administrators

**Project Administrators** have the highest level of control within a project. Their responsibilities typically include:
- **Configuring project settings**: This includes managing project details like the name, key, workflows, issue types, and boards.
- **Managing users and roles**: Administrators can add or remove users from the project and assign roles to them.
- **Customizing workflows and permissions**: Admins can modify workflows, adjust project permissions, and create custom schemes.

Project administrators play a crucial role in ensuring that the project is set up and maintained properly, aligning Jira with the team’s processes.

### 2.4.4 Developers

**Developers** in Jira have permissions to interact with the board and issues related to the project. Their primary functions include:
- **Creating and updating issues**: Developers can create tasks, bugs, and user stories, assign them to themselves or teammates, and move them through the workflow.
- **Tracking progress**: Developers update the status of issues as they progress from "To Do" to "In Progress" to "Done."
- **Collaborating on tasks**: They can comment on issues, upload files, and mention teammates for collaboration.

Developers do not have the authority to alter the project configuration but are key users of the project management interface.

### 2.4.5 Project Users

**Project Users** are individuals who need access to the project but don’t have the full capabilities of developers or administrators. This role could include team members who contribute to tasks but are not directly responsible for development or management, such as:
- **Stakeholders**: Individuals who need to monitor project progress but don’t actively contribute to task execution.
- **Support Staff**: Team members who might help resolve issues or provide additional support but do not work directly on the project.

Project users typically have permissions to view issues, add comments, and potentially create new issues, but cannot make changes to the project’s structure or workflows.

---

This content delves into the essential aspects of setting up Jira, managing projects, and configuring roles, ensuring that users understand both the basic and customizable features of the platform.
# 3. Jira Interface Overview

   3.1 Navigating the Jira dashboard  
   3.2 Understanding the issue navigator  
   3.3 Project sidebar and key components  
       3.3.1 Backlog  
       3.3.2 Active Sprint  
       3.3.3 Roadmap  
       3.3.4 Reports  
   3.4 Configuring personal dashboard  
   3.5 Customizing the project layout  

Understanding the Jira interface is crucial to efficiently manage projects and tasks. This section provides a deep dive into navigating the dashboard, understanding key components, and personalizing the interface for a streamlined workflow.

## 3.1 Navigating the Jira Dashboard

The **Jira dashboard** serves as the main hub from which users can view project progress, access their tasks, and create new issues. It is highly customizable, allowing users to add and configure various gadgets that display project metrics, team performance, and key information.

Key elements of the Jira dashboard include:
- **Project Overview**: Provides an at-a-glance view of the project, displaying key data such as the number of tasks in progress, completed tasks, and upcoming sprints.
- **Favorite Filters**: Allows users to save and access custom filters for issues, based on status, assignee, or other criteria.
- **Activity Stream**: Displays real-time updates on issue changes, including comments, transitions, and new assignments.
- **Gadgets**: Users can add gadgets such as pie charts, sprint burndown charts, and cumulative flow diagrams to monitor project metrics and performance.

## 3.2 Understanding the Issue Navigator

The **issue navigator** is a powerful tool in Jira for searching, filtering, and managing issues across projects. It allows users to create and apply filters to locate specific tasks quickly. The navigator supports both a simple search interface for basic queries and an advanced search using Jira Query Language (JQL) for more complex queries.

Key features of the issue navigator:
- **Simple Search**: Provides basic filters for issues based on fields like status, assignee, project, and labels. Ideal for quickly finding tasks or bugs.
- **Advanced Search (JQL)**: JQL (Jira Query Language) enables users to craft more specific queries using logical operators, functions, and field values. This is useful for generating custom reports or finding issues that meet specific criteria.
- **Bulk Operations**: Allows users to update, transition, or assign multiple issues simultaneously, saving time when managing a large backlog.

## 3.3 Project Sidebar and Key Components

The **project sidebar** in Jira serves as the primary navigation tool within a project, providing quick access to key components and features of the project. Depending on the project type and configuration, the sidebar will include links to essential project tools and reports.

Key components accessible via the project sidebar include:

### 3.3.1 Backlog
The **Backlog** is a repository of all user stories, bugs, and tasks that have been created but not yet prioritized for a sprint or active development. It’s a key component for agile teams, particularly those following the Scrum framework. Teams can drag and drop issues from the backlog into upcoming sprints during sprint planning sessions.

- **Backlog grooming**: Teams regularly refine and prioritize the backlog, ensuring that tasks are well-defined and ready for development.
- **Epic management**: Jira’s backlog also allows users to group tasks under larger epics, helping teams maintain a high-level view of the project’s overall goals.

### 3.3.2 Active Sprint
The **Active Sprint** section is central to Scrum projects, where the team’s current sprint is displayed. It shows tasks in various states (e.g., To Do, In Progress, Done) and allows team members to update the status of their work in real-time by moving tasks across columns.

- **Issue transitions**: As developers work on tasks, they transition issues from one state to another (e.g., from In Progress to Done).
- **Burndown chart**: The active sprint also provides a burndown chart, tracking the team's progress toward completing the sprint on time.

### 3.3.3 Roadmap
The **Roadmap** is used to map out a high-level view of the project’s progress over time. It is ideal for long-term planning and helps teams visualize when specific epics, tasks, or milestones will be worked on and delivered.

- **Timeline visualization**: Roadmaps display tasks and epics on a timeline, giving stakeholders a clear sense of how the project is progressing relative to key dates and deadlines.
- **Dependency management**: Teams can define dependencies between tasks and epics, helping to identify potential bottlenecks or blockers early in the process.

### 3.3.4 Reports
Jira provides a wide variety of **reports** to help teams track progress, identify issues, and optimize their workflows. These reports are critical for agile teams, particularly when conducting sprint reviews and retrospectives.

- **Burndown and Burnup Charts**: Track progress toward completing work in a sprint or project.
- **Velocity Chart**: Shows how much work a team completes in each sprint, helping with future sprint planning.
- **Cumulative Flow Diagram**: Visualizes how issues are distributed across different stages of the workflow over time, highlighting bottlenecks or inefficiencies.
- **Control Chart**: Displays the cycle time for issues, helping teams assess the efficiency of their process.

## 3.4 Configuring Personal Dashboard

Jira allows each user to create and customize their **personal dashboard**. This is helpful for individuals to keep track of the tasks and metrics most relevant to them without having to navigate through different projects.

Steps to configure a personal dashboard:
- **Add gadgets**: Users can choose from various gadgets such as issue statistics, sprint burndown charts, activity streams, and workload summaries.
- **Rearrange layout**: Gadgets can be resized and rearranged to create a layout that best fits the user's needs.
- **Apply filters**: Users can apply saved filters to gadgets, such as displaying only issues assigned to them or issues related to specific projects.

Custom dashboards help streamline individual workflows by bringing all relevant information into a single, organized space.

## 3.5 Customizing the Project Layout

Jira offers various ways to **customize the project layout** to better suit the team’s workflow and needs. This is especially important for teams that require a more personalized interface or need to adapt Jira to specific methodologies beyond the standard Scrum or Kanban setups.

Customization options include:
- **Custom fields**: Add or modify fields to capture additional data points for issues, such as risk levels, estimated completion times, or stakeholder feedback.
- **Custom workflows**: Tailor workflows to the team’s specific process by adding or modifying statuses and transitions between tasks. For example, a software team may need custom statuses such as "Code Review" or "QA Testing" before an issue can be marked as Done.
- **Issue types**: Create custom issue types (e.g., "Change Request" or "Incident") that align with the team's specific project needs.
- **Board columns**: Customize the columns on Kanban or Scrum boards to reflect the team’s workflow stages. For example, a software team might add columns for "Blocked" or "In QA."

Customizing the project layout ensures that Jira aligns with the team’s processes, making it easier to manage tasks and workflows while reducing the friction of adapting to a one-size-fits-all setup.

---

This section covers how to navigate Jira’s interface effectively, from the dashboard to key project components like backlogs, active sprints, and reports. Additionally, it provides insights on how to personalize the interface for both individual users and teams to maximize productivity.

# 4. Issue Management

4.1 Creating issues  
       4.1.1 Types of issues (Epics, Stories, Tasks, Bugs)  
       4.1.2 Subtasks  
   4.2 Assigning issues  
   4.3 Managing issue priorities and labels  
   4.4 Custom fields in issues  
   4.5 Issue transitions and workflows  
       4.5.1 Workflow stages  
       4.5.2 Creating custom workflows  
   4.6 Bulk issue operations  
   4.7 Using issue filters and saved searches  

Effective issue management is at the heart of Jira’s functionality, allowing teams to track work, prioritize tasks, and ensure efficient progress. This section will cover the process of creating, assigning, and managing issues, as well as customizing workflows and utilizing advanced features like bulk operations and filters.

## 4.1 Creating Issues

Creating issues in Jira is a fundamental action that allows team members to break down tasks, define work items, and track progress. An issue represents a single unit of work within a project, and depending on the project type, it can take different forms, such as a feature request, bug, or task.

**Steps to create an issue:**
1. Navigate to the relevant project in Jira.
2. Click on the “Create” button located at the top of the screen.
3. Select the issue type (Epic, Story, Task, Bug, etc.).
4. Provide a summary (title) for the issue.
5. Add a description to provide more context about the task.
6. Optionally, assign the issue to a specific user, set a priority, and add labels.
7. Attach relevant files (documents, screenshots, etc.) if needed.
8. Click “Create” to add the issue to the backlog or sprint.

### 4.1.1 Types of Issues (Epics, Stories, Tasks, Bugs)

In Jira, different issue types represent different levels of granularity and work categories. Here are the most commonly used issue types:

- **Epics**: Large bodies of work that can be broken down into smaller tasks (stories or issues). Epics typically span multiple sprints or releases.
- **Stories**: User-focused features or functionalities that need to be implemented. Stories are usually completed within a sprint.
- **Tasks**: General units of work that need to be completed. A task might not have a direct user-facing component but is necessary for project completion.
- **Bugs**: Issues related to defects or errors in the system that need to be fixed.

Each issue type has specific fields and workflows associated with it, depending on the project configuration. For example, bugs might have additional fields like “Environment” or “Steps to Reproduce.”

### 4.1.2 Subtasks

**Subtasks** allow larger issues to be broken down into smaller, more manageable parts. Subtasks are helpful for tracking progress on complex tasks or when multiple people need to collaborate on different aspects of the same task.

Subtasks:
- Can be assigned to different users, allowing teams to divide work effectively.
- Inherit fields from the parent issue, but can also have custom fields or statuses.
- Are often used to ensure that all smaller tasks under a larger issue (like a story or task) are completed before the parent issue is marked as done.

## 4.2 Assigning Issues

Assigning issues ensures that team members are responsible for completing specific tasks. Issues can be assigned during creation or at any point in the workflow.

Steps to assign an issue:
1. Open the issue that needs to be assigned.
2. Click the "Assignee" field and select the team member from the dropdown list.
3. Alternatively, use the “Assign to me” option to quickly take ownership of an issue.
4. Multiple team members can collaborate on the same issue, but only one individual can be officially assigned at a time.

**Best Practices**:
- Assign issues to the appropriate team member based on expertise and workload.
- Reassign issues as necessary during the course of the workflow (e.g., from development to QA).

## 4.3 Managing Issue Priorities and Labels

Jira allows users to assign **priorities** to issues, helping teams determine which tasks are most important and need to be completed first. Priorities typically range from “Low” to “High” or “Critical,” depending on the project’s configuration.

**Steps to set issue priority**:
1. Open the issue.
2. In the “Priority” field, select the appropriate level (e.g., Low, Medium, High, Critical).
3. Save the issue to update its priority in the backlog or sprint.

In addition to priorities, **labels** can be used to categorize and filter issues. Labels are custom tags that can be applied to issues for easier grouping and reporting.

**Examples of labels**:
- Feature
- Bugfix
- Backend
- Urgent

## 4.4 Custom Fields in Issues

Custom fields allow teams to capture additional information that is not covered by Jira’s default issue fields (e.g., priority, assignee). These fields can be added to issues to track specific data relevant to the project.

Common uses of custom fields:
- **Risk Level**: Add a custom field to track the risk associated with a task or issue.
- **Effort Estimate**: Create a field to capture estimated hours or story points.
- **Approval Status**: Use custom fields for issues that require formal approval.

To create a custom field:
1. Navigate to Jira’s project settings.
2. Select “Issues” and then “Custom Fields.”
3. Click “Create Custom Field,” and choose the appropriate field type (e.g., text, number, dropdown).
4. Add the new custom field to the project’s issue screen.

## 4.5 Issue Transitions and Workflows

Jira’s **workflows** define how issues move through various stages in a project, from creation to completion. Workflows consist of states (e.g., To Do, In Progress, Done) and **transitions**, which are the rules that govern how an issue can move from one state to another.

### 4.5.1 Workflow Stages

The stages of a workflow vary depending on the project type but typically include:
- **To Do**: The issue has been created but work has not started.
- **In Progress**: The issue is actively being worked on.
- **In Review**: The work is complete and under review by another team member or department (optional).
- **Done**: The issue has been resolved and is considered complete.

### 4.5.2 Creating Custom Workflows

Jira allows administrators to create **custom workflows** to fit their team’s processes. Custom workflows can include additional stages or specific transitions to accommodate complex approval processes, development cycles, or testing procedures.

Steps to create a custom workflow:
1. Go to Jira’s “Workflow” settings.
2. Click “Add Workflow” and give it a name.
3. Define the stages (statuses) the issue will go through.
4. Configure the transitions between statuses and add any conditions or validators.
5. Assign the workflow to the relevant issue types in the project.

## 4.6 Bulk Issue Operations

When managing large projects with many issues, Jira’s **bulk operations** feature allows users to perform mass updates on multiple issues at once. Bulk operations save time and ensure consistency across issues.

Common bulk operations:
- **Bulk Assign**: Assign multiple issues to a single user.
- **Bulk Transition**: Move several issues to the next stage in the workflow simultaneously.
- **Bulk Update**: Modify fields (e.g., priority, labels) for multiple issues in one action.

To use bulk operations:
1. Go to the issue navigator.
2. Select the issues you want to perform the operation on.
3. Click on “Bulk Change” and follow the prompts to complete the operation.

## 4.7 Using Issue Filters and Saved Searches

Jira provides powerful filtering options that allow users to narrow down their list of issues based on various criteria. Filters can be saved and shared across the team to streamline recurring tasks like reporting or sprint planning.

To create an issue filter:
1. Navigate to the issue navigator.
2. Use the filter options to define criteria such as project, assignee, status, or custom fields.
3. Click “Save as” to save the filter with a custom name.

Saved filters can be accessed quickly from the dashboard or the project’s sidebar. They can also be used to create **dashboards** or **reports**, making it easier to track specific categories of work.

---

This section provides a comprehensive overview of issue management in Jira, focusing on creating and managing issues, customizing workflows, and using advanced features like filters and bulk operations to increase team efficiency.
# 5. Agile Project Management in Jira

5.1 Scrum Boards  
       5.1.1 Creating and managing sprints  
       5.1.2 Backlog grooming and sprint planning  
       5.1.3 Velocity tracking  
   5.2 Kanban Boards  
       5.2.1 Configuring Kanban columns  
       5.2.2 Managing WIP limits  
       5.2.3 Continuous delivery in Kanban  
   5.3 Epic and story mapping  
   5.4 Version and release management  
       5.4.1 Creating versions  
       5.4.2 Tracking releases  

Agile project management is one of the core functionalities of Jira, especially for teams that utilize methodologies like Scrum and Kanban. This section will cover how to set up and manage these types of projects in Jira, as well as use advanced features to improve visibility, control, and efficiency within agile teams.

## 5.1 Scrum Boards

Scrum boards in Jira are designed to help teams follow the Scrum framework, focusing on delivering incremental work through sprints.

### 5.1.1 Creating and Managing Sprints

Sprints are fundamental in Scrum, representing a fixed period during which a set of tasks must be completed. In Jira, you can easily create and manage sprints to organize your team's work.

**Steps to create and manage a sprint:**
1. Navigate to your project in Jira.
2. Access the **Backlog** view.
3. Click on the “Create Sprint” button at the top of the backlog.
4. Drag and drop issues from the backlog into the newly created sprint.
5. Set a sprint goal to provide clarity on the objectives of the sprint.
6. Start the sprint by clicking “Start Sprint” and selecting the duration (typically two weeks).
7. Monitor progress by moving issues through the workflow and checking the sprint board.
8. Complete or close the sprint once all tasks are finished or the sprint duration ends.

**Best Practices:**
- Keep sprint goals clear and achievable.
- Use the sprint retrospective to assess performance and plan for improvements.

### 5.1.2 Backlog Grooming and Sprint Planning

Backlog grooming (or refinement) ensures that the backlog is up to date, organized, and contains the most relevant issues prioritized for future sprints.

**Steps for backlog grooming:**
1. Regularly review the backlog to remove outdated issues or adjust priorities.
2. Break down large issues (epics) into smaller, manageable tasks.
3. Add estimates to each issue, which helps in sprint planning.
4. Collaborate with the team to prioritize issues for the next sprint.

**Sprint planning steps:**
1. Once the backlog is groomed, hold a sprint planning meeting to select issues.
2. Ensure that all selected issues align with the sprint goal.
3. Assign tasks to team members, ensuring a balanced workload.

### 5.1.3 Velocity Tracking

Velocity is a key metric in Scrum that measures the amount of work completed during a sprint. In Jira, you can use velocity charts to track and improve team performance.

**How to track velocity:**
1. Navigate to the project’s **Reports** section.
2. Select **Velocity Chart** to view completed story points over previous sprints.
3. Analyze the chart to see trends in the team’s capacity.
4. Use the velocity data to inform sprint planning, ensuring that the team's workload is realistic.

**Benefits of velocity tracking:**
- Provides insights into team productivity.
- Helps forecast how much work the team can handle in future sprints.

## 5.2 Kanban Boards

Kanban boards in Jira offer a flexible approach to managing work with a focus on continuous delivery. Unlike Scrum, Kanban doesn’t use sprints but focuses on limiting the work in progress (WIP) and improving workflow efficiency.

### 5.2.1 Configuring Kanban Columns

The Kanban board's columns represent the different stages of your team’s workflow. Customizing these columns is essential to reflect how tasks move through your project.

**Steps to configure Kanban columns:**
1. Open your project in Jira.
2. Access the **Board Settings**.
3. Navigate to **Columns** and add, remove, or rename columns to match your workflow stages.
4. Associate each column with the appropriate issue status (e.g., To Do, In Progress, Done).
5. Adjust the width of the columns and ensure the workflow is intuitive for the team.

**Common workflow stages:**
- To Do: Tasks that are ready to be picked up.
- In Progress: Tasks actively being worked on.
- Done: Tasks that are completed and reviewed.

### 5.2.2 Managing WIP Limits

Work In Progress (WIP) limits help prevent overloading team members by limiting the number of tasks that can be in progress at any given time.

**How to set WIP limits:**
1. Access the **Board Settings** for your Kanban board.
2. Under **Columns**, specify the WIP limit for each column (e.g., only 5 tasks can be in the “In Progress” column).
3. Monitor the board regularly to ensure WIP limits are respected and adjust them as needed.

**Benefits of WIP limits:**
- Reduces multitasking and improves focus.
- Ensures a smooth workflow without bottlenecks.

### 5.2.3 Continuous Delivery in Kanban

Continuous delivery (CD) is an essential practice in Kanban, where work is delivered incrementally and frequently.

**How Jira supports continuous delivery:**
1. Issues are continuously moved from one column to another as progress is made.
2. Jira integrates with DevOps tools (e.g., Bitbucket, GitHub) to automate code deployments as tasks are completed.
3. Teams can track deployment frequency and ensure that software is released smoothly.

**Best Practices:**
- Ensure that the team continuously updates the board to reflect the current state of work.
- Use Jira’s deployment tracking features to visualize the flow from development to production.

## 5.3 Epic and Story Mapping

Epic and story mapping is a crucial process in managing large projects, where big tasks (epics) are broken down into smaller, more manageable stories.

**Steps to manage epics and stories:**
1. Create an epic in Jira to represent a large body of work (e.g., a new feature).
2. Add related user stories under the epic by associating them with the epic in the issue creation screen.
3. Use Jira’s **Epic Panel** to track progress and ensure that all related stories are completed.
4. Prioritize stories based on their importance and dependencies.

**Benefits:**
- Provides a high-level overview of progress.
- Helps teams plan sprints more effectively by focusing on delivering small increments of work.

## 5.4 Version and Release Management

Version and release management in Jira helps teams track software versions, manage deployments, and ensure features are delivered in an organized manner.

### 5.4.1 Creating Versions

A version in Jira represents a set of features or bug fixes that will be delivered together in a release.

**Steps to create a version:**
1. Go to the **Releases** section of your project.
2. Click on **Create Version** and provide a name (e.g., Version 1.0) and a description.
3. Set a start and release date for the version.
4. Associate issues with the version to ensure they are completed before release.

**Best Practices:**
- Use descriptive names for versions to differentiate between releases.
- Track progress on each version by monitoring the issues associated with it.

### 5.4.2 Tracking Releases

Once versions are created, Jira provides tools to track the progress and health of each release.

**Steps to track a release:**
1. In the **Releases** section, select the version you want to track.
2. Use the **Release Burndown Chart** to visualize the remaining work.
3. Review issues in the **Release Page** to identify any blockers or delays.
4. Mark the version as released once all issues are complete.

**Benefits:**
- Provides clear visibility into the release process.
- Helps ensure that all planned features and fixes are delivered on time.

---

This chapter provides an in-depth look at how to use Jira for agile project management, focusing on Scrum and Kanban methodologies, epic and story management, and version tracking. By leveraging Jira’s tools, teams can manage their workflows efficiently and deliver projects on time.
# 6. Jira Reporting and Analytics

   6.1 Built-in reports and charts  
       6.1.1 Burndown and burnup charts  
       6.1.2 Velocity reports  
       6.1.3 Cumulative flow diagram  
       6.1.4 Control charts  
   6.2 Custom reports  
       6.2.1 Creating dashboards  
       6.2.2 Using gadgets for reporting  
   6.3 Tracking team performance  
   6.4 Time tracking and estimation reports  

Jira provides a wide array of reporting and analytics tools that help teams track progress, monitor productivity, and identify bottlenecks in the workflow. This chapter will cover Jira’s built-in reports, customization options, and techniques for leveraging data to improve project outcomes.

## 6.1 Built-in Reports and Charts  
Jira comes with several built-in reports and charts designed to track the progress of work, visualize team velocity, and assess project health. This section will cover the most commonly used reports and how to interpret them.

### 6.1.1 Burndown and Burnup Charts  
Burndown and burnup charts are essential tools for tracking the progress of sprints and releases. This section will explain how to generate and interpret these charts, helping teams monitor the completion of tasks relative to the sprint timeline.

### 6.1.2 Velocity Reports  
Velocity reports show how much work a team can complete in a sprint, allowing project managers to forecast future capacity. Here, users will learn how to generate velocity reports, interpret the data, and use it to improve sprint planning.

### 6.1.3 Cumulative Flow Diagram  
The cumulative flow diagram provides a visual representation of the overall progress of a project, showing the status of tasks over time. This section will guide users on how to generate and use this diagram to identify workflow bottlenecks and ensure a steady flow of tasks.

### 6.1.4 Control Charts  
Control charts are used to measure cycle time and lead time, which are critical for understanding how long tasks take to complete. This section will cover how to generate control charts and interpret the data to improve efficiency and predictability in task delivery.

## 6.2 Custom Reports  
Jira’s flexibility allows users to create custom reports tailored to specific project needs. This section will cover the basics of creating custom reports, including using dashboards and gadgets for reporting.

### 6.2.1 Creating Dashboards  
Users will learn how to create and configure custom dashboards in Jira, organizing data and visualizations to meet the needs of different stakeholders. Practical tips on how to customize dashboards for specific roles and projects will be provided.

### 6.2.2 Using Gadgets for Reporting  
Gadgets are widgets that provide different types of reports and charts. This section will teach users how to add gadgets to their dashboards, configure them to display relevant data, and make the most out of the available reporting options.

## 6.3 Tracking Team Performance  
In this section, users will learn how to use Jira to track the performance of teams, including metrics like velocity, throughput, and individual contribution. Practical techniques for analyzing these metrics and applying them to team management will be covered.

## 6.4 Time Tracking and Estimation Reports  
Jira’s time tracking features allow teams to log hours worked on tasks and compare estimates with actual work done. This section will cover how to set up time tracking in Jira, generate time-tracking reports, and use the data to improve future project estimates and resource allocation.

---

Chapter 6 provides a comprehensive guide to Jira’s reporting and analytics capabilities, helping teams gain insight into their performance and use data to make informed decisions, optimize workflows, and ensure successful project outcomes.

# 7. Jira Automation and Integrations

7.1 Introduction to automation in Jira  
7.2 Creating automation rules  
7.2.1 Triggers, conditions, and actions  
7.3 Integrating Jira with other tools  
7.3.1 Jira and Confluence  
7.3.2 Jira and Bitbucket  
7.3.3 Jira and GitHub  
7.3.4 Third-party integrations via Atlassian Marketplace  
7.4 Webhooks and API usage

# 8. Advanced Jira Customization

8.1 Custom workflows  
8.1.1 Workflow designer  
8.1.2 Workflow conditions, validators, and post functions  
8.2 Issue types and screens customization  
8.3 Advanced permission schemes  
8.4 Custom fields and field configurations  
8.5 Managing notification schemes

# 9. Jira for Service Management (Jira Service Management)

9.1 Overview of Jira Service Management  
9.2 Setting up a service desk project  
9.3 Managing service requests and incidents  
9.4 SLAs and automation rules  
9.5 Asset and configuration management (CMDB)  
9.6 Managing queues and ticket prioritization

# 10. Jira Administration

10.1 Global Jira settings overview  
10.2 Managing users and groups  
10.3 Managing project permissions  
10.4 Backup and restore in Jira  
10.5 Jira upgrades and maintenance  
10.6 Performance tuning and troubleshooting

# 11. Best Practices and Tips

11.1 Agile best practices using Jira  
11.2 Optimizing workflows for team efficiency  
11.3 Effective use of filters and labels  
11.4 Automating repetitive tasks  
11.5 Jira for remote teams

# 12. Conclusion and Certification Preparation

12.1 Recap of key concepts  
12.2 Sample Jira certification questions  
12.3 Preparing for the Jira certification exam  
12.4 Next steps in your Jira journey

# 13. Jira Advanced Workflows

13.1 Workflow transitions and statuses  
13.2 Workflow triggers (e.g., from issue creation, editing, or comments)  
13.3 Workflow validators and conditions  
13.4 Workflow post functions  
13.5 Advanced workflow customizations with ScriptRunner  
13.6 Best practices for maintaining clean workflows

# 14. Jira Query Language (JQL)

14.1 Introduction to Jira Query Language (JQL)  
14.2 Basic JQL syntax  
14.3 Advanced JQL queries  
14.3.1 Filtering by assignee, project, status, etc.  
14.3.2 Using JQL with custom fields  
14.3.3 Chaining queries for complex reports  
14.4 Saving filters and subscriptions  
14.5 Automating reports using JQL

# 15. Jira Software Development Use Cases

15.1 Jira for DevOps  
15.1.1 Using Jira in CI/CD pipelines  
15.1.2 Jira and release management with Bitbucket/GitHub  
15.2 Managing software projects with Jira  
15.2.1 Issue tracking across sprints  
15.2.2 Integrating Jira with code repositories  
15.2.3 Jira for managing bugs and improvements  
15.3 Planning product roadmaps with Jira  
15.3.1 Epic and story breakdown  
15.3.2 Estimating and forecasting using Jira reports

# 16. Jira for Business and Marketing Teams

16.1 Setting up Jira for non-technical projects  
16.2 Customizing workflows for business processes  
16.3 Using Jira to manage marketing campaigns  
16.4 Reporting for business teams  
16.5 Jira for customer support and service management

# 17. Jira for IT and Operations

17.1 Setting up IT projects in Jira  
17.2 Incident and problem management  
17.3 Using Jira for asset and configuration management  
17.4 Tracking SLAs and ensuring service continuity  
17.5 Integrating Jira with ITSM platforms  
17.6 Best practices for handling outages and incidents

# 18. Security in Jira

18.1 Managing user permissions and roles  
18.2 Ensuring data security within Jira projects  
18.3 Configuring project-level and issue-level security  
18.4 Auditing and logging activities in Jira  
18.5 Integrating Jira with Single Sign-On (SSO) systems  
18.6 Ensuring compliance with GDPR and other data protection regulations

# 19. Jira API and ScriptRunner

19.1 Introduction to Jira REST API  
19.2 Authenticating and using the Jira API  
19.3 Automating tasks using API scripts  
19.4 Introduction to ScriptRunner for Jira  
19.4.1 Extending Jira’s functionality with Groovy scripts  
19.4.2 Advanced workflow customization with ScriptRunner  
19.4.3 Automating complex operations

# 20. Jira Marketplace Apps and Plugins

20.1 Introduction to Atlassian Marketplace  
20.2 Popular Jira plugins for extended functionality  
20.2.1 Tempo Timesheets for time tracking  
20.2.2 Zephyr for test management  
20.2.3 Insight for asset management  
20.2.4 Automation for Jira  
20.3 Installing and managing plugins  
20.4 Developing custom plugins for Jira

# 21. Migrating to Jira

21.1 Migrating from other project management tools (e.g., Trello, Asana)  
21.2 Jira Cloud vs Jira Server: Key differences  
21.3 Best practices for migration  
21.3.1 Data migration  
21.3.2 User migration  
21.3.3 Custom fields and workflows  
21.4 Post-migration tasks: Validation and testing

# 22. Jira Governance and Maintenance

22.1 Creating governance policies for Jira usage  
22.2 Maintaining Jira at scale  
22.3 Performance tuning for large Jira instances  
22.4 Archiving old projects and issues  
22.5 Ensuring best practices across teams

# 23. Jira Cloud Administration

23.1 Setting up Jira Cloud  
23.2 Managing cloud-specific settings  
23.3 Cloud-specific security concerns and compliance  
23.4 Scaling Jira Cloud for larger teams  
23.5 Integrating Jira Cloud with Atlassian Access for enhanced security

# 24. Jira Certifications and Career Path

24.1 Jira certifications overview  
24.2 Preparing for Jira Administrator and Jira Project Administrator exams  
24.3 Career opportunities with Jira skills  
24.4 Building a Jira consulting or administration career

# 25. Case Studies and Real-World Applications

25.1 Case study: Jira in a large enterprise software team  
25.2 Case study: Using Jira for agile transformations  
25.3 Case study: Managing a multi-team environment with Jira  
25.4 Case study: Jira for ITIL and IT service management

# 26. Conclusion and Future Trends

26.1 The future of Jira and Atlassian tools  
26.2 Emerging trends in project management tools  
26.3 Jira’s role in the future of DevOps and Agile methodologies