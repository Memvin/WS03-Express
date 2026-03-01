# Workshop 03 -- Building a Web Server with Express.js

## Overview

This project demonstrates how to build a web server using the
**Express.js framework**, including routing, middleware, static file
serving, and structured API endpoints.

The goal of this workshop was to understand how Express simplifies web
server development compared to Node.js's built-in HTTP module.

------------------------------------------------------------------------

## Learning Objectives

By completing this workshop, the following concepts were implemented:

-   Creating a web server using Express.js
-   Implementing routing using Express Router
-   Serving static files using Express middleware
-   Handling 404 (Not Found) and 500 (Server Error) responses
-   Understanding Express middleware order
-   Creating JSON API endpoints

------------------------------------------------------------------------

## Project Description

This Express.js server:

-   Serves a homepage, about page, and contact page
-   Loads CSS stylesheets using Express static middleware
-   Displays custom 404 and 500 error pages
-   Provides JSON API endpoints
-   Uses Express Router for organized API routing

------------------------------------------------------------------------

## Project Structure

    WS03-Express/
    ├── starter/
    │   ├── server.js
    │   ├── package.json
    │   ├── package-lock.json
    │   ├── public/
    │   │   ├── index.html
    │   │   ├── about.html
    │   │   ├── contact.html
    │   │   ├── 404.html
    │   │   ├── 500.html
    │   │   └── styles/
    │   │       └── style.css
    │
    ├── .gitignore
    ├── README.md
    └── requirements.md

------------------------------------------------------------------------

## Implemented Features

### Express App Setup

-   Created Express application instance
-   Configured server to run on port 3000

### Static File Middleware

-   Configured `express.static()` to serve files from the `public`
    directory

### Route Handlers

-   `GET /` → Home page
-   `GET /about` → About page
-   `GET /contact` → Contact page

### API Endpoints (Express Router)

-   `GET /api/time` → Returns current date and timestamp
-   `GET /api/info` → Returns server metadata

### Error Handling Middleware

-   Custom 404 page for unmatched routes
-   Custom 500 page for server errors

### Request Logging Middleware

-   Logs all incoming requests with timestamp and method

------------------------------------------------------------------------

## Running the Server

Navigate to the `starter` directory:

    cd starter

Install dependencies:

    npm install

Start the server:

    node server.js

Open in browser:

-   http://localhost:3000
-   http://localhost:3000/about
-   http://localhost:3000/contact
-   http://localhost:3000/api/time
-   http://localhost:3000/api/info

Stop the server with:

    Ctrl + C

------------------------------------------------------------------------

## Key Concepts Demonstrated

-   Express application creation
-   Middleware order importance
-   Static file serving
-   Route handling with `app.get()`
-   JSON responses using `res.json()`
-   Modular API routing using `express.Router()`
-   Custom error handling middleware

------------------------------------------------------------------------

## Technologies Used

-   Node.js
-   Express.js

------------------------------------------------------------------------

## Conclusion

This workshop demonstrates how Express improves structure, readability,
and scalability compared to manual HTTP server implementation.

The project was successfully migrated from a Node.js HTTP server to a
structured Express application with modular routing and proper
middleware handling.
