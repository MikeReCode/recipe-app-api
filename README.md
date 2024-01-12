# Recipe API Project


## Introduction

Welcome to the Recipe API project! This API allows you to manage recipes, ingredients, tags, and user information. You can interact with the API through various endpoints to perform actions such as retrieving recipes, updating ingredients, managing tags, and more.

 **Technical Stack:** Developed with Python and Django Rest Framework (DRF), the backend utilizes a PostgreSQL database for data integrity. Docker containers separate the application, database, and Nginx server, providing scalability and efficient deployment.

**Deployment:** The entire project is hosted on an AWS EC2 instance, leveraging Docker's containerization benefits.


## API Documentation

The detailed documentation for the API can be found at [ec2-54-224-136-90.compute-1.amazonaws.com/api/docs](http://ec2-54-224-136-90.compute-1.amazonaws.com/api/docs). This Swagger documentation provides comprehensive information about the available endpoints, request methods, request parameters, and response structures.

## Testing Credentials

To facilitate testing, you can use the following credentials:

- **Username:** user1@example.com
- **Password:** 12345678

## Generating Authentication Token

1. **Login:** Navigate to the [Swagger documentation](http://ec2-54-224-136-90.compute-1.amazonaws.com/api/docs) and locate the `POST /api/user/token/` endpoint under the "User" section.

2. **Try it out:** Click on the "Try it out" button for the `POST /api/user/token/` endpoint.

3. **Enter Credentials:** In the "Request body" section, enter the following credentials:
   - **email:** user1@example.com
   - **password:** 12345678

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

