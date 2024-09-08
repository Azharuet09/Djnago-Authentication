## Django User Registration and Login System
This project is a simple Django-based user registration and login system. It provides REST API endpoints for users to create an account and log in.

### Features
User registration with username, email, and password.
User login using username and password.
REST API built using Django REST Framework.
Installation
Follow the steps below to set up the project on your local machine:

### Clone the repository
```python
git clone https://github.com/yourusername/loginproject.git
cd loginproject
```

### Create a virtual environment
```python
python3 -m venv env
source env/bin/activate  # On Windows use `env\Scripts\activate`
```


### Install dependencies
Install all required packages listed in requirements.txt:
```python
pip install -r requirements.txt
```
### Run migrations
Run the following command to apply the migrations and create the necessary database tables:
```python
python manage.py migrate
```
### Run the development server
Start the Django development server:
```python
python manage.py runserver
```
The application will be accessible at 
```python
http://127.0.0.1:8000/
```

## API Endpoints

### User Registration

URL: 
```python
http://127.0.0.1:8000/api/users/register/
```

Method: POST

Request Body (JSON):
```python
{
  "username": "your_username",
  "email": "your_email@example.com",
  "password": "your_password"
}
```

Response (Example):
```python
{
  "message": "User registered successfully"
}
```

This endpoint creates a new user with the provided username, email, and password.

### User Login

URL
```python
http://127.0.0.1:8000/api/users/login/

```
Method: POST

Request Body (JSON):
```python
{
  "username": "your_username",
  "password": "your_password"
}
```
Response (Example for a successful login):
```python
{
  "message": "Login successful"
}
```
Response (Example for an unsuccessful login):
```python
{
  "message": "Invalid credentials"
}
```

This endpoint authenticates the user based on the provided username and password.

