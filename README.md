# Task Management System

This project implements a Task Management System using ReactJS, NodeJS (API gateway and backend), and PostgreSQL.

## Requirements

Before running the application, ensure you have the following software installed:

* **Node.js (version 12 or above):** Used for the backend and API gateway.
* **npm (Node Package Manager):** Used for installing dependencies.
* **PostgreSQL:** Database for storing task data.

## Project Structure

The project is structured as follows:

* **backend/:** Contains the NodeJS ExpressJS REST API.
* **api-gateway/:** Contains the NodeJS ExpressJS API gateway.
* **frontend/:** Contains the ReactJS frontend application.
* **database/:** Contains the SQL script to create the database table.

## Backend (NodeJS - ExpressJS)

The backend provides REST APIs for task management, including creating, updating, and fetching tasks. It uses Sequelize ORM to interact with the PostgreSQL database. Validation is implemented to ensure data integrity, such as unique titles and valid due dates. Error handling provides meaningful error messages.

## Database (PostgreSQL)

The PostgreSQL database stores task information in the `tasks` table. The table includes columns for title, description, due date, status, and priority. Constraints enforce data integrity, and a bonus challenge involves a trigger for automatic status updates.

## API Gateway (NodeJS - ExpressJS)

The API gateway acts as a middleware, logging all requests and performing basic API validation, such as rejecting requests with titles containing "test". It forwards requests to the backend.

## Frontend (ReactJS)

The ReactJS frontend provides a user interface for task management. It allows users to list, filter, create, and update tasks. Local state management is used, and a custom `useTasks.js` hook manages task data. The UI is designed to be responsive and user-friendly.

## Debugging Task

The provided Java function `calculateDaysUntilDue` has a logical error: it calculates the difference in milliseconds, not days. The fix involves converting the millisecond difference to days.

## Installation and Setup

1.  **Clone the repository.**
2.  **Install dependencies:** Navigate to each directory (backend, api-gateway, frontend) and run `npm install`.
3.  **Configure PostgreSQL:** Create a database and update the connection details in the backend configuration.
4.  **Run migrations:** Execute the SQL script in the `database/` directory to create the `tasks` table.
5.  **Start the backend:** Navigate to the `backend/` directory and run `npm start`.
6.  **Start the API gateway:** Navigate to the `api-gateway/` directory and run `npm start`.
7.  **Start the frontend:** Navigate to the `frontend/` directory and run `npm start`.

## Note about the Java debugging task.

The Java debugging task is simply a function that returns the difference between two dates in milliseconds, instead of days. To fix this, the returned value needs to be converted from milliseconds to days.
