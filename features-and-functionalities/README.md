# Airbnb Clone Backend - Functional Requirements

## 📌 Overview

This document outlines the core **functional requirements** of the backend system for an Airbnb Clone. These features define the essential behaviors and interactions between guests, hosts, and administrators within the platform.

---

## 🚀 Functional Modules

### 1. User Management
- User registration (Guest or Host)
- Secure authentication (OAuth and JWT)
- Authorization for admin users
- User profile management

### 2. Host Interaction: Property Listing
- Hosts can create property listings with:
  - Title, description, location, price, amenities, availability
- Hosts can edit or remove their listings

### 3. Guest Interaction: Search and Filtering
- Guests can search properties by:
  - Location
  - Price range
  - Number of guests
- Paginated search results

### 4. Booking Management
- Guests can book properties for selected dates
- Prevent double bookings using date validation
- Cancellable bookings based on policy
- Track booking statuses (pending, confirmed, cancelled)

### 5. Payment Gateway Integration
- Guests can make payments to hosts
- Hosts receive payments once bookings are confirmed
- Support for multiple currencies

### 6. Review and Rating
- Guests can review and rate properties **after booking**
- One review per completed booking

### 7. Notification System
- Hosts receive email and in-app notifications for:
  - New bookings
  - Guest reviews or ratings
  - Payment confirmations
- Guests receive notifications for:
  - Booking confirmations

### 8. Admin Dashboard
- Admins can manage:
- Users
- Property listings
- Bookings
