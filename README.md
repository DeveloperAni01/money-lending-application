
# Money Lending Application Backend

A robust, scalable backend for a money lending application, inspired by platforms like Slice and KreditBee. Built with Node.js, Express, and MongoDB, this backend provides secure APIs for user registration, authentication, profile management, borrowing, and financial recommendations.

---

## Features

- **User Registration & Authentication**: Secure signup, login, logout, and password change with JWT-based authentication.
- **Borrowing System**: Users can borrow money within calculated purchase power and receive monthly repayment calculations.
- **Financial Recommendation**: Personalized borrowing limit recommendations based on user income, expenses, and existing debt.
- **Protected Routes**: Sensitive endpoints secured with JWT and HTTP-only cookies.
- **Input Validation**: Comprehensive validation for all user inputs.
- **Error Handling**: Consistent API error and response structure.
- **Environment Configuration**: Uses `.env` for all sensitive and environment-specific settings.

---

## Tech Stack

- **Node.js** & **Express.js**: Backend framework
- **MongoDB** & **Mongoose**: Database and ODM
- **JWT**: Authentication
- **bcrypt**: Password hashing
- **cookie-parser**: Secure cookie management
- **moment.js**: Date handling
- **dotenv**: Environment variable management
- **debug**: Structured logging

---

## Getting Started

### Prerequisites

- Node.js (v16+ recommended)
- MongoDB instance (local or cloud)
- [Postman](https://www.postman.com/) or similar API client

### Installation

1. **Clone the repository**
   ```sh
   git clone https://github.com/your-username/money-lending-application-backend.git
   cd money-lending-application-backend
   ```

2. **Install dependencies**
   ```sh
   npm install
   ```

3. **Configure environment variables**

   Create a `.env` file in the root directory with the following variables:

   ```
   PORT=8000
   MONGODB_URL=your_mongoDB_url
   ACCESS_TOKEN_SECRET=your_access_token_secret
   REFRESH_TOKEN_SECRET=your_refresh_token_secret
   ACCESS_TOKEN_EXPIRY=your_own_token_expiry
   REFRESH_TOKEN_EXPIRY=your_own_token_expiry
   CORS_ORIGIN=yours_cors_origin
   JSON_LIMIT=your_own_json_limit
   MIN_AGE=your_own_limit_age
   MIN_SALARY=use_your_own
   SAFE_PERCENTAGE=your_own_safe_percentage
   ANNUAL_INTEREST_RATE=your_own_interest_rate
   ```

   Adjust values as needed for your environment.

4. **Start the server**
   ```sh
   npm start
   ```

   The server will run on `http://localhost:8000` by default.

---

## API Documentation

- **Postman Collection**: [View Documentation](https://documenter.getpostman.com/view/36163643/2sA3kUH2cL)
- **Sample Outputs**: [Google Drive Link](https://drive.google.com/drive/folders/16Wq8nzm68oWVQXjzHZ2-hpFBowoIRBkp?usp=drive_link)

---

## Project Structure

```
src/
  app.js                # Express app setup and middleware
  index.js              # Entry point, DB connection, server start
  controllers/
    user.controller.js  # User-related business logic
  db/
    db.js               # MongoDB connection logic
  middlewares/
    auth-middleware.js  # JWT authentication middleware
  models/
    user.model.js       # User Mongoose schema/model
  routes/
    user.routes.js      # User API routes
  utils/
    ...                 # Utility classes and helpers
docs/                   # Project documentation
```

---

## Security Best Practices

- All sensitive data is managed via environment variables.
- Passwords are hashed using bcrypt before storage.
- JWT tokens are stored in HTTP-only, secure cookies.
- All protected routes require valid JWT authentication.

---

## Contributing

Contributions are welcome! Please open issues or submit pull requests for improvements or bug fixes.

---

## License

This project is licensed under the [ISC License](LICENSE).

---

## Author

**Anirban Mondal**

---

## Acknowledgements

- [Express.js](https://expressjs.com/)
- [MongoDB](https://www.mongodb.com/)
- [Mongoose](https://mongoosejs.com/)
- [JWT](https://jwt.io/)
- [bcrypt](https://github.com/kelektiv/node.bcrypt.js)
```

