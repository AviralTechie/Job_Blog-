# Job-News Posting Website (Khoj)

![Node.js](https://img.shields.io/badge/Node.js-v10.8.1-green)
![Express](https://img.shields.io/badge/Express-v4.19.2-red)
![MongoDB](https://img.shields.io/badge/MongoDB-v8.4.4-orange)


## Description
![Project Image](image.png)
* This is a mini project built with Node.js, Express, and MongoDB. It includes authentication using bcrypt and JSON Web Tokens (JWT), session management with express-session and connect-mongo, and more.

## Table of Contents

- [Installation](#installation)
- [Example Code](#example-code)
- [Dependencies](#dependencies)

## Installation 
```bash
cd mini-project
```

```bash
npm install
```

# Start the server
```bash
npm start
```
# Start the server in development mode with nodemon
```bash
npm run dev
```

# Configure

* <.env file>
* PORT=3000
* DB_URL=mongodb://localhost:27017/your_database_name
* SESSION_SECRET=your_session_secret

1. Clone the repository:
      ```bash
   git clone https://github.com/your-username/mini-project.git

## Dependencies

```bash
npm install express-session , bcrypt, connect-mongo,cookie-parser, dotenv, ejs, express, express-ejs-layouts, express-session, jsonwebtoken, method-override, mongoose
```

## Example Code
* app.js (file)
  
```javascript
require('dotenv').config();
const express = require('express');
const expressLayout = require('express-ejs-layouts');
const methodOverride = require('method-override');
const cookieParser = require('cookie-parser');
const MongoStore = require('connect-mongo'); 
const connectDB = require('./server/config/db');
const session = require('express-session');


/* active Route */
const {isActiveRoute} = require('./server/helpers/routeHelpers');

const app = express(); 
const PORT = 5000 || process.env.PORT;

//Connect to DB
connectDB();
 
app.use(express.urlencoded({extended:true}));
app.use(express.json());
app.use(cookieParser());
app.use(methodOverride('_method'));

app.use(session({
    secret : 'keyboard cat',
    resave:false,
    saveUninitialized:true,
    store:MongoStore.create({
        mongoUrl:process.env.MONGODB_URL
    })
}));
//Main Folder
app.use(express.static('public'));

//Template Engine
app.use(expressLayout);
app.set('layout','./layouts/main');
app.set('view engine','ejs');

app.locals.isActiveRoute = isActiveRoute;

app.use('/',require('./server/routes/main'));
app.use('/',require('./server/routes/admin'));

app.listen(PORT, ()=> {
    console.log(`App Listen on port ${PORT}`); 
});

```

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
```
## 

Feel free to customize and expand the sections as needed to fit your project specifics. This structure ensures that all necessary information and code are included in a clear and organized manner.


