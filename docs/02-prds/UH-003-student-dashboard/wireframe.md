# UH-003 — Student Dashboard Wireframe

Version: 1.0.0

Status: Draft

---

# Goal

The Student Dashboard should help students immediately understand:

- Where they stopped.
- What they should study next.
- How much progress they have made.

The dashboard should reduce the number of clicks needed to continue studying.

---

# Information Hierarchy

Priority Order

1. Continue Learning
2. Progress Overview
3. My Courses
4. Recent Activity
5. Quick Actions

---

# Desktop Layout

+--------------------------------------------------------------+
| Logo     Search                 🔔      Profile              |
+--------------------------------------------------------------+

| 👋 Welcome Back, Ahmed                                       |

+--------------------------------------------------------------+
| Continue Learning                                            |
|--------------------------------------------------------------|
| Pharmacology → ANS Drugs                                     |
| ███████████░░░░░░ 65%                                        |
| [ Continue ]                                                 |
+--------------------------------------------------------------+

+--------------------------------------------------------------+
| Progress Overview                                            |
|--------------------------------------------------------------|
| Courses   Lessons   Questions   Study Time                  |
| 4         86        1,245       42 Hours                    |
+--------------------------------------------------------------+

+-----------------------------+-------------------------------+
| My Courses                  | Recent Activity               |
|-----------------------------|-------------------------------|
| Pharmacology                | Completed Lesson              |
| Pathology                   | Solved 30 Questions           |
| Physiology                  | Finished Quiz                 |
| Microbiology                | Watched Video                 |
+-----------------------------+-------------------------------+

+--------------------------------------------------------------+
| Quick Actions                                                |
|--------------------------------------------------------------|
| Browse Courses | Question Bank | Notes | Profile | Settings |
+--------------------------------------------------------------+

---

# Mobile Layout

Logo

👋 Welcome

---------------------

Continue Learning

[ Continue Button ]

---------------------

Progress Overview

---------------------

My Courses

(scroll)

---------------------

Recent Activity

---------------------

Quick Actions

---------------------

Bottom Navigation

Home

Courses

Questions

Profile

---

# Components

## Header

- Logo
- Search
- Notifications
- User Menu

---

## Continue Learning Card

Displays

- Last Course
- Last Lesson
- Progress
- Continue Button

---

## Progress Cards

Displays

- Courses Enrolled
- Lessons Completed
- Questions Solved
- Study Time

---

## Course List

Each Course Card contains

- Thumbnail
- Course Name
- Instructor
- Progress
- Continue Button

---

## Recent Activity

Displays latest actions in chronological order.

---

## Quick Actions

- Browse Courses
- Question Bank
- Notes
- Profile
- Settings

---

# Navigation Rules

Dashboard

↓

Continue Learning

↓

Lesson Player

---

Dashboard

↓

Course

↓

Course Details

---

Dashboard

↓

Question Bank

↓

Question Session

---

# States

Loading

- Skeleton Cards

Empty

- No Courses Yet

Error

- Failed to load dashboard

---

# Responsive Behavior

Desktop

≥ 1024px

Tablet

768–1023px

Mobile

≤ 767px

---

# Accessibility

- Keyboard Navigation
- Screen Reader Support
- Focus Indicators
- Minimum Touch Target 44px
- High Contrast

---

# UX Principles

- One-click resume learning.
- Show the most important information first.
- Keep cognitive load low.
- Minimize scrolling on desktop.
- Prioritize mobile usability.

---

# Future Enhancements

- Weekly Study Goal
- Learning Streak
- Achievement Badges
- AI Recommendations
- Upcoming Exams Widget