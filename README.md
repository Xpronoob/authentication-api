# Authentication-api
This API provides an User system and JWT Authentication
The file http.http contain a example with [REST Client](https://marketplace.visualstudio.com/items?itemName=humao.rest-client) VSCODE Extension 

## Public Routes:

### Get Index
	GET http://localhost:3000/api/v1/ HTTP/1.1
Returns a hello message (JSON).

## Authentication:

### User Register
	POST http://localhost:3000/api/v1/register HTTP/1.1
	content-type: application/json
	{
		"email": "user@user.com",
		"password": "password",
		"name": "user",
		"lastName": "user"
	}
Generates a token and stores it in a cookie, then returns user information (JSON).

### User Login
	POST http://localhost:3000/api/v1/login HTTP/1.1
	content-type: application/json
	{
		"email": "user@user.com",
		"password": "password"
	}
This route allows a user to log in to the application. You must send a JSON object with the email and password fields.

### User Logout
	POST http://localhost:3000/api/v1/logout HTTP/1.1
	content-type: application/json
This route logout a user from the application.

### Get User Profile
	GET http://localhost:3000/api/v1/profile
	Content-Type: application/json
This route returns the information of the authenticated user(JSON).