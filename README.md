
# User Authentication API

A secure REST API built with Spring Boot for user authentication and management, featuring JWT token-based authentication, email verification, and PostgreSQL database integration.

## Features

- **User Registration** - Create new user accounts with email verification
- **User Authentication** - Login with JWT token generation
- **Email Verification** - Account activation via verification codes
- **Protected Endpoints** - Secure user profile and data access
- **Password Security** - Encrypted password storage
- **Database Integration** - PostgreSQL for persistent data storage

## Tech Stack

- **Java 17** - Programming language
- **Spring Boot 3.5.3** - Application framework
- **Spring Security** - Authentication and authorization
- **Spring Data JPA** - Database abstraction layer
- **JWT (JSON Web Tokens)** - Stateless authentication
- **PostgreSQL** - Database
- **Lombok** - Code generation library
- **Gradle** - Build tool

## API Endpoints

### Authentication
- `POST /auth/signup` - Register a new user
- `POST /auth/login` - User login
- `POST /auth/verify` - Verify user account with code
- `POST /auth/resend` - Resend verification code

### User Management
- `GET /users/me` - Get current authenticated user profile
- `GET /users/` - Get all users (protected)

## Prerequisites

- Java 17 or higher
- PostgreSQL database
- Gradle (or use included wrapper)

## Setup & Installation

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd user_authentication
   ```

2. **Configure Database**
    - Create a PostgreSQL database
    - Update `application.properties` with your database credentials

3. **Configure Email Service**
    - Set up email server configuration in `application.properties`

4. **Build and Run**
   ```bash
   ./gradlew bootRun
   ```

The application will start on `http://localhost:8080`

## Security

- Passwords are encrypted using Spring Security
- JWT tokens for stateless authentication
- Email verification required for account activation
- Protected endpoints require valid JWT tokens

## Database Schema

The application uses JPA entities with automatic schema generation. The main entities include:
- User (with authentication details)
- Role-based access control

## Contributing

1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Push to the branch
5. Create a Pull Request

## License

This project is open source and available under the [MIT License](LICENSE).