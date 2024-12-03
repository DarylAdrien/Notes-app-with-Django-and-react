# Notes-app implemented with Django Framework and React(Vite) Framework

A full-stack web application featuring a **React frontend** built using **Vite** and a **Django backend**. The application uses Django REST Framework (DRF) for building RESTful APIs and **JWT (JSON Web Tokens)** for secure user authentication.

---

## Features

- **Frontend:**
  - React with **Vite** for fast builds and optimized performance.
  - Dynamic routing and responsive UI design.
    
- **Backend:**
  - Django REST Framework (DRF) for API development.
  - Secure user authentication using **JWT tokens**.
 
- **Authentication:**
  - Secure user authentication using JWT tokens.
    
- **Database Integration:**
  - Compatible with SQLite (default), PostgreSQL, or MySQL.
    
- **Cross-Origin Support:**
  - CORS enabled for seamless communication between frontend and backend.

---

## Prerequisites

Before you begin, ensure you have the following installed:

- Python (3.8 or newer)
- Node.js (14.x or newer) and npm
- Django (4.x or newer)
- A package manager: `pip` and `virtualenv`
- Git

---

## Installation

### 1. Clone the Repository

      git clone https://github.com/DarylAdrien/Notes-app-with-Django-and-react.git

      cd Notes-app-with-Django-and-react


### 2. Backend Setup (Django + DRF + JWT)

-> Navigate to the backend directory:

      cd backend

-> Create a virtual environment and activate it:

      python -m venv venv
      source venv/bin/activate       # On Windows: venv\Scripts\activate

-> Install dependencies:

      pip install -r requirements.txt

-> Apply database migrations:

      python manage.py migrate

-> Run the development server:

      python manage.py runserver


The backend will be available at http://127.0.0.1:8000.



### 3. Frontend Setup (React with Vite)

-> Navigate to the frontend directory:

      cd frontend
      
-> Install dependencies:

      npm install

-> Start the development server:

      npm run dev

The frontend will be available at http://localhost:5173.



## Authentication
This application uses JWT tokens for secure authentication. The process involves:

Users send credentials (username/password) to the /api/token/ endpoint.

A pair of tokens (Access and Refresh) is returned.

The Access Token is used for authenticated API requests.

The Refresh Token is used to obtain a new Access Token when the current one expires.


### API endpoints for authentication:

Refresh Token: POST /api/token/refresh/

Obtain Token: POST /api/token/


## REST API
The backend is built using Django REST Framework (DRF) and follows RESTful principles. Key endpoints:


### Public Endpoints

/api/user/register/ - Access public data.

### Authenticated Endpoints

/api/notes/ - Access secured data (requires JWT token).

### User Management

/api/user/register/ - User registration.

/api/user/info/ - View/update user profile (requires authentication).

## Contributing

Fork the project.

Create your feature branch: git checkout -b feature-name

Commit your changes: git commit -m 'Add some feature'

Push to the branch: git push origin feature-name

Open a pull request.

## License

This project is licensed under the MIT License. See the LICENSE file for details.
