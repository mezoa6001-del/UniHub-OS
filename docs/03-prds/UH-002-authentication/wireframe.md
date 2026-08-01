# UH-002 — Authentication Wireframe

Version: 1.0.0

Status: Draft

---

# Goal

Provide a simple, secure, and frictionless authentication experience.

The user should be able to create an account or log in within one minute.

---

# Authentication Flow

Visitor

↓

Landing Page

↓

Login / Sign Up

↓

Authentication

↓

Email Verification (First Time Only)

↓

Student Dashboard

---

# Screens

This feature includes five screens.

1. Login
2. Register
3. Forgot Password
4. Email Verification
5. Success Screen

---

# Screen 1 — Login

---------------------------------------------------------

UniHub Logo

Welcome Back 👋

Email

[________________________]

Password

[________________________]

👁 Show Password

Forgot Password?

[ Login ]

──────────── OR ────────────

[ Continue with Google ]

Don't have an account?

Create Account

---------------------------------------------------------

---

# Components

- Logo
- Email Input
- Password Input
- Password Toggle
- Forgot Password Link
- Login Button
- Divider
- Google Button
- Create Account Link

---

# Validation

Email

- Required
- Valid Email

Password

- Required
- Minimum Length

Login Button

Disabled until form is valid.

---

# Screen 2 — Register

---------------------------------------------------------

UniHub Logo

Create Your Account

Full Name

[________________________]

Email

[________________________]

Password

[________________________]

Confirm Password

[________________________]

☐ I agree to the Terms & Privacy Policy

[ Create Account ]

──────────── OR ────────────

[ Continue with Google ]

Already have an account?

Login

---------------------------------------------------------

---

# Validation

Full Name

Required

Minimum 3 characters

---

Email

Required

Unique

Valid format

---

Password

Minimum 8 characters

Uppercase

Lowercase

Number

Special Character

---

Confirm Password

Must match password

---

# Screen 3 — Forgot Password

---------------------------------------------------------

Forgot Password

Enter your email.

We'll send you a password reset link.

Email

[________________________]

[ Send Reset Link ]

Back to Login

---------------------------------------------------------

---

# Screen 4 — Email Verification

---------------------------------------------------------

Verify Your Email

We've sent a verification link to:

student@email.com

Please verify your email before continuing.

[ Resend Email ]

[ Refresh Status ]

---------------------------------------------------------

---

# Screen 5 — Success

---------------------------------------------------------

🎉

Authentication Successful

Redirecting to Dashboard...

---------------------------------------------------------

---

# Mobile Layout

Single Column

100% Width Inputs

Sticky Primary Button

Large Touch Targets

---

# Desktop Layout

Centered Authentication Card

Max Width

420px

Soft Shadow

Rounded Corners

---

# UX Principles

- One primary action per screen.
- Maximum two clicks to register.
- Instant validation.
- Clear error messages.
- Fast loading.
- Accessible keyboard navigation.

---

# Error Messages

Invalid Email

Incorrect Password

Email Already Exists

Weak Password

Email Not Verified

Network Error

Unexpected Error

---

# Success Messages

Account Created Successfully

Password Reset Email Sent

Email Verified

Login Successful

---

# Navigation Rules

Login

↓

Dashboard

Register

↓

Verify Email

↓

Dashboard

Forgot Password

↓

Login

---

# Accessibility

- Keyboard Navigation
- Screen Reader Labels
- High Color Contrast
- Focus Indicators
- Proper Form Labels

---

# Future Improvements

- Passkeys
- Face ID
- Fingerprint Login
- Two-Factor Authentication
- Social Logins