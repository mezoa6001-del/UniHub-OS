# UH-003 — Student Dashboard API

Version: 1.0.0

Status: Draft

---

# Purpose

The Student Dashboard API provides all personalized data required to render the student's home dashboard after authentication.

All endpoints require authentication.

---

# Authentication

Bearer Token (Firebase ID Token)

Required: Yes

---

# Base URL

/api/v1/dashboard

---

# API Overview

| Endpoint | Method | Purpose |
|----------|--------|---------|
| /overview | GET | Dashboard summary |
| /continue-learning | GET | Resume latest lesson |
| /courses | GET | Enrolled courses |
| /recent-activity | GET | Latest activity |
| /quick-actions | GET | Dashboard shortcuts |

---

# GET /overview

## Purpose

Returns dashboard statistics.

### Response

```json
{
  "courses": 4,
  "completedLessons": 86,
  "questionsSolved": 1245,
  "studyHours": 42
}
```

---

# GET /continue-learning

## Purpose

Returns the latest lesson the student was studying.

### Response

```json
{
  "courseId": "course_001",
  "courseTitle": "General Pharmacology",
  "chapterTitle": "Autonomic Nervous System",
  "lessonId": "lesson_032",
  "lessonTitle": "Cholinergic Drugs",
  "progress": 65
}
```

---

# GET /courses

## Purpose

Returns all enrolled courses.

### Response

```json
[
  {
    "id": "course_001",
    "title": "General Pharmacology",
    "progress": 65,
    "thumbnail": "/courses/pharma.png",
    "lastAccessed": "2026-08-01T09:15:00Z"
  }
]
```

---

# GET /recent-activity

## Purpose

Returns the student's latest activity.

### Response

```json
[
  {
    "type": "lesson_completed",
    "title": "Finished ANS Drugs",
    "createdAt": "2026-08-01T10:20:00Z"
  },
  {
    "type": "quiz_completed",
    "title": "Solved CVS Quiz",
    "createdAt": "2026-08-01T09:45:00Z"
  }
]
```

---

# GET /quick-actions

## Purpose

Returns enabled dashboard shortcuts.

### Response

```json
[
  {
    "name": "Browse Courses",
    "icon": "book",
    "url": "/courses"
  },
  {
    "name": "Question Bank",
    "icon": "help-circle",
    "url": "/questions"
  }
]
```

---

# Error Responses

## 401 Unauthorized

```json
{
  "success": false,
  "message": "Authentication required."
}
```

---

## 404 Dashboard Not Found

```json
{
  "success": false,
  "message": "Dashboard data unavailable."
}
```

---

## 500 Internal Server Error

```json
{
  "success": false,
  "message": "Unexpected server error."
}
```

---

# Performance Requirements

- Dashboard response < 500ms
- Cached summary data
- Paginated activity history
- Optimized queries

---

# Security

- Firebase Token Verification
- User can only access their own dashboard
- Rate Limiting
- HTTPS Only
- Audit Logging

---

# Future Endpoints

- GET /study-streak
- GET /recommendations
- GET /weekly-report
- GET /calendar
- GET /notifications