# Bookstore API

A REST API for managing books and authors, developed as an educational project during my studies with Alura. The project was later reorganized to practice a clearer separation between controllers, services, models, and application-level error handling.

## About the project

The API provides CRUD operations for books and authors, along with filtering and pagination. Its main purpose is to demonstrate foundational backend concepts with Node.js, Express, MongoDB, and Mongoose.

This repository is a learning project rather than a production service.

## Features

- Create, list, update, and delete books
- Create, list, update, and delete authors
- Search books by title, publisher, or author
- Paginated book listings
- Request data validation
- Centralized error handling
- MVC-style organization with a service layer

## Tech stack

- Node.js
- Express 5
- MongoDB
- Mongoose
- dotenv
- Nodemon

## Getting started

### Prerequisites

- Node.js
- npm
- A local MongoDB instance or MongoDB Atlas connection

### Installation

```bash
git clone https://github.com/carlosdevj/bookstore-api.git
cd bookstore-api
npm install
```

### Environment variables

Create a `.env` file in the project root:

```env
PORT=3000
DB_CONNECTION_STRING=your_mongodb_connection_string
```

### Running the application

Start the development server:

```bash
npm run dev
```

Start the application without watch mode:

```bash
npm start
```

The API is available at `http://localhost:3000` by default.

## API endpoints

### Books

| Method | Endpoint | Description |
| --- | --- | --- |
| `GET` | `/livros` | List books with pagination |
| `GET` | `/livros/busca` | Search books using query filters |
| `GET` | `/livros/:id` | Retrieve a book by ID |
| `POST` | `/livros` | Create a book |
| `PUT` | `/livros/:id` | Update a book |
| `DELETE` | `/livros/:id` | Delete a book |

Example search:

```http
GET /livros/busca?titulo=Clean%20Code
```

### Authors

| Method | Endpoint | Description |
| --- | --- | --- |
| `GET` | `/autores` | List authors |
| `GET` | `/autores/:id` | Retrieve an author by ID |
| `POST` | `/autores` | Create an author |
| `PUT` | `/autores/:id` | Update an author |
| `DELETE` | `/autores/:id` | Delete an author |

## Project status

This is a completed educational project and is not currently maintained as a production API. Automated tests have not yet been implemented.

## Credits

Developed by [Carlos Gabriel Leal](https://github.com/carlosdevj) as part of his backend studies through Alura.