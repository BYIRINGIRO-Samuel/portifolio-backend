# 🚀 Portfolio Backend - Neural Dynamics

The robust backend core for the **Samuel Byiringiro Portfolio**. This server handles secure communication, contact form dispatching, and system notifications using Node.js and Nodemailer.

## 🛠️ Tech Stack

- **Runtime**: Node.js
- **Framework**: Express.js
- **Email Service**: Nodemailer (SMTP)
- **Security**: CORS, Dotenv, App Passwords
- **Development**: Nodemon

## ⚙️ Setup & Installation

1. **Clone the repository**:
   ```bash
   git clone https://github.com/BYIRINGIRO-Samuel/portifolio-backend.git
   cd portifolio-backend
   ```

2. **Install Dependencies**:
   ```bash
   npm install
   ```

3. **Environment Configuration**:
   Create a `.env` file based on `.env.example`:
   ```env
   PORT=5000
   EMAIL_USER=sender-email@gmail.com
   EMAIL_PASS=your-google-app-password
   RECEIVER_EMAIL=your-recipient-email@gmail.com
   ```

4. **Launch the Server**:
   ```bash
   # Development mode with auto-reload
   npm run dev

   # Production mode
   npm run start
   ```

## 🔌 API Endpoints

### `POST /api/contact`
Receives contact form submissions from the frontend.
- **Payload**: `{ "name": "string", "email": "string", "message": "string" }`
- **Response**: `200 OK` on success, `500 Error` on failure.

## 🔒 Security Policy
This project uses `.env` files to store sensitive credentials. **Never commit your `.env` file to version control.** A `.gitignore` is provided to ensure local secrets stay local. All personal emails are abstracted to environment variables for public safety.
