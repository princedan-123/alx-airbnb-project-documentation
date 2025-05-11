# 🏡 Airbnb Clone – Backend User Stories Documentation

## 📘 Introduction

This project is a **backend system for an Airbnb clone**, focused on building a RESTful API that supports core functionalities for both **Guests** and **Hosts**. The API enables user authentication, property listing management, booking, search, and payments — all tailored to a smooth short-term rental experience.

This README outlines the **functional user stories** that define expected behavior for guests and hosts, serving as a foundation for backend development.

---

## 👤 Guest User Stories

1. **Account Registration**
   - **Story**: As a guest, I want to register an account to manage my bookings and profile.
   - **API Endpoint**: `POST /api/v1/auth/register`
   - **Data**: `{ "email": "...", "password": "...", "name": "..." }`

2. **Secure Login (Email / OAuth)**
   - **Story**: As a guest, I want to log in using email/password or via Facebook.
   - **API Endpoints**:
     - `POST /api/v1/auth/login`
     - `GET /api/v1/auth/facebook`
   - **Token**: JWT should be returned and required for all authenticated routes.

3. **View Available Listings**
   - **Story**: As a guest, I want to browse available properties so I can book.
   - **API Endpoint**: `GET /api/v1/properties`
   - **Response**: Paginated, filterable listing data.

4. **Search and Filter Properties**
   - **Story**: As a guest, I want to search properties by **location**, **price**, and **guest count**.
   - **API Endpoint**: `GET /api/v1/properties?location=&minPrice=&maxPrice=&guests=`
   - **Result**: Paginated JSON of matching properties.

5. **Booking and Payment**
   - **Story**: As a guest, I want to book a property and pay securely in my currency.
   - **API Endpoint**:
     - `POST /api/v1/bookings`
     - `POST /api/v1/payments`
   - **Requirements**:
     - Date validation to prevent double-booking.
     - Payment via Stripe/PayPal.
     - Currency conversion support.

---

## 🏠 Host User Stories

1. **Host Account Registration**
   - **Story**: As a host, I want to register and manage my hosting profile.
   - **API Endpoint**: `POST /api/v1/auth/register?role=host`

2. **Passwordless Login via Email or OAuth**
   - **Story**: As a host, I want easy login (e.g., magic link, Facebook login).
   - **API Endpoint**: `GET /api/v1/auth/oauth/facebook`

3. **Post and Manage Properties**
   - **Story**: As a host, I want to list a property with details like title, description, images, location, price, and availability.
   - **API Endpoints**:
     - `POST /api/v1/properties`
     - `PUT /api/v1/properties/:id`
     - `DELETE /api/v1/properties/:id`

4. **Receive Instant Booking Notifications and Payments**
   - **Story**: As a host, I want instant in-app/email notifications and real-time payments when a booking occurs.
   - **Mechanisms**:
     - WebSockets or Event Emitters for real-time updates.
     - Email service (e.g., SendGrid, Nodemailer).
     - Payment split logic with Stripe Connect.

---

## 🔐 Authentication & Roles

- **JWT-based authentication** for secure access.
- **OAuth 2.0** support for Google/Facebook login.
- Roles:
  - `guest`
  - `host`
  - `admin` (for dashboard control)

---