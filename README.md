# Job Blog Project
![Node Js](https://img.shields.io/badge/NodeJS-v14-green)
![MySQL](https://img.shields.io/badge/MONGODB-v8.40-blue)
![MySQL](https://img.shields.io/badge/Express-blue)
![MySQL](https://img.shields.io/badge/CSS-pink)

## Website Screenshot
![Project Image](image.png)

This is a mini project built with Node.js, Express, and MongoDB. It includes features such as authentication using bcrypt and JSON Web Tokens (JWT), session management with express-session and connect-mongo, and more.

## Features

- User authentication with bcrypt and JWT.
- Secure session management using express-session and connect-mongo.
- CRUD operations for blog posts.
- MongoDB as the database for storing user and blog data.
- Modular and scalable code structure.

## Prerequisites

Ensure you have the following installed on your system:

- [Node.js](https://nodejs.org/) (v14 or later)
- [MongoDB](https://www.mongodb.com/)

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/AviralTechie/Job_Blog-.git
   cd Job_Blog
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Create a `.env` file in the root directory and add the following:
   ```env
   PORT=3000
   MONGO_URI=<your-mongodb-connection-string>
   JWT_SECRET=<your-jwt-secret>
   SESSION_SECRET=<your-session-secret>
   ```

4. Start the MongoDB server locally or ensure your MongoDB Atlas instance is running.

## Usage

1. Start the application:
   ```bash
   npm start
   ```

2. Open your browser and navigate to `http://localhost:3000`.

## Project Structure

```
├── controllers
│   ├── authController.js
│   └── blogController.js
├── models
│   ├── User.js
│   └── Blog.js
├── routes
│   ├── authRoutes.js
│   └── blogRoutes.js
├── views
│   ├── layouts
│   │   └── main.hbs
│   ├── login.hbs
│   ├── register.hbs
│   └── dashboard.hbs
├── public
│   ├── css
│   │   └── styles.css
├── app.js
├── server.js
└── package.json
```

## Key Packages

- `express`: Web framework for Node.js.
- `mongoose`: ODM for MongoDB.
- `bcrypt`: Password hashing.
- `jsonwebtoken`: JWT for authentication.
- `express-session`: Session management.
- `connect-mongo`: MongoDB session store.
- `dotenv`: Environment variable management.
- `hbs`: Handlebars template engine.

## API Endpoints

### Authentication

- **POST** `/auth/register`: Register a new user.
- **POST** `/auth/login`: Login an existing user.
- **POST** `/auth/logout`: Logout the current user.

### Blog Posts

- **GET** `/blogs`: Fetch all blogs.
- **POST** `/blogs`: Create a new blog post.
- **GET** `/blogs/:id`: Fetch a single blog post by ID.
- **PUT** `/blogs/:id`: Update a blog post by ID.
- **DELETE** `/blogs/:id`: Delete a blog post by ID.

## Security Features

- Passwords are hashed using bcrypt.
- JWT is used for stateless authentication.
- Sessions are securely stored in MongoDB using connect-mongo.

## License

This project is licensed under the MIT License.
