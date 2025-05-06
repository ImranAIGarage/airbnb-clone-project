# Airbnb Clone Project

A full-stack Airbnb-style web application that allows users to list, search, book, and review rental properties globally.

---

## Project Goals

- Build a scalable, production-ready rental platform
- Practice full-stack development and collaboration
- Understand database and API design
- Apply real-world software engineering workflows

---

## Technology Stack

### Django
A high-level Python web framework used to build secure and scalable backend services and RESTful APIs.

### PostgreSQL
An open-source relational database used to store structured data like users, properties, and bookings.

### Django REST Framework (DRF)
Used to build RESTful APIs quickly and efficiently with Django.

### GraphQL *(optional)*
A query language for APIs, allowing clients to request only the data they need.

### React
JavaScript library for building dynamic user interfaces and handling frontend routing.

### Tailwind CSS
Utility-first CSS framework that helps rapidly build custom UI designs.

### Docker
Used to containerize the application, making it portable and consistent across environments.

### Git & GitHub
Version control and collaboration platform for code tracking and team contributions.

---

## Database Design

### 1. **Users**
- `id`, `name`, `email`, `passwordHash`, `isHost`
- A user can manage listings and make bookings.

### 2. **Properties**
- `id`, `userId`, `title`, `location`, `pricePerNight`
- A property belongs to a user and can have multiple bookings/reviews.

### 3. **Bookings**
- `id`, `userId`, `propertyId`, `startDate`, `endDate`
- Links guests to properties for specific dates.

### 4. **Reviews**
- `id`, `userId`, `propertyId`, `rating`, `comment`
- Allows users to rate and review properties.

### 5. **Payments**
- `id`, `bookingId`, `amount`, `status`, `paymentMethod`
- Tracks payment transactions tied to bookings.

---

## Team Roles

### Project Manager
Oversees timelines, task allocation, and team coordination.

### Backend Developer
Builds APIs, handles server logic, and integrates the database.

### Frontend Developer
Develops responsive UI and connects frontend to backend APIs.

### Database Administrator
Designs and optimizes the database structure.

### QA Engineer
Tests application functionality and ensures stability.

### DevOps Engineer
Manages deployments, CI/CD, and system uptime.

---

## Feature Breakdown

### User Management
User registration, login, and profile management with roles for hosts and guests.

### Property Management
Hosts can list, edit, and remove properties with images, pricing, and descriptions.

### Booking System
Guests can book available properties for specific dates. System avoids double bookings.

### Reviews and Ratings
Users can leave feedback after their stays to help inform others.

### Payment Integration
Secure booking payments are tracked by method, status, and amount.

### Search and Filtering
Search listings by location, price, availability, and other filters.

### Responsive UI
Works across devices for a seamless user experience.

---

## API Security

### Authentication
JWT tokens ensure only logged-in users can access protected endpoints.

### Authorization
Role-based access (guest vs host) controls permissions for key actions.

### Rate Limiting
Protects the app from abuse by limiting the number of API requests per user/IP.

### Input Validation
Prevents SQL injections and XSS by sanitizing incoming data.

### TTPS Enforcement
Encrypts data in transit to protect sensitive information.

---

## CI/CD Pipeline

### What is CI/CD?
CI/CD automates code integration, testing, and deployment processes. It ensures quick, safe, and consistent delivery of new features.

### Tools Used
- **GitHub Actions**: Runs automated tests and builds on each push.
- **Docker**: Containerizes app environments.
- **Vercel / Netlify / Railway**: Handles automated deployments from GitHub.

