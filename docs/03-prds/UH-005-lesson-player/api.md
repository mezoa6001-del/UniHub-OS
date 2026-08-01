# UH-005 — Lesson Player API

Version: 1.0.0

Status: Draft

---

# Purpose

Provide lesson content, video playback information, downloadable resources, and learning progress.

Authentication is required for all endpoints.

---

# Base URL

/api/v1/lessons

---

# Endpoints

| Endpoint | Method | Auth |
|----------|--------|------|
| /{lessonId} | GET | Required |
| /{lessonId}/resources | GET | Required |
| /{lessonId}/progress | GET | Required |
| /{lessonId}/progress | PATCH | Required |
| /{lessonId}/complete | POST | Required |

---

# GET /{lessonId}

Returns lesson information.

Response

```json
{
  "id": "lesson_032",
  "title": "Cholinergic Drugs",
  "videoUrl": "https://...",
  "duration": 2700,
  "chapter": "Autonomic Nervous System",
  "course": "General Pharmacology"
}
```

---

# GET /{lessonId}/resources

Returns downloadable lesson files.

Response

```json
[
  {
    "id": "file_001",
    "name": "Slides.pdf",
    "type": "pdf",
    "url": "https://..."
  }
]
```

---

# GET /{lessonId}/progress

Returns current student progress.

Response

```json
{
  "progress": 65,
  "completed": false,
  "lastPosition": 1742
}
```

---

# PATCH /{lessonId}/progress

Updates video watch progress.

Request

```json
{
  "lastPosition": 1800,
  "progress": 67
}
```

---

# POST /{lessonId}/complete

Marks lesson as completed.

Response

```json
{
  "success": true
}
```

---

# Errors

401 Unauthorized

403 Enrollment Required

404 Lesson Not Found

500 Internal Server Error

---

# Performance

- Video metadata < 300 ms
- Progress update < 200 ms
- Resources served via CDN