## airbnb-clone-project

## Team Roles

**Backend Developer**: Responsible for implementing API endpoints, database schemas, and business logic.
**Database Administrator**: Manages database design, indexing, and optimizations.
**DevOps Engineer**: Handles deployment, monitoring, and scaling of the backend services.
**QA Engineer**: Ensures the backend functionalities are thoroughly tested and meet quality standards.

## Technology Stack

Django: A high-level Python web framework used for building the RESTful API.
Django REST Framework: Provides tools for creating and managing RESTful APIs.
PostgreSQL: A powerful relational database used for data storage.
GraphQL: Allows for flexible and efficient querying of data.
Celery: For handling asynchronous tasks such as sending notifications or processing payments.
Redis: Used for caching and session management.
Docker: Containerization tool for consistent development and deployment environments.
CI/CD Pipelines: Automated pipelines for testing and deploying code changes.


## Database Design
The database schema is designed to support the core functionalities of a vacation rental platform, such as:

User registration and authentication
Listing properties for rent
Searching and booking properties
Reviewing stays
Processing payments

1. Users

Represents all users on the platform, including both guests and hosts.

# Relationships:

One user can list many properties.
One user can make many bookings.
One user can write many reviews.
One user can make many payments.

2. Properties

Represents properties that are listed for rent by hosts.

# Relationships:

Each property is owned by one host (user).
A property can have many bookings.
A property can have many reviews.

3. Bookings

Represents a reservation made by a guest for a property.

# Relationships:

A booking is made by one user (guest).
A booking is for one property.
A booking may have one payment.

4. Reviews

Captures feedback from guests after their stay.

# Relationships:

A review is written by one user.
A review is about one property.
A user can review a property only once per booking.

5. Payments

Handles transaction records for bookings.
# Relationships:

 Each payment is linked to one booking.
 A user makes many payments, but each payment belongs to one booking.

 ## Feature Breakdown
 1.User management ~deals with user registration,authentication and user details retrival and update~
 2.Property management 
 3.Booking system
 4.Payment system
 5.Review management


 ## API Security
 The key security measures implemented include session management,rate limiting,user authentication using two factor authentication. This security measures are crucial to ensure that transactions performed online via this project's payment system are protected from attacks.

 ## CI/CD Pipeline

 mainly used for continous intergration of features as the project progresses.I opted for docker and github  