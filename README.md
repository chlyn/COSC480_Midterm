# COSC 480: Midterm HTML Form

**By: Chenilyn Joy Espineda**  
**Instructor: Dr. Apollo Tankeh**

---

# Project Dependencies Configuration using Node.js

The project dependencies were configured using **package.json**. The project uses **Node.js** with several packages to support server functionality and application features.

Packages used include:

- **Express** – Handles the backend server and routing
- **MySQL2** – Connects the application to the MySQL database
- **bcrypt** – Hashes user passwords for security
- **Nodemailer** – Sends password reset verification emails
- **dotenv** – Loads environment variables from the `.env` file

Development is run using **nodemon**, which automatically restarts the server whenever changes are made to the project files.

<img width="484" height="503" alt="Screenshot 2026-03-10 at 5 58 46 PM" src="https://github.com/user-attachments/assets/ead6c62a-84ed-4348-8b44-f67a99b55306" />

---

# MySQL Database

The application connects to the MySQL database **midterm_account_db**.

The database contains two main tables:

### Users Table
Stores user account information including:

- First name
- Last name
- Email
- Hashed password
- Major
- Account creation timestamp

### Password Reset Codes Table
Stores verification codes used for password reset requests.

These codes allow the system to verify a user's identity before allowing them to create a new password.

<img width="476" height="186" alt="Screenshot 2026-03-10 at 5 58 02 PM" src="https://github.com/user-attachments/assets/daa96951-4bb8-427f-a1bc-fbcc9269c3c8" />


---

# Backend Server Configuration

The backend server was built using **Node.js and Express**.

The server performs several key functions:

- Imports required Node.js packages
- Loads environment variables using dotenv
- Configures middleware for handling form submissions and JSON requests
- Serves static frontend files
- Connects to the MySQL database
- Configures **Nodemailer** to send password reset verification emails

<img width="1362" height="758" alt="Screenshot 2026-03-10 at 6 01 17 PM" src="https://github.com/user-attachments/assets/27d762e8-b85b-416a-acf3-4cfe1646d5ae" />

---

# Frontend Implementation

The frontend is built using **HTML, CSS, and JavaScript**.

### HTML – `index.html`
Defines the structure of the user interface, including forms for:

- Account creation
- User login
- Email verification
- Password reset
- New password update

### CSS – `style.css`
Provides styling for the application including:

- Layout and page structure
- Form design
- Buttons
- Alerts and notifications
- Responsive interface elements

### JavaScript – `script.js`
Handles client-side functionality including:

- Form submission handling
- Input validation
- Switching between different views
- Sending requests to backend API endpoints

---

# Application Interface

### Account Creation
Users can create a new account by entering:

- First name
- Last name
- Email
- Password
- Major
- Optional minor

User passwords are securely stored using **bcrypt hashing**.

<img width="868" height="834" alt="Screenshot 2026-03-10 at 6 03 26 PM" src="https://github.com/user-attachments/assets/db0030c8-2db3-4d28-9e51-35580ba934f2" />


---

### Login

Registered users can log in using their email and password.

The system verifies the credentials against the hashed password stored in the database.

<img width="845" height="754" alt="Screenshot 2026-03-10 at 6 03 01 PM" src="https://github.com/user-attachments/assets/72332d78-01a0-4d1a-8596-bc5f3746bb67" />

---

### Forget Password Request

If a user forgets their password, they can request a password reset by entering their email address.

<img width="819" height="671" alt="Screenshot 2026-03-10 at 6 05 35 PM" src="https://github.com/user-attachments/assets/be0d394d-4841-4972-b569-a88b65fd670c" />

---

### Email Verification

After submitting a password reset request, the system sends a verification code via email using **Nodemailer**.

The verification code is required to confirm the user's identity.

<img width="660" height="658" alt="Screenshot 2026-03-10 at 6 32 56 PM" src="https://github.com/user-attachments/assets/b9e3e74b-5ba9-49a7-b2b8-c7c337a63da7" />

---

### Verification Code Validation

The user enters the verification code received by email.

The system checks the code against the stored reset code in the database.

<img width="786" height="679" alt="Screenshot 2026-03-10 at 6 33 43 PM" src="https://github.com/user-attachments/assets/1dea7514-f358-47b5-94df-e5cbe06cfd9d" />

---

### New Password Creation

Once the verification code is validated, the user can create a new password.

The new password is securely hashed and updated in the database.

<img width="802" height="657" alt="Screenshot 2026-03-10 at 6 34 34 PM" src="https://github.com/user-attachments/assets/8bba4d11-fef6-47d3-8517-44bdd03fcffc" />

---

### Home Page

After successful login, the user is redirected to the **home page**, where a welcome message and account information are displayed.

<img width="1470" height="956" alt="Screenshot 2026-03-10 at 6 35 05 PM" src="https://github.com/user-attachments/assets/bbf7a69c-ce1f-42b5-b63e-ca9e2f8a551e" />

---
