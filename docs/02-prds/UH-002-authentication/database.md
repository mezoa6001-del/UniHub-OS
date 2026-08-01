# UH-002 — Authentication Database

Version: 1.0.0

Status: Draft

---

# Purpose

Although Firebase Authentication manages user authentication, UniHub maintains its own user database to store application-specific information such as roles, profile data, subscriptions, and progress.

Firebase is the identity provider.

PostgreSQL is the application database.

---

# Database Overview

Firebase Auth
↓

User Authentication

↓

PostgreSQL

↓

Application Data

---

# Tables

## users

Stores user profile information.

| Field | Type | Description |
|--------|------|-------------|
| id | UUID | Primary Key |
| firebase_uid | VARCHAR(128) | Firebase User ID |
| email | VARCHAR(255) | User Email |
| full_name | VARCHAR(150) | User Full Name |
| role | ENUM | student, instructor, admin |
| profile_image | TEXT | Avatar URL |
| email_verified | BOOLEAN | Verification Status |
| status | ENUM | active, suspended, deleted |
| last_login_at | TIMESTAMP | Last Login |
| created_at | TIMESTAMP | Created Date |
| updated_at | TIMESTAMP | Updated Date |

---

## user_sessions

Stores active login sessions.

| Field | Type |
|--------|------|
| id | UUID |
| user_id | UUID |
| device_name | VARCHAR |
| ip_address | VARCHAR |
| user_agent | TEXT |
| refresh_token | TEXT |
| expires_at | TIMESTAMP |
| created_at | TIMESTAMP |

---

## password_reset_logs

Stores password reset history.

| Field | Type |
|--------|------|
| id | UUID |
| user_id | UUID |
| requested_at | TIMESTAMP |
| completed_at | TIMESTAMP |
| ip_address | VARCHAR |

---

## login_logs

Stores authentication history.

| Field | Type |
|--------|------|
| id | UUID |
| user_id | UUID |
| login_method | ENUM(email, google) |
| status | ENUM(success, failed) |
| ip_address | VARCHAR |
| device | VARCHAR |
| created_at | TIMESTAMP |

---

# Relationships

users

↓

user_sessions

users

↓

login_logs

users

↓

password_reset_logs

---

# Constraints

users.email

Unique

Not Null

---

users.firebase_uid

Unique

Not Null

---

role

Allowed Values

- student
- instructor
- admin

---

status

Allowed Values

- active
- suspended
- deleted

---

# Indexes

users.email

users.firebase_uid

login_logs.user_id

user_sessions.user_id

password_reset_logs.user_id

---

# Soft Delete

Users are never permanently deleted.

status = deleted

Account data remains for audit purposes.

---

# Security

Passwords are NEVER stored.

Authentication is fully managed by Firebase.

Only Firebase UID is stored.

Sensitive tokens are encrypted.

---

# Audit

Every login attempt should be recorded.

Every password reset request should be recorded.

Every account status change should be logged.

---

# Future Tables

user_devices

user_preferences

user_notifications

two_factor_authentication

oauth_accounts

security_events

---

# Migration Notes

Migration Name

001_create_users

002_create_user_sessions

003_create_login_logs

004_create_password_reset_logs