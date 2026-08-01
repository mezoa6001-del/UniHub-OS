# UH-004 — Course Details Database Impact

Version: 1.0.0

Status: Draft

---

# Purpose

This feature reads course information and enrollment status.

No new tables are introduced.

---

# Tables Used

- courses
- instructors
- chapters
- lessons
- enrollments
- reviews

---

# Database Impact

## Read

courses

instructors

chapters

lessons

reviews

enrollments

---

## Write

None

---

# Relationships

courses

↓

chapters

↓

lessons

courses

↓

reviews

courses

↓

enrollments

↓

users

---

# Business Rules

Only published courses are visible.

Only approved reviews are returned.

Locked lessons require enrollment.

---

# Indexes

courses.slug

courses.published

reviews.course_id

enrollments.user_id

enrollments.course_id