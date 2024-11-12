
# Velmurugan-654-SB-Foods---Food-Ordering-App SB-Foods---Food-Ordering-App
Food Delivery Application Project Documentation
Project Overview
This food delivery application enables users to browse food items, add them to a cart, and place orders. The app has three components: a frontend (user interface), backend (API and data handling), and an admin panel (for managing menu items and orders).

Key Functionalities
User Interface: Display food items, add items to cart, view cart, and place orders.
Admin Panel: Add, update, and delete food items; manage orders.
Backend: Handles API requests, user authentication, and database interactions.
Project Structure
frontend/
src/
components/
pages/
styles/
backend/
controllers/
models/
routes/
admin/
src/
components/
pages/
styles/
Dependencies and Installation
Frontend (React)
The frontend is built with React and styled with CSS modules.

Installation: cd frontend npm install npm start

Key Libraries:

axios: For API requests.
react-router-dom: For navigation.
context-api: Manages state for cart items.
Example Imports: import React from 'react'; import axios from 'axios'; import { BrowserRouter as Router, Route, Switch } from 'react-router-dom';

Backend (Node.js, Express, MongoDB)
The backend API is created with Node.js and Express, using MongoDB as the database.

Installation: cd backend npm install npm run dev

Key Libraries:

express: API framework.
mongoose: For MongoDB interactions.
bcrypt: For password hashing.
jsonwebtoken: For authentication.
Example Imports: const express = require('express'); const mongoose = require('mongoose'); const jwt = require('jsonwebtoken');

Admin Panel (React)
The admin panel is also a React application for managing menu items and orders.

Installation: cd admin npm install npm start

Key Libraries:

axios: To interact with backend APIs.
react-table: For table management and displaying data.
redux: For state management.
Example Imports: import React from 'react'; import { useDispatch, useSelector } from 'react-redux'; import axios from 'axios';

Database
The application uses MongoDB to store user, food item, and order data. You’ll need a MongoDB connection URI, typically stored in a .env file.

MONGO_URI=mongodb+srv://:@cluster.mongodb.net/food-delivery JWT_SECRET=your_secret_key

Project Setup
Environment Setup:

Ensure MongoDB, Node.js, and React are installed.
Set up .env files for the backend.
Running the Project:

Start the backend server: cd backend npm run dev

Run the frontend and admin panel concurrently in separate terminals.

API Endpoints (Backend)
User Authentication

POST /api/users/register: Register new user
POST /api/users/login: Login user
Food Items

GET /api/foods: Fetch all food items
POST /api/foods: Add a new food item (admin only)
Orders

POST /api/orders: Place a new order
GET /api/orders: Fetch user orders 
