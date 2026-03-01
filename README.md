# Workshop 03 -- Building a Web Server with Express.js

## Overview

This project demonstrates how to build a web server using
**Express.js**, including routing, middleware, static file serving,
structured API endpoints, and error handling.

The goal of this workshop was to understand how Express simplifies
server development compared to Node.js's built-in HTTP module.

------------------------------------------------------------------------

## Learning Objectives

This project demonstrates:

-   Creating a web server using Express.js\
-   Implementing routing using Express Router\
-   Serving static files using Express middleware\
-   Handling 404 (Not Found) and 500 (Server Error) responses\
-   Understanding middleware execution order\
-   Creating JSON API endpoints

------------------------------------------------------------------------

## Project Structure

    WS03-Express/
    ├── server.js
    ├── package.json
    ├── package-lock.json
    ├── public/
    │   ├── index.html
    │   ├── about.html
    │   ├── contact.html
    │   ├── 404.html
    │   ├── 500.html
    │   └── styles/
    │       └── style.css
    ├── .gitignore
    └── README.md

------------------------------------------------------------------------

## Implemented Features

### Express App Setup

-   Express application instance created
-   Server configured to run on `process.env.PORT || 3000`

### Static File Middleware

-   `express.static()` serves files from the `public` directory

### Route Handlers

-   `GET /` → Home page\
-   `GET /about` → About page\
-   `GET /contact` → Contact page

### API Endpoints (Express Router)

-   `GET /api/time` → Returns current date and timestamp\
-   `GET /api/info` → Returns server metadata

### Error Handling Middleware

-   Custom 404 page for unmatched routes\
-   Custom 500 page for server errors

### Request Logging Middleware

-   Logs incoming requests with timestamp and method

------------------------------------------------------------------------

## Running the Server (Local Development)

Install dependencies:

    npm install

Start the server:

    npm start

For development with auto-reload:

    npm run dev

Open in browser:

-   http://localhost:3000\
-   http://localhost:3000/about\
-   http://localhost:3000/contact\
-   http://localhost:3000/api/time\
-   http://localhost:3000/api/info

Stop the server with:

    Ctrl + C

------------------------------------------------------------------------

## Live Deployment

The application is deployed on Render:

https://ws03-express.onrender.com/

------------------------------------------------------------------------

## Technologies Used

-   Node.js\
-   Express.js

------------------------------------------------------------------------

## Conclusion

This workshop demonstrates how Express improves structure, readability,
and scalability compared to manual HTTP server implementation.

The project was successfully structured with modular routing, middleware
layering, static file handling, and deployment-ready configuration.
