# MERN Todo App

A simple MERN (MongoDB, Express, React, Node.js) stack application with a todo list functionality.

## Features

- Add, toggle, and delete todos
- Backend with Express and MongoDB
- Frontend with React and Axios
- CORS enabled for cross-origin requests

## Prerequisites

- Node.js
- MongoDB (local or cloud instance)
- npm or yarn

## Installation

1. Clone the repository
2. Install backend dependencies:
   ```
   cd backend
   npm install
   ```
3. Install frontend dependencies:
   ```
   cd ../frontend
   npm install
   ```

## Configuration

1. Backend: In `backend/.env`, update the `MONGO_URI` if needed (default: mongodb://localhost:27017/mernapp) and `PORT` (default: 5000)
2. Frontend: In `frontend/.env`, update `REACT_APP_API_URL` to match your backend URL (default: http://localhost:5000)

## Running the App

1. Start MongoDB
2. Start the backend:
   ```
   cd backend
   npm run dev
   ```
3. Start the frontend:
   ```
   cd frontend
   npm start
   ```
4. Open http://localhost:3000 in your browser

## API Endpoints

- GET /api/todos - Get all todos
- POST /api/todos - Create a new todo
- PUT /api/todos/:id - Update a todo
- DELETE /api/todos/:id - Delete a todo