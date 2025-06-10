[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-2e0aaae1b6195c2367325f4f02e2d04e9abb55f0b24a779b69b11b9e10269abc.svg)](https://classroom.github.com/online_ide?assignment_repo_id=19742959&assignment_repo_type=AssignmentRepo)
# Express.js RESTful API Assignment

This assignment focuses on building a RESTful API using Express.js, implementing proper routing, middleware, and error handling.

## Assignment Overview

You will:
1. Set up an Express.js server
2. Create RESTful API routes for a product resource
3. Implement custom middleware for logging, authentication, and validation
4. Add comprehensive error handling
5. Develop advanced features like filtering, pagination, and search

## Getting Started

1. Accept the GitHub Classroom assignment invitation
2. Clone your personal repository that was created by GitHub Classroom
3. Install dependencies:
   ```
   npm install
   ```
4. Run the server:
   ```
   npm start
   ```

## Files Included

- `Week2-Assignment.md`: Detailed assignment instructions
- `server.js`: Starter Express.js server file
- `.env.example`: Example environment variables file

## Requirements

- Node.js (v18 or higher)
- npm or yarn
- Postman, Insomnia, or curl for API testing

## API Endpoints

The API will have the following endpoints:

- `GET /api/products`: Get all products
- `GET /api/products/:id`: Get a specific product
- `POST /api/products`: Create a new product
- `PUT /api/products/:id`: Update a product
- `DELETE /api/products/:id`: Delete a product

# Product API

A simple Express.js REST API for managing products.

## Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/) (v14 or higher recommended)
- [npm](https://www.npmjs.com/)

### Installation

1. Clone the repository:
   ```sh
   git clone https://github.com/PLP-MERN-Stack-Development/week-2-express-js-assignment-x88-code.git
   cd week-2-express-js-assignment-x88-code
   ```

2. Install dependencies:
   ```sh
   npm install
   ```

3. (Optional) Copy the example environment file and edit as needed:
   ```sh
   copy .env.example .env
   ```

### Running the Server

```sh
npm start
```

The server will start on [http://localhost:3000](http://localhost:3000) by default.

---

## API Documentation

### Root

- **GET /**  
  Returns a welcome message.

---

### Products

#### Get all products

- **GET /api/products**
- **Response:**
  ```json
  [
    {
      "id": "1",
      "name": "Laptop",
      "description": "High-performance laptop with 16GB RAM",
      "price": 1200,
      "category": "electronics",
      "inStock": true
    },
    ...
  ]
  ```

#### Get a product by ID

- **GET /api/products/:id**
- **Response (200):**
  ```json
  {
    "id": "1",
    "name": "Laptop",
    "description": "High-performance laptop with 16GB RAM",
    "price": 1200,
    "category": "electronics",
    "inStock": true
  }
  ```
- **Response (404):**
  ```json
  { "message": "Product not found" }
  ```

#### Create a new product

- **POST /api/products**
- **Request Body:**
  ```json
  {
    "name": "Tablet",
    "description": "10-inch display tablet",
    "price": 300,
    "category": "electronics",
    "inStock": true
  }
  ```
- **Response (201):**
  ```json
  {
    "id": "generated-uuid",
    "name": "Tablet",
    "description": "10-inch display tablet",
    "price": 300,
    "category": "electronics",
    "inStock": true
  }
  ```
- **Response (400):**
  ```json
  { "message": "Name and price are required" }
  ```

#### Update a product

- **PUT /api/products/:id**
- **Request Body:** (any fields to update)
  ```json
  {
    "price": 350,
    "inStock": false
  }
  ```
- **Response (200):**
  ```json
  {
    "id": "1",
    "name": "Laptop",
    "description": "High-performance laptop with 16GB RAM",
    "price": 350,
    "category": "electronics",
    "inStock": false
  }
  ```
- **Response (404):**
  ```json
  { "message": "Product not found" }
  ```

#### Delete a product

- **DELETE /api/products/:id**
- **Response (200):**
  ```json
  {
    "id": "1",
    "name": "Laptop",
    "description": "High-performance laptop with 16GB RAM",
    "price": 1200,
    "category": "electronics",
    "inStock": true
  }
  ```
- **Response (404):**
  ```json
  { "message": "Product not found" }
  ```

---

## Environment Variables

See `.env.example` for required variables.

---

## Example .env File

See below for the `.env.example` file.