# Bitasmbl-ProTaskify

A professional web-based task management application built with React, Node.js, Express.js, and PostgreSQL. It features JWT-based user authentication, project-scoped CRUD operations, and priority-driven task views through RESTful APIs.

## Tech Stack
- Express.js
- PostgreSQL
- React
- Node.js

## Requirements
- Implement JWT authentication for secure user login (Hint: Use jsonwebtoken library to sign and verify tokens)
- Design RESTful CRUD APIs for tasks and projects (Hint: Use Express.js routing and controllers)
- Model relational data in PostgreSQL (Hint: Use pg library for queries)
- Implement front-end state management (Hint: Use React hooks and context)

## Installation
1. Clone the repository:
   bash
   git clone https://github.com/yourusername/Bitasmbl-ProTaskify.git
   cd Bitasmbl-ProTaskify
   
2. Install server dependencies:
   bash
   cd server
   npm install
   
3. Install client dependencies:
   bash
   cd ../client
   npm install
   
4. Create a `.env` file in the `server` directory with the following variables:
   
   DATABASE_URL=your_postgresql_connection_string
   JWT_SECRET=your_jwt_secret
   PORT=5000
   
5. Create a `.env` file in the `client` directory if needed:
   
   REACT_APP_API_URL=http://localhost:5000/api
   

## Usage
1. Start the backend server:
   bash
   cd server
   npm run dev
   
2. Start the frontend application:
   bash
   cd client
   npm start
   
3. Open your browser and navigate to `http://localhost:3000` to access the application.
4. Register a new account, create projects, and manage tasks with priority-driven views.

## Implementation Steps
1. Initialize the monorepo with separate `server` and `client` folders.
2. Set up the Express.js server and configure middleware (CORS, body-parser).
3. Connect to PostgreSQL using the `pg` library and manage connection pooling.
4. Implement JWT-based authentication with `jsonwebtoken` (register, login, token verification).
5. Define `Project` and `Task` models and create migrations for relational schema.
6. Build RESTful routes and controllers for project and task CRUD operations.
7. Structure the React app using Create React App and organize components.
8. Configure global state management using React Context and hooks (`useContext`, `useReducer`).
9. Create authentication pages (Login, Register) and protect routes using JWT tokens.
10. Develop project dashboard and task views, integrating priority sorting and filtering.
11. Test API endpoints and UI components to ensure data consistency and error handling.
12. Deploy the server and client applications to your preferred hosting providers.

## API Endpoints
### Authentication
- POST `/api/auth/register` - Register a new user
- POST `/api/auth/login` - Authenticate user and receive JWT token

### Projects
- GET `/api/projects` - List all projects for authenticated user
- POST `/api/projects` - Create a new project
- GET `/api/projects/:projectId` - Get project details
- PUT `/api/projects/:projectId` - Update a project
- DELETE `/api/projects/:projectId` - Delete a project

### Tasks
- GET `/api/projects/:projectId/tasks` - List tasks in a project
- POST `/api/projects/:projectId/tasks` - Create a new task in a project
- GET `/api/projects/:projectId/tasks/:taskId` - Get task details
- PUT `/api/projects/:projectId/tasks/:taskId` - Update a task
- DELETE `/api/projects/:projectId/tasks/:taskId` - Delete a task