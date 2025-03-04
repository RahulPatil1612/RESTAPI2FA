# Objective:

The REST API 2-Factor Authentication (2FA) Module helps implement two-factor authentication for REST APIs.

The application must send a request to obtain a token using basic credentials (Username and Password) along with a secret key that is already associated with the user's account details.

Once the token is received, the user can request the actual resource by passing the valid token in the request header.

# Dependencies:

• Studio pro version 9.24.23

# Configuration:

• Import the REST API 2-Factor Authentication Module from the Mendix marketplace.

• Module requires additional validation for the secret key. Before using this module, create an association between the Account entity and the SecretKey entity from the 2FA module.

• The secret key is used for additional validation.

	•	When a user is created, this secret key should also be generated and provided to the user.
  
	•	The user must send this secret key during token generation, and the system will retrieve the key from the Account association and validate it.
  
**JWT (JSON Web Token) Entity:**

The JWT entity includes the following fields:

•	sub: Represents the subject, typically the user or entity the token is about.

•	exp: Defines the expiration time of the token. After this time, the token is no longer valid.

•	iss: Identifies the issuer of the token.

•	nbf: Stands for "Not Before," specifying the time before which the token should not be accepted.

•	iat: Stands for "Issued At," indicating when the token was issued.

•	jti: A unique identifier for the token, often used to prevent replay attacks.

•	kid: Represents the Key ID, used to identify which key was used to sign the token.

# Screenshots:
![Screenshot 2025-03-04 134738](https://github.com/user-attachments/assets/cdba36c6-971a-45a5-bce6-9e91b1cc4e99)
![Screenshot 2025-03-04 134823](https://github.com/user-attachments/assets/34309770-f739-4373-9027-407ad3cc33fe)
![Screenshot 2025-03-04 134850](https://github.com/user-attachments/assets/000cede2-7caa-4417-b06f-c6908d8ddfd4)

