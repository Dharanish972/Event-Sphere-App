Event Sphere App
The main goal of Event Sphere is to provide a simple and efficient online platform for event management and registration. It helps users easily discover and register for events while enabling organizers to create, manage, and monitor events from a single system.

Languages Used in goal

HTML (HyperText Markup Language)

Creates the basic structure of the website.
Used to design pages such as Home, Login, Registration, and Event Details.

CSS (Cascading Style Sheets)

Improves the appearance of the website.
Adds colors, layouts, fonts, animations, and responsive designs.

JavaScript

Adds interactivity and functionality.
Handles user actions such as registration, event creation, searching events, and form validation.

Local Storage

Stores user and event data inside the browser.
Allows data to remain available even after refreshing the page.
Key Features
User Registration and Login
Event Creation and Management
Event Registration System
Search and Filter Events
View Event Details
Dashboard for Upcoming Events
Responsive User Interface
Real-World Uses

Educational Institutions
Managing symposiums, workshops, seminars, and cultural events.

Companies
Organizing meetings, training sessions, conferences, and employee events.

Community Organizations
Conducting sports tournaments, charity events, awareness programs, and public gatherings.

Advantages
Reduces manual paperwork.
Saves time and effort for organizers and participants.
Provides quick and easy event registration.
Centralizes event information in one place.
Accessible through any web browser.
Improves event organization and user experience

Event Sphere is a frontend-based event management application developed using HTML, CSS, JavaScript, and Local Storage. It simplifies the process of event creation, management, and registration, making it useful for colleges, companies, and organizations that conduct events regularly.

 Project Statement
The Event Sphere App is designed to simplify event management and participation. It provides a unified platform where organizers can publish events, users can discover and register, and administrators can oversee smooth operations. The app bridges the gap between event hosts and attendees, ensuring seamless communication, scheduling, and engagement.

 Objectives
Provide a centralized hub for event discovery and booking.

Enable organizers to create, manage, and promote events efficiently.

Offer users personalized event recommendations based on interests.

Ensure secure registration, ticketing, and payment integration.

Facilitate real-time updates, notifications, and reminders.

Support analytics for organizers to track attendance and engagement.

 Requirements Gathering
Functional Requirements:

Event creation and publishing

User registration and login

Ticket booking and payment gateway

Notifications and reminders

Event search and filtering

Analytics dashboard for organizers

Non-Functional Requirements:

Scalability to handle large events

Secure authentication and data protection

Cross-platform accessibility (Web & Mobile)

High performance and low latency

 User Identification
Event Organizers → Create, manage, and analyze events.

Attendees/Users → Discover, register, and participate in events.

Administrators → Monitor system health, manage users, and ensure compliance.

 Module Identification
Authentication Module

User login, signup, and role-based access.

Event Management Module

Event creation, editing, scheduling, and publishing.

User Dashboard Module

Personalized event feed, recommendations, and registrations.

Ticketing & Payment Module

Secure ticket booking, payment gateway integration, and receipts.

Notification Module

Real-time alerts, reminders, and updates.

Analytics & Reporting Module

Attendance tracking, engagement metrics, and organizer insights.

Admin Control Module

User management, event approval, and system monitoring.

                    +----------------------+
                    |      Event Sphere    |
                    +----------------------+

      User/Participant                    Organizer
              |                                |
              |                                |
   ---------------------          -------------------------
   | Register Account |          | Create Event          |
   | Login            |          | Update Event          |
   | Browse Events    |          | Delete Event          |
   | View Event Info  |          | Manage Registrations  |
   | Register Event   |          | View Reports          |
   | Make Payment     |          | Send Notifications    |
   | Download Ticket  |          -------------------------
   | View Registration|
   ---------------------
              |
              |
      Payment Gateway
              |
      ----------------
      | Process Payment |
      ----------------

              |
              |
             Admin
              |
      -------------------------
      | Manage Users          |
      | Manage Events         |
      | Verify Payments       |
      | Generate Reports      |
      | Manage System Settings|
      
      UML USE CASE DIAGRAM
              User
          |
          +----> Register
          +----> Login
          +----> Browse Events
          +----> Register Event
          +----> Make Payment
          +----> Download Ticket

      Organizer
          |
          +----> Create Event
          +----> Manage Event
          +----> Manage Registrations
          +----> Generate Reports

        Admin
          |
          +----> Manage Users
          +----> Manage Events
          +----> Verify Payments
          +----> System Maintenance

   Payment Gateway
          |
          Process Payment 


          Database Requirement Analysis for Event Sphere App
Introduction

The Event Sphere App is an event management and registration system that allows users to discover, register, and participate in various events. The database is designed to store and manage information related to users, events, registrations, payments, tickets, and event organizers. A well-structured database ensures efficient data storage, retrieval, and management while maintaining data integrity and security.

Functional Requirements
1. User Management

The system should:

Store user registration details.
Allow users to log in and manage their profiles.
Maintain user contact information.
Support different user roles such as Participant, Organizer, and Admin.
2. Event Management

The system should:

Store event information.
Allow organizers to create, update, and delete events.
Maintain event schedules, venues, and capacities.
Display event details to users.
3. Event Registration

The system should:

Allow users to register for events.
Track registration status.
Maintain participant records for each event.
Prevent registrations beyond event capacity.
4. Payment Management

The system should:

Store payment details.
Track payment status.
Link payments to event registrations.
Maintain transaction records.
5. Ticket Management

The system should:

Generate tickets after successful registration.
Store ticket information.
Maintain ticket validity and status.
6. Notification Management

The system should:

Store notification records.
Send event updates and reminders.
Maintain notification history.
7. Reporting and Analytics

The system should:

Generate registration reports.
Provide event participation statistics.
Track payment summaries.
Data Requirements

The database should store the following information:

User Data
User ID
Name
Email
Phone Number
Password
Role
Registration Date
Event Data
Event ID
Event Name
Description
Category
Date and Time
Venue
Capacity
Status
Registration Data
Registration ID
User ID
Event ID
Registration Date
Registration Status
Payment Data
Payment ID
Registration ID
Amount
Payment Method
Transaction ID
Payment Status
Payment Date
Ticket Data
Ticket ID
Registration ID
Ticket Number
QR Code
Ticket Status
Notification Data
Notification ID
User ID
Message
Notification Date
Status
Non-Functional Requirements
Performance
Fast retrieval of event and registration information.
Support multiple users simultaneously.
Security
Secure storage of user credentials.
Protection of payment information.
Role-based access control.
Reliability
Accurate data storage and retrieval.
Consistent transaction processing.
Scalability
Ability to handle increasing numbers of users and events.
Availability
Database should be available whenever users access the system.
Main Entities
User
Event
Organizer
Registration
Payment
Ticket
Notification
Admin
Relationships
One User can register for many Events.
One Event can have many Registrations.
One Registration has one Payment.
One Registration generates one Ticket.
One Organizer manages many Events.
One User can receive many Notifications.
One Admin manages multiple Users and Events.

+------------------+
|      USER        |
+------------------+
| User_ID (PK)     |
| Name             |
| Email            |
| Phone            |
| Password         |
| Role             |
+------------------+
         |
         | Registers
         | 1:M
         v
+------------------+
|  REGISTRATION    |
+------------------+
| Registration_ID  |
| User_ID (FK)     |
| Event_ID (FK)    |
| Register_Date    |
| Status           |
+------------------+
         |
         | 1:1
         v
+------------------+
|    PAYMENT       |
+------------------+
| Payment_ID (PK)  |
| Registration_ID  |
| Amount           |
| Payment_Method   |
| Payment_Status   |
| Payment_Date     |
+------------------+
         |
         | 1:1
         v
+------------------+
|     TICKET       |
+------------------+
| Ticket_ID (PK)   |
| Registration_ID  |
| Ticket_Number    |
| QR_Code          |
| Ticket_Status    |
+------------------+


+------------------+
|   ORGANIZER      |
+------------------+
| Organizer_ID(PK) |
| Name             |
| Email            |
| Phone            |
+------------------+
         |
         | Creates
         | 1:M
         v
+------------------+
|      EVENT       |
+------------------+
| Event_ID (PK)    |
| Organizer_ID(FK) |
| Event_Name       |
| Description      |
| Category         |
| Event_Date       |
| Venue            |
| Capacity         |
| Status           |
+------------------+
         ^
         |
         | M:1
         |
+------------------+
|  REGISTRATION    |
+------------------+


+------------------+
|      ADMIN       |
+------------------+
| Admin_ID (PK)    |
| Name             |
| Email            |
| Password         |
+------------------+
         |
         | Manages
         |
         v
+------------------+
| USER / EVENT     |
+------------------+


+------------------+
|  NOTIFICATION    |
+------------------+
| Notification_ID  |
| User_ID (FK)     |
| Message          |
| Date_Time        |
| Status           |
+------------------+
         ^
         |
         | 1:M
         |
+------------------+
|      USER        |
+------------------+

Database Schema Creation for Event Sphere App
1.USER
| Attribute         | Key |
| ----------------- | --- |
| User_ID           | PK  |
| Name              |     |
| Email             |     |
| Phone_Number      |     |
| Password          |     |
| Role              |     |
| Registration_Date |     |

2.ORGANIZER

| Attribute    | Key |
| ------------ | --- |
| Event_ID     | PK  |
| Organizer_ID | FK  |
| Event_Name   |     |
| Description  |     |
| Category     |     |
| Event_Date   |     |
| Start_Time   |     |
| End_Time     |     |
| Venue        |     |
| Capacity     |     |
| Status       |     |

3.EVENT

| Attribute    | Key |
| ------------ | --- |
| Event_ID     | PK  |
| Organizer_ID | FK  |
| Event_Name   |     |
| Description  |     |
| Category     |     |
| Event_Date   |     |
| Start_Time   |     |
| End_Time     |     |
| Venue        |     |
| Capacity     |     |
| Status       |     |

4.REGISTRATION

| Attribute           | Key |
| ------------------- | --- |
| Registration_ID     | PK  |
| User_ID             | FK  |
| Event_ID            | FK  |
| Registration_Date   |     |
| Registration_Status |     |

5.PAYMENT

| Attribute       | Key |
| --------------- | --- |
| Payment_ID      | PK  |
| Registration_ID | FK  |
| Amount          |     |
| Payment_Method  |     |
| Transaction_ID  |     |
| Payment_Status  |     |
| Payment_Date    |     |

6.TICKET

| Attribute       | Key |
| --------------- | --- |
| Ticket_ID       | PK  |
| Registration_ID | FK  |
| Ticket_Number   |     |
| QR_Code         |     |
| Issue_Date      |     |
| Ticket_Status   |     |

7.NOTIFICATION

| Attribute         | Key |
| ----------------- | --- |
| Notification_ID   | PK  |
| User_ID           | FK  |
| Message           |     |
| Notification_Date |     |
| Status            |     |

8.ADMIN

| Attribute | Key |
| --------- | --- |
| Admin_ID  | PK  |
| Name      |     |
| Email     |     |
| Password  |     |
| Role      |     |

UI Wireframe Design for Event Sphere App
1. Home Page
2. +--------------------------------------------------+
|                 EVENT SPHERE                     |
+--------------------------------------------------+
| Home | Events | My Tickets | Profile | Login     |
+--------------------------------------------------+

|  Search Events __________________ [Search]       |

+--------------------------------------------------+
| Featured Event                                   |
| Event Image                                      |
| Event Name                                       |
| Date | Venue                                     |
| [View Details]                                  |
+--------------------------------------------------+

+--------------------------------------------------+
| Upcoming Events                                  |
| Event Card 1                                     |
| Event Card 2                                     |
| Event Card 3                                     |
+--------------------------------------------------+
2. User Registration Page
+--------------------------------------+
|         Create Account               |
+--------------------------------------+

| Full Name      [____________]        |
| Email          [____________]        |
| Phone Number   [____________]        |
| Password       [____________]        |
| Confirm Pass   [____________]        |

|        [ Register ]                  |

| Already have an account? Login       |
+--------------------------------------+
3. Login Page
+--------------------------------------+
|              Login                   |
+--------------------------------------+

| Email      [____________]            |
| Password   [____________]            |

|        [ Login ]                     |

| Forgot Password?                     |
| Create New Account                   |
+--------------------------------------+
4. Event Listing Page
+--------------------------------------------------+
|                    EVENTS                         |
+--------------------------------------------------+

| Search Event _______________________              |

+--------------------------------------------------+
| Event Image                                      |
| Event Name                                       |
| Date | Venue                                     |
| Category                                          |
| [View Details]                                  |
+--------------------------------------------------+

+--------------------------------------------------+
| Event Image                                      |
| Event Name                                       |
| Date | Venue                                     |
| Category                                          |
| [View Details]                                  |
+--------------------------------------------------+
5. Event Details Page
+--------------------------------------------------+
|                 EVENT DETAILS                     |
+--------------------------------------------------+

| Event Banner Image                               |

| Event Name                                       |
| Date: __________                                 |
| Time: __________                                 |
| Venue: _________                                 |
| Organizer: _____                                 |

| Description                                      |
| ______________________________________________   |
| ______________________________________________   |

| Registration Fee: ₹_____                         |

|           [ Register Now ]                       |
+--------------------------------------------------+
6. Registration Form Page
+--------------------------------------+
|        EVENT REGISTRATION            |
+--------------------------------------+

| Name         [____________]          |
| Email        [____________]          |
| Phone        [____________]          |

| Event Name: __________________       |

|        [ Confirm Registration ]      |
+--------------------------------------+
7. Payment Page
+--------------------------------------+
|            PAYMENT                   |
+--------------------------------------+

| Event Name : __________              |
| Amount     : ₹______                 |

| Payment Method                       |
| ( ) UPI                              |
| ( ) Credit Card                      |
| ( ) Debit Card                       |
| ( ) Net Banking                      |

|       [ Pay Now ]                    |
+--------------------------------------+
8. Ticket Page
+--------------------------------------------------+
|                 E-TICKET                          |
+--------------------------------------------------+

| Ticket Number : EVT12345                         |
| Event Name    : __________                       |
| Participant   : __________                       |
| Date & Time   : __________                       |
| Venue         : __________                       |

|            [ QR CODE ]                           |

|       [ Download Ticket ]                        |
+--------------------------------------------------+
9. Organizer Dashboard
+--------------------------------------------------+
|              ORGANIZER DASHBOARD                  |
+--------------------------------------------------+

| Total Events : 10                                |
| Registrations: 350                               |
| Revenue      : ₹50,000                           |
+--------------------------------------------------+

| [Create Event]                                   |

+--------------------------------------------------+
| My Events                                        |
| Event 1  [Edit] [Delete]                         |
| Event 2  [Edit] [Delete]                         |
+--------------------------------------------------+
10. Admin Dashboard
+--------------------------------------------------+
|                ADMIN DASHBOARD                    |
+--------------------------------------------------+

| Total Users      : 500                           |
| Total Events     : 50                            |
| Total Revenue    : ₹2,00,000                     |
+--------------------------------------------------+

| [Manage Users]                                   |
| [Manage Events]                                  |
| [View Reports]                                   |
| [System Settings]                                |
+--------------------------------------------------+
Main Screens
Home Page
User Registration
Login
Event Listing
Event Details
Registration Form
Payment
Ticket Generation
Organizer Dashboard
Admin Dashboard








      


