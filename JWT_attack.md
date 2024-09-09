# Background
- JWT (JSON web token) is a standard formate for sending cryptographic signed JSON between system.
- Most commonly used to send information that claimed to be of user such as: authentication, session handling, access control mechanism.
- JWT have 3 part, seperate by dot. Header, payload and signature.
- JWS (JSON web signature)
- JWE (JSON web encryption)
## JWT attack
- Send modified JWTs to server.
- Developer decide many details of implementation of JWTs, so they may introduce vulnerbility into the application. Resulting the error when application handle the JWT
