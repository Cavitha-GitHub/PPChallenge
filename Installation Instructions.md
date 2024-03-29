**Installation Instructions**

**Pre-requisites**

**Create Connection References:**

Create the following connection references:
•	Dataverse
•	Teams
•	Approvals
•	O365 Groups

**Create Offline Profile**

Setup Mobile Offline Profile

**Create Microsoft Teams - Team & Channel**

Create a team (if does not exist) and supervisor channel and gather the id's  as mentioned below:
•	Supervisor Channel Id - Used to send teams message when an inspector rejects the request To get the channel id, go to the channel and copy the id inbetween "threadId=" and "&ctx=channel"
•	Team Group Id - Used to create a group calendar event when an inspector accepts the request To get the team group id, go to the team, click on 3 dots and choose "Get link to team". The copy the group id value
The owner of the flow should also be a member of the team/channel

**Initialize flow approval tables in your environment**

The solution uses built-in approval actions of Power Automate, and therefore require it to be installed in the environment.
If you're installing the solution in a new environment or one in which approvals haven't been used in the past, the approval tables must be initialized before you can install the solution. The easiest way to do this is to create a "dummy" approval flow.
•	Go to flow.microsoft.com and select your environment.
•	Select + Create.
•	Select Instant cloud flow.
•	Pick manually trigger a flow as the trigger, and enter Admin | Dummy Approval Flow as the name.
•	Build an instant flow.
•	Select + New Step to add an approval action to the flow, and then search for and select Create an approval.
•	Select a dummy title, and enter your email address under Assigned to.
•	In the upper-right corner, select Test, and then select I'll perform the trigger action.
•	Select Save & Test.
•	Select Run Flow.

Note
This flow can take up to ten minutes to run initially. After it runs, you can delete the flow because it won't be needed anymore.
Select Solutions on the left side panel, and you should now see two new Flow Approvals solutions. Note that the presence of these solutions was the point of this step, and the way you know it succeeded.

**Import the solution**

1.	Download the CoE Starter Kit compressed file Cavitha-GitHub/PPChallenge. Extract the zip file after downloading and before moving on to the next step. 
2.	Import the solution:
a.	If you're installing into a production environment, use the BuildingInspection _x_x_x_xx_managed.zip solution file from the download.
b.	If you’re installing into a dev environment, use the BuildingInspection_. x_x_x_xx_.zip solution file from the download.
3.	Update environment variable values by using the relevant information. The environment variables are used to store application and flow configuration data with data specific to your organization or environment. This means that you only have to set the value once per environment and it will be used in all necessary flows and apps in that environment. All the flows in the solution depend on all environment variables' being configured.

**Turn on flow**

Make sure the **Send notification when inspection scheduled** is turned on.

**Share Apps**

Share Inspections Scheduler, Model Driven App with Supervisors

Share Inspections Manager, Canvas App with Inspectors
