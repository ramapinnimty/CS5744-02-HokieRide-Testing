---
id: phase-1
title: Authentication/Security Phase
sidebar_label: Authentication/Security Phase
---

## Build

The build for this phase consists of both the modules: DE-1, DE-2.


## Purpose

The purpose of this phase is to validate the working of the user (driver and rider) signup and login functionalities. Additionally, this phase ensures that the user information is stored securely and is well protected. Requirements FR-1, FR-2, FR-11, FR-12, NFR-1, NFR-3, NFR-6, and NFR-7 will be covered in this phase.

## Test Cases

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



## Additional Software

SSO, Multi-factor authentication (2FA etc), SHA keys for password protection etc.
