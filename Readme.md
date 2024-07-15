# Django REST Framework Movie Project

This project is a basic learning application built using Django REST Framework. It allows users to manage and retrieve information about movies, including filtering by genre (action and comedy). 

## Features

- CRUD operations for movie data.
- Filtering movies by genre (action and comedy).
- Image upload for movie posters.

## Models

The project contains a single model `Moviedata` with the following fields:
- `name`: CharField, maximum length 200.
- `duration`: FloatField.
- `rating`: FloatField.
- `typ`: CharField, maximum length 200, default value 'action'.
- `image`: ImageField, with an upload path 'Images/' and a default image 'Images/None/Noimg.jpg'.

## Endpoints

The application exposes the following endpoints:

- `/movies/`: Provides access to all movie data.
- `/action/`: Filters and provides access to action movies.
- `/comedy/`: Filters and provides access to comedy movies.

## Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/AtharvaDeokar21/DRF.git
   cd django-movie-project
   ```
2. **Create a virtual env:**
    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows use `venv\Scripts\activate`
    ```
3. **Install the dependencies:**
    ```bash
    pip install -r requirements.txt
    ```
4. **Apply migrations:**
    ```bash
    python manage.py migrate
    ```
5. **Run the development server:**
    ```bash
    python manage.py runserver
    ```
## Usage

### Adding Movie Data
You can add movie data using the Django admin interface or through the API endpoints.

### Django Admin Interface:
Navigate to http://127.0.0.1:8000/admin/
Log in with your superuser credentials.
Add movies through the Moviedata model.

### API Endpoints:
Viewing Movies
All Movies:
Navigate to http://127.0.0.1:8000/movies/
Action Movies:
Navigate to http://127.0.0.1:8000/action/
Comedy Movies:
Navigate to http://127.0.0.1:8000/comedy/

## Dependencies
- Django
- Django REST Framework
- Pillow (for image handling)