# Inspection App

To build an app to help building inspectors to complete their day to day inspection tasks. The City of Santa Monica publishes their Building Permit Inspection Schedule as open data. Building inspectors need to travel to various locations throughout the day to inspect building that are under construction. Building inspector supervisors need to ensure timely delivery of services and analyze overall trends. The app will help Building and Safety Division manage their requests for building permit inspections.

![image](https://user-images.githubusercontent.com/10726964/179200615-758663eb-148f-4e92-b4d3-15835586dabb.png)

**Data Flow**

Scheduled import of data from the website

**Model Driven App**

Once data is imported, the supervisor can use a Model Driven app to review the data and assign the inspector, choose estimate inspection date/time and upload any relevant documentation needed to the request. 

Once an inspector has been assigned, a flow is triggered which sends an approval request to the inspector and they can accept the request or decline. If declined a teams notification is sent to the supervisor channel to take further action. If accepted a group event is created in the group calendar and individuals can add the invite to their calendar if needed.

The model driven app has business rules to check for valid data entry such as permit expiration date should not be less than issuance date, make estimated inspection date mandatory when an inspector is assign and to enable the permit issue stage only after the supervisor has approved the inspection.

A business process flow to guide the supervisor through the various stages. The model driven app is enabled for offline mode to enable supervisor to make field visits and use the app , when network coverage is poor in the inspection site.

**Canvas App**

As inspectors are field based, they would

**Solution Components**

**Tables**

**Flows**

**Environmental Variables**

**Security Groups**

**Field Secruity Profile**
