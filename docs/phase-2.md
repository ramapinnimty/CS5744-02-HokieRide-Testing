---
id: phase-2
title: Data Persistence/ Manipulation Phase
sidebar_label: Data Persistence/ Manipulation Phase
---

## Build

This build for this phase is designed to test DE-1 i.e. the Model-View-Controller, particularly the Model and Controller elements and DE-2 by testing for the integration of external services with the application.

## Purpose

The objective for this phase is to test that the data is properly created, stored, and retrieved for the purpose of ride creation, ride booking and viewing of ride history. The core of the application workflow is tested in this phase. The functional requirements tested in this phase are: FR-3 - FR-10, FR-13 - FR-20, along with NFR-6. This phase will ensure that valid details are successfully stored in the database after field values are cleaned. Additionally, it tests that if there are null, erroneous or invalid data values, the appropriate system response is produced. It will also test that the external services such as Google Maps, PayPal (amongst other payment applications) are well integrated into the system and are capable of being functional when needed.


This phase would test the following portions of the system:

1. Ride creation workflow - Add Ride, View Passengers, Accept/Reject passenger requests, receive payment, confirm ride. (driver)
2. Ride booking workflow - Enter source/dest, check ride availability, choose ride, make payment, receive confirmation. (rider)
3. Ride History Views - View Ride History (rider and driver).


## Test Cases

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


## Additional Software

Since much of this phase consists of testing the database and creation of different model objects in order to test different scenarios, it could be more efficient and effective to introduce automated testing. Although database testing can be tedious and there exists few tools that can help with database testing, **Selenium** offers some help on automating the process. To perform integration testing without going through the UI, we can programmatically send HTTP requests to the different URLs and assert the state of the system afterwards. These HTTP request tests can be automated to ease the testing process.  This can be done using tools like **TestComplete** as well as Selenium. Additionally, with the integration of third-party services, access to Google Maps API, Google location API, Paypal Payment API etc. would be necessary for testing.

