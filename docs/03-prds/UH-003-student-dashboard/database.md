# UH-003 — Student Dashboard Database

Version: 1.0.0

Status: Draft

---

# Purpose

The Student Dashboard aggregates personalized information from multiple tables.

It does not own business data; instead, it retrieves and combines information related to the authenticated student.

---

# Data Sources

The dashboard reads data from:

- users
- enrollments
- courses
- lessons
- lesson_progress
- question_sessions
- activities

---

# Tables

## users

Stores student profile information.

| Field | Type |
|--------|------|
| id | UUID |
| full_name | VARCHAR |
| profile_image | TEXT |
| role | ENUM |
| created_at | TIMESTAMP |

---

## courses

Stores published courses.

| Field | Type |
|--------|------|
| id | UUID |
| title | VARCHAR |
| thumbnail | TEXT |
| instructor_id | UUID |
| total_lessons | INTEGER |
| published | BOOLEAN |

---

## enrollments

Represents purchased/enrolled courses.

| Field | Type |
|--------|------|
| id | UUID |
| user_id | UUID |
| course_id | UUID |
| enrolled_at | TIMESTAMP |

---

## lessons

Course lessons.

| Field | Type |
|--------|------|
| id | UUID |
| course_id | UUID |
| title | VARCHAR |
| duration | INTEGER |
| order_index | INTEGER |

---

## lesson_progress

Tracks lesson completion.

| Field | Type |
|--------|------|
| id | UUID |
| user_id | UUID |
| lesson_id | UUID |
| progress_percentage | INTEGER |
| completed | BOOLEAN |
| last_watched_at | TIMESTAMP |

---

## question_sessions

Stores solved question sessions.

| Field | Type |
|--------|------|
| id | UUID |
| user_id | UUID |
| questions_answered | INTEGER |
| correct_answers | INTEGER |
| completed_at | TIMESTAMP |

---

## activities

Stores timeline activity.

| Field | Type |
|--------|------|
| id | UUID |
| user_id | UUID |
| type | VARCHAR |
| title | VARCHAR |
| metadata | JSONB |
| created_at | TIMESTAMP |

---

# Relationships

users
│
├── enrollments
│      │
│      └── courses
│
├── lesson_progress
│      │
│      └── lessons
│
├── question_sessions
│
└── activities

---

# Dashboard Queries

## Continue Learning

Latest lesson where:

- completed = false

Ordered by:

last_watched_at DESC

Limit:

1

---

## My Courses

Join:

enrollments

↓

courses

Calculate progress from:

lesson_progress

---

## Progress Overview

Calculate:

- Total Courses
- Completed Lessons
- Remaining Lessons
- Questions Solved
- Total Study Time

---

## Recent Activity

Latest 10 activities.

Ordered by:

created_at DESC

---

# Indexes

enrollments.user_id

lesson_progress.user_id

lesson_progress.lesson_id

activities.user_id

activities.created_at

question_sessions.user_id

---

# Security

- Users can only read their own records.
- Dashboard queries must always filter by authenticated user_id.
- No cross-user access is permitted.

---

# Performance

- Cache dashboard overview for 5 minutes.
- Paginate activities.
- Limit enrolled courses per request.
- Optimize joins with indexes.

---

# Future Tables

study_goals

study_streaks

achievements

notifications

learning_recommendations

---

# Migration Notes

005_create_enrollments

006_create_lessons

007_create_lesson_progress

008_create_question_sessions

009_create_activities