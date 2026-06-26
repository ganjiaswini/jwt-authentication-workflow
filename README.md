# jwt-authentication-workflow
A Python-based demonstration of JWT authentication workflow, including Access Tokens, Refresh Tokens, token validation, authentication, authorization, and token lifecycle management.
# JWT Authentication Workflow

## Objective

Understand token-based authentication systems using JSON Web Tokens (JWT).

## Project Overview

This project demonstrates JWT authentication workflow including token generation, validation, access token lifecycle, refresh token lifecycle, authentication, and authorization.

## JWT Structure

A JWT consists of three parts:

1. Header
2. Payload
3. Signature

Format:

Header.Payload.Signature

### Header

Contains token type and signing algorithm.

### Payload

Contains user information and claims.

### Signature

Used to verify that the token has not been modified.

## Authentication vs Authorization

### Authentication

Authentication verifies the identity of a user.

Example:

* Login using username and password.

### Authorization

Authorization determines what resources a user can access.

Example:

* Admin can manage users.
* User can access personal profile.

## Access Token

An Access Token is a short-lived token used to access protected resources.

Features:

* Short expiration period
* Used for API access
* Contains user claims

## Refresh Token

A Refresh Token is a long-lived token used to generate a new Access Token after expiration.

Features:

* Longer validity period
* Improves user experience
* Reduces repeated logins

## Authentication Workflow

1. User enters credentials.
2. Server validates credentials.
3. Server generates Access Token and Refresh Token.
4. Client stores tokens.
5. Client uses Access Token to access resources.
6. Server validates token.
7. If expired, Refresh Token generates a new Access Token.

## Token Lifecycle Diagram

User Login
|
v
Generate Access Token + Refresh Token
|
v
Access Protected Resource
|
v
Validate Access Token
/ 
Valid  Expired
|        |
v        v
Access   Use Refresh Token
Granted      |
v
Generate New Access Token

## Installation

pip install PyJWT

## Run

python jwt_authentication.py

## Technologies Used

* Python
* PyJWT

## Learning Outcomes

* JWT Structure
* Access and Refresh Tokens
* Authentication and Authorization
* Token Validation
* Authentication Workflow

## Conclusion

This project demonstrates how JWT-based authentication works using Access Tokens and Refresh Tokens while maintaining secure and scalable user authentication.
