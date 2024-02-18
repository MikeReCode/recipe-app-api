# Recipe API Project

## Introduction

Welcome to the Recipe API project! This API allows you to manage recipes, ingredients, tags, and user information. You can interact with the API through various endpoints to perform actions such as retrieving recipes, updating ingredients, managing tags, and more.

**Technical Stack:** Developed with Python and Django Rest Framework (DRF), the backend utilizes a PostgreSQL database for data integrity. Docker containers separate the application, database, and Nginx server, providing scalability and efficient deployment.

## Local Deployment with Docker

To deploy the Recipe API locally using Docker, follow these steps:

1. **Clone Repository**: Clone the Recipe API repository from GitHub to your local machine.

2. **Navigate to Project Directory**: Open a terminal and navigate to the root directory of the cloned repository.

3. **Build Docker Containers**: Run the following command to build the Docker containers: `docker-compose up --build`


## API Documentation

The detailed documentation for the API can be found at `GET /api/docs` . This Swagger documentation provides comprehensive information about the available endpoints, request methods, request parameters, and response structures.

## Creating a User

To create a user for testing purposes, use the following endpoint:

- **POST** `/api/user/create/`

Provide the required information such as email and password in the request body to register a new user.


## Generating Authentication Token

1. **Login:** Navigate to the Swagger documentation`GET /api/docs` and locate the `POST /api/user/token/` endpoint under the "User" section.

2. **Try it out:** Click on the "Try it out" button for the `POST /api/user/token/` endpoint.

3. **Enter Credentials:** In the "Request body" section, enter the user credentials created previously.

4. **Execute:** Click the "Execute" button to send the request.

5. **Token Response:** In the response section, you will receive a JSON response containing the access token. It should look like this:
   ```json
   {
     "token": "410fde59351b5bf31ced70b4a6de0d74a918d9"
   }

6. **Copy Token:** Copy the generated access token.

7. **Authenticate Swagger Documentation:** In the Swagger documentation, locate the "Authorize" button in the top right corner.

8. **Set TokenAuth (apiKey):** Choose "TokenAuth" from the dropdown menu, and paste the copied token into the "Value" field. Make sure to include the prefix "Token " before the token.

   Example: `Token 410fde59351b5bf31ced70b4a6de0d74a918d9`

9. **Authorize:** Click the "Authorize" button to save the authentication token.

## Endpoints

Now that you have successfully authenticated, you can explore and interact with the following API endpoints:

### Health Check
- **GET** `/api/health-check/`

### Recipe Ingredients
- **GET** `/api/recipe/ingredients/`
- **PUT** `/api/recipe/ingredients/{id}/`
- **PATCH** `/api/recipe/ingredients/{id}/`
- **DELETE** `/api/recipe/ingredients/{id}/`

### Recipe Recipes
- **GET** `/api/recipe/recipes/`
- **POST** `/api/recipe/recipes/`
- **GET** `/api/recipe/recipes/{id}/`
- **PUT** `/api/recipe/recipes/{id}/`
- **PATCH** `/api/recipe/recipes/{id}/`
- **DELETE** `/api/recipe/recipes/{id}/`
- **POST** `/api/recipe/recipes/{id}/upload_image/`

### Recipe Tags
- **GET** `/api/recipe/tags/`
- **PUT** `/api/recipe/tags/{id}/`
- **PATCH** `/api/recipe/tags/{id}/`
- **DELETE** `/api/recipe/tags/{id}/`

### User
- **POST** `/api/user/create/`
- **GET** `/api/user/me/`
- **PUT** `/api/user/me/`
- **PATCH** `/api/user/me/`
- **POST** `/api/user/token/`

Feel free to explore and interact with these endpoints to manage your recipe data efficiently. 

