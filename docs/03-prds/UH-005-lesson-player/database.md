# UH-005 — Lesson Player Database Impact

Version: 1.0.0

Status: Draft

---

# Purpose

The Lesson Player reads lesson data and updates student progress.

---

# Tables Used

- lessons
- lesson_resources
- lesson_progress
- enrollments

---

# Read Operations

- Load lesson information
- Load lesson resources
- Verify enrollment
- Load saved progress

---

# Write Operations

- Update lesson progress
- Mark lesson as completed

---

# Relationships

courses

↓

chapters

↓

lessons

↓

lesson_resources

↓

lesson_progress

---

# Business Rules

Only enrolled students can access lessons.

Progress updates continuously while watching.

Completing a lesson updates overall course progress.

---

# Indexes

lessons.course_id

lesson_progress.user_id

lesson_progress.lesson_id

lesson_resources.lesson_id