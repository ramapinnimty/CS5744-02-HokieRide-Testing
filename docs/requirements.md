---
id: requirements
title: Requirements
sidebar_label: Requirements
---

This section details the scope of the requirements and design characteristics tested in each of the testing phases - (Authentication phase, Ride Booking phase - Location, Ride Booking phase - Details, Ride Booking phase - Payment, Ride History phase). We plan to cover most of the requirements both functional and non functional and leave out some of the requirements that are not fully operated or controllable by the current system since they are fully dependent on external services and systems that the software is connected to. The system consists of two major design modules - the MVC Module( Design element - 1 ), which will be referred to as DE-1, and the Client Server Module( Design element - 2 ) which will be referred to as DE-2 here on. Furthermore, there are modules in DE-1 within each layer of the MVC architecture. The model layer has - Driver, customer, vehicle, driver trip, passenger trip, payment models. The view layer has - Sign up and login view, Driver view (Home, requests, reservation), Passenger view (Home, matches, reservations), Map view, Payment view, Trip history view. Each of the requirements listed below is tested based on the DE and module it belongs to.


## Requirements Tested

### Functional Requirements

#### Student Driver

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


#### Student Passenger

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


### Non-functional requirements

- **NR-1** - The application should load in about 5 seconds and once the user logs in, the homepage of the application should load within 3 seconds.
- **NR-2** - The application should be scalable and be able to handle at least 34,000 users (approximate current enrollment at VT).
- **NR-3** - The application should be able to protect the privacy of the users and their personal information.
- **NR-4** - The application should be able to run on multiple operating systems such as android and IOS as well as the desktop.
- **NR-6** - Passengers should be able to see all available matches to drivers that update every time a trip that matches their preferences is posted.
- **NR-7** - Payment information such as card details should be kept confidential.



## Requirements not tested

### Non-functional requirements

- **NR-5** - The application should be extensible in order to incorporate any future changes in case any new features need to be added.
- **NR-8** - The application should be able to offer quick response time through notifications since ride sharing can be time-sensitive at times.
- **NR-9** - The application should be easily maintainable by the administrator in order to fix any bugs or run timely updates.
- **NR-10** - The application should be available to use at any time of the day without any server downtime issues.






