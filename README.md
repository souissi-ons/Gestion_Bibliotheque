# Library API project

A simple Library Management REST API built with Node.js and Express.
This project demonstrates DevOps best practices: Containerization, CI/CD, Observability, and Security.

## Prerequisites

- Node.js (v18+)
- Docker
- Git

## 🚀 Getting Started Locally

1. **Install dependencies:**
   ```bash
   npm install
   ```

2. **Start the server:**
   ```bash
   npm start
   ```

3. **Check the API:**
   The server runs on `http://localhost:3000`.
   - Health Check: `http://localhost:3000/health`

## 🐳 Docker Usage

Build and run the application using Docker.

1. **Build the image:**
   ```bash
   docker build -t library-api .
   ```

2. **Run the container:**
   ```bash
   docker run -p 3000:3000 library-api
   ```

## 📖 API Documentation

| Method | Endpoint      | Description          | Body Example                                    |
| :----- | :------------ | :------------------- | :---------------------------------------------- |
| GET    | `/books`      | List all books       | N/A                                             |
| GET    | `/books/:id`  | Get a book by ID     | N/A                                             |
| POST   | `/books`      | Add a new book       | `{ "title": "DevOps", "author": "Gene Kim" }`   |
| GET    | `/health`     | Health check (UP)    | N/A                                             |
| GET    | `/metrics`    | Prometheus metrics   | N/A                                             |

## 🔍 Observability

- **Logs**: The application outputs structured JSON logs to `stdout`.
- **Metrics**: Prometheus metrics are available at `/metrics`.
