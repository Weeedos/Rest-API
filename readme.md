# REST API Documentation

## Overview

This documentation provides details about the REST API for a simple authentication and book management system. The API includes endpoints for user authentication (login, register, logout) and book management (retrieve, add, update, delete).

## Authentication Endpoints

### Login

**Endpoint:**

POST /api/auth/login

**Request Body:**

{
  "username": "example",
  "password": "password123"
}

**Response:**

200 OK: Successful login (Body: User ID)

400 Bad Request: Invalid username or password (Body: Error message)

### Register

**Endpoint:**

POST /api/auth/register

**Request Body:**

{
  "username": "newuser",
  "email": "newuser@example.com",
  "password": "newpassword123"
}

**Response:**

200 OK: Registration successful (Body: Result)
400 Bad Request: Missing parameters or registration failure (Body: Error message)

### Logout

**Endpoint:**

DELETE /api/auth/logout

**Response:**

200 OK: Logout successful
400 Bad Request: Unable to logout (Body: Error message)

## Book Management Endpoints

### Retrieve Books

**Endpoint:**

GET /api/book

**Response:**

200 OK: Successfully retrieved books (Body: Array of book objects)
400 Bad Request: Not authenticated (Body: Error message)

### Add Book

**Endpoint:**

POST /api/book

**Request Body:**

{
  "name": "New Book",
  "author": "Author Name",
  "createdDate": "2023-12-01"
}

**Response:**

200 OK: Book added successfully (Body: Result)
400 Bad Request: Missing values or something went wrong (Body: Error message)

### Update Book

**Endpoint:**

PUT /api/book

**Request Body:**

{
  "id": "bookId",
  "name": "Updated Book",
  "author": "Updated Author",
  "createdDate": "2023-12-02"
}

**Response:**

200 OK: Book updated successfully (Body: Result)
400 Bad Request: Missing values or something went wrong (Body: Error message)

### Delete Book

**Endpoint:**

DELETE /api/book

**Request Body:**

{
  "id": "bookId"
}

**Response:**

200 OK: Book deleted successfully (Body: Result)
400 Bad Request: Book ID is missing or something went wrong (Body: Error message)


# How to Run Locally

**1. Install Node.js and npm.**

**2. Clone the repository and navigate to the project folder.**

### Install dependencies:
```
npm install
```
**3. Set up your MySQL database and update the database configuration in the database.js file.**

**4. Start the server:**
```
npm start
```
**The server will be running on http://localhost:5000.**
