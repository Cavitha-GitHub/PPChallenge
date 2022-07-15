# Inspection App

To build an app to help building inspectors to complete their day to day inspection tasks. The City of Santa Monica publishes their Building Permit Inspection Schedule as open data. Building inspectors need to travel to various locations throughout the day to inspect building that are under construction. Building inspector supervisors need to ensure timely delivery of services and analyze overall trends. The app will help Building and Safety Division manage their requests for building permit inspections.

**Inspection Process**

The diagram below depicts the inspection process.

![image](https://user-images.githubusercontent.com/10726964/179200615-758663eb-148f-4e92-b4d3-15835586dabb.png)

**User Persona**

  Admin - Admin/Maintainence of the system ( future )
  
  Supervisor - Creates & Assigns Inspections, Reviews Inspection reports and issues building permit
  
  Inspector - Carries out the inspection and uploads any relevant documentation

**Import data - Automated Process**

A dataflow is run at 7 p.m GST to import the inspection requests from the dataset published in the below website

https://data.smgov.net/Permits-Licenses/Permit-Inspections-Schedule/xird-2kxi

The schedule can be changed as desired.

**Schedule Inspections**

The supervisor can use the **Inspections Scheduler**, a Model Driven app to review the inspections and carry out the following tasks:
    Assign an inspector
    Choose an estimated inspection arrival date/time
    Upload any relevant documentation/report that needs to be updated during inspection.
    Review inspection
    Issue building permit

The model driven app has business rules to check for valid data entry such as permit expiration date should not be less than issuance date, make estimated inspection date mandatory when an inspector is assigned and to enable the permit issue stage only after the supervisor has approved the inspection.

A business process flow guides the supervisor through the various stages. The model driven app is enabled for offline mode to enable the supervisor to use the app while making field visits with poor network coverage.


**Manage Scheduled Inspections**

As inspectors can use the **Inspections Manager**, a canvas app to manage inspections assigned to them.

The app has the following functionality:

  Displays the logged in user's image, name and email address
  Provides details of inspections in list view and calendar view
  Reporting and Approval review features ( to be implemented )
  
**Solution Components**

The artecfacts are packaged into a managed (test & prod environment) & unmanaged (dev environment) solutions and consist of the following objects:

**Tables**
For the purpose of simplicity, only 3 tables are used in the project
  Building Inspection Request - Custom table created to store the inspection data
  Supervisor BPF - Created by business process flow to save details about the process stages
  Users - System table that contains the users of power platform/environment.

**Flows**


**Environmental Variables**

**Security Groups**

**Field Secruity Profile**

**Disclaimer :** The project has been developed to showcase the power of Power Platform and it's ease of use to quickly create apps and map an organisation's business prorcess. The project is work in progress and it should be tested before using it in production environment.
