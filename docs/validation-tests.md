---
id: validation-tests
title: Validation Tests
sidebar_label: Validation Tests
---

## Build

The build for this phase consists of both the design elements i.e. DE-1, DE-2. 

## Purpose

The purpose of this build is to ensure that the software actually meets the requirements for the project. It can also be defined as a testing to validate that the product fulfills its intended use when deployed in an appropriate environment. The build consists of the entire system - meaning all modules or design elements of the system. Validation tests are organized around a traceability matrix (specified at the end), that maps the validation test cases to the requirements for the project. This build would involve various types of software testing – integration tests, system tests, user acceptance tests, regression tests, cross browser and cross device testing. 

## Test Cases

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


## Additional Software

The System Reliability tests under this phase can be automated with the help of certain tools. **JMeter** can be used as a load testing tool for analyzing the performance of a variety of services, with a focus on web applications. **Webserver Stress Tool** can be used to evaluate whether the system’s performance is as expected when it is low on resources. An example for stress testing could be when multiple users are trying to perform the same transactions on the same data.


## Traceability Matrix

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

