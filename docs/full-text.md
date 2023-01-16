---
id: full-text
title: Full Text
sidebar_label: Full Text
---

## Test Scope
### Introduction

**Project Title:** Test Plan for RideVT

**Authors:** Aparna Ganesh, Mayur Dhepe, Purna Srivatsa, Rama Krishna Pinnimty

The system for which this test document is written for is the ride-sharing system called RideVT. It is aimed towards being a beneficial and efficient system for Virginia Tech students who need assistance for transportation purposes. RideVT has been designed to transport one or multiple passengers to locations they desire and be a cost-efficient choice for students by sharing their rides with others. The following pages will document how the system will be tested, along with its individual system modules, through a series of integration and validation tests.

### Requirements

This section details the scope of the requirements and design characteristics tested in each of the testing phases - (Authentication phase, Ride Booking phase - Location, Ride Booking phase - Details, Ride Booking phase - Payment, Ride History phase). We plan to cover most of the requirements both functional and non functional and leave out some of the requirements that are not fully operated or controllable by the current system since they are fully dependent on external services and systems that the software is connected to. The system consists of two major design modules - the MVC Module( Design element - 1 ), which will be referred to as DE-1, and the Client Server Module( Design element - 2 ) which will be referred to as DE-2 here on. Furthermore, there are modules in DE-1 within each layer of the MVC architecture. The model layer has - Driver, customer, vehicle, driver trip, passenger trip, payment models. The view layer has - Sign up and login view, Driver view (Home, requests, reservation), Passenger view (Home, matches, reservations), Map view, Payment view, Trip history view. Each of the requirements listed below is tested based on the DE and module it belongs to.


#### Requirements Tested

##### Functional Requirements

###### Student Driver

- **FR-1** -  The driver should be able to sign up for the VT ride-sharing system and successfully login to the system.
- **FR-2** - The driver should be able to add their personal information - name, major, and academic standing.
- **FR-3** - The driver should be able to add their pick-up point(s) and end destination.
- **FR-4** - The driver should be able to add all the drop-off locations within the route to the end destination.
- **FR-5** - The driver should be able to add the date and time of their trip.
- **FR-6** - The driver should be able to set their list price for the trip.
- **FR-7** - The driver should be able to add the number of seats and luggage capacity available for the trip.
- **FR-8** - The driver should be able to view the passenger’s information and accept or deny their request for the ride.
- **FR-9** - The driver should be able to add a payment method linked to their account (bank account, credit card, debit card)
- **FR-10** - The driver should be able to see all their past ride history.


###### Student Passenger

- **FR-11** - The passenger should be able to sign up for the VT ride-sharing system and successfully log in to the system.
- **FR-12** - The passenger should be able to add their personal information - name, major, and academic standing.
- **FR-13** - The passenger should be able to sort all the available drivers by destination, drop-off points, and requested price.
- **FR-14** - The passenger should be able to see the trip time.
- **FR-15** - The passenger should be able to add the number of luggage(s) they would like to bring.
- **FR-16** - The passenger should be able to view the driver’s information.
- **FR-17** - The passenger should be able to request a ride from the driver.
- **FR-18** - The passenger should be able to add a payment method linked to their account (bank account, credit card, debit card)
- **FR-19** - The passenger should be able to make a successful payment to the driver.
- **FR-20** - The passenger should be able to see all their past ride history.


##### Non-functional requirements

- **NR-1** - The application should load in about 5 seconds and once the user logs in, the homepage of the application should load within 3 seconds.
- **NR-2** - The application should be scalable and be able to handle at least 34,000 users (approximate current enrollment at VT).
- **NR-3** - The application should be able to protect the privacy of the users and their personal information.
- **NR-4** - The application should be able to run on multiple operating systems such as android and IOS as well as the desktop.
- **NR-6** - Passengers should be able to see all available matches to drivers that update every time a trip that matches their preferences is posted.
- **NR-7** - Payment information such as card details should be kept confidential.



#### Requirements not tested

##### Non-functional requirements

- **NR-5** - The application should be extensible in order to incorporate any future changes in case any new features need to be added.
- **NR-8** - The application should be able to offer quick response time through notifications since ride sharing can be time-sensitive at times.
- **NR-9** - The application should be easily maintainable by the administrator in order to fix any bugs or run timely updates.
- **NR-10** - The application should be available to use at any time of the day without any server downtime issues.


### Traceability Matrix

#### Functional Requirements

| Design Architecture | Requirement ID | Design ID | Testing Phase |
|---------------------|----------------|-----------|---------------|
| MVC | FR-1 | DE-1 | Authentication/Security
| MVC |	FR-2 | DE-1 | Authentication/Security
| Client-Server | FR-3 | DE-2 | Ride Booking/Creation Phase, UI Phase |
| Client-Server	| FR-4 | DE-2 | Ride Booking/Creation Phase, UI Phase |
| MVC |	FR-5 | DE-1 | Ride Booking/Creation Phase, UI Phase |
| MVC | FR-6 | DE-1 | Ride Booking/Creation Phase, UI Phase |
| MVC | FR-7 | DE-1 | Ride Booking/Creation Phase, UI Phase |
| MVC | FR-8 | DE-1	| Ride Booking/Creation Phase, UI Phase |
| Client-Server	| FR-9 | DE-2 | Ride Booking/Creation Phase, UI Phase |
| MVC |	FR-10 | DE-1 | Ride Booking/Creation Phase, UI Phase |
| MVC |	FR-11 |	DE-1 |	Authentication/Security |
| MVC | FR-12 |	DE-1 |	Authentication/Security |
| MVC | FR-13 |	DE-1 |	Ride Booking/Creation Phase, UI Phase |
| Client-Server | FR-14	| DE-2 | Ride Booking/Creation Phase, UI Phase |
| MVC |	FR-15 |	DE-1 | Ride Booking/Creation Phase, UI Phase |
| MVC |	FR-16 | DE-1 | Ride Booking/Creation Phase, UI Phase |
| MVC | FR-17 | DE-1 | Ride Booking/Creation Phase, UI Phase |
| Client-Server | FR-18 | DE-2 | Ride Booking/Creation Phase, UI Phase |
| Client-Server	| FR-19	| DE-2 | Ride Booking/Creation Phase, UI Phase |
| MVC |	FR-20 |	DE-1 | Ride Booking/Creation Phase, UI Phase |


#### Non-Functional Requirements

| Design Architecture | Requirement ID | Design ID | Testing Phase |
|---------------------|----------------|-----------|---------------|
| MVC | NFR-1 | DE-1 | Authentication/Security, System Reliability |
| MVC | NFR-2 | DE-1 | System Reliability |
| MVC |	NFR-3 |	DE-1 | Authentication/Security, System Reliability |
| MVC | NFR-4 | DE-1 | System Reliability |
| MVC | NFR-5 | DE-1 | Not Tested |
| MVC | NFR-6 | DE-1 | Authentication/Security, System Reliability |
| Client-Server	| NFR-7 | DE-2 | Authentication/Security |
| MVC and Client-Server	| NFR-8	| DE-1/DE-2	| Not Tested |
| MVC | NFR-9 | DE-1 | Not Tested |
| MVC | NFR-10 | DE-2 | Not Tested |


## Test Plan

### Plan Overview

The RideVT system uses 2 architectural styles for each of the two design elements. The Design Element - **DE-1** uses Model-View-Controller (MVC) architectural style and the Design Element - **DE-2** uses Client-Server architectural style.


### Phases 
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


#### Reason for choosing this Test Plan to carry out the integration testing

As a review, the flow of testing phases is from Authentication/Security phase to Data Persistence/Manipulation Phase, then the User Interface Phase and finally the System Reliability Phase. This was deemed to be a good test plan to carry out integration testing because it tackles the functional priorities of the application in a consecutive manner. 

To elaborate, the authentication and security phase is tested first because it is the initial step to start and continue using the RideVT application and it is of utmost importance that details are confidential regarding their payment methods.The next phase is the core of the application which is a good way to test the interaction between two of the design elements, the MVC architecture and client-server architecture which uses third-party services like Google Maps, PayPal etc. Testing this phase is crucial to ensuring the functionality of the application by observing system behavior when manipulating and retrieving data.The user interface is the next aspect to test since the “View” part of MVC model is more meaningful to test if the Model and Controller elements have been tested prior (through the previous phase). The UI is what the client interacts with, therefore it is important that any data manipulation triggers the UI to make changes and vice versa. Lastly, the system reliability phase focuses on the non-functional requirements that build upon the application in terms of performance, scalability, reliability and interoperability. These are more high level requirements that can only be tested after core functionality is implemented and tested as well. 

Having this test plan allows for an incremental approach in testing and this helps improve defect and error identification. With these phases planned, there are integrated tests within each phase as well as between phases. Therefore, these set of builds and test procedures were deemed to be the most strategic approach to testing the application.


# Test Procedures for Builds

## Authentication/Security Phase

### Build

The build for this phase consists of both the modules: DE-1, DE-2.


### Purpose

The purpose of this phase is to validate the working of the user (driver and rider) signup and login functionalities. Additionally, this phase ensures that the user information is stored securely and is well protected. Requirements FR-1, FR-2, FR-11, FR-12, NFR-1, NFR-3, NFR-6, and NFR-7 will be covered in this phase.

### Test Cases

| Test | Goal | Procedure & Expected behavior |
|------|------|-----------|
1.1 | Validate Driver SignUp Information | Verify that the system raises appropriate error messages for the corresponding input fields when fed with erroneous data. Additionally, check if the system stores the provided information in the database and notifies the Driver in case the registration was successful.
1.2 | Request/Redirect Driver to Login | Verify that the system either requests or redirects an existing Driver to login when he/she tries to register.
1.3 | Validate Driver Login Credentials | Validate the credentials entered by the Driver and notify through a success or a failure message if they match or do not match with the records in our database.
1.4 | Validate Rider SignUp Information | Verify that the system raises appropriate error messages for the corresponding input fields when fed with erroneous data. Additionally, check if the system stores the provided information in the database and notifies the Rider in case the registration was successful.
1.5 | Request/Redirect Rider to Login | Verify that the system either requests or redirects an existing Rider to login when he/she tries to register.
1.6 | Validate Rider Login Credentials | Validate the credentials entered by the Rider and notify through a success or a failure message if they match or do not match with the records in our database.
1.7 | Application load/render times | Verify that the system boots up within 5 seconds and does not take more than 3 seconds to render the homepage after successful login.
1.8 | Protection of the user (driver & rider) information | Ensure that the system keeps the user sessions private & isolated. Also check if it stores all the critical user-related information securely (using encryption) in the database.
1.9 | Verify the Precision & Recall of the matching drivers | Verify the extent (i.e, accuracy and relative count) to which the system fetches the available drivers matching the rider preferences.



### Additional Software

SSO, Multi-factor authentication (2FA etc), SHA keys for password protection etc.

## Data Persistence/ Manipulation Phase

### Build

This build for this phase is designed to test DE-1 i.e. the Model-View-Controller, particularly the Model and Controller elements and DE-2 by testing for the integration of external services with the application.

### Purpose

The objective for this phase is to test that the data is properly created, stored, and retrieved for the purpose of ride creation, ride booking and viewing of ride history. The core of the application workflow is tested in this phase. The functional requirements tested in this phase are: FR-3 - FR-10, FR-13 - FR-20, along with NFR-6. This phase will ensure that valid details are successfully stored in the database after field values are cleaned. Additionally, it tests that if there are null, erroneous or invalid data values, the appropriate system response is produced. It will also test that the external services such as Google Maps, PayPal (amongst other payment applications) are well integrated into the system and are capable of being functional when needed.


This phase would test the following portions of the system:

1. Ride creation workflow - Add Ride, View Passengers, Accept/Reject passenger requests, receive payment, confirm ride. (driver)
2. Ride booking workflow - Enter source/dest, check ride availability, choose ride, make payment, receive confirmation. (rider)
3. Ride History Views - View Ride History (rider and driver).


### Test Cases

| Test | Goal | Procedure & Expected behavior|
|------|------|-----------|
2.1 | Creation of a ride | Feed details to the system in order to create a ride and ensure that the correct success or error messages are generated based on whether there are any null, erroneous, or invalid values. Check to see that Google Maps API is able to accurately pinpoint current location, destination points, drop-off points, calculate distance and update estimated time arrival (ETA) for each of the locations. If successful, check that the database contains the ride, otherwise see that the system has thrown an error. For accepted rides, verify that the database stores cleaned field values for the ride details. |
| 2.2 | Request for a ride | For a particular ride, request the ride and check that the system is capable of sending notifications to the driver linked to the ride. For that request, test that all passenger details such as pickup, drop off location, luggages, etc., are obtainable. If any details are erroneous, check that error messages are received and no confirmation notifications are sent to the driver.
2.3 | Confirm or reject a ride and send appropriate notifications | For a particular ride, confirm the ride by accepting the request. Check that the system sends out a confirmation notification to the requesting passenger for payment and that an ETA is calculated between the requested driver’s location and the passenger’s location.. If denied, ensure the appropriate notification is sent. Verify that respective ride updates have been made in the database.
2.4 | Search for rides sorted based on destination | Given a specific destination, check that the system queries for all available rides. Results obtained should be sorted by distance to destination. If any null or invalid data is searched for, the appropriate system response should be given.
2.5 | Search for rides sorted based on drop-off points | Given a specific drop-off point, check that the system queries for all available rides. Results obtained should be sorted by distance to drop-off point. If any null or invalid data is searched for, the appropriate system response should be given.
2.6 | Search for rides sorted based on price | Given a desired price range, check that the system queries for all available rides. Results obtained should be sorted by given price range. If any null or invalid data is searched for, the appropriate system response should be given. Additionally, if price values are invalid, the appropriate error message should be received.
2.7 | Add number of luggages (passenger) | Provided a luggage amount/value, add it to the passenger’s details. Proceed to check whether the database can retrieve this detail associated with a passenger. If a null or invalid value is provided, test that no value is stored for the passenger’s luggage amount in the database.
2.8 | Make a payment and receiving confirmation | Feed the system with payment details and check that the system provides appropriate confirmation of the transaction if it is successful. Test that the system does not send confirmation messages and an error response is produced if the transaction has been interrupted or invalid details are presented.
2.9 | View ride history  | Given a passenger, test that after a few accepted rides, the database is able to accurately retrieve all details of past ride details. Test the same capability for a given driver. Check that all details about the ride, including passenger details, are obtainable. 


### Additional Software

Since much of this phase consists of testing the database and creation of different model objects in order to test different scenarios, it could be more efficient and effective to introduce automated testing. Although database testing can be tedious and there exists few tools that can help with database testing, **Selenium** offers some help on automating the process. To perform integration testing without going through the UI, we can programmatically send HTTP requests to the different URLs and assert the state of the system afterwards. These HTTP request tests can be automated to ease the testing process.  This can be done using tools like **TestComplete** as well as Selenium. Additionally, with the integration of third-party services, access to Google Maps API, Google location API, Paypal Payment API etc. would be necessary for testing.


## User Interface Phase

### Build

The build for this phase consists of the design element DE-1 i.e. the Model-View-Controller element, more specifically the View element.

### Purpose

The purpose of this phase is to ensure that all the fields, labels, buttons, and other elements on the screen work as expected. It ensures that all the views or pages in the application function as expected. It primarily involves testing different UI elements, if they are in their correct place as per the UX designs, they correctly respond to user inputs. Various UI functionalities like testing if the visibility (hide/show an element), disability (enable/disable input on particular element), etc. can be tested in this phase. UI testing involves testing the visual elements to verify that they are functioning according to requirements – in terms of functionality and performance. All the Functional Requirements (FR-1 to FR-20) that have some User interface involved with them would be tested under this phase. 

### Test Cases

| Test | Goal | Procedure & Expected behavior |
|------|------|-----------|
3.1 | Users (driver & passenger) can view and enter their personal information on the sign up view.  | In the Sign Up view, enter personal information in all fields i.e. name, email, password, major, academic standing, etc. On clicking the sign up button, the user is prompted to the login view according to their role to enter their email address and password. 
3.2 | Users (driver & passenger) can view and enter login details on the login view. | In the login view, enter the email and password (used when creating the profile). On clicking the login button, the user should be redirected to the Home View.
3.3 | Driver can fill up the ride information and add a ride through the Home View. | In the driver’s Home view, enter the pickup location, stopping points, end destination and other fields needed to create a ride. On clicking the Create Ride button, the user should be able to see the created ride with all the ride details.
3.4 | Driver can view all the requests from passengers along with their information and accept/reject a request on the Requests View. | In the driver’s Requests view, validate that all the requests from passengers are displayed in the expected format, along with all their information. Validate that on clicking the accept/reject button, the carpool requests gets accepted or denied.  
3.5 | Driver can view new requests once they are available. | Validate that the Driver’s Requests view automatically refreshes once new requests are available and the passenger information gets displayed correctly.
3.6 | Driver can view the reservation details and the payment processing state on the Reservation View. | Validate that the reservation information gets correctly displayed - trip date, available seats in car, payment processing state for each passenger.
3.7 | Passenger can fill up the trip information and the price they are willing to pay on Home View. | In the passenger’s Home View, enter the source and destination of the trip, along with the luggage details and price they are willing to pay. After entering all the trip details, passenger is redirected to the Matches View. 
3.8 | Passenger can view new matches once they are available.  | Validate that the Passenger’s Matches view automatically refreshes once new matches are available and information about all the available trips gets displayed correctly.
3.9 | Passenger can sort all the available trips by distance to destination & price range. | Validate that the available trips get sorted correctly on the basis of distance to destination & price range.
3.10 | Passenger can see the Matches View as pending until the driver accepts the trip. | Validate that the Matches View stays pending until the driver accepts the trip on their end.
3.11 | Passenger can make a reservation for up to 30 days in advance of the trip. | Validate that the user can fill up the reservation details and make an advance payment to secure the seat.
3.12 | Passenger can view all the information for them to be able to meet the driver. | Make the payment to the driver. After the payment, ensure that the reservation is secured and the screen displays all the information for them to be able to meet the driver.
3.13 | Passenger & driver can view the navigation information on the Map View. | On Map View, enter the source and destination of the trip, and validate if the total trip time and estimated time of arrival get displayed correctly. Validate that the driver and passenger are able to view the navigation information throughout the trip.
3.14 | Passenger can make a secure payment through the Payment View. | Accept the ride request from the driver’s end. Enter credit card details on the Payment View. Validate that an appropriate screen gets displayed when the payment is complete. 
3.15 | Passenger and Driver can view a list of previous trips offered or taken. | Validate the user can see a list of their previous trips on the Trip History View. Validate that the view displays all of the collected data like pickup, drop-off points, passengers, luggage, driver information, etc.



### Additional Software

The User interface tests under this phase can be automated with the help of certain tools or software. Some automation tools like **Selenium** or **Cypress** can be used to automate the UI testing. Since tests can be written in any language under these frameworks and can be carried out under any underlying OS. The main challenge in User Interface testing is to deal with frequent changes in the UI and ensuring that all tests are adapted to the new changes.


## System Reliability Phase

### Build

The build for this phase consists of both the design elements i.e. DE-1, DE-2. 

### Purpose

The purpose of this phase is to test all the non-functional requirements of the system. It tests all the aspects which are not tested in functional testing. It is intended to test the readiness of a system according to nonfunctional criteria that functional testing never takes into account. The purpose of this phase is to increase usability, efficiency, maintainability and portability of the product. Other major non functional requirements that would be tested in this phase include system security, scalability and extensibility and performance. All the Non Functional Requirements NFR-1 to NFR-10 would be tested under this phase except NFR-5, NFR-8, NFR-9, NFR-10.


### Test Cases

| Test | Goal | Procedure & Expected behavior |
|------|------|-----------|
4.1 | Application loads in about 5 seconds once the user logs in. | Enter the email and password on the login page and validate that the Home View loads within 3 seconds.
4.2 | Application should be able to protect the privacy of the users and their personal information. | Perform vulnerability scans through automated software to scan a system against known vulnerability signatures. Perform penetration testing to simulate an attack from a malicious hacker. Ensure that the correct design pattern is followed such that security and privacy of user data is handled without affecting application performance. Ensure that passwords are encrypted and stored in a secure way. Ensure that payment services are secure through integration with external payment gateways.
4.3 | Application should be able to run on multiple operating systems. | Validate if the application runs properly on multiple operating systems including Android, IOS and desktop OS. Determine the look and feel of the application in the various browser types and various browser versions.
4.4 | Application should be extensible in order to incorporate any future changes. | Measure the level of effort required to add new features to the system. Perform regression on the existing features to ensure the new functionality does not break the existing one. Ensure that the right architecture is chosen during the design phase.
4.5 | Passengers should be able to see all available matches that are continuously updating. | Enter matching trip details for both driver and passenger, and validate if the Matches View updates with the newly available rides every time.
4.6 | Payment information should be kept confidential. | Validate that payment services are secure through integration with external payment gateways.
4.7 | Application performance is as expected under normal and expected conditions. | Validates that the system performs as expected when concurrent users access the application and get the expected response time.


### Additional Software

The System Reliability tests under this phase can be automated with the help of certain tools. **JMeter** can be used as a load testing tool for analyzing the performance of a variety of services, with a focus on web applications. **Webserver Stress Tool** can be used to evaluate whether the system’s performance is as expected when it is low on resources. An example for stress testing could be when multiple users are trying to perform the same transactions on the same data.


## Validation Tests

### Build

The build for this phase consists of both the design elements i.e. DE-1, DE-2. 

### Purpose

The purpose of this build is to ensure that the software actually meets the requirements for the project. It can also be defined as a testing to validate that the product fulfills its intended use when deployed in an appropriate environment. The build consists of the entire system - meaning all modules or design elements of the system. Validation tests are organized around a traceability matrix (specified at the end), that maps the validation test cases to the requirements for the project. This build would involve various types of software testing – integration tests, system tests, user acceptance tests, regression tests, cross browser and cross device testing. 

### Test Cases

| Test | Goal | Procedure & Expected behavior |
|------|------|-----------|
1 | Error message gets displayed when email and/or password fields are left blank on the login page. | Launch the URL for login view, leave both email and password fields (or either of them) blank. Validate that appropriate error message gets displayed to enter an email or or password. 
2 | Error message gets displayed when the user enters an invalid email and/or password on the login page. | Launch the URL for login view - <br />I. enter correct email, incorrect password. <br />II. enter incorrect email, correct password. <br />III. enter incorrect email and password. Validate that error message gets displayed to enter the appropriate fields correctly.
3 | User is navigated to the next page, on entering valid email and password. | Launch the URL for login view - enter both email and password fields correctly. Validate that the user is navigated to the Home View.
4 | System should be protected from SQL injection attacks. | Within the application, wherever there is a free text entry, enter a SQL statement instead of normal text input. For example, in any input text box enter:  **SELECT * FROM Users WHERE UserId = 105 OR 1=1;** <br />Validate that it does not query the database and return records. Ensure that the user input is sanitized and unwanted characters and strings are filtered or escaped to prevent the injection of harmful codes into the system.
5 | System should gracefully handle bad data from external systems. | Send API request from the application to the payment gateway. When the payment gateway responds with bad data, the system should throw a user-friendly exception to the end user. 
6 | System should enable easy communication between drivers and passengers. All workflows from every end user’s perspective should execute smoothly. | Validate that the entire ride booking or ride creation/acceptance workflows work smoothly for both the entities - drivers & passengers. <br /> •	Validate that Requests View should show updated ride requests from passengers, every time a new request is made. <br /> •	Validate that Matches View should show updated trips available list, every time a new trip matches with the passenger’s trip details. <br /> •	Validate that the entire payment workflow processes properly and is secured - the system should track if the passenger has successfully paid their dues to the driver and if the driver has successfully received the payment. <br /> •	Validate that passenger and driver should be able to successfully add their trip details including trip times, source/destination points, drop-off/pick up points, luggage amount, expected payment details, etc. <br /> •	Validate that the Reservation requests are processed properly by the system and are secured. <br /> •	Validate that both users are able to view their trip histories with all their trip information. <br /> •	Validate that passenger and driver should be able to view correct and updated navigation information through integration with Google maps server. <br /> •	Validate that passengers are able to make trip requests successfully. <br /> •	Validate that drivers are able to view the incoming trip requests and accept/deny requests.
7 | System should meet all the non-functional requirements.  | Validate that all the views of the system load within 3-5 seconds with no significant delays. <br />•	Validate that no system operation takes a significant amount of time. <br />•	Validate that all the exceptions thrown from the server are user friendly and easily understood by the user. <br />•	Validate that passed all the security tests by performing penetration tests and vulnerability scans. <br />•	Validate that new features can easily be added to the feature without taking significant effort to add them and such that the existing features do not break.  <br />•	Validate if the application runs properly on multiple operating systems and underlying hardware and different browsers. <br />•	Trace out all the security loopholes in the system.
8 | All the user interfaces within the system should get displayed and updated in real time as expected. | Apart from the basic app functionality like ensuring all views are functioning as expected, validate that the UI does not have any visual bugs. For example <br /> I.	Misaligned texts or buttons. <br /> II.	Overlapping images or texts. <br /> III.	Partially visible elements. <br />IV.	Responsive layout issues. For example, a table rendering correctly on the desktop browser but rendering incorrectly on a mobile browser.
9 | System should efficiently save, update and retrieve data from/to the database for the purpose of ride creation, ride booking and viewing of ride history. | <br />• Validate that the passengers are able to create a trip request successfully. System should retrieve matching available trips from the database efficiently and display them to the passenger. <br />•	Validate that drivers are able to create a trip successfully. System should be able to retrieve all trip requests from passengers to the driver in real time.<br />•	Searching and sorting operations on data should be efficient - for example, sorting the available trips data on Matches View based on the distance to destination.<br />•	Validate that the system processes the payment transactions smoothly and securely.
10 | Perform User Acceptance tests (UAT) on the system. | UAT, or user acceptance testing, is the most important type of testing for any piece of software. The app's usage pattern and frequently visited areas are provided by UAT. This will be useful in choosing the app's future features.
11 | System should be scalable and be able to handle at least 34,000 users. | Performance testing must be conducted based on the predicted demand in order to ensure that the search, map loading time, and other transactions meet the performance requirements both during peak and off-peak loads.
12 | System should ensure data accuracy in multiple points. | The entire system should be checked to assure data accuracy. This will include the data of the passenger, driver, trip information, trip fares, the distance calculations, etc. The accuracy of every data displayed on the app needs to be verified for its correctness.


### Additional Software

The System Reliability tests under this phase can be automated with the help of certain tools. **JMeter** can be used as a load testing tool for analyzing the performance of a variety of services, with a focus on web applications. **Webserver Stress Tool** can be used to evaluate whether the system’s performance is as expected when it is low on resources. An example for stress testing could be when multiple users are trying to perform the same transactions on the same data.


### Traceability Matrix

| Test Number | Requirement ID |
|-------------|----------------|
1 | FR-1, FR-11 
2 | FR-1, FR-11
3 | FR-1, FR-11
4 | FR-1, FR-2, FR-3, FR-4, FR-5, FR-6, FR-7, FR-9, FR-11, FR-12, FR-15, FR-18.<br />(All FRs where user can input any information through a text box).
5 | FR-9, FR-18, FR-19, FR-3, FR-4, FR-13, FR-14
6 | FR-1 to FR-20
7 | NFR-1 to NFR-10, except NFR-5, NFR-8, NFR-9, NFR-10
8 | FR-1 to FR-20 (all functional requirements that have some UI involved with them).
9 | FR-3 - FR-10, FR-13 - FR-20, NFR-6
10 | N/A (User Acceptance Testing)
11 | NFR-2
12 | FR-1 to FR-20


## Conclusion

It is important to understand that not every possible testing situation can be covered. The plan's strategy focuses on the key integrations between the two design elements that make up the RideVT system. The test plan should change as the system's design and requirements are refined. This test plan offers a strong foundation for starting to implement testing strategies and plans that will improve the quality of the software.