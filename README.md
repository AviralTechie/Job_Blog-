# Mini Project

![Node.js](https://img.shields.io/badge/Node.js-14.x-green)
![Express](https://img.shields.io/badge/Express-4.x-red)
![MongoDB](https://img.shields.io/badge/MongoDB-4.x-orange)
![Project Image](image.png)

## Description

This is a mini project built with Node.js, Express, and MongoDB. It includes authentication using bcrypt and JSON Web Tokens (JWT), session management with express-session and connect-mongo, and more.

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Dependencies](#dependencies)

## Installation 

cd mini-project

npm install

# Start the server

npm start

# Start the server in development mode with nodemon
npm run dev

# Dependencies to be install 
npm install express-session , bcrypt, connect-mongo,cookie-parser, dotenv, ejs, express, express-ejs-layouts, express-session, jsonwebtoken, method-override, mongoose 


1. Clone the repository:
      ```bash
   git clone https://github.com/your-username/mini-project.git
   npm install express-session , bcrypt, connect-mongo,cookie-parser, dotenv, ejs, express, express-ejs-layouts, express-session, jsonwebtoken, method-override, mongoose

### Package.json

```json
{
  "name": "mini-project",
  "version": "1.0.0",
  "main": "index.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1",
    "start": "node app.js",
    "dev": "nodemon app.js"
  },
  "keywords": [],
  "author": "",
  "license": "ISC",
  "dependencies": {
    "bcrypt": "^5.1.1",
    "connect-mongo": "^5.1.0",
    "cookie-parser": "^1.4.6",
    "dotenv": "^16.4.5",
    "ejs": "^3.1.10",
    "express": "^4.19.2",
    "express-ejs-layouts": "^2.5.1",
    "express-session": "^1.18.0",
    "jsonwebtoken": "^9.0.2",
    "method-override": "^3.0.0",
    "mongoose": "^8.4.4"
  },
  "devDependencies": {
    "nodemon": "^3.1.0"
  },
  "description": ""
}


