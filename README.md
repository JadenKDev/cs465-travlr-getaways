# Travlr Getaways

**CS-465: Full Stack Development I**

Travlr Getaways is a full-stack travel application built using the MEAN stack. The project includes a customer-facing website, an Angular administrative interface, a REST API, MongoDB persistence, and token-based authentication.

## Technology Stack

- **MongoDB** — Stores trip and user data
- **Express.js** — Handles server routing and REST API endpoints
- **Angular** — Provides the administrative single-page application
- **Node.js** — Runs the server-side application
- **Mongoose** — Defines and interacts with MongoDB models
- **Handlebars** — Renders the customer-facing website
- **JSON Web Tokens (JWT)** — Provides authentication for protected operations

## Application Architecture

The project contains two user interfaces that interact with the same backend data.

### Customer Website

The customer-facing portion of the application uses Express and Handlebars to render trip information.

Trip data is retrieved from the REST API and displayed through server-rendered views.

### Administrative SPA

The administrative interface is built with Angular and provides functionality for managing trip information.

The Angular application includes:

- Trip listing
- Add trip form
- Edit trip form
- Reactive form validation
- Angular services for API communication
- Administrator login
- JWT storage and authentication state
- HTTP interceptor for authenticated requests

### REST API

Express provides REST endpoints used by both the server-rendered site and the Angular application.

Available trip endpoints include:

| Method | Endpoint | Purpose |
| --- | --- | --- |
| GET | `/api/trips` | Retrieve all trips |
| GET | `/api/trips/:tripCode` | Retrieve a specific trip |
| POST | `/api/trips` | Add a new trip |
| PUT | `/api/trips/:tripCode` | Update an existing trip |

Authentication endpoints include:

| Method | Endpoint | Purpose |
| --- | --- | --- |
| POST | `/api/register` | Register a user |
| POST | `/api/login` | Authenticate a user and return a JWT |

Trip creation and update operations require authentication.

## Database

Trip information is stored in MongoDB using Mongoose.

Each trip contains information including:

- Trip code
- Name
- Length
- Start date
- Resort
- Price per person
- Image
- Description

The application originally progressed from static data to JSON-based data and ultimately to persistent MongoDB storage.

## Authentication

The final version of the project adds administrator authentication.

Passwords are salted and hashed before storage. Successful authentication generates a JSON Web Token that expires after one hour.

The Angular application stores the token locally and uses an HTTP interceptor to attach the token to authenticated API requests.

Protected API operations verify the JWT before allowing changes to trip data.

## Project Progression

The repository preserves the development of the application across separate course modules:

- **module1** — Initial Express application and MVC structure
- **module2** — Dynamic routing and Handlebars views
- **module3** — Trip data integration
- **module4** — MongoDB and Mongoose persistence
- **module5** — REST API implementation
- **module6** — Angular administrative application
- **module7** — Authentication and application security

`module7` represents the final version of the course project.

## What I Implemented

Throughout the project I worked with both the frontend and backend portions of the application, including:

- Building Express routes and controllers
- Working with Handlebars templates
- Creating MongoDB/Mongoose models
- Building REST API endpoints
- Connecting application data to MongoDB
- Building Angular components
- Creating Angular services for API communication
- Implementing reactive forms
- Adding and editing trip records
- Implementing user registration and login
- Hashing and salting passwords
- Generating and validating JWTs
- Protecting write operations with authentication
- Adding an Angular HTTP interceptor for authenticated requests

## Skills Demonstrated

- Full-Stack Web Development
- JavaScript
- TypeScript
- Angular
- Node.js
- Express.js
- MongoDB
- Mongoose
- REST APIs
- MVC Architecture
- Reactive Forms
- Authentication
- JSON Web Tokens
- Client-Server Architecture

## Course Context

This project was completed for **CS-465: Full Stack Development I** at Southern New Hampshire University.

The course project was developed incrementally across multiple modules, with each branch preserving a stage of the application's development.
