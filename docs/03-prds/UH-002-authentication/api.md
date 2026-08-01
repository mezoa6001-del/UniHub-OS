# UH-002 — Authentication API

Version: 1.0.0

Status: Draft

---

# Purpose

The Authentication API provides secure user authentication and identity management using Firebase Authentication.

The backend is responsible for user profiles, roles, and permissions.

Authentication itself is handled by Firebase.

---

# Authentication Provider

Firebase Authentication

Supported Methods

- Email & Password
- Google Sign-In

---

# Base URL

/api/v1/auth

---

# Authentication Flow

User

↓

Firebase Authentication

↓

Firebase ID Token

↓

Backend Verification

↓

JWT Session

↓

Protected APIs

---

# Endpoints

| Endpoint | Method | Authentication |
|----------|--------|----------------|
| /register | POST | No |
| /login | POST | No |
| /google | POST | No |
| /logout | POST | Yes |
| /verify-email | POST | Yes |
| /forgot-password | POST | No |
| /refresh-session | POST | Yes |
| /me | GET | Yes |

---

# POST /register

## Purpose

Create a new user account.

### Request

```json
{
  "fullName": "Ahmed Mohamed",
  "email": "ahmed@example.com",
  "password": "StrongPassword123!"
}
```

### Success Response

```json
{
  "success": true,
  "message": "Account created successfully. Please verify your email."
}
```

---

# POST /login

### Request

```json
{
  "email": "ahmed@example.com",
  "password": "StrongPassword123!"
}
```

### Success Response

```json
{
  "success": true,
  "token": "jwt_token",
  "user": {
    "id": "user_001",
    "role": "student"
  }
}
```

---

# POST /google

Authenticate using Google Sign-In.

Response format is identical to `/login`.

---

# POST /logout

Invalidate the current session.

### Success Response

```json
{
  "success": true,
  "message": "Logged out successfully."
}
```

---

# POST /verify-email

Marks the user's email as verified after Firebase verification.

---

# POST /forgot-password

### Request

```json
{
  "email": "ahmed@example.com"
}
```

### Success Response

```json
{
  "success": true,
  "message": "Password reset email sent."
}
```

---

# POST /refresh-session

Returns a refreshed authentication token.

---

# GET /me

Returns the authenticated user's profile.

### Response

```json
{
  "id": "user_001",
  "fullName": "Ahmed Mohamed",
  "email": "ahmed@example.com",
  "role": "student",
  "emailVerified": true
}
```

---

# Error Responses

400 Bad Request

```json
{
  "success": false,
  "message": "Invalid request."
}
```

401 Unauthorized

```json
{
  "success": false,
  "message": "Invalid credentials."
}
```

403 Forbidden

```json
{
  "success": false,
  "message": "Email verification required."
}
```

429 Too Many Requests

```json
{
  "success": false,
  "message": "Too many attempts. Try again later."
}
```

500 Internal Server Error

```json
{
  "success": false,
  "message": "Unexpected server error."
}
```

---

# Validation Rules

Email

- Required
- Valid email format

Password

- Minimum 8 characters
- At least one uppercase letter
- At least one lowercase letter
- At least one number
- At least one special character

Full Name

- Required
- 3–100 characters

---

# Security

- HTTPS Only
- Firebase Token Verification
- JWT Session Management
- Rate Limiting
- Input Validation
- Secure Cookies (Web)
- CSRF Protection
- Audit Logging

---

# Performance Targets

Login Response < 500ms

Register Response < 700ms

Password Reset < 500ms

---

# Future APIs

- POST /2fa/setup
- POST /2fa/verify
- POST /login/apple
- POST /login/microsoft
- GET /devices
- DELETE /devices/{id}