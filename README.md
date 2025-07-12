COMPANY: CODEC TECHNOLOGIES

NAME: MANIMEGALAI S

DESIGNATION: PYTHON DEVELOPER INTERN

DURATION: 1 MONTH

OUTPUT:

<img width="1336" height="646" alt="Screenshot 2025-07-12 114657" src="https://github.com/user-attachments/assets/d758d5bc-3a98-406b-84e0-9d486e420fe5" />



<img width="1332" height="650" alt="Screenshot 2025-07-12 114713" src="https://github.com/user-attachments/assets/6982064e-962a-49cd-bbe7-88c9997e543b" />


DESCRIPTION: 
PURPOSE OF THE APP:
This web application is a secure **user authentication system** using:

Flask as the web framework
Flask-Bcrypt for password hashing
Flask-JWT-Extended for managing secure sessions using JWT tokens stored in cookies
A JSON file (`users.json`) to store user credentials persistently


KEY FUNCTIONALITIES:
1.User Registration

 A user can create a new account by entering a username and password.
The password is hashed using `bcrypt` to enhance security, so it's never stored in plain text.
 The hashed password and username are saved in a file called `users.json`, which acts as a simple local user database.

2. User Login

A user can log in with their registered credentials.
On form submission, the system looks up the `users.json` file for the entered username.
If the user exists, it compares the entered password with the hashed one using `bcrypt`.
If matched, a JWT token is created, identifying the user.
This token is then saved in the browser as a **secure HTTP cookie**, enabling session management.

3. JWT Token Management

 The JWT token:
 Identifies the currently logged-in user.
 Expires after 30 minutes of inactivity for added security.
 Is stored in a browser cookie to maintain session across page visits.

 4.Dashboard (Protected Route)

 After login, the user is redirected to a secure dashboard.
 This dashboard page can only be accessed if a valid JWT token exists in the user's cookie.
 If someone tries to access it without logging in, they’ll be blocked.

5. Logout

A logout button on the dashboard triggers a POST request.
This clears the JWT cookie and redirects the user back to the login page, ending their session.

USER INTERFACE:
The interface is simple and mobile-friendly, created using embedded HTML and CSS. It includes:

A clean registration form
A clean login form
A protected dashboard
Navigation links to switch between login and registration
The layout is styled using minimal CSS embedded directly in the app to make it easy to view on both desktop and mobile.

SECURITY CONSIDERATIONS:

 Passwords are never stored in plain text.
 Sessions use JWT tokens, stored in cookies (not in localStorage or headers), which is more secure.
 Cookies have configurations to prevent misuse:

   SameSite policy is set (prevents CSRF in most cases).
   CSRF protection is turned off (but this should be enabled in production).
   Tokens expire after 30 minutes for session safety.



