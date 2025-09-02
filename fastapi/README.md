# Workout Tracker Backend

A FastAPI-based REST API for managing workout routines and exercises with user authentication.

## Getting Started

1. Install dependencies:
```bash
pip install -r requirements.txt
```

2. Set up environment variables:
```bash
cp .env.example .env
# Edit .env with your configuration
```

3. Run the development server:
```bash
uvicorn api.main:app --reload
```

The API will be available at `http://localhost:8000`

## Features

- JWT-based user authentication
- User registration and login
- CRUD operations for workouts
- CRUD operations for routines
- Many-to-many relationship between workouts and routines
- SQLite database with SQLAlchemy ORM

## API Endpoints

### Authentication
- `POST /auth/` - Register new user
- `POST /auth/token` - Login and get access token

### Workouts
- `GET /workouts/workouts` - Get all workouts
- `POST /workouts/` - Create new workout
- `DELETE /workouts/` - Delete workout

### Routines
- `GET /routines/` - Get all routines
- `POST /routines/` - Create new routine
- `DELETE /routines/` - Delete routine

## Tech Stack

- FastAPI
- SQLAlchemy ORM
- SQLite Database
- JWT Authentication
- Bcrypt for password hashing
- Pydantic for data validation
- Uvicorn ASGI server
