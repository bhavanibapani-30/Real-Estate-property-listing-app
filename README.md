🏡 Real Estate Property Listing Application

A full-stack Real Estate Property Listing Application built using FastAPI, React, PostgreSQL, Docker, and JWT Authentication.

The application allows users to browse, search, and manage real estate properties. It supports secure authentication, role-based access control, property management, favorites, reviews, and an intuitive React frontend.

Tech Stack Used
Backend
Python
FastAPI
PostgreSQL
SQLAlchemy Async
AsyncPG
Pydantic
Uvicorn
Alembic
JWT Authentication
Frontend
React
Vite
Axios
CSS
Database
PostgreSQL
Tools
Docker
Docker Compose
pgAdmin
Postman
Git & GitHub
VS Code
Features
User Authentication

The authentication module supports:

User Registration
User Login
JWT Access Token
Refresh Token
Secure Password Hashing
Role-Based Authorization

Supported roles:

Admin
Seller
Buyer
Property Management

Users can:

Create Property Listings
View All Properties
View Property Details
Update Property Listings
Delete Property Listings

Each property contains:

Title
Description
Property Type
Purpose (Sale/Rent)
Price
Area
Bedrooms
Bathrooms
Furnishing Status
Parking Availability
Property Images
Amenities
Address
City
State
Country
ZIP Code
Agent Details

Property IDs are generated using UUID.

Property Search & Filtering

Users can search properties based on:

Location
Property Type
Price Range
Bedrooms
Bathrooms
Furnishing Status
Favorites

Registered users can:

Add Property to Favorites
Remove Property from Favorites
View Favorite Properties
Reviews & Ratings

Users can:

Add Reviews
Update Reviews
Delete Reviews
View Property Reviews
Amenities

The system supports management of amenities such as:

Air Conditioning
Parking
Garden
Swimming Pool
Security
Internet
Gym
Location Management

Supports management of:

Countries
States
Cities
Notifications

The application provides notification support for important user activities.

Frontend

The React frontend provides:

Responsive User Interface
Login & Registration Pages
Property Listing Page
Property Details Page
Favorites Page
Dashboard
Property Management Forms
Search & Filter Functionality
Project Structure
Real-Estate-Property-Listing-App/

├── app/
├── frontend/
├── docker/
├── alembic/
├── tests/
├── requirements.txt
├── run.py
├── README.md
└── .gitignore
Project Setup
1. Clone Repository
git clone https://github.com/bhavanibapani-30/Real-Estate-property-listing-app.git

Move into the project folder:

cd Real-Estate-property-listing-app
2. Create Virtual Environment
python -m venv .venv

Activate virtual environment.

Windows:

.venv\Scripts\activate

Linux/Mac:

source .venv/bin/activate
3. Install Backend Dependencies
pip install -r requirements.txt
4. Create Environment File

Create a .env file in the project root.

Example variables:

DATABASE_URL=
JWT_SECRET_KEY=
ACCESS_TOKEN_EXPIRE_MINUTES=
REFRESH_TOKEN_EXPIRE_DAYS=

Do not push the .env file to GitHub.

PostgreSQL Docker Setup

PostgreSQL runs using Docker Compose.

Start Docker containers:

cd docker
docker compose start

Verify containers:

docker ps
Run the Backend

Return to the project root:

cd ..

Run FastAPI:

python run.py

Backend runs at:

http://localhost:8000

Swagger Documentation:

http://localhost:8000/docs
Run the Frontend

Open another terminal.

Navigate to the frontend folder:

cd frontend

Install packages (first time only):

npm install

Run React application:

npm run dev

Frontend runs at:

http://localhost:3000
Project Startup Order
Step 1

Start PostgreSQL

cd docker
docker compose start
docker ps
Step 2

Run Backend

cd ..
python run.py
Step 3

Open another terminal.

Step 4

Run Frontend

cd frontend
npm install
npm run dev
API Documentation

Swagger UI

http://localhost:8000/docs

ReDoc

http://localhost:8000/redoc
API Modules

The backend provides REST APIs for:

Authentication
Users
Properties
Amenities
Favorites
Reviews
Notifications
Locations
Admin

All APIs can be tested using:

Swagger UI
Postman
pgAdmin Connection

Use pgAdmin to manage PostgreSQL.

Example connection:

Host:

localhost

Port:

5432

Database:

(Your database name)

Username:

(Your PostgreSQL username)

Password:

(Your PostgreSQL password)
Useful Commands

Start Docker

docker compose start

View Running Containers

docker ps

Stop Containers

docker compose stop

Reset Database

docker compose down -v

Run Backend

python run.py

Run Frontend

cd frontend
npm run dev

Save Python Packages

pip freeze > requirements.txt
Git Ignore

The project ignores:

.env
.venv
__pycache__
node_modules
Python cache files
IDE settings

Never commit environment variables or secrets to GitHub.

Future Improvements
Property Recommendation System
Google Maps Integration
Email Notifications
Payment Integration
Property Analytics Dashboard
Advanced Search Filters
Image Optimization
Deployment to Cloud
Summary

This project demonstrates a modern full-stack real estate application using:

FastAPI
React
PostgreSQL
Docker
Async SQLAlchemy
JWT Authentication
REST APIs
CRUD Operations
Role-Based Access Control

It serves as a foundation for building scalable real estate management systems.