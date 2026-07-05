
DAY-2 JWT 

JWT stands for JSON Web Token.
•	It is a secure token used to identify a user after they log in.
•	Instead of asking the user to enter their username and password on every request, the server gives them a JWT token.
•	The user sends this token with every request.
•	The server checks the token and knows who the user is.

Need to jwt
Without JWT,
Every request would require
Username
Password
Example
Open Home Page
→ Enter password

Open Profile
→ Enter password

Open Orders
→ Enter password

Open Cart
→ Enter password
This is not practical.










 


What does JWT look like?

eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9 - Like a string

It looks like one long string.
Notice there are 3 parts separated by dots.
xxxxx.yyyyy.zzzzz

 




Part 1 : Header
The header tells
•	Which algorithm is used 
•	What type of token it is

 

Part 2 : Payload
Payload contains user information.
 


Part 3 : Signature

This is the most important part.
Signature ensures
Nobody modified the JWT.
Suppose payload is
Role = USER
A hacker changes it to
Role = ADMIN
The signature will no longer match.
Server rejects the token.

