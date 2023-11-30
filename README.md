[![Tests](https://github.com/anikethbabu/recipe-app-api/actions/workflows/checks.yml/badge.svg)](https://github.com/anikethbabu/recipe-app-api/actions/workflows/checks.yml)

# recipe-app-api
Welcome to the Recipe Management API project! This project leverages the power of Docker, Django, Django Rest Framework (DRF), Postgres, Nginx, Pillow, and DRF-Spectacular to create a robust REST API. The API is designed to facilitate the creation and management of recipes, allowing users to organize their culinary creations with tags, descriptions, preparation time, pictures, and more.

## Prerequisites
This project requires docker and docker-compose to run
Before running the application, ensure that the following prerequisites are met:
- [Docker](https://www.docker.com/)
- [Docker Compose](https://docs.docker.com/compose/)

## How to run the project
1. Clone the repository:
```
git clone https://github.com/anikethbabu/recipe-app-api
```
2. Navigate to the project directory:
```
cd recipe-app-api
```

3. Run the folowing command to start the application using Docker Compose:
```
docker-compose -f docker-compose-deploy.yml up
```
This command will pull the necessary Docker images, build the application, and start the containers

4. Once the application is running, access the Swagger API documentation at http://127.0.0.1/api/docs

## Authenticating User
### Step 1: Create a User
1. Scroll down to the User APIs section in the Swagger UI.
2. Locate the POST /user/create/ endpoint.
3. Click on the endpoint to expand it, revealing the input fields.
4. Fill in the required information such as email, password, and name to create a new user.
5. Click the "Execute" button to send the request and create the user.
### Step 2: Obtain Authentication Token
1. Scroll up to find the Token APIs section in the Swagger UI.
2. Locate the POST /user/token/ endpoint.
3. Click on the endpoint to expand it, revealing the input fields.
4. Enter the email and password of the user created in Step 1.
5. Click the "Execute" button to send the request and obtain an authentication token.
### Step 3: Authorize with Token
1. Once you receive the authentication token, copy it.
2. Scroll up to the top of the Swagger UI.
3. Click the "Authorize" button.
4. In the "Value" field, prepend your token with the word 'Token' and a space. For example: Token yourtoken.
5. Click the "Authorize" button to set the authorization token.
### Step 4: Verify Authentication
1. Scroll down to the User APIs section again.
2. Locate the GET /user/me/ endpoint.
3. Click on the endpoint to expand it.
4. Click the "Execute" button to send the request and retrieve the user details.
5. If the request is successful and returns the user information, congratulations! You have successfully logged in, and now you are free to explore and try out all the available APIs.

Now you can explore and interact with other APIs in the Swagger UI with the authorization.