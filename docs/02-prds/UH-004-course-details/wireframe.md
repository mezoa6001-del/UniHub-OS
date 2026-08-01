# UH-004 — Course Details Wireframe

Version: 1.0.0

Status: Draft

---

# Goal

Help students understand the course, trust the instructor, and either enroll or continue learning.

---

# Information Hierarchy

1. Course Overview
2. Continue Learning / Buy
3. Course Content
4. Instructor
5. Reviews
6. Related Courses

---

# Desktop Layout

+--------------------------------------------------------------+
| Navbar                                                       |
+--------------------------------------------------------------+

+--------------------------------------------------------------+
| Thumbnail | Course Title                                     |
|           | Instructor                                       |
|           | ⭐ 4.9 (1,245 Reviews)                           |
|           | 32 Lessons • 8 Chapters • 18 Hours              |
|           |                                                  |
|           | [ Continue Learning ] OR [ Enroll Now ]         |
+--------------------------------------------------------------+

+--------------------------------------------------------------+
| Course Description                                           |
+--------------------------------------------------------------+

+--------------------------------------------------------------+
| Course Content                                               |
|--------------------------------------------------------------|
| ▼ Chapter 1                                                  |
|    • Lesson 1                                                |
|    • Lesson 2                                                |
|                                                             |
| ▶ Locked Lessons (Visitors)                                |
+--------------------------------------------------------------+

+--------------------------------------------------------------+
| Instructor                                                   |
|--------------------------------------------------------------|
| Photo | Name | Bio | Courses | Rating                       |
+--------------------------------------------------------------+

+--------------------------------------------------------------+
| Student Reviews                                              |
+--------------------------------------------------------------+

+--------------------------------------------------------------+
| Related Courses                                              |
+--------------------------------------------------------------+

---

# Mobile Layout

Thumbnail

Course Title

Instructor

⭐⭐⭐⭐⭐

Continue Learning / Enroll

-------------------------

Course Description

-------------------------

Course Content (Accordion)

-------------------------

Instructor

-------------------------

Reviews

-------------------------

Related Courses

---

# Components

## Header

- Course Thumbnail
- Course Title
- Instructor
- Rating
- Statistics

---

## Primary CTA

Visitor

- Enroll Now

Student

- Continue Learning

---

## Course Content

Accordion

Each lesson displays:

- Lesson Number
- Lesson Title
- Duration
- Lock Status

---

## Instructor Card

- Profile Image
- Name
- Bio
- Experience

---

## Reviews

- Rating Summary
- Student Comments

---

## Related Courses

Horizontal Cards

---

# States

Loading

- Skeleton Loader

Empty

- No Reviews

Error

- Course Not Found

---

# Navigation

Landing

↓

Course Details

↓

Enroll

↓

Dashboard

OR

↓

Continue Learning

↓

Lesson Player

---

# Responsive

Desktop ≥1024px

Tablet 768–1023px

Mobile ≤767px