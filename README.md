# 🔐 Google OAuth Secrets Keeper App

A secure web application built with Node.js and Express.js that allows users to register or sign in using **Google OAuth 2.0** or traditional **email-password authentication**. After authentication, users can anonymously share and view "secrets" — personal messages submitted securely.

---

## 🌐 Features

- 🔐 Google OAuth 2.0 login and registration
- 🔑 Local authentication with secure password hashing using bcrypt
- 💬 Submit and view anonymous secrets
- 🛡️ Secure sessions with express-session
- 🗃️ PostgreSQL database integration for persistent storage
- 📐 EJS templating engine for frontend rendering

---

## 🧩 Tech Stack

- **Backend:** Node.js, Express.js
- **Frontend:** EJS
- **Authentication:** Passport.js, Google OAuth 2.0, bcrypt
- **Database:** PostgreSQL
- **Session Management:** express-session
- **Environment Configuration:** dotenv

---

## 📦 Dependencies

```
"bcrypt": "^5.1.1",
"body-parser": "^1.20.2",
"dotenv": "^16.3.1",
"ejs": "^3.1.9",
"express": "^4.18.2",
"express-session": "^1.17.3",
"passport": "^0.7.0",
"passport-google-oauth2": "^0.2.0",
"passport-local": "^1.0.0",
"pg": "^8.11.3"
```

# 🚀 Getting Started
## 1. Clone the Repository
```
git clone https://github.com/yourusername/google-oauth-secrets-app.git
cd google-oauth-secrets-app
```
## 2. Install Dependencies
```
npm install
```
## 3. Set Up .env File
```
PORT=3000
SESSION_SECRET=your_session_secret
GOOGLE_CLIENT_ID=your_google_client_id
GOOGLE_CLIENT_SECRET=your_google_client_secret
GOOGLE_CALLBACK_URL=http://localhost:3000/auth/google/secrets
DATABASE_URL=your_postgresql_database_url
```
##  Run the App
```
nodemon index.js
```
Visit http://localhost:3000 in your browser.

# 📁 Project Structure
```
├── app.js
├── views/
│   ├── home.ejs
│   ├── login.ejs
│   ├── register.ejs
│   ├── secrets.ejs
│   └── submit.ejs
├── public/
├── .env
├── package.json
└── README.md
```
# 🛡️ Security Notes
Passwords are hashed using bcrypt.
Session data is securely stored using express-session.
Always keep your OAuth and session secrets in the .env file and never commit them to Git.

