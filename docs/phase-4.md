---
id: phase-4
title: System Reliability Phase
sidebar_label: System Reliability Phase
---

## Build

The build for this phase consists of both the design elements i.e. DE-1, DE-2. 

## Purpose

The purpose of this phase is to test all the non-functional requirements of the system. It tests all the aspects which are not tested in functional testing. It is intended to test the readiness of a system according to nonfunctional criteria that functional testing never takes into account. The purpose of this phase is to increase usability, efficiency, maintainability and portability of the product. Other major non functional requirements that would be tested in this phase include system security, scalability and extensibility and performance. All the Non Functional Requirements NFR-1 to NFR-10 would be tested under this phase except NFR-5, NFR-8, NFR-9, NFR-10.


## Test Cases

| Test | Goal | Procedure & Expected behavior |
|------|------|-----------|
4.1 | Application loads in about 5 seconds once the user logs in. | Enter the email and password on the login page and validate that the Home View loads within 3 seconds.
4.2 | Application should be able to protect the privacy of the users and their personal information. | Perform vulnerability scans through automated software to scan a system against known vulnerability signatures. Perform penetration testing to simulate an attack from a malicious hacker. Ensure that the correct design pattern is followed such that security and privacy of user data is handled without affecting application performance. Ensure that passwords are encrypted and stored in a secure way. Ensure that payment services are secure through integration with external payment gateways.
4.3 | Application should be able to run on multiple operating systems. | Validate if the application runs properly on multiple operating systems including Android, IOS and desktop OS. Determine the look and feel of the application in the various browser types and various browser versions.
4.4 | Application should be extensible in order to incorporate any future changes. | Measure the level of effort required to add new features to the system. Perform regression on the existing features to ensure the new functionality does not break the existing one. Ensure that the right architecture is chosen during the design phase.
4.5 | Passengers should be able to see all available matches that are continuously updating. | Enter matching trip details for both driver and passenger, and validate if the Matches View updates with the newly available rides every time.
4.6 | Payment information should be kept confidential. | Validate that payment services are secure through integration with external payment gateways.
4.7 | Application performance is as expected under normal and expected conditions. | Validates that the system performs as expected when concurrent users access the application and get the expected response time.


## Additional Software

The System Reliability tests under this phase can be automated with the help of certain tools. **JMeter** can be used as a load testing tool for analyzing the performance of a variety of services, with a focus on web applications. **Webserver Stress Tool** can be used to evaluate whether the system’s performance is as expected when it is low on resources. An example for stress testing could be when multiple users are trying to perform the same transactions on the same data.
