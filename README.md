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

---

### Login

Registered users can log in using their **email and password**.

The system verifies the credentials against the **hashed password stored in the database**.

---

### Password Reset Request

If a user forgets their password, they can request a password reset by entering their **email address**.

---

### Email Verification

After submitting a password reset request, the system sends a **verification code via email** using **Nodemailer**.

The verification code is required to confirm the user's identity.

---

### Verification Code Validation

The user enters the verification code received by email.

The system checks the code against the stored reset code in the database.

---

### New Password Creation

Once the verification code is validated, the user can create a **new password**.

The new password is securely **hashed and updated in the database**.

---

### Home Page

After successful login, the user is redirected to the **home page**, where a welcome message and account information are displayed.

---
