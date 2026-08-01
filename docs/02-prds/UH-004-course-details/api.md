# UH-004 — Course Details API

Version: 1.0.0

Status: Draft

---

# Purpose

Provide all information required to display a course and determine the student's enrollment status.

Authentication is optional.
Some fields are only returned for enrolled students.

---

# Base URL

/api/v1/courses

---

# Endpoints

| Endpoint | Method | Auth |
|----------|--------|------|
| /{courseId} | GET | Optional |
| /{courseId}/content | GET | Optional |
| /{courseId}/reviews | GET | Optional |
| /{courseId}/related | GET | Optional |

---

# GET /{courseId}

Returns course information.

Response

```json
{
  "id": "course_001",
  "title": "General Pharmacology",
  "description": "...",
  "thumbnail": "...",
  "price": 499,
  "rating": 4.9,
  "reviews": 1245,
  "duration": "18 Hours",
  "chapters": 8,
  "lessons": 32,
  "isEnrolled": false
}
```

---

# GET /{courseId}/content

Returns chapters and lessons.

Visitors receive only preview lessons.

Enrolled students receive all lessons.

---

# GET /{courseId}/reviews

Returns approved reviews.

Supports pagination.

---

# GET /{courseId}/related

Returns recommended courses.

Maximum 6 courses.

---

# Errors

401 Unauthorized

403 Enrollment Required

404 Course Not Found

500 Internal Server Error

---

# Performance

Course Details < 500 ms

Reviews Pagination

Image CDN

Server Cache Enabled