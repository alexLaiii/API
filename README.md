# Museum React App API

The Museum React App API provides data to the Museum React App, allowing users to view information about museum collections and exhibitions.

## Features

The Museum React App API provides the following features:

- User registration and login.
- User authentication with JWT tokens.
- Retrieving a user's favorite exhibits.
- Adding and removing exhibits from a user's favorites list.
- Retrieving a user's recently viewed exhibits.
- Adding and removing exhibits from a user's history list.



## Endpoints

The following endpoints are available in the Museum React App API:

### `POST /api/user/register`

This endpoint allows users to register for a new account in the museum app. Users must provide their name, email, and password.

Here are some useful tags for this section:

- `#jwt-authentication`: Describes the JWT authentication required for all endpoints.
- `#mongodb-connection`: Describes how to set up a MongoDB database and update the connection string in `user-service.js`.

### `POST /api/user/login`

This endpoint allows users to log in to the museum app. Users must provide their email and password. Upon successful login, a JWT token is returned that can be used for subsequent requests.

### `GET /api/user/favourites`

This endpoint returns a list of a user's favorite museum exhibits. Authentication is required for this endpoint.

### `PUT /api/user/favourites/:id`

This endpoint allows users to add a museum exhibit to their list of favorites. The `:id` parameter specifies the ID of the exhibit to add. Authentication is required for this endpoint.

### `DELETE /api/user/favourites/:id`

This endpoint allows users to remove a museum exhibit from their list of favorites. The `:id` parameter specifies the ID of the exhibit to remove. Authentication is required for this endpoint.

### `GET /api/user/history`

This endpoint returns a list of a user's recently viewed museum exhibits. Authentication is required for this endpoint.

### `PUT /api/user/history/:id`

This endpoint allows users to add a museum exhibit to their list of recently viewed exhibits. The `:id` parameter specifies the ID of the exhibit to add. Authentication is required for this endpoint.

### `DELETE /api/user/history/:id`

This endpoint allows users to remove a museum exhibit from their list of recently viewed exhibits. The `:id` parameter specifies the ID of the exhibit to remove. Authentication is required for this endpoint.


## Dependencies

The following dependencies are required to run the Museum React App API:

- Express
- Passport
- Passport-JWT
- MongoDB
- cors
- dotenv

## Getting Started

To run the Museum React App API, you'll need to install the necessary dependencies and set up a MongoDB database.

1. Clone this repository to your local machine.
2. Run `npm install` to install the required dependencies.
3. Set up a MongoDB database and update the connection string in `user-service.js`.
4. Set the `JWT_SECRET` environment variable to a secret string of your choice.
5. Run `node server.js` to start the local server.

If you're looking for an easy way to deploy your Museum React App API, you can use the [Cyclic](https://cyclic.app/) platform. With Cyclic, you can quickly deploy your API and start using it in your Museum Web App.

Here are the steps to deploy your Museum React App API on Cyclic:

1. Create a Cyclic account if you don't already have one.
2. Create a new Cyclic project and select the Node.js template.
3. Connect your Cyclic project to your GitHub repository that contains your Museum React App API code.
4. Set the `JWT_SECRET` environment variable in Cyclic to the same secret value you used when running the API locally.
5. Start the server in Cyclic by running `npm start`.

That's it! Your Museum React App API is now deployed and ready to use.
