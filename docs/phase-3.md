---
id: phase-3
title: User Interface Phase
sidebar_label: User Interface Phase
---

## Build

The build for this phase consists of the design element DE-1 i.e. the Model-View-Controller element, more specifically the View element.

## Purpose

The purpose of this phase is to ensure that all the fields, labels, buttons, and other elements on the screen work as expected. It ensures that all the views or pages in the application function as expected. It primarily involves testing different UI elements, if they are in their correct place as per the UX designs, they correctly respond to user inputs. Various UI functionalities like testing if the visibility (hide/show an element), disability (enable/disable input on particular element), etc. can be tested in this phase. UI testing involves testing the visual elements to verify that they are functioning according to requirements – in terms of functionality and performance. All the Functional Requirements (FR-1 to FR-20) that have some User interface involved with them would be tested under this phase. 

## Test Cases

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



## Additional Software

The User interface tests under this phase can be automated with the help of certain tools or software. Some automation tools like **Selenium** or **Cypress** can be used to automate the UI testing. Since tests can be written in any language under these frameworks and can be carried out under any underlying OS. The main challenge in User Interface testing is to deal with frequent changes in the UI and ensuring that all tests are adapted to the new changes.
