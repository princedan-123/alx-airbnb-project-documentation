use Case Diagram for Airbnb Platform

This README provides a description of the use case diagram illustrating the functionalities of a simplified Airbnb platform. The diagram outlines the interactions between two primary actors, the Guest and the Host, and the various use cases they can engage with within the Airbnb system.

## Actors

* **Guest:** An individual who uses the Airbnb platform to find and book accommodations.
* **Host:** An individual who uses the Airbnb platform to list their property for booking by guests.

## Use Cases

The following use cases are depicted in the diagram:

* **User Registration:** Allows new users (both Guests and Hosts) to create an account on the platform.
    * **<<include>> User Profile Set Up:** This mandatory included use case details the process of providing necessary personal and profile information after registration.
* **(Authentication):** Enables registered users (Guests and Hosts) to securely log in to their accounts.
    * **<<include>> Credential Verification:** This mandatory included use case represents the process of verifying the provided login credentials.
* **Property Booking/Listing:** This use case encompasses two distinct but related actions:
    * **Guest:** Browsing and booking available properties.
    * **Host:** Creating and managing property listings.
    * **<<extend>> Error Message:** Under certain conditions within the "Property Booking/Listing" use case, the system may extend to display an error message (e.g., invalid dates, unavailable property).
* **Payment:** Allows Guests to pay for their bookings.
    * **Payment Methods:** This includes options for payment via Paypal and Credit Card.
    * **<<include>> Payout to Host:** This mandatory included use case details the process of transferring payment from the Guest to the Host after a booking is completed (or according to the platform's policy).

## Relationships Between Use Cases

* **<<include>> (Inclusion):** Indicates that the base use case explicitly incorporates the behavior of the included use case. The included use case is essential for the base use case to function. For example, "User Registration" must include "User Profile Set Up," and "Authentication" must include "Credential Verification." Similarly, "Payment" includes "Payout to Host."
* **<<extend>> (Extension):** Indicates that the extending use case adds optional behavior to the base use case. The base use case can function independently of the extending use case. For example, "Error Message" extends "Property Booking/Listing" only when certain conditions are met.

## System Boundary

The rectangle labeled "Airbnb" defines the boundary of the system under consideration. All the use cases reside within this boundary, representing the functionalities offered by the Airbnb platform. The actors (Guest and Host) interact with the system from outside this boundary.

## Purpose

This use case diagram provides a high-level overview of the key interactions and functionalities within the Airbnb platform from the perspective of the Guest and the Host. It helps to understand the main features of the system and the relationships between them.