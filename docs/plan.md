---
id: plan
title: Plan Overview
sidebar_label: Plan Overview
---


The RideVT system uses 2 architectural styles for each of the two design elements. The Design Element - **DE-1** uses Model-View-Controller (MVC) architectural style and the Design Element - **DE-2** uses Client-Server architectural style.


## Phases - 
Testing will consist of these **four integration phases** for incrementally testing identifiable pieces of the system and will test the following portions or characteristics of the system - 

1. **Authentication/Security phase** -
<br /> Validate the working of the user (driver and rider) signup and login functionalities and overall security and privacy aspects of the system. 

2. **Data Manipulation phase** - 
<br />
Test the following portions of the system - 
<br /> • Ride creation workflow - Add Ride, View Passengers, Accept/Reject passenger requests, receive payment, confirm ride. (driver)
<br /> • Ride booking workflow - Enter source/dest, check ride availability, choose ride, make payment, receive confirmation. (rider)
<br /> • Ride History Views - View Ride History (rider and driver). 

3. **User Interface phase** -
<br /> Test the behavior of the user interface, UI validations, etc as data is updated in real time.

4. **System Reliability phase** - 
<br />
Test the non-functional aspects of the system.


### Reason for choosing this Test Plan to carry out the integration testing

As a review, the flow of testing phases is from Authentication/Security phase to Data Persistence/Manipulation Phase, then the User Interface Phase and finally the System Reliability Phase. This was deemed to be a good test plan to carry out integration testing because it tackles the functional priorities of the application in a consecutive manner. 

To elaborate, the authentication and security phase is tested first because it is the initial step to start and continue using the RideVT application and it is of utmost importance that details are confidential regarding their payment methods.The next phase is the core of the application which is a good way to test the interaction between two of the design elements, the MVC architecture and client-server architecture which uses third-party services like Google Maps, PayPal etc. Testing this phase is crucial to ensuring the functionality of the application by observing system behavior when manipulating and retrieving data.The user interface is the next aspect to test since the “View” part of MVC model is more meaningful to test if the Model and Controller elements have been tested prior (through the previous phase). The UI is what the client interacts with, therefore it is important that any data manipulation triggers the UI to make changes and vice versa. Lastly, the system reliability phase focuses on the non-functional requirements that build upon the application in terms of performance, scalability, reliability and interoperability. These are more high level requirements that can only be tested after core functionality is implemented and tested as well. 

Having this test plan allows for an incremental approach in testing and this helps improve defect and error identification. With these phases planned, there are integrated tests within each phase as well as between phases. Therefore, these set of builds and test procedures were deemed to be the most strategic approach to testing the application.








