# BuildMason

BuildMason is a command-line tool for generating scaffolding projects with different configurations.

It currently supports creating a basic Flask project, a Flask REST API project, and a Flask project with Blueprints.

## Installation

```bash
pip install buildmason
```

## Usage
```bash
buildmason COMMAND [OPTIONS] [ARGS]...
```
### Commands

- basic-flask-project: Generates a basic Flask project.
- rest-api: Generates a Flask REST API project.
- blueprint: Generates a Flask project with Blueprints.

#### Options
--help: Show this message and exit.

## Getting Started

### Basic Flask Project
```bash

buildmason basic-flask-project
```

This command will generate a basic Flask project structure. This is a simple Flask project that creates `/` route and renders an index.html page.
[Project template link](https://github.com/Worm4047/buildmason-basic-flask/tree/main/%7B%7Bcookiecutter.project_name%7D%7D)
#### Project Structure
```
{{cookiecutter.project_name}}/
├── README.md
├── app
│   ├── __init__.py
│   └── templates
│       └── home.html
├── config.py
├── requirements.txt
└── run.py
````

### Flask REST API Project
```bash
buildmason rest-api
```
This command will generate a Flask project with REST API configuration. This is a simple Flask project for a REST API with user data. The project defines a user data model and creates/queries the data. [Project template link](https://github.com/Worm4047/buildmason-flask-rest/tree/main/%7B%7Bcookiecutter.project_name%7D%7D)

#### Project Structure
```
{{cookiecutter.project_name}}/
├── app/
│   ├── __init__.py
│   ├── models/
│   │   ├── __init__.py
│   │   ├── user.py
│   ├── services/
│   │   ├── __init__.py
│   │   ├── user_service.py
│   ├── utils/
│   │   ├── __init__.py
│   │   ├── config.py
│   ├── app.py
├── tests/
│   ├── __init__.py
│   ├── resources/
│   │   ├── __init__.py
│   │   ├── test_user_resource.py
│   ├── services/
│   │   ├── __init__.py
│   │   ├── test_user_service.py
├── venv/ (virtual environment)
├── requirements.txt
```

### Flask Blueprint Project
```bash
buildmason blueprint
```
This command will generate a Flask project with Blueprints. This is a simple Flask project that allows user login into the web application. We make use several components
- Flask-Login library for session management
- built-in Flask utility for hashing passwords
- Add protected pages to the app for logged in users only
- Use Flask-SQLAlchemy to create a User model
- Create sign-up and login forms for the users to create accounts and log in
- Flash error messages back to users when something goes wrong
- Use information from the user’s account to display on the profile page

[Project template link](https://github.com/Worm4047/buildmason-flask-blueprint/tree/master/%7B%7Bcookiecutter.project_name%7D%7D)
#### Project Structure
```
{{cookiecutter.project_name}}/
├── app
│   ├── __init__.py
│   ├── models
│   │   ├── __init__.py
│   │   └── user.py
│   ├── routes
│   │   ├── __init__.py
│   │   ├── auth.py
│   │   └── main.py
│   └── templates
│       ├── base.html
│       ├── index.html
│       ├── login.html
│       ├── profile.html
│       └── signup.html
├── requirements.txt
├── run.py
└── tests
    ├── __init__.py
    ├── models
    │   ├── __init__.py
    │   └── test_models.py
    └── routes
        ├── test_auth.py
        └── test_main.py

```

## Contributing
Feel free to contribute to this project. Open issues or submit pull requests on the GitHub repository.

## License
This project is licensed under the MIT License - see the LICENSE file for details.



